---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met reizen
description: Aan de slag met reizen
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: reis, ontdek, begin
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 7f21098d5ae157f1c0d3de3aa584564c6f73310a
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 1%

---


# Aan de slag met reizen{#jo-general-principle}

Gebruik [!DNL Journey Optimizer] om in real time orchestratiefase samen te stellen met gebruik van contextuele gegevens die zijn opgeslagen in gebeurtenissen of gegevensbronnen.

Ontwerp multistep geavanceerde scenario&#39;s aangedreven door de volgende mogelijkheden:

* Verzend in real time **unitaire levering** teweeggebracht wanneer een gebeurtenis wordt ontvangen, of **in partij** gebruikend het publiek van Adobe Experience Platform.

* Gebruik **contextafhankelijke gegevens** van gebeurtenissen, informatie van Adobe Experience Platform, of gegevens van de diensten van derdeAPI.

* Gebruik **ingebouwde acties** om berichten te verzenden die in [!DNL Journey Optimizer] worden ontworpen of **douaneacties** tot stand te brengen als u een derdesysteem gebruikt om uw berichten te verzenden.

* Met de **reisontwerper**, bouwt uw multi-step gebruiksgevallen: sleep en laat gemakkelijk een ingangsgebeurtenis of een gelezen publieksactiviteit vallen, voeg voorwaarden toe en verzend gepersonaliseerde berichten.

>[!NOTE]
>
>De gidsen en de beperkingen van de reis zijn gedetailleerd in [ deze pagina ](../start/guardrails.md)

## Stappen om een reis te maken{#steps-journey}

Met Adobe Journey Optimizer kunt u persoonlijke reizen ontwerpen en ordenen vanaf één canvas. De belangrijkste stappen om een reis tot stand te brengen zijn:

![](assets/journey-creation-process.png)

➡️ [ ontdekt deze eigenschap in video ](#video)

Adobe Journey Optimizer bevat een omnichannel orchestration canvas dat marketers in staat stelt marketingactiviteiten te harmoniseren met een-op-een-klantenservice. Met de gebruikersinterface kunt u activiteiten van het palet naar het canvas slepen om uw reis te maken.

![](assets/interface-journeys.png)

Leer hoe te om uw eerste reis in [ te beginnen en te creëren deze pagina ](journey-gs.md).

De omnichannel reisontwerper helpt u multi-step reizen met gericht publiek, updates bouwen die op klanten of bedrijfsinteractie in real time worden gebaseerd, en omnichannel berichten gebruikend een intuïtieve belemmering-en-dalingsinterface.

![](assets/journey38.png)

Lees meer in [ deze sectie ](using-the-journey-designer.md).

Als gegevensingenieur, zijn de stappen om uw reizen, met inbegrip van Gegevensbronnen, Gebeurtenissen en Acties te vormen gedetailleerd in [ deze sectie ](../configuration/about-data-sources-events-actions.md).


## Gebruiksscenario’s{#uc-journey}

Leer hoe u reizen kunt maken in de volgende gebruiksgevallen van begin tot eind.

Zaken voor zakelijk gebruik:

* [Multikanaalberichten verzenden](journeys-uc.md)
* [Een bericht verzenden met Campagne v7/v8](ajo-ac.md)
* [Een bericht verzenden naar abonnees](message-to-subscribers-uc.md)

Gevallen van technisch gebruik:

* [Verzamelingen dynamisch doorgeven met behulp van aangepaste handelingen](collections.md)
* [Productie beperken met externe gegevensbronnen en aangepaste handelingen](limit-throughput.md)

## Journeyversies{#journey-versions}

In de reislijst, worden alle reisversies getoond met het versieaantal. Zie [deze pagina](../building-journeys/using-the-journey-designer.md).

Wanneer u een reis zoekt, verschijnen de nieuwste versies bij de eerste keer dat de toepassing wordt geopend boven aan de lijst. Vervolgens kunt u de gewenste sortering definiëren en wordt deze door de toepassing als gebruikervoorkeur behouden. De versie van de reis wordt ook weergegeven boven aan de interface van de reiseditie, boven het canvas.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Gewoonlijk kan een profiel niet meerdere keren op dezelfde reis tegelijk aanwezig zijn. Als de terugkeer wordt toegelaten, kan een profiel een reis opnieuw ingaan, maar kan het niet doen tot zij dat vorige geval van de reis volledig verlaten. [Meer informatie](end-journey.md).

Als u zich aan een levende reis moet aanpassen, creeer een nieuwe versie van uw reis.

1. Open de meest recente versie van uw livereis, klik op **[!UICONTROL Create a new version]** en bevestig deze.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >U kunt alleen een nieuwe versie maken van de meest recente versie van een reis.

1. Breng uw wijzigingen aan, klik op **[!UICONTROL Publish]** en bevestig de selectie.

Vanaf het moment dat de reis wordt gepubliceerd, zullen individuen naar de recentste versie van de reis gaan. Mensen die al een vorige versie hebben ingevoerd, blijven er totdat ze klaar zijn met de reis. Als ze later weer dezelfde reis maken, gaan ze naar de meest recente versie.

Reisversies kunnen afzonderlijk worden gestopt. Alle versies van reizen hebben dezelfde naam.

Wanneer u een nieuwe versie van een reis publiceert, beëindigt de vorige versie automatisch en schakelt aan de **Gesloten** status. Er kan geen toegang tot de reis plaatsvinden. Zelfs als u de laatste versie stopt, blijft de vorige versie gesloten.

## Hoe kan ik-video {#video}

Ontdek de onderdelen van een reis en begrijp de grondbeginselen van het maken van een reis op het canvas.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)
