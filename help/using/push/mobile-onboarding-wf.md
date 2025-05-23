---
solution: Journey Optimizer
product: journey optimizer
title: Snelstartworkflow voor mobiele instaptoegang
description: Leer hoe u de workflow voor snel starten bij mobiel instappen kunt gebruiken
topic: Mobile
feature: Push
role: Admin
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 364ef926-3f92-4297-acbd-a283668106ac
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 2%

---

# Snelstartworkflow voor mobiele instaptoegang {#mobile-wf}

Het nieuwe **mobiele onboarding snel beginwerkschema** is een nieuwe producteigenschap om Adobe Experience Platform Mobile SDK snel te vormen, begint mobiele gebeurtenisgegevens te verzamelen en te bevestigen, en dupberichten met [!DNL Journey Optimizer] te verzenden.

Deze mogelijkheid is via de startpagina van **[!DNL Adobe Experience Platform Data Collection]** toegankelijk voor alle klanten als openbare Beta.

## Aan de slag{#gs-mobile-wf}

Deze nieuwe werkstroom automatiseert de opstelling van de Inzameling van Gegevens door het totale aantal kliks te verminderen en de mobiele configuratie voor Journey Optimizer te versnellen. Dit snelle beginwerkschema neemt u door vier gemakkelijke stappen aan [ opstelling ](##setup-mobile-wf), [ uit ](#implement-mobile-wf), [ bevestigt ](#valid-mobile-wf), en [ herziet ](#review-mobile-wf) uw mobiele configuratie.

Als u toegang wilt tot de nieuwe workflow voor snel aan boord gaan van mobiele apparaten, bladert u naar **[!DNL Data Collection]** via de oplossingsschakeloptie. Selecteer vervolgens de **[!DNL Start Collecting Mobile Data]** -kaart op de startpagina.

![](assets/mobile-wf-home.png)

Hieronder vindt u een aantal aanvullende kenmerken:

* Eenvoudige workflow in vier stappen en gebruikersinterface.
* Levert een basisopstelling om mobiele gebeurtenisgegevens via [ Adobe Experience Platform Mobile SDK ](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} te beginnen verzamelen  in notulen.
* De capaciteit om een basis mobiele duw gebeurtenis leveraging [ Adobe Experience Platform Assurance ](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=nl-NL){target="_blank"} te testen en te bevestigen .
* Auto leidt tot en vormt alle noodzakelijke Inzameling van Gegevens, en de activa van Journey Optimizer.
* In productbegeleiding en tooltips.
* Verstrekt een natuurlijke overgang voor geavanceerdere implementatie indien nodig.

## Instellen {#setup-mobile-wf}

In de eerste stap van deze workflow worden automatisch alle benodigde gegevensverzamelingen en Journey Optimizer-elementen gemaakt en geconfigureerd, zoals Mobile Properties, Mobile Extensions, Journey Optimizer Extension, Rules, Data Elements, enzovoort.

Nadat u de Beta-voorwaarden hebt geaccepteerd, voert u de naam van uw mobiele app in en klikt u op **[!DNL Next]** .

![](assets/mobile-wf-setup.png)

Geef informatie op voor iOS- en Android-platforms, zoals de toepassings-id en verificatietoetsen of het sleutelbestand.

## Implementeren{#implement-mobile-wf}

De volgende stap bevat stapsgewijze instructies voor het installeren van de code op uw mobiele app.

![](assets/mobile-wf-add-code.png)


## Valideren{#valid-mobile-wf}

De implementatie controleren en controleren om deze te valideren. U kunt een testpushmelding verzenden.

![](assets/mobile-wf-valid.png)


## Controleren {#review-mobile-wf}

De automatische opstelling wordt gedaan. U kunt nu naar de eigenschap mobile van uw tag gaan, uw regels of gegevenselement configureren en pushmeldingen verzenden met Adobe Journey Optimizer.

![](assets/mobile-wf-done.png)


**Verwante onderwerpen**

* [Aan de slag met pushmeldingen](get-started-push.md)
* [Gegevensstroom van pushmeldingen en componenten](push-gs.md)
* [Het pushkanaal configureren](push-configuration.md)
* [Pushmeldingenrapport](../reports/journey-global-report-cja-push.md#push-global)
* [Een pushmelding maken](create-push.md)
