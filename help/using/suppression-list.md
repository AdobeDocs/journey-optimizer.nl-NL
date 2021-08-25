---
title: Onderdrukkingslijst
description: Leer wat de onderdrukkingslijst is, wat het doel ervan is en wat er in staat.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: ea2bb0c2956781138a0c7f2d0babfd91070dd351
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 2%

---

# Onderdrukkingslijst {#suppression-list}

Een suppressielijst bestaat uit e-mailadressen die u van uw leveringen wilt uitsluiten, omdat het verzenden naar deze contacten uw verzendende reputatie en leveringspercentages zou kunnen beschadigen.

De [!DNL Journey Optimizer] suppressielijst wordt beheerd op uw eigen milieuniveau.

Het verzamelt e-mailadressen en domeinen die over alle brievenings in één enkele cliëntmilieu worden onderdrukt, betekenend specifiek voor een IMS organisatie ID verbonden aan een zandbakidentiteitskaart

<!--It gathers spam complaints, hard bounces, and soft bounces that occur consistently.-->

## Waarom een suppressielijst? {#why-suppression-list}

Om de e-mailberichten te controleren die door hun inbox eigenaars worden ontvangen en ervoor te zorgen zij slechts ontvangen die zij willen, hebben de dienstverleners van Internet (ISPs) en commerciële spamfilters hun merkgebonden algoritmen om de algemene reputatie van e-mailafzenders te volgen die op de IP adressen wordt gebaseerd en die domein(s) verzenden zij gebruiken.

Als je geen feedback krijgt (zoals spamklachten, stuitingen, enzovoort) in aanmerking genomen, zullen zij uw reputatie verminderen. De suppressielijst helpt u met het respecteren van ISPs terugkoppelen.

Ontvangers van wie de e-mailadressen worden onderdrukt, worden automatisch uitgesloten van het verzenden van berichten. Hierdoor wordt de levering versneld, omdat het foutenpercentage een belangrijk effect heeft op de leveringssnelheid.

## Wat staat er op de onderdrukkingslijst? {#what-s-on-suppression-list}

De e-mailadressen worden als volgt toegevoegd aan de lijst van onderdrukking:

* Alle **harde grenzen** en **spamklachten** verzenden automatisch de overeenkomstige e-mailadressen naar de suppressielijst na één enkel voorkomen.

* **Bij zachte** <!--and temporary **ignored** errors--> grenzen wordt niet direct een e-mailadres naar de lijst met onderdrukking verzonden, maar wordt een foutenteller gegenereerd. Verscheidene [retry](configuration/retries.md) worden dan uitgevoerd, en wanneer de foutenteller de drempel bereikt, wordt het adres toegevoegd aan de onderdrukkingslijst.

* U kunt [**manueel** ook toevoegen een adres of een domein](configuration/manage-suppression-list.md#add-addresses-and-domains) aan de onderdrukkingslijst.

Leer meer op harde en zachte grenzen in [deze sectie](#delivery-failures).

>[!NOTE]
>
>Gebruikers met een abonnement kunnen geen adressen naar de onderdrukkingslijst verzenden omdat zij geen e-mails van [!DNL Journey Optimizer] ontvangen. Hun keuze wordt op het niveau van de Experience Platform behandeld. Meer informatie over [opting-out](../using/consent.md).
<!--Email addresses of recipients who **unsubscribe** from your sendings are NOT sent to the suppression list. Confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

Voor elk adres, de fundamentele reden voor onderdrukking en de onderdrukkingscategorie (zacht, hard, enz.) worden weergegeven in de lijst met onderdrukking. Leer meer bij de toegang tot van en het beheren van de suppressielijst in [dit sectie](configuration/manage-suppression-list.md).

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

>[!NOTE]
>
>De profielen met de status **[!UICONTROL Suppressed]** worden uitgesloten tijdens het verzenden van berichten. Daarom, terwijl **Reis rapporteert** deze profielen zal tonen als die door de reis ([Leessegment](building-journeys/read-segment.md) en [Bericht](building-journeys/journeys-message.md) activiteiten) zijn bewogen, **E-mailrapporten** zullen niet hen in **[!UICONTROL Sent]** metriek omvatten aangezien zij voorafgaand aan e-mail verzenden worden gefilterd.
>
>Leer meer op [Levend Rapport](reports/live-report.md) en [Globaal Rapport](reports/global-report.md). Om de reden voor alle uitsluitingsgevallen te weten te komen, kunt u [de Dienst van de Vraag van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html) gebruiken.

### Leveringsfouten {#delivery-failures}

Er zijn twee soorten fouten wanneer een levering mislukt:

* **Hard stuiteren**. Een vaste stuit geeft een ongeldig e-mailadres aan (een e-mailadres dat niet bestaat). Dit omvat een stuitbericht van de ontvangende e-mailserver waarin expliciet wordt vermeld dat het adres ongeldig is.
* **Zwak stuiteren**. Dit is een tijdelijke e-mailstuit die optrad voor een geldig e-mailadres.
<!--* **Ignored**. This is an email bounce that occurred for a valid email address but is known to be temporary, such as a failed connection attempt, a temporary Spam-related issue (email reputation), or a temporary technical issue.-->

Een **harde stuit** voegt automatisch het e-mailadres aan de onderdrukkingslijst toe.

Een **zachte stuit** <!--or an **ignored** error--> die te vaak voorkomt verzendt ook het e-mailadres naar de onderdrukkingslijst na verscheidene herpogingen. [Meer informatie over opnieuw proberen](configuration/retries.md)

Als u aan deze adressen blijft verzenden, kan het uw leveringstarieven beïnvloeden, omdat het ISPs vertelt dat u geen beste praktijken van het onderhoud van de e-mailadreslijst kunt volgen, en daarom geen betrouwbare afzender kan zijn.

### Spam-klachten {#spam-complaints}

De suppressielijst verzamelt e-mailadressen die uw bericht als spam merken. Bijvoorbeeld, als iemand aan de klantendienst schrijft die verzoekt om nooit post opnieuw van u te ontvangen, zal het e-mailadres van die persoon over uw geval worden onderdrukt en u zult niet meer aan dat adres kunnen leveren.

Het verzenden aan ontvangers nadat zij een spamklacht indienen kan een enorme invloed op uw verzendende reputatie hebben, omdat het ISPs meedeelt dat u ongewenste e-mails kunt verzenden en niet aan uw ontvangers kunt luisteren.

Dit zou tot uw IP adres of verzendend domein kunnen leiden die worden geblokkeerd, wat met deze adressen kan worden vermeden die op de suppressielijst zijn.

<!--### Unsubscriptions {#unsubscriptions}

Every email sent to recipients must include an unsubscribe link. Upon clicking this link, if a recipient confirms [opting out](consent.md), the corresponding email address is immediately sent to the suppression list. This user must not receive communication from your brand until subscribed again.
NOT TRUE > "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

<!--MOVED to Configuration/Retries section

The threshold is set at three errors:
* For the same delivery, at the third attempt, the address is suppressed.
* If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the third attempt.
When a delivery is successful after a retry, the error counter of the address is reinitialized.

### Retries {#retries}

If a message fails due to a temporary bounce of the **Ignored** type, retries will be performed for **3.5 days** from the time the message was added to the email queue.

The minimum delay between retries and the maximum number of retries to be performed are ///managed by the Enhanced MTA/// based on how well an IP is performing, both historically and currently at a given domain.

After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->
