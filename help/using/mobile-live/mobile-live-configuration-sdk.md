---
solution: Journey Optimizer
product: journey optimizer
title: Het actieve activiteitenkanaal configureren
description: Leer hoe u uw Adobe Experience Platform Mobile SDK-integratie configureert
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Integratie van live-activiteiten met Adobe Experience Platform Mobile SDK {#mobile-live-config-sdk}

>[!BEGINSHADEBOX]

* [Aan de slag met Live-activiteiten](get-started-mobile-live.md)
* [Live activity-configuratie](mobile-live-configuration.md)
* **[Levende integratie van de Activiteit met Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**
* [Live-activiteiten maken](create-mobile-live.md)
* [Veelgestelde vragen](mobile-live-faq.md)
* [Rapport voor live-activiteitencampagne](../reports/campaign-global-report-cja-activity.md)


>[!ENDSHADEBOX]

De Adobe Experience Platform Mobile SDK biedt ingebouwde ondersteuning voor Apple Live-activiteiten. Hierdoor kan uw app realtime, dynamische updates rechtstreeks weergeven op het Lock Screen en Dynamic Island zonder de app te openen.

1. [Vereiste modules importeren](#import)

   Importeer de volgende modules: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]** .

1. [&#x200B; bepalen attributen &#x200B;](#attributes)

   Omgaan met `LiveActivityAttributes` , neemt u de kenmerken `LiveActivityData` en a `ContentState` op.

1. [Live activiteiten registreren](#register)

   Gebruik `Messaging.registerLiveActivity()` na SDK-initialisatie.

1. [Widgetconfiguratie maken](#widget)

   Implementeer `ActivityConfiguration` voor zowel de interface Scherm vergrendelen als de interface van Dynamic Island.

1. [Live-activiteiten lokaal starten (optioneel)](#local)

   Live-activiteiten kunnen op afstand worden gestart via Journey Optimizer of lokaal binnen de toepassingscode.

1. [Ondersteuning voor foutopsporing toevoegen (optioneel)](#debug)

   Implementeer `LiveActivityAssuranceDebuggable` voor Assurance.

Controleer of de volgende minimale versies zijn geïnstalleerd om de juiste configuratie en compatibiliteit te garanderen.

>[!BEGINSHADEBOX]

**Eerste vereisten:**

* **iOS:**
   * **iOS16.1 of later**: De basis Levende functionaliteit van de activiteit
   * **iOS 17.2+**: Push-to-start steun
   * **iOS 18+**: De steun van het Kanaal van de uitzending
* **Xcode:** 14.0 of later
* **Swift:** 5.7 of later
* **Afhankelijkheden:** AEPCore, AEPMessaging, AEPMessagingLiveActivity, ActivityKit

>[!ENDSHADEBOX]

## Stap 1: Vereiste modules importeren {#import}

Om aan de slag te gaan, moet u eerst de volgende modules importeren: **[!DNL AEPMessaging]**, **[!DNL AEPMessagingLiveActivity]**, **[!DNL ActivityKit]** .

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## Stap 2: Definieer de kenmerken van uw actieve activiteit {#attributes}

Maak een structuur die voldoet aan het protocol `LiveActivityAttributes` . Hiermee definieert u zowel de statische gegevens als de dynamische inhoudsstatus voor uw Live-activiteit.

De belangrijkste componenten zijn:

* **`liveActivityData`** (vereist) dat Adobe Experience Platform-specifieke gegevens bevat.
   * Voor individuele gebruikers: gebruik `LiveActivityData(liveActivityID: "unique-id")`
   * Voor uitzending: gebruik `LiveActivityData(channelID: "channel-id")`

* Statische kenmerken, aangepaste eigenschappen die specifiek zijn voor uw gebruiksscenario, bijvoorbeeld `restaurantName` .

* **`ContentState`** definieert dynamische gegevens die kunnen worden bijgewerkt tijdens de levenscyclus van Live-activiteit. De eigenschap moet `Codable` en `Hashable` bevatten.

* Met `LiveActivityOrigin` wordt aangegeven of een activiteit lokaal binnen de app is gestart of op afstand via een pushmelding, ondersteund in iOS 17.2 en hoger. Met deze waarde kan de SDK onderscheid maken tussen lokaal geïnitieerde en extern geactiveerde Live-activiteiten tijdens het verzamelen van gegevens.

**Voorbeelden**

```swift
@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
    // Mandatory: AEP Integration Data
    var liveActivityData: LiveActivityData
    
    // Static Attributes: Custom properties that do not change
    var restaurantName: String
    
    // Dynamic Content State: Data that can be updated
    struct ContentState: Codable, Hashable {
        var orderStatus: String
    }
}
```

```swift
@available(iOS 16.1, *)
public struct LiveActivityData: Codable {
    /// Unique identifier for broadcast Live activity channels
    public let channelID: String?
     
    /// Unique identifier for individual Live activities
    public let liveActivityID: String?
     
    /// Indicates local vs remote creation
    public let origin: LiveActivityOrigin?
     
    // Initializers
    public init(channelID: String)        // For broadcast Live activities
    public init(liveActivityID: String)   // For individual Live activities
}
```

U kunt ook meerdere typen Live-activiteiten registreren voor uw app:

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## Stap 3: Live activiteiten registreren {#register}

Registreer de typen Live-activiteiten in uw `AppDelegate` na de SDK-initialisatie. U kunt dan het volgende doen:

* Schakelt automatische push-to-start tokenverzameling in (iOS 17.2+)
* Automatisch tokens voor updates van actieve activiteiten verzamelen
* Maakt levenscyclusbeheer en gebeurtenistracering mogelijk

**Voorbeeld voor een Levende activiteit van de voedsellevering:**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## Stap 4: Live-activiteiten-widgets maken {#widgets}

Live activiteiten worden via widgets weergegeven. U moet een widgetbundel en -configuratie maken:

**Voorbeeld voor een Levende activiteit van de voedsellevering:**

```swift
@main
struct FoodDeliveryWidgetBundle: WidgetBundle {
    var body: some Widget {
        FoodDeliveryLiveActivityWidget()
    }
}

@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityWidget: Widget {
    var body: some WidgetConfiguration {
        ActivityConfiguration(for: FoodDeliveryLiveActivityAttributes.self) { context in
            // Lock Screen UI
            VStack {
                Text("Order from \(context.attributes.restaurantName)")
                Text("Status: \(context.state.orderStatus)") // possible status may include "Ordered", "Order accepted", "Preparing", "On the Way","Delivered"
            }
        } dynamicIsland: { context in
            // Dynamic Island UI
            DynamicIsland {
                // Expanded UI
            } compactLeading: {
                // Compact leading UI
            } compactTrailing: {
                // Compact trailing UI
            } minimal: {
                // Minimal UI
            }
        }
    }
}
```

## Stap 5: Een actieve activiteit lokaal starten (optioneel) {#local}

Hoewel Journey Optimizer op afstand Live-activiteiten kan starten, kunt u deze ook lokaal starten:

**Voorbeeld voor een Levende activiteit van de voedsellevering:**

```swift
let attributes = FoodDeliveryLiveActivityAttributes(
    liveActivityData: LiveActivityData(liveActivityID: "order123"),
    restaurantName: "Pizza Palace"
)

let contentState = FoodDeliveryLiveActivityAttributes.ContentState(
    orderStatus: "Ordered"
)

let activity = try Activity<FoodDeliveryLiveActivityAttributes>.request(
    attributes: attributes,
    contentState: contentState,
    pushType: .token
)
```

## Stap 6: Ondersteuning voor foutopsporing toevoegen (optioneel) {#debug}

Indien nodig kunt u fouten in Live activity-schema&#39;s opsporen in Adobe Assurance:

**Voorbeeld voor een Levende activiteit van de voedsellevering:**

```swift
@available(iOS 16.1, *)
extension FoodDeliveryLiveActivityAttributes: LiveActivityAssuranceDebuggable {
    static func getDebugInfo() -> (attributes: FoodDeliveryLiveActivityAttributes, state: ContentState) {
        return (
            FoodDeliveryLiveActivityAttributes(
                liveActivityData: LiveActivityData(liveActivityID: "debug-order-123"),
                restaurantName: "Debug Restaurant"
            ),
            ContentState(orderStatus: "Ordered")
        )
    }
}
```


