---
solution: Journey Optimizer
product: journey optimizer
title: Bericht exporteren in Journey Optimizer
description: Leer hoe u berichten exporteert
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: exporteren, berichten, HIPAA, e-mails, SMS, configuratie
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
source-git-commit: ab0f100d53cb987919eb134442bf05e64c30719a
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 1%

---

# Inhoud van berichten exporteren {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Verzonden inhoud behouden en exporteren"
>abstract="Als u deze optie selecteert, kunt u de inhoud van de verzonden e-mail- of SMS-berichten met deze configuratie schrijven naar een [!DNL Experience Platform] -gegevensset. Records blijven 7 kalenderdagen na inname bewaard, gedurende welke u ze naar uw eigen opslag kunt exporteren."

>[!AVAILABILITY]
>
>Deze mogelijkheid is alleen beschikbaar voor het e-mail- en sms-kanaal, voor organisaties die de add-on service Message Export hebben aangeschaft. Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

**Uitvoer van het Bericht** laat u verzonden e-mail en SMS berichtinhoud van [!DNL Journey Optimizer] naar uw eigen opslag via [!DNL Adobe Experience Platform] bestemmingen overbrengen, die u toelaten om gegevens uit [!DNL Experience Platform] in externe eindpunten te leveren. [Meer informatie](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"}

Met deze eigenschap, wordt de inhoud van e-mail en SMS berichten die via [!DNL Journey Optimizer] worden verzonden die voor de uitvoer zijn duidelijk geschreven aan de [!DNL Experience Platform] **Dataset van de Uitvoer van het Bericht van AJO**. [&#x200B; leer meer over datasets &#x200B;](../data/get-started-datasets.md)

De verslagen worden dan bewaard in de dataset voor zeven kalenderdagen vanaf opneming, waarin u hen uit naar het externe systeem van uw keus kunt uitvoeren.

## Guardrails

* Deze eigenschap steunt slechts de **E-mail** en **SMS** kanalen.
* De verslagen in de Dataset van de Uitvoer van het Bericht van AJO worden behouden **voor zeven kalenderdagen van opname**.
* Backfill wordt niet ondersteund voor berichten die worden verzonden voordat Message Export is ingeschakeld, zoals hieronder wordt beschreven.

## Bericht exporteren inschakelen {#enable-message-export}

Het aan boord nemen proces voor de eigenschap van de Uitvoer van het Bericht bestaat uit twee stappen:

1. [&#x200B; opstelling de uitvoerdataflow &#x200B;](#set-up-export-dataflow) in [!DNL Experience Platform];
1. [&#x200B; laat de Uitvoer van het Bericht &#x200B;](#config-message-export) bij de kanaalconfiguratie in [!DNL Journey Optimizer] toe.

>[!WARNING]
>
>Alleen nieuwe records na het inschakelen van exporteren en verzenden van berichten worden weergegeven. Er wordt geen ondersteuning geboden voor back-ups van inhoud voordat u het exportproces instelt en de optie Bericht exporteren inschakelt.

### De exportgegevensstroom instellen {#set-up-export-dataflow}

Voordat u uw gegevens kunt exporteren, moet u het exportproces instellen door de [!DNL Experience Platform] -bestemming en de gegevensset te definiëren die worden gebruikt. Voer de onderstaande stappen uit.

>[!NOTE]
>
>Deze instelling moet voor elke sandbox worden geconfigureerd.

1. Kies een Experience Platform [&#x200B; bestemmingstype &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/destination-types){target="_blank"}. Een lijst van beschikbare bestemmingsplatforms die klaar zijn om gegevens te ontvangen is beschikbaar op [&#x200B; deze pagina &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. In [!DNL Experience Platform], vorm uw bestemming door geloofsbrieven, emmertje/container, wegprefix, en veiligheidsopties te bepalen. [&#x200B; leer hoe &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Creeer een stroom van de datasetuitvoer gebruikend de volgende gegevens:

   * De dataset van Source: uitgezochte **Dataset van de Uitvoer van het Bericht van AJO**.
   * Bestandsindeling: selecteer JSON of Parquet (kies een optie op basis van downstreamgereedschappen).
   * Plan: zorg ervoor dat het programma binnen het retentievenster van 7 dagen wordt uitgevoerd.

### Bericht exporteren inschakelen in de kanaalconfiguratie {#config-message-export}

Om de Uitvoer van het Bericht op uw campagnes en reizen toe te passen, moet u de specifieke optie op het niveau van de kanaalconfiguratie toelaten. Voer de onderstaande stappen uit.

1. In [!DNL Journey Optimizer], geef of creeer de gewenste E-mail of van SMS [&#x200B; kanaalconfiguratie &#x200B;](channel-surfaces.md#create-channel-surface) uit.

1. Selecteer de optie **[!UICONTROL Enable Message Export]** .

   ![](assets/config-message-export.png)

1. Sla uw wijzigingen op en verzend uw kanaalconfiguratie.

Zodra u berichten via campagnes of reizen gebruikend deze kanaalconfiguratie hebt verzonden, worden de e-mail en de berichten van SMS geschreven aan de **Dataset van de Uitvoer van het Bericht van AJO**. U kunt [&#x200B; tot de verslagen &#x200B;](#access-exported-data) in de dataset dan toegang hebben en hen uitvoeren naar uw geselecteerde opslagbestemming die op de de uitvoerdataflow wordt gebaseerd die u bepaalde.

>[!NOTE]
>
>Als u de schakeloptie **[!UICONTROL Enable Message Export]** uitschakelt, worden nieuwe records voor deze kanaalconfiguratie niet meer opgenomen in de gegevensset. Bestaande records blijven bewaard totdat het retentietijdstip is verlopen.

## Geëxporteerde berichtengegevens openen {#access-exported-data}

Nadat de berichten gebruikend een kanaalconfiguratie met toegelaten de Uitvoer van het Bericht zijn verzonden, kunt u tot de uitgevoerde gegevens in de **Dataset van de Uitvoer van het Bericht van AJO toegang hebben en herzien**.

De geëxporteerde berichtgegevens weergeven:

1. Navigeer in [!DNL Journey Optimizer] naar **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** in de linkernavigatie. [&#x200B; leer meer over datasets &#x200B;](../data/get-started-datasets.md)

1. Zorg ervoor u systeem-geproduceerde datasets toont.

1. Selecteer de **Dataset van de Uitvoer van het Bericht van AJO** van de lijst.

   ![](assets/datasets-list.png)

1. Klik op de pagina met gegevens over de gegevensset op **[!UICONTROL Preview dataset]** om de meest recente records weer te geven.

   ![](assets/ajo-message-export-dataset.png)

De dataset bevat uitvoerige informatie voor elk bericht dat via de kanaalconfiguratie met toegelaten de Uitvoer van het Bericht wordt verzonden, met inbegrip van: onderwerpregel, berichtlichaam, ontvangend e-mailadres of telefoonaantal, verzender adres of telefoonaantal, verzonden datum en tijd, verpersoonlijkingsgegevens, en meer.

Alle verslagen in de dataset worden behouden voor **zeven kalenderdagen van opname**. Tijdens deze bewaarperiode, kunt u tot de gegevens voor nalevingscontroles, wettelijke onderzoeken toegang hebben, of het uitvoeren naar uw eigen opslagsysteem via de gevormde bestemming van Experience Platform.

