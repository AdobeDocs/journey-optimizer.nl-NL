---
title: Onderdrukkingslijst
description: Leer wat de onderdrukkingslijst is, wat het doel ervan is en wat er in staat.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 2%

---

# Onderdrukkingslijst {#suppression-list}

Een suppressielijst bestaat uit e-mailadressen die u van uw leveringen wilt uitsluiten, omdat het verzenden naar deze contacten uw verzendende reputatie en leveringspercentages zou kunnen beschadigen.

De [!DNL Journey Optimizer] de suppressielijst wordt beheerd op uw eigen milieuniveau.

Het verzamelt e-mailadressen en domeinen die over alle post in één enkele cliëntmilieu worden onderdrukt, betekenend specifiek voor een organisatie ID verbonden aan een zandbak identiteitskaart

## Waarom een suppressielijst? {#why-suppression-list}

Om de e-mailberichten te controleren die door hun inbox eigenaars worden ontvangen en ervoor te zorgen zij slechts ontvangen die zij willen, hebben de dienstverleners van Internet (ISPs) en commerciële spamfilters hun merkgebonden algoritmen om de algemene reputatie van e-mailafzenders te volgen die op de IP adressen wordt gebaseerd en die domein(s) verzenden zij gebruiken.

Als je geen feedback krijgt (zoals spamklachten, stuitingen, enzovoort) in aanmerking genomen, zullen zij uw reputatie verminderen. De suppressielijst helpt u met het respecteren van ISPs terugkoppelen.

Ontvangers van wie de e-mailadressen worden onderdrukt, worden automatisch uitgesloten van het verzenden van berichten. Hierdoor wordt de levering versneld, omdat het foutenpercentage een belangrijk effect heeft op de leveringssnelheid.

## Wat staat er op de onderdrukkingslijst? {#what-s-on-suppression-list}

De e-mailadressen worden als volgt toegevoegd aan de lijst van onderdrukking:

* Alles **harde tegenstellingen** en **spamklachten** Stuur de bijbehorende e-mailadressen automatisch naar de suppressielijst na één exemplaar.

* **Zachte golven** Stuur niet meteen een e-mailadres naar de onderdrukkingslijst, maar er wordt een foutenteller ingesteld. Meerdere [opnieuw](../configuration/retries.md) worden dan uitgevoerd, en wanneer de foutenteller de drempel bereikt, wordt het adres toegevoegd aan de onderdrukkingslijst.

* U kunt ook [**handmatig** een adres of domein toevoegen](../configuration/manage-suppression-list.md#add-addresses-and-domains) aan de onderdrukkingslijst.

Meer informatie over harde stuit en zachte stuit in [deze sectie](#delivery-failures).

>[!NOTE]
>
>Gebruikers met een abonnement kunnen geen adressen naar de onderdrukkingslijst verzenden omdat ze geen e-mails ontvangen van [!DNL Journey Optimizer]. Hun keuze wordt op het niveau van de Experience Platform behandeld. Meer informatie over [uitkiezen](../messages/consent.md).

Voor elk adres, de fundamentele reden voor onderdrukking en de onderdrukkingscategorie (zacht, hard, enz.) worden weergegeven in de lijst met onderdrukking. Meer informatie over het openen en beheren van de suppressielijst vindt u in [deze sectie](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>De profielen met **[!UICONTROL Suppressed]** status worden uitgesloten tijdens het verzenden van berichten. Daarom moet **Reisrapporten** geeft aan dat deze profielen door de reis zijn gegaan ([Segment lezen](../building-journeys/read-segment.md) en [Bericht](../building-journeys/journeys-message.md) de **E-mailrapporten** worden niet opgenomen in de **[!UICONTROL Sent]** Metrische gegevens worden uitgefilterd voordat e-mail wordt verzonden.
>
>Meer informatie over de [Live rapport](../reports/live-report.md) en [Algemeen rapport](../reports/global-report.md). Als u de reden voor alle uitsluitingsgevallen wilt achterhalen, kunt u de opdracht [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.

### Leveringsfouten {#delivery-failures}

Er zijn twee soorten fouten wanneer een levering mislukt:

* **Hard stuiteren**. Een vaste stuit geeft een ongeldig e-mailadres aan (een e-mailadres dat niet bestaat). Dit omvat een stuitbericht van de ontvangende e-mailserver waarin expliciet wordt vermeld dat het adres ongeldig is.
* **Zachte stuit**. Dit is een tijdelijke e-mailstuit die optrad voor een geldig e-mailadres.

A **harde stoot** voegt het e-mailadres automatisch toe aan de onderdrukkingslijst.

A **zachte stoot** <!--or an **ignored** error--> dat te vaak voorkomt verzendt ook het e-mailadres naar de onderdrukkingslijst na verscheidene pogingen. [Meer informatie over opnieuw proberen](../configuration/retries.md)

Als u aan deze adressen blijft verzenden, kan het uw leveringstarieven beïnvloeden, omdat het ISPs vertelt dat u geen beste praktijken van het onderhoud van de e-mailadreslijst kunt volgen, en daarom geen betrouwbare afzender kan zijn.

### Spam-klachten {#spam-complaints}

De suppressielijst verzamelt e-mailadressen die uw bericht als spam merken. Bijvoorbeeld, als iemand aan de klantendienst schrijft die verzoekt om nooit post opnieuw van u te ontvangen, zal het e-mailadres van die persoon over uw geval worden onderdrukt en u zult niet meer aan dat adres kunnen leveren.

Het verzenden aan ontvangers nadat zij een spamklacht indienen kan een enorme invloed op uw verzendende reputatie hebben, omdat het ISPs meedeelt dat u ongewenste e-mails kunt verzenden en niet aan uw ontvangers kunt luisteren.

Dit zou tot uw IP adres of verzendend domein kunnen leiden die worden geblokkeerd, wat met deze adressen kan worden vermeden die op de suppressielijst zijn.
