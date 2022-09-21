---
title: Algemeen rapport
description: Leer hoe u gegevens uit het algemene rapport kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 2%

---

# Aan de slag met Global Report {#global-report}

>[!NOTE]
>
> Als aangepaste query&#39;s via API&#39;s worden gemaakt wanneer u de Query-service gebruikt, verwacht u enige vertraging voor uw rapporten.

Gebruik de **[!UICONTROL Global report]** om de impact van uw reizen en leveringen over een bepaalde periode te meten.

* Als u een reis of leveringen in het kader van een reis wilt richten, vanaf **[!UICONTROL Journeys]** en klik op de knop **[!UICONTROL View report]** knop. Je kunt dan de wereldwijde rapporten Journey, Email, SMS en Push vinden.

   ![](assets/report_journey.png)

* Als u een campagne wilt richten, van **[!UICONTROL Campaigns]** , opent u uw campagne en klikt u op de knop **[!UICONTROL Reports]** knop.

   ![](assets/report_campaign.png)

* Als u van wilt schakelen **[!UICONTROL Live report]** aan de **[!UICONTROL Global report]** voor uw levering klikt u op **[!UICONTROL All time]** met de tabschakeloptie.

   ![](assets/report_5.png)

Voor een gedetailleerde lijst van elke metrisch beschikbaar in Adobe Journey Optimizer, verwijs naar [deze pagina](#list-of-components-global)

## Het dashboard aanpassen {#modify-dashboard}

Elk rapportdashboard kan worden gewijzigd door de tijdsperiode te wijzigen en widgets te vergroten of te verkleinen of te verwijderen. Het wijzigen van de widgets heeft alleen invloed op het dashboard van de huidige gebruiker. Andere gebruikers zien hun eigen dashboards of de dashboards die standaard zijn ingesteld.

1. Van uw Globale rapport, selecteer een tijd van het Begin en van het Eind om specifieke gegevens te richten.

   ![](assets/report_modify_1.png)

1. Kies of u testgebeurtenissen wilt uitsluiten van uw rapporten met de schakelbalk. Raadpleeg voor meer informatie over testgebeurtenissen [deze pagina](../building-journeys/testing-the-journey.md).

   De **[!UICONTROL Exclude test events]** Deze optie is alleen beschikbaar voor Journey-rapporten.

   ![](assets/report_modify_2.png)

1. Klikken **[!UICONTROL Modify]** om het dashboard aan te passen.

   ![](assets/report_modify_3.png)

1. Pas de widgetgrootte aan door de rechterbenedenhoek te slepen.

   ![](assets/report_modify_4.png)

1. Klikken **[!UICONTROL Remove]** om een widget te verwijderen die u niet nodig hebt.

   ![](assets/report_modify_5.png)

1. Als u tevreden bent met de weergavevolgorde en de grootte van de widgets, klikt u op **[!UICONTROL Save]**.

Uw dashboard wordt nu opgeslagen. Uw verschillende wijzigingen worden opnieuw toegepast voor een later gebruik van uw live rapporten. Gebruik indien nodig de **[!UICONTROL Reset]** gebruiken om de standaardvolgorde van widgets en widgets te herstellen.

## Lijst met componenten {#list-of-components-global}

De lijsten hieronder geven u de lijst van metriek die in rapporten en hun definities afhankelijk van het leveringstype wordt gebruikt.

### Reiscijfers {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrisch<br/> </th> 
   <th> Definitie<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>Handelingen zijn uitgevoerd<br/> </td> 
   <td> Het totale aantal acties dat met succes voor een reis wordt uitgevoerd.<br/> </td> 
</tr> 
  <tr> 
   <td> Ingevoerde profielen<br/> </td> 
   <td> Het totale aantal personen dat de inreisgebeurtenis van de reis heeft bereikt.<br/> </td> 
</tr>
  <tr> 
   <td> Fout in handeling<br/> </td> 
   <td>Het totale aantal fouten dat is opgetreden voor handelingen.<br/> </td> 
</tr> 
  <tr> 
   <td> Beëindigde profielen<br/> </td> 
   <td> Het totale aantal personen dat de reis heeft verlaten.<br/> </td> 
</tr> 
  <tr> 
   <td> Afgebroken individuele reis<br/> </td> 
   <td> Het totale aantal individuele reizen dat niet succesvol is uitgevoerd.<br/> </td> 
</tr> 
 </tbody> 
</table>

### Metrische gegevens voor e-mail en SMS {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrisch<br/> </th> 
   <th> Definitie<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> Bounces<br/> </td> 
   <td> Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.<br/> </td> 
</tr> 
  <tr> 
   <td> Bouncepercentage<br/> </td> 
   <td> Percentage van e-mails dat is teruggestuurd in vergelijking met verzonden e-mails.<br/> </td> 
</tr>
  <tr> 
   <td> Klikken<br/> </td> 
   <td> Aantal keer dat er op een inhoud in een e-mail is geklikt.<br/> </td> 
</tr> 
  <tr> 
   <td> Afgeleverd <br/> </td> 
   <td> Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.<br/></td> 
</tr> 
  <tr> 
   <td> Leveringssnelheid<br/> </td> 
   <td> Percentage berichten verzonden.<br/> </td> 
</tr>
  <tr> 
   <td> Fouten<br/> </td> 
   <td> Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.<br/> </td> 
</tr> 
  <tr> 
   <td> Foutfrequentie<br/> </td> 
   <td> Percentage fouten die optraden tijdens een levering waardoor deze niet kon worden verzonden, vergeleken met verzonden e-mailberichten.<br/> </td> 
</tr>
  <tr> 
   <td> Uitgesloten<br/> </td> 
   <td> Aantal profielen dat door Adobe Journey Optimizer is uitgesloten.<br/> </td> 
</tr>
  <tr> 
   <td> Hard stuiteren<br/> </td> 
   <td> Het totale aantal permanente fouten, zoals een onjuist e-mailadres. Dit omvat een foutbericht waarin expliciet wordt aangegeven dat het adres ongeldig is, zoals Onbekende gebruiker.<br/> </td>
</tr>
  <tr> 
   <td> Genegeerd<br/> </td> 
   <td> Het totale aantal tijdelijke gegevens, zoals Buiten-kantoor, of een technische fout, bijvoorbeeld als het type afzender postmaster is.<br/> </td> 
</tr>
   <tr> 
   <td>Aanbiedingskliktarief<br/> </td> 
   <td>Percentage gebruikers dat interactie had met het aanbod.<br/> </td> 
</tr>
   <tr> 
   <td>Afbeeldingsfrequentie voorstel<br/> </td> 
   <td>Percentage geopende aanbiedingen in verhouding tot het aantal verzonden aanbiedingen.<br/> </td> 
</tr>
   <tr> 
   <td>Naam voorstel<br/> </td> 
   <td> Naam van de aanbieding die in de levering is toegevoegd. Raadpleeg deze voor meer informatie over plaatsing <a href="../offers/offer-library/creating-personalized-offers.md">page</a>.<br/> </td> 
</tr>
   <tr> 
   <td>Voorstel verzonden<br/> </td> 
   <td>Het totale aantal verzendingen voor de aanbieding.<br/> </td> 
</tr> 
  <tr>
   <td>Geopende items<br/> </td> 
   <td> Aantal keren dat het bericht is geopend.<br/> </td> 
</tr> 
  <tr> 
   <td> OpenRate<br/> </td> 
   <td> Het totale aantal geopende e-mails in verhouding tot het aantal geleverde e-mails.<br/> </td> 
</tr>
  <tr> 
   <td>Plaatsingsnaam<br/> </td> 
   <td> Naam van de plaatsing die u hebt gebruikt om uw voorstel weer te geven. Raadpleeg deze voor meer informatie over plaatsing <a href="../offers/offer-library/creating-placements.md">page</a>. </td> 
</tr> 
  <tr> 
   <td> Hernieuwde pogingen<br/> </td> 
   <td> Aantal e-mails in de wachtrij voor nieuwe pogingen.<br/> </td> 
</tr> 
  <tr> 
   <td> Verzonden<br/> </td> 
   <td> Het totale aantal verzendt voor de levering.<br/> </td> 
</tr>
  <tr> 
   <td> Zachte stuit<br/> </td> 
   <td> Het totale aantal tijdelijke fouten, zoals een volledig postvak.<br/> </td> 
</tr>
  <tr> 
   <td> Spam-klachten<br/> </td> 
   <td> Aantal keren dat een bericht als spam of junk werd verklaard.<br/> </td> 
</tr>
  <tr> 
   <td> Gericht<br/> </td> 
   <td> Het totale aantal berichten dat tijdens de leveringsanalyse wordt verwerkt.<br/> </td> 
</tr> 
  <tr> 
   <td> Unieke klikken<br/> </td> 
   <td> Aantal ontvangers dat op een inhoud in een e-mail heeft geklikt.<br/> </td> 
</tr> 
  <tr> 
   <td>Unieke klikfrequentie<br/> </td> 
   <td> Percentage gebruikers dat interactie had met de levering.<br/> </td> 
</tr>
  <tr> 
   <td> Unieke open<br/> </td> 
   <td>Aantal ontvangers dat de levering heeft geopend.<br/> </td> 
</tr> 
  <tr> 
   <td> Uitschrijvingen<br/> </td> 
   <td> Aantal klikken op de verbinding van het unsubscription.<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
### Experimentation metrics {#experimentation-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td><br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td><br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>
-->

### Metrische gegevens voor pushmeldingen {#push-notification-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrisch<br/> </th> 
   <th> Definitie<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Acties<br/> </td> 
   <td> Het totale aantal acties op de geleverde pushmelding, bijvoorbeeld klikken op de knop of ontslag.<br/> </td> 
</tr>
  <tr> 
   <td>Bounces<br/> </td> 
   <td> Totaal van fouten die tijdens levering en automatische terugkeerverwerking met betrekking tot het totale aantal verzonden berichten worden gecumuleerd.<br/> </td> 
</tr> 
  <tr> 
   <td> Bouncepercentage<br/> </td> 
   <td> Percentage pushmeldingen dat is teruggestuurd in vergelijking met verzonden pushberichten.<br/> </td>
</tr>
  <tr> 
   <td> Afgeleverd<br/> </td> 
   <td> Het aantal berichten dat is verzonden in verhouding tot het totale aantal verzonden berichten.<br/> </td> 
</tr> 
  <tr> 
   <td> Leveringsgraad<br/> </td> 
   <td> Percentage pushberichten verzonden.<br/> </td> 
</tr>
  <tr> 
   <td>Engages<br/> </td> 
   <td> Het totale aantal keren dat wordt geopend en de acties voor deze pushmelding, bijvoorbeeld als het profiel de pushmelding heeft geopend of als op een knop is geklikt.<br/> </td> 
</tr> 
  <tr> 
   <td> Betrokkenheid<br/> </td> 
   <td> Percentage van het aantal keren dat wordt geopend en handelingen voor deze pushmelding, bijvoorbeeld als het profiel de pushmelding heeft geopend of als op een knop is geklikt.<br/> </td> 
</tr>
  <tr> 
   <td> Fouten<br/> </td> 
   <td> Het totale aantal fouten dat is opgetreden tijdens een levering waardoor deze niet naar profielen kan worden verzonden.<br/> </td> 
</tr>
  <tr> 
   <td> Foutfrequentie<br/> </td> 
   <td> Percentage fouten die optraden tijdens een levering waardoor deze niet kon worden verzonden, vergeleken met verzonden pushberichten.<br/> </td> 
</tr> 
  <tr> 
   <td> Uitgesloten<br/> </td> 
   <td> Aantal profielen dat door Adobe Journey Optimizer is uitgesloten.<br/> </td> 
</tr>
  <tr> 
   <td> Geopende items<br/> </td> 
   <td> Het totale aantal pushberichten dat aan het apparaat is geleverd en waarop gebruikers hebben geklikt om de app te openen. Dit is gelijkaardig aan de Duw klikt behalve zal een Duw Open niet teweeggebracht worden als het bericht werd verworpen.<br/> </td> 
</tr> 
  <tr> 
   <td> Open rate<br/> </td> 
   <td> Percentage geopende pushmeldingen.<br/> </td> 
</tr> 
  <tr> 
   <td> Verzonden<br/> </td> 
   <td> Het totale aantal verzendt voor de levering.<br/> </td> 
</tr> 
  <tr> 
   <td> Gericht<br/> </td> 
   <td> Het totale aantal pushberichten dat tijdens de leveringsanalyse is verwerkt.<br/> </td> 
</tr>  
 </tbody> 
</table>

### Metrische gegevens van bestemmingspagina {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrisch<br/> </th> 
   <th> Definitie<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>Bounces<br/> </td> 
   <td>Aantal personen die niet met de landingspagina in wisselwerking stonden en de actie van het intekenen niet voltooiden.<br/> </td> 
</tr>
 <tr> 
   <td>Stuitpercentage<br/> </td> 
   <td>Aantal personen dat niet met de landingspagina in wisselwerking stond en de actie van het intekenen niet voltooide, in verhouding tot het totale aantal bezoeken.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Klikken<br/> </td> 
   <td>Aantal keren dat op een inhoud is geklikt op de bestemmingspagina.<br/> </td> 
</tr>
 <tr> 
   <td>Klikfrequentie<br/> </td> 
   <td>Percentage klikken op de bestemmingspagina.<br/> </td>
</tr>
<tr>
<td>Conversie<br/> </td> 
   <td>Aantal personen dat interactie had met de landingspagina, bijvoorbeeld geabonneerd op een formulier.<br/> </td> 
</tr>
<tr>
   <td>Conversiepercentage<br/> </td> 
   <td>Aantal personen dat met de aanlandingspagina heeft gecommuniceerd, bv. op een formulier geabonneerd, in verhouding tot het totale aantal bezoeken.<br/> </td> 
</tr>
 <tr> 
   <td>Reis(en)<br/> </td> 
   <td>Aantal bezoeken aan uw landingspagina die van een reis komen.<br/> </td> 
</tr>
 <tr> 
   <td>Andere bronnen<br/> </td> 
   <td>Aantal bezoeken aan uw landingspagina die van een externe bron in plaats van een reis komen.<br/> </td> 
</tr>
 <tr> 
   <td>Totaal aantal bezoeken<br/> </td> 
   <td> Het totale aantal bezoeken aan uw landingspagina dat afkomstig is van reizen en externe bronnen, inclusief meerdere bezoeken van één ontvanger.<br/> </td> 
</tr>
 <tr> 
   <td>Unieke bezoekers<br/> </td> 
   <td>Aantal personen dat uw landingspagina heeft bezocht, meerdere bezoeken van één ontvanger worden niet in aanmerking genomen.<br/> </td> 
</tr>
 <tr> 
   <td>Bezoeken<br/> </td> 
   <td>Aantal bezoeken aan uw landingspagina, met inbegrip van veelvoudige bezoeken van één ontvanger.<br/> </td> 
</tr>
 </tbody> 
</table>

