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
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 2%

---

# Onderdrukkingslijst {#suppression-list}

Een suppressielijst bestaat uit adressen en domeinen die u van uw leveringen wilt uitsluiten, omdat het verzenden naar deze contacten uw verzendende reputatie en leveringspercentages zou kunnen beschadigen.

De onderdrukkingslijst van [!DNL Journey Optimizer] wordt beheerd op uw eigen milieuniveau, d.w.z. voor een bepaalde zandbak.

Het verzamelt e-mailadressen en domeinen die over alle post in één enkele cliëntmilieu worden onderdrukt, betekenend specifiek voor een organisatie ID verbonden aan een zandbak identiteitskaart

>[!NOTE]
>
>Adobe houdt een bijgewerkte lijst bij van bekende slechte adressen waarvan is aangetoond dat ze schadelijk zijn voor de service en de mailingreputatie, en zorgt ervoor dat er geen e-mailberichten aan hen worden bezorgd. Deze lijst wordt beheerd in een algemene suppressielijst die door alle Adobe-klanten wordt gebruikt. De adressen en domeinnamen in de globale suppressielijst worden verborgen. Alleen het aantal uitgesloten ontvangers wordt vermeld in de leveringsverslagen.

Bovendien kunt u hefboomwerkingJourney Optimizer **HULPMIDDELEN API van de Onderdrukking** om uw uitgaande berichten te controleren gebruikend onderdrukking en lijsten van gewenste personen. [&#x200B; Leer hoe te met de HULPMIDDEL te werken REST API &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## Waarom een suppressielijst? {#why-suppression-list}

Om de e-mailberichten te controleren die door hun inbox eigenaars worden ontvangen en ervoor te zorgen zij slechts ontvangen die zij willen, hebben de dienstverleners van Internet (ISPs) en commerciële spamfilters hun merkgebonden algoritmen om de algemene reputatie van e-mailafzenders te volgen die op de IP adressen wordt gebaseerd en die domein(s) verzenden zij gebruiken.

Als je geen rekening houdt met hun feedback (zoals klachten over spam, stuitingen, enz.), zullen ze je reputatie inschatten. De suppressielijst helpt u met het respecteren van ISPs terugkoppelen.

Ontvangers van wie de e-mailadressen worden onderdrukt, worden automatisch uitgesloten van het verzenden van berichten. Hierdoor wordt de levering versneld, omdat het foutenpercentage een belangrijk effect heeft op de leveringssnelheid.

## Wat staat er op de onderdrukkingslijst? {#what-s-on-suppression-list}

De adressen worden toegevoegd aan de onderdrukkingslijst als volgt:

* Al **harde grenzen** en **spamklachten** verzenden automatisch de overeenkomstige adressen naar de onderdrukkingslijst na één enkel voorkomen. Leer meer over spamklachten in [&#x200B; deze sectie &#x200B;](#spam-complaints).

* **zachte grenzen** verzenden niet onmiddellijk een adres naar de onderdrukkingslijst, maar zij verhogen een foutenteller. Verscheidene [&#x200B; opnieuw probeert &#x200B;](../configuration/retries.md) wordt dan uitgevoerd, en wanneer de foutenteller de drempel bereikt, wordt het adres toegevoegd aan de suppressielijst.

* U kunt ook [**manueel** een adres of een domein &#x200B;](../configuration/manage-suppression-list.md#add-addresses-and-domains) aan de onderdrukkingslijst toevoegen.

Leer meer over harde stuitingen en zachte stuitingen in [&#x200B; deze sectie &#x200B;](#delivery-failures).

>[!NOTE]
>
>Gebruikers met een abonnement kunnen geen adressen naar de onderdrukkingslijst verzenden omdat ze geen e-mails van [!DNL Journey Optimizer] ontvangen. Hun keuze wordt op Experience Platform-niveau geregeld. Leer meer over [&#x200B; opting-out &#x200B;](../privacy/opt-out.md).

Voor elk adres, worden de fundamentele reden voor onderdrukking en de onderdrukkingscategorie (zacht, hard, enz.) getoond in de onderdrukkingslijst. Leer meer over de toegang tot van en het beheren van de suppressielijst in [&#x200B; deze sectie &#x200B;](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>De profielen met de status **[!UICONTROL Suppressed]** worden tijdens het verzenden van berichten uitgesloten. Daarom terwijl de **rapporten van de Reis** deze profielen zullen tonen zoals die door de reis ([&#x200B; gelezen Publiek &#x200B;](../building-journeys/read-audience.md) en [&#x200B; berichtactiviteiten &#x200B;](../building-journeys/journeys-message.md)) zijn bewogen, zullen de **E-mail rapporten** niet hen in de **[!UICONTROL Sent]** metriek omvatten aangezien zij voorafgaand aan e-mail het verzenden worden uitgefilterd.
>
>Leer meer over het [&#x200B; Levende Rapport &#x200B;](../reports/live-report.md) en [&#x200B; rapport van Customer Journey Analytics &#x200B;](../reports/report-gs-cja.md). Om de reden voor alle uitsluitingsgevallen te weten te komen, kunt u de [&#x200B; Dienst van de Vraag van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} gebruiken.

### Leveringsfouten {#delivery-failures}

Er zijn twee soorten fouten wanneer een levering mislukt:

* **Vaste stuit**. Een vaste stuit geeft een ongeldig e-mailadres aan (een e-mailadres dat niet bestaat). Dit omvat een stuitbericht van de ontvangende e-mailserver waarin expliciet wordt vermeld dat het adres ongeldig is.
* **Zachte stuit**. Dit is een tijdelijke e-mailstuit die optrad voor een geldig e-mailadres.

A **hard stuiteren** voegt automatisch het e-mailadres aan de suppressielijst toe.

A **zachte stuit** <!--or an **ignored** error--> die voorkomt ook verzendt het e-mailadres naar de onderdrukkingslijst na verscheidene herpogingen. [&#x200B; Leer meer over pogingen &#x200B;](../configuration/retries.md)

Als u aan deze adressen blijft verzenden, kan het uw leveringstarieven beïnvloeden, omdat het ISPs vertelt dat u geen beste praktijken van het onderhoud van de e-mailadreslijst kunt volgen, en daarom geen betrouwbare afzender kan zijn.

### Spam-klachten {#spam-complaints}

De suppressielijst verzamelt e-mailadressen die uw bericht als spam merken. Bijvoorbeeld, als iemand aan de klantendienst schrijft die verzoekt om nooit post opnieuw van u te ontvangen, zal het e-mailadres van die persoon over uw geval worden onderdrukt en u zult niet meer aan dat adres kunnen leveren.

Het verzenden aan ontvangers nadat zij een spamklacht indienen kan een enorme invloed op uw verzendende reputatie hebben, omdat het ISPs meedeelt dat u ongewenste e-mails kunt verzenden en niet aan uw ontvangers kunt luisteren.

Dit zou tot uw IP adres of verzendend domein kunnen leiden die worden geblokkeerd, wat met deze adressen kan worden vermeden die op de suppressielijst zijn.

Sommige ISPs biedt een terugkoppelt lijn (FBL) aan die de e-mailafzender toestaat om automatisch op de hoogte te worden gebracht wanneer de gebruiker die een e-mail ontvangt verkiest om het als spam te merken. [Meer informatie](deliverability.md#feedback-loops)
