---
title: Een SMS-bericht maken
description: Meer informatie over het maken van een SMS-bericht in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 630b8ef5a140709161b24256083b2104be5b6121
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 5%

---

# Een SMS-bericht maken {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS-ontwerp"
>abstract="Voeg uw tekstbericht toe en begin het met de Redacteur van de Uitdrukking aan te passen."

Eenmaal [een bericht gemaakt](get-started-content.md), gebruikt u de **[!UICONTROL SMS]** om de instellingen en inhoud voor het SMS-bericht te definiëren.


>[!AVAILABILITY]
>
>Het SMS-kanaal is momenteel alleen beschikbaar voor een aantal organisaties (Beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

![](assets/sms_1.png)

Als dit de eerste keer is die tot een SMS-bericht leidt, zorg er dan voor dat het SMS-kanaal is geconfigureerd. [Meer informatie](../configuration/sms-configuration.md).

## Je SMS-inhoud definiëren{#sms-content}

Voer de volgende stappen uit om uw SMS-bericht aan te passen:

1. Klik op de knop **[!UICONTROL Add text message]** om de Expressieeditor te openen.

   ![](assets/sms_3.png)

1. Gebruik de Expressieeditor om inhoud te definiëren. U kunt elk kenmerk gebruiken om inhoud aan te passen, zoals de profielnaam of plaats. Meer informatie over personalisatie in de Expressieeditor vindt u in [deze sectie](../personalization/personalize.md)

   >[!NOTE]
   >
   > Een SMS-bericht kan maximaal 160 tekens bevatten, inclusief spaties en regeleinden.

   ![](assets/sms_2.png)

1. Klikken **[!UICONTROL Save]** wanneer uw bericht klaar is.

## Je SMS valideren{#sms-preview}

Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen. Als u [persoonlijke inhoud](../personalization/personalize.md), kunt u controleren hoe deze inhoud in het bericht wordt getoond, leveraging de gegevens van het testprofiel.

Blader naar de **[!UICONTROL Preview]** tab.

Raadpleeg [deze sectie](../design/preview.md) voor meer informatie.

## Je SMS publiceren {#sms-publish}

Zodra uw bericht klaar is, kunt u het publiceren om het voor uitvoering beschikbaar te maken met **[!UICONTROL Publish]** knop. Deze actie publiceert de nieuwe versie van het bericht dat voor de volgende terechtstellingen in uw reizen zal worden gebruikt.

Je SMS-bericht kan nu worden gebruikt voor een reis. [Leer hoe u reizen maakt](../building-journeys/journey-gs.md).

## Opt-in en opt-out{#sms-opt-in-out}

Voor alle marketingberichten moet het SMS een manier bevatten waarop de ontvangers het abonnement gemakkelijk kunnen opzeggen. Als u het abonnement opzegt, worden de profielen automatisch verwijderd uit het publiek van toekomstige marketingberichten. Het toevoegen van een koppeling voor het opzeggen van abonnementen is niet verplicht voor transactiemeldingen.

De ontvangers van SMS kunnen met opt-in en opt-out sleutelwoorden antwoorden. Conform de industriestandaarden en -voorschriften verwerkt Adobe Journey Optimizer automatisch de volgende trefwoorden in binnenkomende berichten: START, STOP en ONTSTOP. Deze trefwoorden activeren automatische standaardantwoorden van de SMS-provider.

Raadpleeg de volgende video voor meer informatie over de manier waarop native ondersteuning voor binnenkomende trefwoorden (start, stop en unstop) werkt voor SMS.

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

## Hoe kan ik-video

Leer hoe te, auteur, en omvat SMS overseinen in uw klantenreizen te vormen.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)

**Verwante onderwerpen**

* [Sms-kanaal configureren](../configuration/sms-configuration.md)
* [Sms-rapport](../reports/journey-global-report.md#sms-global)
* [Een nieuw bericht maken](get-started-content.md)
* [Een bericht toevoegen in een journey](../building-journeys/journeys-message.md)
