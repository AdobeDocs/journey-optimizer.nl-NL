---
solution: Journey Optimizer
product: journey optimizer
title: Expressies bewerken
description: Leer hoe u expressies kunt bewerken.
exl-id: bf0a905f-00af-4ed7-9e4f-bf8cb0af9ea9
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '2030'
ht-degree: 29%

---


# Expressies bewerken {#edit-expressions}

>[!NOTE]
>
>De sectie hieronder verstrekt informatie over hoe te met de uitdrukkingsredacteur te werken om regels te bouwen. Onthoud dat de syntaxis die wordt gebruikt om regels te bouwen verschilt van de syntaxis die wordt gebruikt om personalisatie toe te voegen.

## Werken met de expressie-editor {#edit}

Als u een expressie bewerkt, moet u handmatig voorwaarden invoeren om een regel te vormen. In deze modus kunt u geavanceerde functies gebruiken, waarmee u de waarden kunt manipuleren die worden gebruikt voor het uitvoeren van specifieke query&#39;s, zoals het manipuleren van datums, tekenreeksen, numerieke velden en sorteren.

De expressie-editor is beschikbaar via de knop Constructor **[!UICONTROL Edit expression]** , beschikbaar voor de velden **[!UICONTROL Attribute]** en **[!UICONTROL Value]** wanneer u een aangepaste voorwaarde configureert.

| Toegang van het **gebied van Attributen** | Toegang van het **gebied van de Waarde** |
| --- | --- |
| ![&#x200B; de redacteur van de Uitdrukking voor het gebied van Attributen &#x200B;](assets/rule-builder-expression-access-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![&#x200B; de redacteur van de Uitdrukking voor het gebied van de Waarde &#x200B;](assets/rule-builder-expression-access-value.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

De uitdrukkingsredacteur verstrekt:

* Een **inputgebied (1)** waar de uitdrukking wordt bepaald.
* Een lijst van beschikbare **gebieden (2)** die in de uitdrukking kunnen worden gebruikt en aan de het richten dimensie van de vraag beantwoorden.
* **de functies van de Helper (3)**, die door categorie wordt gesorteerd.

Bewerk de expressie door een expressie rechtstreeks in het invoerveld in te voeren. Als u een veld of hulpfunctie wilt toevoegen, plaatst u de cursor in de expressie waar u deze wilt toevoegen en klikt u op +.

![&#x200B; de redacteurinterface van de Uitdrukking &#x200B;](assets/rule-builder-expression-editor.png){zoomable="yes"}

## Helpfuncties

Met het gereedschap voor het bewerken van query&#39;s kunt u geavanceerde functies gebruiken om complexe filtering uit te voeren op basis van de gewenste resultaten en de typen gemanipuleerde gegevens. De volgende functies zijn beschikbaar:

### Geaggregeerd

Samengevoegde functies voeren berekeningen uit op een reeks waarden.

<table>
<tbody>
<tr>
<td><strong>Naam</strong></td>
<td><strong>Beschrijving</strong></td>
<td><strong>Syntaxis</strong></td>
</tr>
<tr>
<td><strong>Avg</strong></td>
<td>Hiermee wordt het gemiddelde van een kolom met het getaltype geretourneerd</td>
<td>Avg(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>Aantal</strong></td>
<td>Telt de niet-null waarden van een kolom</td>
<td>Count(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>CountAll</strong></td>
<td>Telt de geretourneerde waarden (alle velden)</td>
<td>CountAll()</td>
</tr>
<tr>
<td><strong>Aftelbaar</strong></td>
<td>Telt de verschillende niet-null-waarden van een kolom</td>
<td>Countdifferent(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>Max</strong></td>
<td>Retourneert de maximumwaarde van een getal, tekenreeks of datumtekstkolom</td>
<td>Max(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>Min</strong></td>
<td>Hiermee wordt de minimale waarde van een getal, tekenreeks of kolom met het gegevenstype geretourneerd</td>
<td>Min(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>StdDev</strong></td>
<td>Retourneert de standaardafwijking van een getal, tekenreeks of datumkolom</td>
<td>StdDev(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>StringAgg</strong></td>
<td>Retourneert de samenvoeging van de waarden van een kolom met tekenreekstype, gescheiden door het teken in het tweede argument.</td>
<td>StringAgg(&lt;Value&gt;, &lt;String&gt;)</td>
</tr>
<tr>
<td><strong>Som</strong></td>
<td>Hiermee wordt de som van de waarden van een getal, tekenreeks of kolom met het gegevenstype geretourneerd</td>
<td>Sum(&lt;value&gt;)</td>
</tr>
</tbody>
</table>

### Datum

Datumfuncties manipuleren datum- of tijdwaarden.

<table>
<tbody>
<tr>
<td><strong>Naam</strong></td>
<td><strong>Beschrijving</strong></td>
<td><strong>Syntaxis</strong></td>
</tr>
<tr>
<td><strong>AddDays</strong></td>
<td>Hiermee voegt u een aantal dagen toe aan een datum</td>
<td>AddDays(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>AddHours</strong></td>
<td>Hiermee voegt u een aantal uren toe aan een datum</td>
<td>AddHours(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>AddMinutes</strong></td>
<td>Hiermee wordt een aantal minuten toegevoegd aan een datum</td>
<td>AddMinutes(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>AddMonths</strong></td>
<td>Hiermee voegt u een aantal maanden toe aan een datum</td>
<td>AddMonths(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>AddSeconds</strong></td>
<td>Hiermee wordt een aantal seconden toegevoegd aan een datum</td>
<td>AddSeconds(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>AddYaren</strong></td>
<td>Hiermee wordt een aantal jaren toegevoegd aan een datum</td>
<td>AddYear(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>ConvertNTZ</strong></td>
<td>Hiermee wordt tijdstempel NTZ (tijdstempel zonder tijdzone) omgezet in TZ (tijdstempel met tijdzone) door gedefinieerde sessie TZ toe te passen</td>
<td>ConvertNTZ(&lt;date+time&gt;)</td>
</tr>
<tr>
<td><strong>DateCmp</strong></td>
<td>Twee datums vergelijken</td>
<td>DateCmp(&lt;date&gt;, &lt;date&gt;)</td>
</tr>
<tr>
<td><strong>DateOnly</strong></td>
<td>Retourneert alleen de datum (met tijd om 00:00)</td>
<td>DateOnly(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>Dag</strong></td>
<td>Retourneert het getal dat de dag van de datum vertegenwoordigt</td>
<td>Dag (&lt;datum&gt;)</td>
</tr>
<tr>
<td><strong>DayOfYear</strong></td>
<td>Retourneert het getal van de dag in het jaar van de datum</td>
<td>DayOfYear(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgo</strong></td>
<td>Retourneert de datum die overeenkomt met de huidige datum min n dagen</td>
<td>DaysAgo(&lt;number&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgoInt</strong></td>
<td>Retourneert de datum (geheel getal jjjjmmdd) die overeenkomt met de huidige datum min n dagen</td>
<td>DaysAgoInt(&lt;number&gt;)</td>
</tr>
<tr>
<td><strong>DaysDiff</strong></td>
<td>Retourneert het aantal dagen tussen twee datums</td>
<td>DaysDiff(&lt;einddatum&gt;, &lt;begindatum&gt;)</td>
</tr>
<tr>
<td><strong>DaysOld</strong></td>
<td>Retourneert de leeftijd in dagen van een datum</td>
<td>DaysOld(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>GetDate</strong></td>
<td>Retourneert de huidige systeemdatum van de server</td>
<td>GetDate()</td>
</tr>
<tr>
<td><strong>Uur</strong></td>
<td>Retourneert het uur van de datum</td>
<td>Uur(&lt;datum&gt;)</td>
</tr>
<tr>
<td><strong>HoursDiff</strong></td>
<td>Retourneert het aantal uren tussen twee datums</td>
<td>HoursDiff(&lt;einddatum&gt;, &lt;begindatum&gt;)</td>
</tr>
<tr>
<td><strong>Minute</strong></td>
<td>Retourneert de minuten van de datum</td>
<td>Minuut(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>MinutesDiff</strong></td>
<td>Retourneert het aantal minuten tussen twee datums</td>
<td>MinutesDiff(&lt;end date&gt;, &lt;start date&gt;)</td>
</tr>
<tr>
<td><strong>Maand</strong></td>
<td>Retourneert het getal dat de maand van de datum vertegenwoordigt</td>
<td>Maand (&lt;datum&gt;)</td>
</tr>
<tr>
<td><strong>MonthsAgo</strong></td>
<td>Retourneert de datum die overeenkomt met de huidige datum min n maanden</td>
<td>MonthsAgo(&lt;number&gt;)</td>
</tr>
<tr>
<td><strong>MonthsDiff</strong></td>
<td>Retourneert het aantal maanden tussen twee datums</td>
<td>MonthsDiff(&lt;end date&gt;, &lt;start date&gt;)</td>
</tr>
<tr>
<td><strong>MonthsOld</strong></td>
<td>Retourneert de leeftijd in maanden van een datum</td>
<td>MonthsOld(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>Oudst</strong></td>
<td>Retourneert de oudste datum in een bereik</td>
<td>Oudst(&lt;datum, datum&gt;)</td>
</tr>
<tr>
<td><strong>Seconde</strong></td>
<td>Retourneert de seconden van de datum</td>
<td>Second(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>SecondsDiff</strong></td>
<td>Retourneert het aantal seconden tussen twee datums</td>
<td>SecondsDiff(&lt;einddatum&gt;, &lt;begindatum&gt;)</td>
</tr>
<tr>
<td><strong>Subdagen</strong></td>
<td>Hiermee trekt u een aantal dagen van een datum af</td>
<td>SubDays(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>SubHours</strong></td>
<td>Hiermee wordt een aantal uren van een datum afgetrokken</td>
<td>SubHours(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>SubMinutes</strong></td>
<td>Hiermee wordt een aantal minuten van een datum afgetrokken</td>
<td>SubMinutes(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>Submaanden</strong></td>
<td>Hiermee trekt u een aantal maanden van een datum af</td>
<td>SubMonths(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>SubSeconds</strong></td>
<td>Trekt een aantal seconden van een datum af</td>
<td>SubSeconds(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>Subjaren</strong></td>
<td>Hiermee trekt u een aantal jaren van een datum af</td>
<td>SubYear(&lt;date&gt;, &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>ToDate</strong></td>
<td>Converteert een datum + tijd als datum</td>
<td>TotDatum (&lt;datum + tijd&gt;)</td>
</tr>
<tr>
<td><strong>ToDateTime</strong></td>
<td>Zet een tekenreeks om in een datum + tijd</td>
<td>ToDateTime(&lt;string&gt;)</td>
</tr>
<tr>
<td><strong>ToTimestamp</strong></td>
<td>Hiermee wordt een tekenreeks omgezet in een tijdstempel</td>
<td>ToTimestamp(&lt;string&gt;)</td>
</tr>
<tr>
<td><strong>ToTimeZone</strong></td>
<td>Converteert een datum + tijd naar een tijdzone</td>
<td>ToTimeZone(&lt;date&gt;, &lt;tijdzone&gt;)</td>
</tr>
<tr>
<td><strong>TruncDate</strong></td>
<td>Rondt een datum + tijd aan het dichtstbijzijnde tweede</td>
<td>TruncDate(@lastModified, &lt;aantal seconden&gt;)</td>
</tr>
<tr>
<td><strong>TruncDateTZ</strong></td>
<td>Rondt een datum + tijd aan een bepaalde precisie die in seconden wordt uitgedrukt</td>
<td>TruncDateTZ(&lt;date&gt;, &lt;number of seconds&gt;, &lt;time zone&gt;)</td>
</tr>
<tr>
<td><strong>TruncQuarter</strong></td>
<td>Rondt een datum af op het kwartaal</td>
<td>TruncQuarter(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>TruncTime</strong></td>
<td>Rondt het tijdsdeel af tot de dichtstbijzijnde seconde</td>
<td>TruncTime(&lt;date&gt;, &lt;number of seconds&gt;)</td>
</tr>
<tr>
<td><strong>Truncweek</strong></td>
<td>Rondt een datum af naar de week</td>
<td>TruncWeek(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>TruncYear</strong></td>
<td>Rondt een datum + tijd tot 1 januari van het jaar</td>
<td>TruncYear(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>WeekDay</strong></td>
<td>Retourneert een getal dat de dag in de week van de datum vertegenwoordigt (0=maandag, 6=zondag)</td>
<td>WeekDay(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>Jaar</strong></td>
<td>Retourneert het getal dat het jaar van de datum vertegenwoordigt</td>
<td>Jaar (&lt;datum&gt;)</td>
</tr>
<tr>
<td><strong>YearAndMonth</strong></td>
<td>Retourneert het getal dat het jaar en de maand van de datum vertegenwoordigt.</td>
<td>YearAndMonth(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>JarenAgo</strong></td>
<td>Geeft als resultaat het aantal jaren tussen een bepaalde datum en de huidige datum</td>
<td>YearAgo(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>YearDiff</strong></td>
<td>Retourneert het aantal jaren tussen twee datums</td>
<td>YarenDiff(&lt;einddatum&gt;, &lt;begindatum&gt;)</td>
</tr>
<tr>
<td><strong>JarenOud</strong></td>
<td>Retourneert de leeftijd in jaren van een datum</td>
<td>YearOld(&lt;date&gt;)</td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>Merk op dat de **DateOnly** functie rekening houdt met timezone van de server, niet de exploitant.


### Geomarketing

De geomarketing-functies worden gebruikt om geografische waarden te manipuleren.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> Retourneert de afstand tussen twee punten die worden gedefinieerd door hun lengte en breedte, uitgedrukt in graden.<br /> </td> 
   <td> Distance(&lt;Lengtegraad A&gt;, &lt;Breedtegraad A&gt;, &lt;Lengtegraad B&gt;, &lt;Breedtegraad B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Numeriek

De numerieke functies worden gebruikt om tekst om te zetten in getallen.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> Retourneert de absolute waarde van een getal<br /> </td> 
   <td> Abs(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> Retourneert het laagste gehele getal dat groter is dan of gelijk is aan een getal<br /> </td> 
   <td> Ceil(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> Retourneert het grootste gehele getal dat groter is dan of gelijk is aan een getal <br /> </td> 
   <td> Floor(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> Retourneert het hoogste van twee getallen<br /> </td> 
   <td> Greatest(&lt;nummer 1&gt;, &lt;nummer 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> Retourneert het laagste van twee getallen<br /> </td> 
   <td> Least(&lt;nummer 1&gt;, &lt;nummer 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> Keert de rest van de geheelverdeling van n1 door n2 terug <br /> </td> 
   <td> Mod(&lt;nummer 1&gt;, &lt;nummer 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> Retourneert de verhouding van twee getallen uitgedrukt als een percentage<br /> </td> 
   <td> Percent(&lt;nummer 1&gt;, &lt;nummer 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> Hiermee wordt de willekeurige waarde geretourneerd<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> Rondt een getal af naar n decimalen<br /> </td> 
   <td> Round(&lt;nummer&gt;, &lt;aantal decimalen&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> Hiermee wordt het teken van het getal geretourneerd<br /> </td> 
   <td> Sign(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> Hiermee wordt een geheel getal omgezet in een zwevende waarde<br /> </td> 
   <td> ToDouble(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> Zet een zwevende waarde om in een 64-bits geheel getal<br /> </td> 
   <td> ToInt64(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> Hiermee wordt een zwevende waarde omgezet in een geheel getal<br /> </td> 
   <td> ToInteger(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> Kapt aantal decimalen af van n1 tot n2<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Overige

Deze tabel bevat de resterende beschikbare functies.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong> AESEncrypt </strong><br /> </td> 
   <td> Codeer koord dat in argument wordt verstrekt <br /> </td> 
   <td> AESEncrypt (&lt;value&gt;) <br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> Retourneert waarde 1 als de voorwaarde true is. Als niet, keert het waarde 2 terug.<br /> </td> 
   <td> Case(When(&lt;voorwaarde&gt;, &lt;waarde 1&gt;), Else(&lt;waarde 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> Hiermee verwijdert u de markering in de waarde<br /> </td> 
   <td> ClearBit(&lt;identificatiecode&gt;, &lt;markering&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> Retourneert waarde 2 als waarde 1 null of nihil is, anders wordt waarde 1 geretourneerd<br /> </td> 
   <td> Coalesce(&lt;waarde 1&gt;, &lt;waarde 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> Retourneert waarde 3 als waarde 1 = waarde 2. Indien niet waarde 4 terugkeert.<br /> </td> 
   <td> Decode(&lt;waarde 1&gt;, &lt;waarde 2&gt;, &lt;waarde 3&gt;, &lt;waarde 4&gt;)<br /> </td>  
  </tr>

<tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> Retourneert waarde 1 (mag alleen worden gebruikt als parameter van de case-functie)<br /> </td> 
   <td> Else (&lt;value 1&gt;, &lt;value 2&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> Extraheert het domein uit een e-mailadres<br /> </td> 
   <td> GetEmailDomain(&lt;waarde&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> Hiermee wordt de URL van de server van de spiegelpagina opgehaald<br /> </td> 
   <td> GetMirrorURL(&lt;waarde&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> Retourneert waarde 1 als de expressie true is. Als niet, keert waarde 2 <br /> terug </td> 
   <td> Iif(&lt;voorwaarde&gt;, &lt;waarde 1&gt;, &lt;waarde 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> Geeft aan of de markering zich in de waarde bevindt<br /> </td> 
   <td> IsBitSet(&lt;identificatiecode&gt;, &lt;markering&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> Retourneert waarde 2 als tekenreeks 1 leeg is, anders retourneert u waarde 3 <br /> </td> 
   <td> IsEmptyString (&lt;value 1&gt;, &lt;value 2&gt;, &lt;value 3&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong> NewUID </strong><br /> </td> 
   <td> Retourneert een unieke id <br /> </td> 
   <td> NewUID() <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> Retourneert de lege tekenreeks als het argument NULL is<br /> </td> 
   <td> NoNull(&lt;waarde&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> Retourneert het regelnummer<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> Hiermee wordt de markering in de waarde geforceerd<br /> </td> 
   <td> SetBit(&lt;identificatiecode&gt;, &lt;markering&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> Hiermee wordt een getal omgezet in een Booleaanse waarde<br /> </td> 
   <td> ToBoolean(&lt;nummer&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> Retourneert waarde 1 als de expressie true is. Als niet, keert het waarde 2 terug (kan slechts als parameter van de case functie worden gebruikt) <br /> </td> 
   <td> When(&lt;voorwaarde&gt;, &lt;waarde 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### String

De tekenreeksfuncties worden gebruikt om een set tekenreeksen te manipuleren.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> Geeft aan of alle parameters niet null en niet leeg zijn<br /> </td> 
   <td> AllNonNull2(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> Geeft aan of alle parameters niet null en niet leeg zijn<br /> </td> 
   <td> AllNonNull3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> Ascii </strong><br /> </td> 
   <td> Keert de waarde van ASCII van het eerste karakter in het koord terug.<br /> </td> 
   <td> Ascii(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> Hiermee wordt het teken geretourneerd dat overeenkomt met de ASCII-code ‘n’<br /> </td> 
   <td> Char(&lt;number&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> Keert de positie van koord 2 in koord 1 terug.<br /> </td> 
   <td> Charindex(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> dataLength </strong><br /> </td> 
   <td> Keert de grootte in bytes van het koord terug <br /> </td> 
   <td> dataLength(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> Retourneert de n-de (van 1 tot en met n) regel van de tekenreeks<br /> </td> 
   <td> GetLine(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> Retourneert de derde parameter als de eerste twee parameters gelijk zijn. Indien niet, keert de laatste parameter <br /> terug </td> 
   <td> IfEquals(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> Geeft aan of het als parameter doorgegeven memo null is<br /> </td> 
   <td> IsMemoNull(&lt;memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> Voegt de doorgegeven tekenreeksen samen als parameters. Voegt ruimten tussen de koorden toe indien nodig.<br /> </td> 
   <td> JuxtWords(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> Voegt de doorgegeven tekenreeksen samen als parameters. Voegt indien nodig spaties tussen de tekenreeksen toe <br /> </td> 
   <td> JuxtWords3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> Retourneert de eerste n tekens van de tekenreeks<br /> </td> 
   <td> Left(&lt;string&gt;, &lt;number&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> Keert de lengte van het koord <br /> terug </td> 
   <td> Lengte (&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> Lijn </strong><br /> </td> 
   <td> Regel n uit tekenreeks extraheren <br /> </td> 
   <td> Regel (&lt;string&gt;,&lt;number&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> Hiermee wordt de tekenreeks in kleine letters geretourneerd<br /> </td> 
   <td> Lower(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> Hiermee wordt de voltooide tekenreeks links geretourneerd<br /> </td> 
   <td> LPad (&lt;String&gt;, &lt;Number&gt;, &lt;Char&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> Hiermee worden spaties links van de tekenreeks verwijderd<br /> </td> 
   <td> Ltrim(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> Retourneert een hexadecimale representatie van de MD5-toets van een tekenreeks<br /> </td> 
   <td> Md5Digest(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> Hiermee wordt opgegeven of het memo de tekenreeks bevat die als parameter is doorgegeven<br /> </td> 
   <td> MemoContains(&lt;memo&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> NodeValue </strong><br /> </td> 
   <td> Extraheert de waarde van een gebied van XML van zijn XPath en de gebiedsgegevens <br /> </td> 
   <td> NodeValue (&lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> Vervangt alle voorkomen van een gespecificeerde koordwaarde met een andere koordwaarde.<br /> </td> 
   <td> Replace(&lt;String&gt;,&lt;String&gt;,&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> Retourneert de laatste n tekens van de tekenreeks<br /> </td> 
   <td> Right(&lt;tekenreeks&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> Hiermee wordt de voltooide tekenreeks aan de rechterkant geretourneerd<br /> </td> 
   <td> RPad(&lt;string&gt;, &lt;number&gt;, &lt;character&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> Hiermee worden spaties rechts van de tekenreeks verwijderd<br /> </td> 
   <td> Rtrim(&lt;tekenreeks&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> Hexadecimale vertegenwoordiging van de sleutel SHA256 van een koord.<br /> </td> 
   <td> Sha256Digest (&lt;String&gt;) <br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> Hexadecimale vertegenwoordiging van de sleutel SHA512 van een koord.<br /> </td> 
   <td> Sha512Digest (&lt;String&gt;) <br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> Retourneert de tekenreeks met de eerste letter van elk woord in hoofdletters<br /> </td> 
   <td> Smart(&lt;tekenreeks&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> Extraheert substring die bij karakter n1 van het koord en van lengte n2 begint <br /> </td> 
   <td> Substring(&lt;tekenreeks&gt;, &lt;offset&gt;, &lt;lengte&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> Zet het getal om in een tekenreeks<br /> </td> 
   <td> ToString (&lt;number&gt;, &lt;number&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> Hiermee wordt de tekenreeks in hoofdletters geretourneerd<br /> </td> 
   <td> Upper(&lt;tekenreeks&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> Retourneert de externe sleutel van een koppeling die als een parameter is doorgegeven als de andere twee parameters gelijk zijn<br /> </td> 
   <td> VirtualLink(&lt;nummer&gt;, &lt;nummer&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> Retourneert de externe sleutel (tekst) van een koppeling die als parameter wordt doorgegeven als de andere twee parameters gelijk zijn<br /> </td> 
   <td> VirtualLinkStr(&lt;tekenreeks&gt;, &lt;nummer&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Venster

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_Over__</strong><br /> </td> 
   <td> Voer de SQL functievraag uit die als 1st parameter, over Verdeling of Orde door de gebieden is ingegaan als 2de parameter <br /> is ingegaan </td> 
   <td> _Over_ (&lt;Value&gt;, &lt;Value&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> Hiermee wordt een aflopende sortering toegepast<br /> </td> 
   <td> Desc(&lt;waarde 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> Hiermee wordt het resultaat binnen de partitie gesorteerd<br /> </td> 
   <td> OrderBy(&lt;waarde 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> Verdeelt het resultaat van een query op een lijst<br /> </td> 
   <td> PartitionBy(&lt;waarde 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> Produceert een lijnaantal dat op de lijstverdeling en op een sorterende opeenvolging wordt gebaseerd.<br /> </td> 
   <td> RowNum(PartitionBy(&lt;waarde 1&gt;), OrderBy(&lt;waarde 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
