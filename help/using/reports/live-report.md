---
title: Live-rapport
description: Leer hoe u gegevens uit het live rapport kunt gebruiken
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 8dd48bb2-a805-4c46-a16c-c68173a9ac08
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 2%

---

# Aan de slag met Live-rapport {#live-report}

Gebruik de **[!UICONTROL Live report]** om de impact en prestaties van uw reizen en uw berichten in een ingebouwd dashboard in real-time te meten en te visualiseren.
Gegevens zijn beschikbaar in het dialoogvenster **[!UICONTROL Live report]** zodra je levering is verzonden of je reis wordt uitgevoerd vanuit de **[!UICONTROL Last 24hrs]** tab.

* Als je een reis wilt afleggen in het kader van een reis, vanaf de **[!UICONTROL Journeys]** en klik op de knop **[!UICONTROL View report]** knop.

   ![](assets/report_journey.png)

* Als u een campagne wilt richten, van **[!UICONTROL Campaigns]** , opent u uw campagne en klikt u op de knop **[!UICONTROL Reports]** knop.

   ![](assets/report_campaign.png)

* Als u van wilt schakelen **[!UICONTROL Global report]** aan de **[!UICONTROL Live report]** voor uw levering klikt u op **[!UICONTROL Last 24hrs]** met de tabschakeloptie.

   ![](assets/report_3.png)

Voor een gedetailleerde lijst van elke metrisch beschikbaar in Adobe Journey Optimizer, verwijs naar [deze pagina](#list-of-components-live).

## Het dashboard aanpassen {#modify-dashboard}

Elk rapportdashboard kan worden gewijzigd door widgets te vergroten of te verkleinen of te verwijderen. Het wijzigen van de widgets heeft alleen invloed op het dashboard van de huidige gebruiker. Andere gebruikers zien hun eigen dashboards of de dashboards die standaard zijn ingesteld.

1. Kies of u testgebeurtenissen wilt uitsluiten van uw rapporten met de schakelbalk. Raadpleeg voor meer informatie over testgebeurtenissen [deze pagina](../building-journeys/testing-the-journey.md).

   De **[!UICONTROL Exclude test events]** Deze optie is alleen beschikbaar voor Journey-rapporten.

   ![](assets/report_modify_6.png)

1. Als u widgets wilt vergroten of verkleinen of verwijderen, klikt u op **[!UICONTROL Modify]**.

   ![](assets/report_modify_7.png)

1. Pas de widgetgrootte aan door de rechterbenedenhoek te slepen.

   ![](assets/report_modify_8.png)

1. Klikken **[!UICONTROL Remove]** om een widget te verwijderen die u niet nodig hebt.

   ![](assets/report_modify_9.png)

1. Als u tevreden bent met de weergavevolgorde en de grootte van de widgets, klikt u op **[!UICONTROL Save]**.

Uw dashboard wordt nu opgeslagen. Uw verschillende wijzigingen worden opnieuw toegepast voor een later gebruik van uw live rapporten. Gebruik indien nodig de **[!UICONTROL Reset]** gebruiken om de standaardvolgorde van widgets en widgets te herstellen.

## Lijst met componenten {#list-of-components-live}

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
   <td> Totaal aantal fouten gecumuleerd tijdens levering en automatische terugkeringsverwerking.<br/> </td> 
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
   <td> Aantal verzonden berichten.<br/></td> 
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
   <td>Aantal personen die niet met de landingspagina in wisselwerking stonden en de actie van het intekenen niet voltooiden.<br/> </td> 
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
   <td>Aantal personen dat interactie had met de landingspagina, bijvoorbeeld geabonneerd op een formulier.<br/> </td> 
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

