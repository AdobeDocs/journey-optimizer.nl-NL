---
title: Een bericht verzenden naar abonnees
description: Leer hoe u een reis bouwt om een bericht naar de abonnees van een lijst te verzenden
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: dee8dbac067dac851af02d87a3dece1ba2b29376
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 3%

---

# Hoofdlettergebruik: een bericht sturen naar de abonnees van een lijst{#send-a-message-to-the-subscribers-of-a-list}

Het doel van dit gebruiksgeval is een reis tot stand te brengen om een bericht naar de abonnees van een lijst te verzenden.

In dit voorbeeld wordt **[!UICONTROL Consent and Preference Details]** veldgroep van [!DNL Adobe Experience Platform] wordt gebruikt. Als u deze veldgroep wilt zoeken, gaat u naar **[!UICONTROL Data Management]** menu, kiest u **[!UICONTROL Schemas]**. Op de **[!UICONTROL Field groups]** voert u de naam van de veldgroep in het zoekveld in.

![Deze veldgroep bevat het abonnementselement](assets/consent-and-preference-details-field-group.png)

Om deze reis te vormen, volg deze stappen:

1. Maak een reis die begint met een **[!UICONTROL Read]** activiteit. [Meer informatie](journey-gs.md).
1. Voeg een **[!UICONTROL Message]** activiteit, met een e-mail, aan de reis. [Meer informatie](journeys-message.md).
1. In de **[!UICONTROL Email parameters]** van de **[!UICONTROL Message]** activiteiteninstellingen, vervang het standaard e-mailadres (`PersonalEmail.adress`) met het e-mailadres van de abonnees van de lijst:

   1. Klik op de knop **[!UICONTROL Enable parameter override]** pictogram rechts van **[!UICONTROL Address]** en klik vervolgens op de knop **[!UICONTROL Edit]** pictogram.

      ![](assets/message-to-subscribers-uc-1.png)

      U kunt het e-mailadres alleen wijzigen als u het bericht al eerder hebt gepubliceerd.

   1. Voer in de expressieeditor de expressie in om de e-mailadressen van de abonnees op te halen. [Meer informatie](expression/expressionadvanced.md).

      In dit voorbeeld wordt een expressie getoond die verwijzingen naar kaartvelden bevat:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      In dit voorbeeld worden de volgende functies gebruikt:

      | -functie | Beschrijving | Voorbeeld |
      | --- | --- | --- |
      | `entry` | Verwijs naar een kaartelement volgens geselecteerde namespace | Een specifieke abonnementenlijst bekijken |
      | `firstEntryKey` | De eerste entry-sleutel van een kaart ophalen | Het eerste e-mailadres van abonnees ophalen |

      In dit voorbeeld krijgt de abonnementenlijst de naam `daily-email`. E-mailadressen worden gedefinieerd als sleutels in het dialoogvenster `subscribers` kaart, die aan de kaart van de abonnementenlijst wordt verbonden.

      Meer informatie over [verwijzingen naar velden](expression/field-references.md) in expressies.

      ![](assets/message-to-subscribers-uc-2.png)

   1. In de **[!UICONTROL Add an expression]** dialoogvenster, klikt u op **[!UICONTROL Ok]**.

   ![](assets/message-to-subscribers-uc-3.png)

1. Beëindig de reis met een **[!UICONTROL End]** activiteit.
