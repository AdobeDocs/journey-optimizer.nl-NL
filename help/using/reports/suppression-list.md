---
solution: Journey Optimizer
product: journey optimizer
title: Onderdrukkingslijst
description: 'Leer hoe u de suppressielijst kunt gebruiken:'
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 30018b08da7c02d9d9aac431db2fa39f91163cfd
workflow-type: tm+mt
source-wordcount: '787'
ht-degree: 2%

---

# Onderdrukkingslijst {#suppression-list}

Een suppressielijst bestaat uit adressen en domeinen die u van uw leveringen wilt uitsluiten, omdat het verzenden naar deze contacten uw verzendende reputatie en leveringspercentages zou kunnen beschadigen.

De [!DNL Journey Optimizer] de suppressielijst wordt beheerd op uw eigen milieuniveau, d.w.z. voor een bepaalde zandbak.

Het verzamelt e-mailadressen en domeinen die over alle post in één enkele cliëntmilieu worden onderdrukt, betekenend specifiek voor een organisatie ID verbonden aan een zandbak identiteitskaart

>[!NOTE]
>
>Adobe houdt een bijgewerkte lijst bij van bekende slechte adressen waarvan is aangetoond dat ze de betrokkenheid en de mailingreputatie schaden, en zorgt ervoor dat er geen e-mails aan hen worden bezorgd. Deze lijst wordt beheerd in een globale suppressielijst die over alle klanten van de Adobe gemeenschappelijk is. De adressen en domeinnamen in de globale suppressielijst worden verborgen. Alleen het aantal uitgesloten ontvangers wordt vermeld in de leveringsverslagen.

Bovendien kun je Journey Optimizer gebruiken **REST-API onderdrukken** om uw uitgaande berichten te controleren gebruikend onderdrukking en lijsten van gewenste personen. [Leer hoe u met de REST API voor onderdrukking werkt](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## Waarom een suppressielijst? {#why-suppression-list}

Om de e-mailberichten te controleren die door hun inbox eigenaars worden ontvangen en ervoor te zorgen zij slechts ontvangen die zij willen, hebben de dienstverleners van Internet (ISPs) en commerciële spamfilters hun merkgebonden algoritmen om de algemene reputatie van e-mailafzenders te volgen die op de IP adressen wordt gebaseerd en die domein(s) verzenden zij gebruiken.

Als je geen feedback krijgt (zoals spamklachten, stuitingen, enzovoort) in aanmerking genomen, zullen zij uw reputatie verminderen. De suppressielijst helpt u met het respecteren van ISPs terugkoppelen.

Ontvangers van wie de e-mailadressen worden onderdrukt, worden automatisch uitgesloten van het verzenden van berichten. Hierdoor wordt de levering versneld, omdat het foutenpercentage een belangrijk effect heeft op de leveringssnelheid.

## Wat staat er op de onderdrukkingslijst? {#what-s-on-suppression-list}

De adressen worden toegevoegd aan de onderdrukkingslijst als volgt:

* Alles **harde tegenstellingen** en **spamingklachten** Verzend automatisch de overeenkomstige adressen naar de onderdrukkingslijst na één enkel voorkomen.

* **Zachte golven** niet onmiddellijk een adres naar de onderdrukkingslijst verzenden, maar zij verhogen een foutenteller. Meerdere [opnieuw proberen](../configuration/retries.md) worden dan uitgevoerd, en wanneer de foutenteller de drempel bereikt, wordt het adres toegevoegd aan de onderdrukkingslijst.

* U kunt [**handmatig** een adres of domein toevoegen](../configuration/manage-suppression-list.md#add-addresses-and-domains) aan de onderdrukkingslijst.

Meer informatie over harde stuit en zachte stuit in [deze sectie](#delivery-failures).

>[!NOTE]
>
>Gebruikers met een abonnement kunnen geen adressen naar de onderdrukkingslijst verzenden omdat ze geen e-mails ontvangen van [!DNL Journey Optimizer]. Hun keuze wordt op het niveau van de Experience Platform behandeld. Meer informatie over [opt-out](../privacy/opt-out.md).

Voor elk adres, de fundamentele reden voor onderdrukking en de onderdrukkingscategorie (zacht, hard, enz.) worden weergegeven in de lijst met onderdrukking. Meer informatie over het openen en beheren van de suppressielijst vindt u in [deze sectie](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>De profielen met **[!UICONTROL Suppressed]** status worden uitgesloten tijdens het proces voor het verzenden van berichten. Daarom moet **Reisrapporten** geeft aan dat deze profielen door de reis zijn gegaan ([Publiek lezen](../building-journeys/read-audience.md) en [berichtenactiviteiten](../building-journeys/journeys-message.md)), **E-mailrapporten** worden niet opgenomen in de **[!UICONTROL Sent]** Metrische gegevens worden uitgefilterd voordat e-mail wordt verzonden.
>
>Meer informatie over de [Live rapport](../reports/live-report.md) en [Algemeen rapport](../reports/global-report.md). Als u de reden voor alle uitsluitingsgevallen wilt achterhalen, kunt u de opdracht [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}.

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
