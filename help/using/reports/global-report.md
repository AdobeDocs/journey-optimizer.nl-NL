---
solution: Journey Optimizer
product: journey optimizer
title: Algemeen rapport
description: Leer hoe u gegevens uit het algemene rapport kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Aan de slag met Global Report {#global-report}

>[!AVAILABILITY]
>
>De huidige ervaring met rapportage wordt vanaf de release van oktober opgeheven. Na deze datum wordt de nieuwe ervaring met rapportage de norm. We raden u aan bekend te maken met de nieuwe functies en functies om een soepele overgang te garanderen. [ worden begonnen met Journey Optimizer nieuwe het Melden interface.](report-gs-cja.md)

>[!NOTE]
>
> Als aangepaste query&#39;s via API&#39;s worden gemaakt wanneer u de Query-service gebruikt, verwacht u enige vertraging voor uw rapporten.

Gebruik **[!UICONTROL Global report]** om de impact van uw reizen en leveringen over een geselecteerde tijdsperiode te meten.

* Als u een reis of leveringen in de context van een reis, van het **[!UICONTROL Journeys]** menu wilt richten, toegang uw reis en klik de **[!UICONTROL View report]** knoop. Je kunt dan de wereldwijde rapporten Journey, Email, SMS en Push vinden.

  ![](assets/report_journey.png)

* Als u een campagne als doel wilt instellen, opent u de campagne vanuit het menu **[!UICONTROL Campaigns]** en klikt u op de knop **[!UICONTROL Reports]** .

  ![](assets/report_campaign.png)

* Als u van **[!UICONTROL Live report]** aan **[!UICONTROL Global report]** voor uw levering wilt overschakelen, klik **[!UICONTROL All time]** van de lusjeschakelaar.

  ![](assets/report_5.png)

Voor een gedetailleerde lijst van elke metrisch beschikbaar in Adobe Journey Optimizer, verwijs naar [ deze pagina ](#list-of-components-global)

## Het dashboard aanpassen {#modify-dashboard}

Elk rapportdashboard kan worden gewijzigd door de tijdsperiode te wijzigen en widgets te vergroten of te verkleinen of te verwijderen. Het wijzigen van de widgets heeft alleen invloed op het dashboard van de huidige gebruiker. Andere gebruikers zien hun eigen dashboards of de dashboards die standaard zijn ingesteld.

1. Van uw Globale rapport, selecteer een tijd van het Begin en van het Eind om specifieke gegevens te richten.

   ![](assets/report_modify_1.png)

1. Voor uw Reis- rapporten die veelvoudige gevormde **[!UICONTROL Actions]** impliceren, kies specifieke **[!UICONTROL Action]** van het drop-down menu.

1. Als u slechts één of meerdere terugkomende berichten wilt richten, selecteer het van **[!UICONTROL Execution time]** drop-down.

   ![](assets/report_modify_12.png)

1. Kies of u testgebeurtenissen wilt uitsluiten van uw rapporten met de schakelbalk. Voor meer informatie over testgebeurtenissen, verwijs naar [ deze pagina ](../building-journeys/testing-the-journey.md).

   De optie **[!UICONTROL Exclude test events]** is alleen beschikbaar voor Journey-rapporten.

   ![](assets/report_modify_2.png)

1. Klik op **[!UICONTROL Modify]** om het dashboard aan te passen.

   ![](assets/report_modify_3.png)

1. Pas de widgetgrootte aan door de rechterbenedenhoek te slepen.

   ![](assets/report_modify_4.png)

1. Klik op **[!UICONTROL Remove]** om een widget te verwijderen die u niet nodig hebt.

   ![](assets/report_modify_5.png)

1. Als u tevreden bent met de weergavevolgorde en de grootte van de widgets, klikt u op **[!UICONTROL Save]** .

1. Als u de manier wilt aanpassen waarop uw gegevens worden weergegeven, kunt u schakelen tussen verschillende visualisatieopties, zoals grafieken, tabellen en donutgrafieken.

   ![](assets/report_modify_10.png)

Uw dashboard wordt nu opgeslagen. Uw verschillende wijzigingen worden opnieuw toegepast voor een later gebruik van uw live rapporten. Gebruik indien nodig de optie **[!UICONTROL Reset]** om de standaardvolgorde van widgets en widgets te herstellen.

## Uw rapporten exporteren {#export-reports}

U kunt uw verschillende rapporten eenvoudig exporteren naar de indelingen PDF of CSV, zodat u deze kunt delen of afdrukken. De stappen voor het exporteren van rapporten worden in de onderstaande tabbladen beschreven.

➡️ [ ontdekt deze eigenschap in video ](#video-csv)


>[!BEGINTABS]

>[!TAB  Uitvoer uw rapport als Csv- dossier ]

1. Klik in uw rapport op **[!UICONTROL Export]** en selecteer **[!UICONTROL CSV file]** om een CSV-bestand op algemeen rapportniveau te genereren.

   ![](assets/export_1.png)

1. U kunt er ook voor kiezen om gegevens uit een specifieke widget te exporteren. Klik op **[!UICONTROL Export widget data to CSV]** naast de geselecteerde widget.

   ![](assets/export_3.png)

1. Het bestand wordt automatisch gedownload en kan zich in uw lokale bestanden bevinden.

   Als u het bestand op rapportniveau hebt gegenereerd, bevat het gedetailleerde informatie voor elke widget, inclusief de titel en gegevens.

   Als u het bestand op widgetniveau hebt gegenereerd, bevat dit specifiek gegevens voor de geselecteerde widget.

>[!TAB  Uitvoer uw rapport als dossier van PDF ]

1. Klik in uw rapport op **[!UICONTROL Export]** en selecteer **[!UICONTROL PDF file]** .

   ![](assets/export_2.png)

1. Configureer het document in het venster Afdrukken naar wens. Welke opties beschikbaar zijn, is afhankelijk van de browser.

1. Kies of u het rapport wilt afdrukken of opslaan als PDF.

1. Zoek de map waarin u het bestand wilt opslaan, geef het bestand een andere naam als dat nodig is en klik op Opslaan.

Uw rapport is nu beschikbaar voor weergave of delen in een PDF-bestand.



>[!ENDTABS]


### Rapporten exporteren (video) {#video-csv}

Leer hoe u een CSV-rapport voor een rapport en voor één widget downloadt in de volgende Hoe kan ik-video.

>[!VIDEO](https://video.tv.adobe.com/v/3424603?quality=12)



>[!CONTEXTUALHELP]
>id="ajo_report_campaign_ctr"
>title="CTR"
>abstract="CTR-widget"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_clicks"
>title="Klikken"
>abstract="Widget klikken"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_delivered"
>title="Afgeleverd"
>abstract="Widget geleverd"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_overview"
>title="Overzicht van Campaign"
>abstract="Widget Campagneoverzicht"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_funnel"
>title="Resultaten van Campagnescheitrechter"
>abstract="De widget voor camerastructuurresultaten"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_tracking_link"
>title="Labels voor bijgehouden koppelingen"
>abstract="Widget met bijgehouden koppelingslabels"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_displays"
>title="Weergaven"
>abstract="Widget weergeven"

<!--campaign email-->

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_delivered_click"
>title="Bezorgde &amp; klik trend"
>abstract="Geleverde &amp; klik trendwidget"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_delivery_status"
>title="Leveringsstatus"
>abstract="Widget voor leveringsstatus"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_sending_statistics"
>title="Statistieken verzenden"
>abstract="Widget Statistieken verzenden"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracking_statistics"
>title="Trackingstatistieken"
>abstract="Widget statistieken bijhouden"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_domains"
>title="E-maildomeinen"
>abstract="Widget E-maildomeinen"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracked_link"
>title="Labels voor bijgehouden koppelingen"
>abstract="Widget trackkoppelingslabels"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracked_link_urls"
>title="URL&#39;s van bijgehouden koppeling"
>abstract="Widget URL&#39;s van beheerde koppelingen"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_subjects"
>title="E-mailonderwerpen"
>abstract="Widget E-mailonderwerpen"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_bounce_reasons"
>title="Stuitingsredenen"
>abstract="Widget Stuitredenen"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_exclude"
>title="Redenen uitsluiten"
>abstract="Widget Redenen uitsluiten"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_error"
>title="Foutredenen"
>abstract="Widget Foutredenen"


<!--campaign push-->

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_sending_statistics"
>title="Statistieken verzenden"
>abstract="Widget Statistieken verzenden"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracking_statistics"
>title="Trackingstatistieken"
>abstract="Widget statistieken bijhouden"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracked_link"
>title="Labels voor bijgehouden koppelingen"
>abstract="Widget trackkoppelingslabels"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracked_link_urls"
>title="URL&#39;s van bijgehouden koppeling"
>abstract="Widget URL&#39;s van beheerde koppelingen"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_bounce_reasons"
>title="Stuitingsredenen"
>abstract="Widget Stuitredenen"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_exclude"
>title="Uitgesloten redenen"
>abstract="Widget Uitgesloten redenen"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_email_error"
>title="Foutredenen"
>abstract="Widget Foutredenen"

<!--campaign inapp-->


>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_impression"
>title="Impressie en klik op trend"
>abstract="Impressie en klik op trendwidget"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_clicks"
>title="Klikken"
>abstract="Widget klikken"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_displays"
>title="Weergaven"
>abstract="Widget weergeven"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracking_data"
>title="Gegevens bijhouden"
>abstract="Widget Gegevens bijhouden"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracked_link"
>title="Labels voor bijgehouden koppelingen"
>abstract="Widget met bijgehouden koppelingslabels"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracked_link_urls"
>title="URL&#39;s van bijgehouden koppeling"
>abstract="Widget URL&#39;s van beheerde koppelingen"

<!--campaign sms-->


>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_delivered_click"
>title="Bezorgde &amp; klik trend"
>abstract="Geleverde &amp; klik trendwidget"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_delivery_status"
>title="Leveringsstatus"
>abstract="Widget voor leveringsstatus"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_tracked_link"
>title="Labels voor bijgehouden koppelingen"
>abstract="Widget trackkoppelingslabels"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_tracked_link_urls"
>title="URL&#39;s van bijgehouden koppeling"
>abstract="Widget URL&#39;s van beheerde koppelingen"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_inbound"
>title="Binnenkomend SMS-bericht"
>abstract="Binnenkomende SMS-berichtenwidget"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_message_type"
>title="Soort SMS-bericht"
>abstract="Widget voor SMS-berichttype"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_providers"
>title="SMS-providers"
>abstract="Widget SMS-providers"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_bounce"
>title="Stuitingsredenen"
>abstract="Widget Stuitredenen"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_exclude"
>title="Redenen uitsluiten"
>abstract="Widget Redenen uitsluiten"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_error"
>title="Foutredenen"
>abstract="Widget Foutredenen"
