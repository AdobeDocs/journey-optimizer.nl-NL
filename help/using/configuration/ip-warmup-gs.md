---
solution: Journey Optimizer
product: journey optimizer
title: Ga aan de slag met IP-opwarmingsplannen
description: Leer hoe te om een IP warmup plan uit te voeren
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, groep, subdomeinen, leverbaarheid
hide: true
hidefromtoc: true
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---

# Ga aan de slag met IP-opwarmingsplannen {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* **[Ga aan de slag met IP-opwarming](ip-warmup-gs.md)**
* [IP-warmtecampagnes maken](ip-warmup-campaign.md)
* [Creeer een IP warmlopingsplan](ip-warmup-plan.md)
* [Voer het IP-opwarmingsplan uit](ip-warmup-running.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>De IP warmup eigenschap is momenteel beschikbaar als bèta om gebruikers slechts te selecteren. Neem contact op met de klantenservice van de Adobe om deel te nemen aan het bètaprogramma.

Met [!DNL Journey Optimizer], kunt u IP warmteopwerkschema&#39;s op een gestandaardiseerde en efficiënte manier direct van het gebruikersinterface uitvoeren die de beste praktijken voor optimale leverbaarheid volgt.

>[!CAUTION]
>
>Deze functie geldt alleen voor het e-mailkanaal.

Wanneer e-mails met een nieuw platform worden verzonden, zijn internetproviders (ISP&#39;s) verdacht van IP-adressen die niet worden herkend. Als er plotseling grote hoeveelheden e-mails worden verzonden, markeren de ISP&#39;s deze vaak als spam.

Als u wilt voorkomen dat spam wordt gemarkeerd, kunt u het verzonden volume progressief verhogen met de functie voor IP-warmteopruimingsplannen. Een nieuwe optie in het dialoogvenster **[!UICONTROL Administration]** kunt u dit beter doen in plaats van complexe dagelijkse reizen te maken. Dit zou een vlotte ontwikkeling van de startfase moeten verzekeren en u toelaten om het algemene tarief van ongeldige adressen te verminderen.

>[!NOTE]
>
>Meer weten over het verbeteren van je e-mailreputatie dankzij de opwarming van de IP in [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

De belangrijkste stappen om een IP opwarmingsplan uit te voeren zijn als volgt:

1. U moet eerst één of meerdere campagnes met IP toegelaten warmup optie creëren. [Meer informatie](ip-warmup-campaign.md) <!--this is usually done by a marketer persona??)-->

1. Creeer een IP warmup plan en upload uw plan. [Meer informatie](ip-warmup-plan.md) <!--this is usually done by a deliverability consultant??-->

1. Pas elke fase van uw plan aan en activeer de looppas. [Meer informatie](ip-warmup-running.md)
