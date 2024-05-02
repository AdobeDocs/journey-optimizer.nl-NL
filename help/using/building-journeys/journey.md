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
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 1%

---


# Aan de slag met reizen{#jo-general-principle}

Gebruiken [!DNL Journey Optimizer] gebruiken voor het maken van realtime-formulieren voor het orkestgebruik met gebruik van contextuele gegevens die zijn opgeslagen in gebeurtenissen of gegevensbronnen.

Ontwerp multistep geavanceerde scenario&#39;s aangedreven door de volgende mogelijkheden:

* In real time verzenden **unitaire levering** geactiveerd wanneer een gebeurtenis wordt ontvangen, of **in batch** met Adobe Experience Platform-publiek.

* Hefboomwerking **contextafhankelijke gegevens** uit gebeurtenissen, informatie van Adobe Experience Platform of gegevens van externe API-services.

* Gebruik de **ingebouwde handelingen** om berichten te verzenden die zijn ontworpen in [!DNL Journey Optimizer] of maak **aangepaste handelingen** als u een systeem van derden gebruikt om uw berichten te verzenden.

* Met de **reisontwerper** bouwt u gebruiksscenario&#39;s voor meerdere stappen samen: sleep en zet eenvoudig een entry-gebeurtenis of een activiteit voor een lezenpubliek neer, voeg voorwaarden toe en verzend gepersonaliseerde berichten.

>[!NOTE]
>
>Reishandleidingen en -beperkingen worden beschreven in [deze pagina](../start/guardrails.md)

## Stappen om een reis te maken{#steps-journey}

Met Adobe Journey Optimizer kunt u persoonlijke reizen ontwerpen en ordenen vanaf één canvas. De belangrijkste stappen om een reis tot stand te brengen zijn:

![](assets/journey-creation-process.png)

➡️ [Deze functie in video detecteren](#video)

Adobe Journey Optimizer bevat een omnichannel orchestration canvas dat marketers in staat stelt marketingactiviteiten te harmoniseren met een-op-een-klantenservice. Met de gebruikersinterface kunt u activiteiten van het palet naar het canvas slepen om uw reis te maken.

![](assets/interface-journeys.png)

Leer hoe u begint en uw eerste reis maakt in [deze pagina](journey-gs.md).

De omnichannel reisontwerper helpt u multi-step reizen met gericht publiek, updates bouwen die op klanten of bedrijfsinteractie in real time worden gebaseerd, en omnichannel berichten gebruikend een intuïtieve belemmering-en-dalingsinterface.

![](assets/journey38.png)

Meer informatie in [deze sectie](using-the-journey-designer.md).

Als gegevensingenieur, zijn de stappen om uw reizen te vormen, met inbegrip van Gegevensbronnen, Gebeurtenissen en Acties gedetailleerd in [deze sectie](../configuration/about-data-sources-events-actions.md).


## Gebruiksscenario’s{#uc-journey}

Leer hoe u reizen kunt maken in de volgende gebruiksgevallen van begin tot eind.

Zaken voor zakelijk gebruik:

* [Multikanaalberichten verzenden](journeys-uc.md)
* [Een bericht verzenden met Campagne v7/v8](ajo-ac.md)
* [Een bericht verzenden naar abonnees](message-to-subscribers-uc.md)

Gevallen van technisch gebruik:

* [Verzamelingen dynamisch doorgeven met behulp van aangepaste handelingen](collections.md)
* [Leveringen opwaarderen](ramp-up-deliveries-uc.md)
* [Productie beperken met externe gegevensbronnen en aangepaste handelingen](limit-throughput.md)

## Journeyversies{#journey-versions}

In de reislijst, worden alle reisversies getoond met het versieaantal. Zie [deze pagina](../building-journeys/using-the-journey-designer.md).

Wanneer u een reis zoekt, verschijnen de nieuwste versies bij de eerste keer dat de toepassing wordt geopend boven aan de lijst. Vervolgens kunt u de gewenste sortering definiëren en wordt deze door de toepassing als gebruikervoorkeur behouden. De versie van de reis wordt ook weergegeven boven aan de interface van de reiseditie, boven het canvas.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Gewoonlijk kan een profiel niet meerdere keren op dezelfde reis tegelijk aanwezig zijn. Als re-entry wordt toegelaten, kan een profiel een reis opnieuw ingaan, maar kan het niet doen tot zij dat vorige geval van de reis volledig verlaten. [Meer informatie](end-journey.md).

Als u zich aan een levende reis moet aanpassen, creeer een nieuwe versie van uw reis.

1. Open de nieuwste versie van uw livereis en klik op **[!UICONTROL Create a new version]** en bevestigen.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >U kunt alleen een nieuwe versie maken van de meest recente versie van een reis.

1. Breng de gewenste wijzigingen aan en klik op **[!UICONTROL Publish]** en bevestigen.

Vanaf het moment dat de reis wordt gepubliceerd, zullen individuen naar de recentste versie van de reis gaan. Mensen die al een vorige versie hebben ingevoerd, blijven er totdat ze klaar zijn met de reis. Als ze later weer dezelfde reis maken, gaan ze naar de meest recente versie.

Reisversies kunnen afzonderlijk worden gestopt. Alle versies van reizen hebben dezelfde naam.

Wanneer u een nieuwe versie van een reis publiceert, automatisch beëindigt de vorige versie en schakelt naar **Gesloten** status. Er kan geen toegang tot de reis plaatsvinden. Zelfs als u de laatste versie stopt, blijft de vorige versie gesloten.

## Hoe kan ik-video {#video}

Ontdek de onderdelen van een reis en begrijp de grondbeginselen van het maken van een reis op het canvas.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)
