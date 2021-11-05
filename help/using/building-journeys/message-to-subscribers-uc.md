---
title: Een bericht verzenden naar abonnees
description: Leer hoe u een reis bouwt om een bericht naar de abonnees van een lijst te verzenden
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 59ee283f50850e160e7a6506c1f0deab1976f20c
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 2%

---

# Een bericht verzenden naar de abonnees van een lijst

Het doel van dit gebruiksgeval is een reis tot stand te brengen om een bericht naar de abonnees van een lijst te verzenden.

In dit voorbeeld wordt **[!UICONTROL Consent and Preference Details]** veldgroep van [!DNL Adobe Experience Platform] wordt gebruikt. Als u deze veldgroep wilt zoeken, gaat u naar **[!UICONTROL Data Management]** menu, kiest u **[!UICONTROL Schemas]**. Op de **[!UICONTROL Field groups]** voert u de naam van de veldgroep in het zoekveld in.

![Deze veldgroep bevat het abonnementselement](../assets/consent-and-preference-details-field-group.png)

Om deze reis te vormen, volg deze stappen:

1. Maak een reis die begint met een **[!UICONTROL Read]** activiteit. [Meer informatie](journey-gs.md).
1. Voeg een **[!UICONTROL Message]** activiteit, met een e-mail, aan de reis. [Meer informatie](journeys-message.md).
1. In de **[!UICONTROL Email parameters]** van de **[!UICONTROL Message]** activiteiteninstellingen, vervang het standaard e-mailadres (`PersonalEmail.adress`) met het e-mailadres van de abonnees van de lijst:

   1. Klik op de knop **[!UICONTROL Enable parameter override]** pictogram rechts van **[!UICONTROL Address]** en klik vervolgens op de knop **[!UICONTROL Edit]** pictogram.

      ![](../assets/message-to-subscribers-uc-1.png)

      U kunt het e-mailadres alleen wijzigen als u het bericht al eerder hebt gepubliceerd.

   1. Voer in de expressieeditor de expressie in om de e-mailadressen van de abonnees op te halen. [Meer informatie](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html){target=&quot;_blank&quot;}.

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

      Meer informatie over [verwijzingen naar velden](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/syntax/field-references.html) in expressies.

      ![](../assets/message-to-subscribers-uc-2.png)

   1. In de **[!UICONTROL Add an expression]** dialoogvenster, klikt u op **[!UICONTROL Ok]**.

   ![](../assets/message-to-subscribers-uc-3.png)

1. Beëindig de reis met een **[!UICONTROL End]** activiteit.




