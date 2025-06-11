---
solution: Journey Optimizer
product: journey optimizer
title: Bijgewerkte ervaring met rapporten
description: Aan de slag met alle tijdrapporten
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: bfd88d2a-e7b8-4e3b-85a1-4a14b0ba56dc
source-git-commit: a9349cedc4da2a8e76e53f9e2b5185270cda2558
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 2%

---

# Aan de slag met alle tijdrapporten {#channel-report-gs-cja}

>[!CONTEXTUALHELP]
>id="cja_connections_enable_cja"
>title="Customer Journey Analytics inschakelen"
>abstract="Als u dit rapport in Customer Journey Analytics wilt analyseren, neemt u contact op met uw beheerder om ervoor te zorgen dat uw organisatie Customer Journey Analytics heeft aangeschaft en dat de integratie correct is geconfigureerd."
>additional-url="https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/channels/email/design-email/add-content/content-components#add-content-components" text="Customer Journey Analytics"

Journey Optimizer-rapportering wordt geleverd met een verbeterde interoperabiliteit met Customer Journey Analytics-mogelijkheden, standaardisering van de rapportage op beide platforms en verbetering van de consistentie en betrouwbaarheid van gegevens. Deze naadloze integratie tussen Journey Optimizer en Customer Journey Analytics zorgt voor een duidelijker beeld van de prestatiesmetriek, waardoor gebruikers beter geïnformeerde beslissingen kunnen nemen.

De toegang tot deze rapporteringsmogelijkheden hangt van de context en productgebieden af:

* **reizen** - als u een reis of leveringen in de context van een reis, van het **[!UICONTROL Journeys]** menu wilt richten, toegang tot uw reis en klik de **[!UICONTROL View report]** knoop.

  In de lijst met bestaande reizen kunt u ook **[!UICONTROL Report]** selecteren in het menu Geavanceerd van de geselecteerde reis. [ leer meer over het rapport van de Reis ](journey-global-report-cja.md)

  ![](assets/gs-cja-report-3.png)

* **Campagnes** - als u een campagne, van het **[!UICONTROL Campaigns]** menu wilt richten, toegang tot uw campagne en klik dan de **[!UICONTROL Reports]** knoop **[!UICONTROL View all time report]**.

  In de lijst met bestaande campagnes kunt u ook **[!UICONTROL Report]** selecteren in het menu Geavanceerd van de geselecteerde campagne. [ leer meer over het rapport van de Campagne ](campaign-global-report-cja.md)

  ![](assets/gs-cja-report-2.png)

* **Globaal** - als u metriek voor alle campagnes en reizen binnen uw milieu wilt richten, heb toegang tot het **Overzicht** rapport door aan het **[!UICONTROL Reports]** menu binnen de **[!UICONTROL Journey Management]** sectie te navigeren. [ leer meer over het rapport van het Overzicht ](channel-report-cja.md)

  ![](assets/gs-cja-report-1.png)

>[!IMPORTANT]
>
>De rapportage in Adobe Journey Optimizer is momenteel gestandaardiseerd voor UTC. De mogelijkheid om de rapporttijdzone aan te passen zal in een toekomstige versie worden geïntroduceerd.

## Vereisten {#prerequisites}

* Als u **niet** eigen Customer Journey Analytics bent, of als u het bezit maar **&#x200B;**&#x200B;geen toegang tot om het even welk het productprofiel van Customer Journey Analytics heeft, worden de toestemmingen beheerd in Journey Optimizer. In dit geval hebt u de machtiging **[!UICONTROL View channel reports]** of gerelateerde rollen nodig. [Meer informatie](../administration/permissions.md)

* Als u **&#x200B;**&#x200B;Customer Journey Analytics bezit en toegang tot een het productprofiel van Customer Journey Analytics hebt, hebt u nodig:

   * **[!UICONTROL Audience Creation]** en **[!UICONTROL Audience View]** voor Customer Journey Analytics. [Meer informatie](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/technotes/access-control){target="_blank"}

   * **[!UICONTROL Manage profiles]** machtiging voor Adobe Journey Optimizer. [Meer informatie](../administration/permissions.md)

* Uw Customer Journey Analytics gegevensmeningen moeten met het volgende plaatsen worden gevormd: **Reeks als standaardgegevensmening in Adobe Journey Optimizer**. [ leer meer over gegevensmeningen ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}


## Alle tijdrapporten per kanaal

Alle tijd zijn de globale rapporten beschikbaar voor al uw kanalen. Selecteer het rapport voor het kanaal u meer details moet krijgen.

### Uitgaande kanalen

Selecteer een uitgaand kanaal om bijbehorende **globale rapporten van alle tijd** te ontdekken.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="email" src="../channels/assets/do-not-localize/email.png">
<div align="center"><p><strong>Email channel</strong></p><p><a href="campaign-global-report-cja-email.md"><strong>Campagnerapport</strong></a></p><p><a href="journey-global-report-cja-email.md"><strong>Reisrapport</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-sms.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><p><strong>SMS-kanaal</strong></p><p><a href="campaign-global-report-cja-sms.md"><strong>Campagnerapport</strong></a></p><p><a href="journey-global-report-cja-sms.md"><strong>Reisrapport</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-push.md"><img alt="duwen" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><p><strong>Push-kanaal</strong></p><p><a href="campaign-global-report-cja-push.md"><strong>Campagnerapport</strong></a></p><p><a href="journey-global-report-cja-push.md"><strong>Reisrapport</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-direct.md"><img alt="direct mail" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><p><strong>Direct mailkanaal</strong></p><p><a href="campaign-global-report-cja-direct.md"><strong>Campagnerapport</strong></a></p><p><a href="journey-global-report-cja-direct.md"><strong>Reisrapport</strong></a></p></div></td>
</tr></table>

### Binnenkomende ervaringen

Selecteer een binnenkomende ervaring om bijbehorende **globale rapporten van alle tijd** te ontdekken.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="in-app" src="../channels/assets/do-not-localize/inapp.jpg">
<div align="center"><p><strong>Kanaal in app</strong></p><p><a href="campaign-global-report-cja-inapp.md"><strong>Campagnerapport</strong></a></p><p><a href="journey-global-report-cja-inapp.md"><strong>Reisrapport</strong></a></p></div></td>
<td><p><img alt="web" src="../channels/assets/do-not-localize/web.jpg"></p>
<div align="center"><p><strong>Webkanaal</strong></p><p><a href="campaign-global-report-cja-web.md"><strong>Campagnerapport</strong></a></p><p><a href="journey-global-report-cja-web.md"><strong>Reisrapport</strong></a></p></div></td>
<td><img alt="code-gebaseerde ervaring" src="../channels/assets/do-not-localize/code.png">
<div align="center"><p><strong>Ervaringen op basis van code</strong></p><p><a href="campaign-global-report-cja-code.md"><strong>Campagnerapport</strong></a></p><p><a href="campaign-global-report-cja-code.md"><strong>Reisrapport</strong></a></p></div></td>
<td><img alt="inhoudskaarten" src="../channels/assets/do-not-localize/cards.png">
<div align="center"><p><strong>Inhoudskaarten</strong></p><p><a href="campaign-global-report-cja-content.md"><strong>Campagnerapport</strong></a></p><p><a href="journey-global-report-cja-content.md"><strong>Reisrapport</strong></a></p></div></td>
</tr></table>

## Hoe kan ik-video{#video}

In de onderstaande video ziet u hoe u de verbeterde Journey Optimizer-rapportage met Customer Journey Analytics kunt gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/3430413)