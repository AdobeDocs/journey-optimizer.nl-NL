---
solution: Journey Optimizer
product: journey optimizer
title: Een SMS/MMS-bericht maken
description: Meer informatie over het maken van een SMS/MMS-bericht in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 2%

---

# Een SMS/MMS/RCS-bericht maken {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Een tekstbericht maken"
>abstract="Om een tekstbericht (SMS/MMS/RCS) tot stand te brengen, voeg een actie van SMS in een reis of een campagne toe en begin het met de verpersoonlijkingsredacteur aan te passen."

>[!AVAILABILITY]
>
>RCS is geen HIPAA-Ready Service en mag niet worden gebruikt voor het verzamelen, opslaan of verwerken van gevoelige persoonlijke gegevens, waaronder toegestane gezondheidsgegevens, zoals persoonlijke gezondheidsinformatie, die uw organisatie anders in Journey Optimizer mag verwerken.

U kunt tekst (SMS), RCS- en MMS-berichten (Rich Communication) en multimedia-berichten met Adobe Journey Optimizer ontwerpen en verzenden. U moet eerst een actie van SMS in een reis of een campagne toevoegen, en dan de inhoud van het tekstbericht bepalen, zoals hieronder beschreven. Adobe Journey Optimizer biedt ook mogelijkheden om uw tekstberichten te testen voordat ze worden verzonden, zodat u de rendering, personalisatiekenmerken en alle andere instellingen kunt controleren.

In overeenstemming met de industriestandaarden en -voorschriften moeten alle SMS/MMS-marketingberichten een manier bevatten waarop de ontvangers hun abonnement gemakkelijk kunnen opzeggen. Om dit te doen, kunnen de ontvangers van SMS met opt-in en opt-out sleutelwoorden antwoorden. [&#x200B; Leer hoe te om opt-out te beheren &#x200B;](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

## Een tekstbericht toevoegen {#create-sms-journey-campaign}

Blader op de onderstaande tabbladen om te leren hoe u een tekstbericht (SMS/MMS/RCS) kunt toevoegen aan een campagne of een reis.

>[!BEGINTABS]

>[!TAB voeg een tekstbericht aan een Reis  toe]

1. Open uw reis dan belemmering en laat vallen een activiteit van SMS van de **sectie van Acties** van het palet.

   ![](assets/sms_create_1.png)

1. Verstrek basisinformatie over uw bericht (etiket, beschrijving, categorie), dan kies de berichtconfiguratie aan gebruik.

   ![](assets/sms_create_2.png)

   Voor meer informatie over hoe te om een reis te vormen, verwijs naar [&#x200B; deze pagina &#x200B;](../building-journeys/journey-gs.md)

   Het veld **[!UICONTROL configuration]** wordt standaard voorgevuld met de laatste configuratie die de gebruiker voor dat kanaal heeft gebruikt.

U kunt nu de inhoud van uw SMS-bericht ontwerpen via de knop **[!UICONTROL Edit content]** , zoals hieronder wordt beschreven.

>[!TAB  voeg een tekstbericht aan een Campagne toe ]

1. Open het menu **[!UICONTROL Campaigns]** en klik op **[!UICONTROL Create campaign]** .

1. Selecteer het type campagne dat u wilt uitvoeren

   * **Gepland - Op de markt brengend**: voer onmiddellijk de campagne of op een gespecificeerde datum uit. Geplande campagnes zijn gericht op het verzenden van marketingberichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **API-teweeggebracht - Marketing/Transactioneel**: voer de campagne uit gebruikend een API vraag. API-getriggerde campagnes zijn gericht op het verzenden van marketing- of transactiemeldingen, d.w.z. berichten die worden verzonden na een actie van een individu: wachtwoordinstelling, winkelwagentje enz.

1. Bewerk in de sectie **[!UICONTROL Properties]** de items **[!UICONTROL Title]** en **[!UICONTROL Description]** van uw campagne.

1. Klik op de knop **[!UICONTROL Select audience]** om het doelpubliek in de lijst met beschikbare Adobe Experience Platform-soorten publiek te definiëren. [Meer informatie](../audience/about-audiences.md).

1. Kies in het veld **[!UICONTROL Identity namespace]** de naamruimte die u wilt gebruiken om de personen van het geselecteerde publiek te identificeren. [Meer informatie](../event/about-creating.md#select-the-namespace).

1. Kies in de sectie **[!UICONTROL Actions]** de **[!UICONTROL SMS]** en selecteer of maak een nieuwe configuratie.

   Leer meer over de configuratie van SMS op [&#x200B; deze pagina &#x200B;](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Klik op **[!UICONTROL Create experiment]** om uw inhoudexperiment te configureren en behandelingen te maken om de prestaties te meten en de beste optie voor uw doelgroep te identificeren. [Meer informatie](../content-management/content-experiment.md)

1. Geef in de sectie **[!UICONTROL Actions tracking]** op of u wilt bijhouden of er op koppelingen in uw SMS-bericht wordt geklikt.

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe te om **[!UICONTROL Schedule]** van uw campagne in [&#x200B; te vormen deze sectie &#x200B;](../campaigns/create-campaign.md#schedule).

1. Kies in het menu **[!UICONTROL Action triggers]** de **[!UICONTROL Frequency]** van uw SMS-bericht:

   * Eenmaal
   * Dagelijks
   * Wekelijks
   * Maand

U kunt nu de inhoud van uw tekstbericht ontwerpen via de knop **[!UICONTROL Edit content]** , zoals hieronder wordt beschreven.

>[!ENDTABS]

## SMS/RCS-inhoud definiëren{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="Je SMS-inhoud definiëren"
>abstract="Pas en verpersoonlijk uw tekstberichten (SMS/MMS/RCS) aan door de verpersoonlijkingsredacteur te gebruiken om de inhoud te bepalen en dynamische elementen op te nemen."

Volg onderstaande stappen om de inhoud van uw bericht te configureren. De montages voor MMS zijn gedetailleerd in [&#x200B; deze sectie &#x200B;](#mms-content).

1. Klik in het configuratiescherm van de reis of campagne op de knop **[!UICONTROL Edit content]** om de inhoud van het tekstbericht te configureren.

1. Klik op het veld **[!UICONTROL Message]** om de personalisatie-editor te openen.

   Voor RCS overseinen met Infobip, Twilio, of andere derdeleveranciers, kleef de vereiste JSON nuttige lading in uw [&#x200B; configuratie van douaneSMS &#x200B;](sms-configuration-custom.md#api-credential).

   ![](assets/sms-content.png)

1. Gebruik de verpersoonlijkingsredacteur om inhoud te bepalen, verpersoonlijking en dynamische inhoud toe te voegen. U kunt elk kenmerk gebruiken, bijvoorbeeld de profielnaam of plaats. U kunt ook voorwaardelijke regels definiëren. Blader naar de volgende pagina&#39;s om meer over [&#x200B; verpersoonlijking &#x200B;](../personalization/personalize.md) en [&#x200B; dynamische inhoud &#x200B;](../personalization/get-started-dynamic-content.md) in de verpersoonlijkingsredacteur te leren.

1. Nadat u de inhoud hebt gedefinieerd, kunt u bijgehouden URL&#39;s aan uw bericht toevoegen. Open hiertoe het menu **[!UICONTROL Helper functions]** en selecteer **[!UICONTROL Helpers]** .

   Om de functie te gebruiken die URL verkort, moet u eerst een subdomein vormen dat dan aan uw configuratie zal worden verbonden. [Meer informatie](sms-subdomains.md)

   >[!NOTE]
   >
   > Als u SMS-subdomeinen wilt openen en bewerken, moet u over de machtiging **[!UICONTROL Manage SMS Subdomains]** in de productiesandbox beschikken. Leer meer over toestemmingen in [&#x200B; deze sectie &#x200B;](../administration/high-low-permissions.md).

   ![](assets/sms_tracking_1.png)

1. Klik in het menu **[!UICONTROL Helper functions]** op **[!UICONTROL URL function]** en selecteer vervolgens **[!UICONTROL Add URL]** .

   ![](assets/sms_tracking_2.png)

   <!--The URL shortening function cannot be used within a fragment. TBC-->

1. Plak in het veld `originalUrl` de URL die u wilt verkorten en klik op **[!UICONTROL Save]** .

   >[!CAUTION]
   >
   > De levensduur van korte URL&#39;s is ingesteld op 30 dagen. Na deze periode zijn deze korte URL&#39;s niet meer toegankelijk en wordt het bericht `404 short-code not found` weergegeven.

1. Klik op **[!UICONTROL Save]** en controleer uw bericht in de voorvertoning. U kunt nu uw berichtinhoud zoals die in [&#x200B; wordt gedetailleerd deze sectie &#x200B;](#sms-mms-test) testen en controleren.

## Uw MMS-inhoud definiëren{#mms-content}

U kunt uw communicatie verbeteren door MMS-berichten (Multimedia Message Service) te verzenden, waardoor het delen van media zoals video&#39;s, foto&#39;s, audioclips en GIF&#39;s en meer mogelijk is. Bovendien staat MMS maximaal 1600 tekens tekst in uw bericht toe.

>[!NOTE]
>
> Het kanaal van MMS komt met een paar beperkingen die op [&#x200B; worden vermeld deze pagina &#x200B;](../start/guardrails.md#sms-guardrails).

Ga als volgt te werk om MMS-inhoud te maken:

1. Creeer SMS zoals die in [&#x200B; wordt beschreven deze sectie &#x200B;](#create-sms-journey-campaign).

1. Bewerk uw inhoud van SMS zoals die in [&#x200B; wordt gedetailleerd deze sectie &#x200B;](#sms-content).

1. Schakel de optie MMS in om media toe te voegen aan uw SMS-inhoud.

   ![](assets/sms_create_6.png)

1. Voeg een **[!UICONTROL Title]** toe aan uw media.

1. Voer in het veld **[!UICONTROL Media]** de URL van uw media in.

   ![](assets/sms_create_7.png)

1. Klik op **[!UICONTROL Save]** en controleer uw bericht in de voorvertoning. U kunt nu de inhoud van uw bericht testen en controleren, zoals hieronder wordt beschreven.

## Uw berichten testen en verzenden {#sms-mms-test}

Gebruik de knop **[!UICONTROL Simulate content]** om een voorvertoning weer te geven van de inhoud van uw tekstbericht, verkorte URL&#39;s en gepersonaliseerde inhoud.

![](assets/sms-content-preview.png)

Nadat u de tests hebt uitgevoerd en de inhoud hebt gevalideerd, kunt u uw tekstbericht naar het publiek sturen. Deze stappen zijn gedetailleerd op [&#x200B; deze pagina &#x200B;](send-sms.md)

Zodra verzonden, kunt u het effect van uw SMS binnen de Campagne of rapporten van de Reis meten. Raadpleeg [deze sectie](../reports/campaign-global-report-cja-sms.md) voor meer informatie over rapporten.

**Verwante onderwerpen**

* [Een tekstbericht voorvertonen, testen en verzenden](send-sms.md)
* [Sms-kanaal configureren](sms-configuration.md)
* [SMS/MMS-rapporten](../reports/journey-global-report-cja-sms.md)
* [Een bericht toevoegen tijdens een rit](../building-journeys/journeys-message.md)
* [Een bericht toevoegen aan een campagne](../campaigns/create-campaign.md)
