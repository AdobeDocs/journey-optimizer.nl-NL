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
badge: label="Beperkte beschikbaarheid" type="Informative"
hide: true
hidefromtoc: true
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
source-git-commit: c62653af3c1eacaaf55dcf181d33f2253521e33d
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 1%

---

# Inhoud van berichten exporteren {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Verzonden inhoud behouden en exporteren"
>abstract="Als u deze optie selecteert, kunt u de inhoud van de verzonden e-mail- of SMS-berichten met deze configuratie schrijven naar een [!DNL Experience Platform] -gegevensset. Records worden gedurende 3 kalenderdagen bewaard, gedurende welke u ze naar uw eigen opslag kunt exporteren."

>[!AVAILABILITY]
>
>Deze functie is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

**Uitvoer van het Bericht** laat u verzonden e-mail en SMS berichtinhoud van [!DNL Journey Optimizer] naar uw eigen opslag via [!DNL Adobe Experience Platform] bestemmingen overbrengen, die toelaten om gegevens uit [!DNL Experience Platform] in externe eindpunten te leveren. [Meer informatie](https://experienceleague.adobe.com/nl/docs/experience-platform/destinations/home){target="_blank"}

Met deze eigenschap, wordt de inhoud van e-mail en SMS berichten die via [!DNL Journey Optimizer] worden verzonden die voor de uitvoer zijn duidelijk geschreven aan de [!DNL Experience Platform] **Dataset van de Uitvoer van het Bericht van AJO**.

De verslagen worden dan bewaard in de **Dataset van de Uitvoer van het Bericht van AJO** voor drie kalenderdagen, waarin u hen uit naar het externe systeem van uw keus kunt uitvoeren.
<!--
## Terminology

* **[!DNL Experience Platform] destinations** - Framework to deliver data out of Experience Platform into external endpoints. [Learn more](https://experienceleague.adobe.com/nl/docs/experience-platform/destinations/home){target="_blank"}
* **AJO Message Export Dataset** - An [!DNL Experience Platform] dataset which stores the message content of email and SMS messages sent via [!DNL Journey Optimizer] which have been marked for export.
* **Retention**: Records in the AJO Message Export Dataset are retained for 3 calendar days from ingestion.-->

## Guardrails

* Deze functie ondersteunt alleen de e-mail- en SMS-kanalen.
* De verslagen in de Dataset van de Uitvoer van het Bericht van AJO worden bewaard drie kalenderdagen vanaf opneming.
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

1. Kies een Experience Platform [&#x200B; bestemmingstype &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/destinations/destination-types){target="_blank"}. Een lijst van beschikbare bestemmingsplatforms die klaar zijn om gegevens te ontvangen is beschikbaar op [&#x200B; deze pagina &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. In [!DNL Experience Platform], vorm uw bestemming door geloofsbrieven, emmertje/container, wegprefix, en veiligheidsopties te bepalen. [&#x200B; leer hoe &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Creeer een stroom van de datasetuitvoer gebruikend de volgende gegevens:

   * De dataset van Source: uitgezochte **Dataset van de Uitvoer van het Bericht van AJO**.
   * Bestandsindeling: selecteer JSON of Parquet (kies een optie op basis van downstreamgereedschappen).
   * Plan: zorg ervoor dat het programma binnen het retentievenster van 3 dagen wordt uitgevoerd.

### Bericht exporteren inschakelen in de kanaalconfiguratie {#config-message-export}

Om de Uitvoer van het Bericht op uw campagnes en reizen toe te passen, moet u de specifieke optie op het niveau van de kanaalconfiguratie toelaten. Voer de onderstaande stappen uit.

1. In [!DNL Journey Optimizer], geef of creeer de gewenste E-mail of van SMS [&#x200B; kanaalconfiguratie &#x200B;](channel-surfaces.md#create-channel-surface) uit.

1. Selecteer de optie **[!UICONTROL Enable Message Export]** .

   ![](assets/config-message-export.png)

1. Sla uw wijzigingen op en verzend uw kanaalconfiguratie.

De e-mail en SMS berichten die via campagnes of reizen worden verzonden gebruikend deze kanaalconfiguratie worden geschreven aan de **Dataset van de Uitvoer van het Bericht van AJO**. De records worden vervolgens naar de geselecteerde opslagbestemming geëxporteerd op basis van de exportgegevensstroom die u hebt gedefinieerd.

Als u de schakeloptie **[!UICONTROL Enable Message Export]** uitschakelt, worden nieuwe records voor deze kanaalconfiguratie niet meer opgenomen in de gegevensset. Bestaande records blijven bewaard totdat het retentietijdstip is verlopen.
