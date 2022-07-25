---
title: Een SMS-bericht maken
description: Meer informatie over het maken van een SMS-bericht in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 3%

---

# Een SMS-bericht maken {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS-ontwerp"
>abstract="Voeg uw tekstbericht toe en begin het met de redacteur van de Uitdrukking aan te passen."

Gebruiken [!DNL Journey Optimizer] om tekstberichten naar uw klanten op hun mobiele apparaten te verzenden. U kunt berichten in tekstformaat van de redacteur van SMS tot stand brengen, personaliseren en voorproef.

Eenmaal [SMS toegevoegd](get-started-content.md) en gedefinieerde basisinstellingen, kunt u de **[!UICONTROL Actions: SMS]** in het rechterdeelvenster om de inhoud voor het SMS-bericht te maken.

>[!AVAILABILITY]
>
>Het SMS-kanaal is momenteel alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

![](assets/sms-edit-content.png)

Als dit de eerste keer is die tot een SMS-bericht leidt, zorg er dan voor dat het SMS-kanaal is geconfigureerd. [Meer informatie](../configuration/sms-configuration.md).

## Je SMS-inhoud definiëren{#sms-content}

Voer de volgende stappen uit om uw SMS-bericht aan te passen:

1. Klik op de knop **[!UICONTROL Message]** om de Expressieeditor te openen.

   ![](assets/sms-content.png)

1. Gebruik de expressie-editor om inhoud te definiëren. U kunt elk kenmerk gebruiken om inhoud aan te passen, zoals de profielnaam of plaats. Meer informatie over personalisatie in de Expressieeditor in [deze sectie](../personalization/personalize.md).

1. Klikken **[!UICONTROL Save]** en controleer uw bericht in de voorvertoning.

   ![](assets/sms-content-preview.png)


## Je SMS valideren{#sms-preview}

Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen. Als u [persoonlijke inhoud](../personalization/personalize.md), kunt u controleren hoe deze inhoud in het bericht wordt getoond, leveraging de gegevens van het testprofiel.

Als u wilt visualiseren hoe uw SMS-bericht wordt weergegeven op mobiele apparaten, klikt u op de knop **[!UICONTROL Simulate content]** tab. Meer informatie over het simuleren van inhoud vindt u in [deze sectie](../design/preview.md).

U moet ook waarschuwingen controleren in het bovenste gedeelte van de editor.  Sommige zijn eenvoudige waarschuwingen, maar andere kunnen voorkomen dat u het bericht gebruikt. Meer informatie in [deze sectie](alerts.md).

![](assets/sms-alert-button.png)


## Opt-in en opt-out{#sms-opt-in-out}

Voor alle marketingberichten moet het SMS een manier bevatten waarop de ontvangers het abonnement gemakkelijk kunnen opzeggen. Als u het abonnement opzegt, worden de profielen automatisch verwijderd uit het publiek van toekomstige marketingberichten. Het toevoegen van een koppeling voor het opzeggen van abonnementen is niet verplicht voor transactiemeldingen.

De ontvangers van SMS kunnen met opt-in en opt-out sleutelwoorden antwoorden. Conform de industriestandaarden en -voorschriften verwerkt Adobe Journey Optimizer automatisch de volgende trefwoorden in binnenkomende berichten: START, STOP en ONTSTOP. Deze trefwoorden activeren automatische standaardantwoorden van de SMS-provider.

Raadpleeg de volgende video voor meer informatie over de manier waarop native ondersteuning voor binnenkomende trefwoorden (start, stop en unstop) werkt voor SMS.

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

<!--
## How-to video

Learn how to configure, author, and include SMS messaging into your customer journeys.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)
-->
**Verwante onderwerpen**

* [Sms-kanaal configureren](../configuration/sms-configuration.md)
* [Sms-rapport](../reports/journey-global-report.md#sms-global)
* [Een nieuw bericht maken](get-started-content.md)
* [Een bericht toevoegen in een journey](../building-journeys/journeys-message.md)
