---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met tekstberichten (SMS/MMS/RCS)
description: Meer informatie over het maken en verzenden van tekstberichten in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
source-git-commit: de418dc4feefd99231155c550ad3a51e4850ee66
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 3%

---

# Aan de slag met tekstberichten {#get-started-sms}

Gebruik [!DNL Journey Optimizer] om tekstberichten (SMS/MMS/RCS) naar uw klanten op hun mobiele apparaten te verzenden. U kunt berichten in tekstformaat van de redacteur tot stand brengen, personaliseren en voorproef.

Tekstberichten kunnen worden gemaakt en verzonden tijdens een rit of in een campagne. Gebruik voor SMS, MMS en RCS de SMS-handeling.

* In a **Reis**. Creeer een reis, voeg een activiteit van SMS toe, en bepaal basismontages. Blader vervolgens naar het deelvenster SMS-handelingen aan de rechterkant om de inhoud voor het SMS-, MMS- of RCS-bericht te maken. [ leer hoe te om een reis ](../building-journeys/journey-gs.md) tot stand te brengen

* In a **Campagne**. Maak een campagne, selecteer SMS als uw actie en definieer basisinstellingen. Vervolgens bewerkt u de inhoud van het bericht om het SMS-, MMS- of RCS-bericht te definiëren dat u wilt verzenden. Leer hoe te om [ een actiecampagne ](../campaigns/campaign-action.md#action-campaign-action) te creëren | [ een API-teweeggebrachte campagne ](../campaigns/api-triggered-campaigns.md) | [ een georkestreerde campagne ](../orchestrated/create-orchestrated-campaign.md#create)

>[!IMPORTANT]
>
>Als dit uw eerste keer het creëren van tekstberichten is, zorg ervoor het kanaal van SMS is gevormd. [Meer informatie](sms-configuration.md)

## Mogelijkheden voor tekstberichten {#sms-capabilities}

Adobe Journey Optimizer biedt uitgebreide mogelijkheden voor tekstberichten om uw klanten op meerdere kanalen te betrekken:

**SMS (de Korte Dienst van het Bericht)**

Verzend alleen-tekstberichten van maximaal 160 tekens. SMS is de meest ondersteunde indeling voor tekstberichten op alle mobiele apparaten.

**MMS (Multimedia Dienst van het Bericht)**

Verbeter uw communicatie met multimedia-inhoud, zoals video&#39;s, afbeeldingen, audioclips en GIF&#39;s. In MMS-berichten zijn naast mediabestanden maximaal 1600 tekens toegestaan. [ leer meer over MMS beperkingen ](../start/guardrails.md#sms-guardrails)

**RCS (Rich Communication Services)**

Verzend branded, interactieve berichten met geavanceerde eigenschappen zoals carrousels, rijke kaarten, voorgestelde acties, en verbeterde media steun. RCS verstrekt een rijkere overseinenervaring op gesteunde apparaten.

## Belangrijkste kenmerken {#key-features}

**Personalization &amp; Dynamische Inhoud**

Creeer gepersonaliseerde tekstberichten gebruikend de verpersoonlijkingsredacteur. Voeg profielkenmerken, voorwaardelijke inhoud en dynamische gegevens toe om berichten op maat te maken voor individuele ontvangers. [ Leer over verpersoonlijking ](../personalization/personalize.md)

**de Veelvoudige Steun van de Leverancier**

Adobe Journey Optimizer integreert met toonaangevende SMS-serviceproviders:

* **Sinch** - [ gids van de Configuratie ](sms-configuration-sinch.md)
* **Twilio** - [ gids van de Configuratie ](sms-configuration-twilio.md)
* **Infobip** - [ gids van de Configuratie ](sms-configuration-infobip.md)
* **Leveranciers van de Douane** - Vorm een andere leverancier van SMS gebruikend de integratie van douaneAPI. [Meer informatie](sms-configuration-custom.md)

**het Kortere maken URL &amp; het Volgen**

Voeg verkorte, trackable URLs aan uw berichten toe om betrokkenheid te controleren. Subdomeinconfiguratie is vereist voor URL-verkorting. [ Leer hoe te om subdomeinen van SMS te vormen ](sms-subdomains.md)

**Opt-out Beheer**

De naleving van industriestandaarden en -voorschriften garanderen door middel van een geïntegreerd opt-outbeheer. Journey Optimizer verwerkt automatisch standaardtrefwoorden (STOP, QUIT, CANCEL, enz.) voor Sinch- en Infobip-providers. [ Leer over opt-out beheer ](sms-opt-out.md)

**Voorproef &amp; het Testen**

Test uw tekstberichten voordat u ze verzendt met testprofielen en voorbeeldgegevens. Geef een voorvertoning weer van de personalisatie, de inhoud en de opmaak om te controleren of de berichten correct worden weergegeven. [ Leer hoe te om berichten ](send-sms.md) te verzenden

**Rapportering &amp; Analytics**

Houd de prestaties van uw SMS-campagnes en reizen bij met uitgebreide rapportagemogelijkheden:

* [SMS-campagnerapporten](../reports/campaign-global-report-cja-sms.md)
* [Vervoersrapporten voor SMS](../reports/journey-global-report-cja-sms.md)

## Configuratievereisten {#configuration-requirements}

Voordat u tekstberichten verzendt, moet u:

1. **kies een leverancier van SMS** - Uitgezocht van Sinch, Twilio, Infobip, of vorm een douaneleverancier
2. **Opstelling API geloofsbrieven** - Integreer API van uw leverancier tokens en de dienst IDs met Journey Optimizer
3. **creeer kanaalconfiguraties** - de configuraties van opstellingsSMS voor marketing en transactionele berichten
4. **vormt subdomeinen (facultatief)** - vereist slechts als u van plan bent om het verkorten van URL in uw berichten te gebruiken

Deze configuratiestappen worden typisch uitgevoerd door een Beheerder van het Systeem. [ worden begonnen met de configuratie van SMS ](sms-configuration.md)

## Handleiding voor snel starten {#quick-start}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="sms-configuration.md">
<img alt="Validatie" src="../assets/do-not-localize/sms-config.jpg">
</a>
<div>
<a href="sms-configuration.md"><strong>Sms-kanaal configureren</strong></a>
</div>
<p>Stel uw SMS-provider en kanaalconfiguraties in</p>
</td>
<td>
<a href="create-sms.md">
<img alt="Lood" src="../assets/do-not-localize/sms-create.jpeg">
</a>
<div><a href="create-sms.md"><strong> creeer een tekstbericht </strong></a>
</div>
<p>Ontwerp en pas uw inhoud van SMS, MMS, of RCS aan</p>
</td>
<td>
<a href="send-sms.md">
<img alt="Onfrequent" src="../assets/do-not-localize/sms-sending.jpg">
</a>
<div>
<a href="send-sms.md"><strong> Voorproef &amp; verzend </strong></a>
</div>
<p>Uw tekstberichten testen en verzenden naar uw publiek</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="Validatie" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong> beheert opt-outs </strong></a>
</div>
<p>Afhandeling van afmeldingsverzoeken en naleving garanderen</p>
</td>
</tr></table>

## Aanvullende bronnen {#additional-resources}

Blader hieronder naar de onderwerpen voor meer informatie over tekstberichten in Journey Optimizer.

+++Configuratiehulplijnen

Leer hoe u uw SMS-omgeving instelt en configureert:

* [Overzicht van de SMS-kanaalconfiguratie](sms-configuration.md)
* [SMS-kanaalconfiguraties maken](sms-configuration-surface.md)
* [SMS-subdomeinen configureren voor verkorting van URL&#39;s](sms-subdomains.md)

+++

+++Hulplijnen bij instellen provider

De geleidelijke configuratie voor elke dienstverlener van SMS:

* [Sinch-provider configureren](sms-configuration-sinch.md)
* [Twilio-provider configureren](sms-configuration-twilio.md)
* [Infobip-provider configureren](sms-configuration-infobip.md)
* [Aangepaste SMS-provider configureren](sms-configuration-custom.md)

+++

+++Inhoud maken en beheren

Maak, personaliseer en beheer de inhoud van uw tekstbericht:

* [SMS/MMS-berichten maken](create-sms.md)
* [Berichten voorvertonen, testen en verzenden](send-sms.md)
* [Personalization in tekstberichten](../personalization/personalize.md)
* [Dynamische inhoud](../personalization/get-started-dynamic-content.md)
* [SMS-inhoud genereren met AI Assistant](../content-management/generative-text.md)

+++

+++Compatibiliteit en privacy

Zorg ervoor dat uw tekstberichten voldoen aan de regels en privacystandaarden:

* [Uitschakelen, beheer](sms-opt-out.md)
* [Privacy en toestemming](../privacy/opt-out.md#opt-out-decision-management)

+++

+++Prestaties bijhouden

Bewaak en analyseer uw SMS-campagnes en reisprestaties:

* [SMS-campagnerapporten](../reports/campaign-global-report-cja-sms.md)
* [Vervoersrapporten voor SMS](../reports/journey-global-report-cja-sms.md)

+++

+++Integratie van reizen en campagnes

Leer hoe u SMS kunt opnemen in uw klantenreizen en campagnes:

* [SMS-berichten toevoegen aan reizen](../building-journeys/journeys-message.md)
* [SMS-campagnes maken](../campaigns/create-campaign.md)

+++

## Hoe kan ik-video&#39;s {#videos}

**vorm en verzend SMS berichten**

Leer hoe u sms-berichten configureert, opstelt en opneemt in uw klantjourneys.

+++Zie video

>[!VIDEO](https://video.tv.adobe.com/v/3420509?learn=on)

+++

**Onderzoek mobiele overseinenmogelijkheden**

Ontdek de uitgebreide mogelijkheden voor mobiel berichtenverkeer die Adobe Journey Optimizer aan marketers biedt.

+++Zie video

>[!VIDEO](https://video.tv.adobe.com/v/3426021?quality=12&learn=on)

+++

**verzend brandde RCS- berichten**

Leer hoe u merkgebonden, interactieve RCS-berichten in Adobe Journey Optimizer configureert en verzendt met een aangepaste SMS-provider.

+++Zie video

>[!VIDEO](https://video.tv.adobe.com/v/3464755)

+++

**Verwante onderwerpen**

* [Berichten toevoegen tijdens reizen](../building-journeys/journeys-message.md)
* [Marketingscampagnes maken](../campaigns/create-campaign.md)
* [Afvoerkanalen en beperkingen](../start/guardrails.md#sms-guardrails)
* [ SMS en mobiele overseinenleerprogramma&#39;s ](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/channels/sms-channel/sms-mms-messages-overview){target="_blank"}
