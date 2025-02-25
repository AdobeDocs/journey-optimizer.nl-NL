---
solution: Journey Optimizer
product: journey optimizer
title: Bladeren en uw reizen filteren
description: Bladeren en filteren in Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: reis, eerste, begin, snel-begin, publiek, gebeurtenis, actie
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 2%

---

# Bladeren en uw reizen filteren {#browse-journeys}

## Toegang tot reizen {#journey-access}

### Reisdashboard {#dashboard-jo}

Klik in de menusectie JOURNEY MANAGEMENT op **[!UICONTROL Journeys]** . Er zijn twee tabbladen beschikbaar: **[!UICONTROL Overview]** en **[!UICONTROL Browse]** .

* Op het tabblad **[!UICONTROL Overview]** wordt een dashboard weergegeven met de belangrijkste maatstaven voor uw reizen:

   * **verwerkte Profielen**: totaal aantal profielen die in de laatste 24 uren worden verwerkt
   * **Levende reizen**: totaal aantal levende reizen met verkeer over de laatste 24 uren. De actieve reizen omvatten **Eenheids reizen** (gebeurtenis-gebaseerd) en **ritten van de Partij** (gelezen publiek).
   * **tarief van de Fout**: verhouding van alle profielen in fout vergeleken met het totale aantal profielen die over de laatste 24 uren inging.
   * **verwerpt tarief**: verhouding van alle verworpen profielen vergeleken met het totale aantal profielen die de afgelopen 24 uren inging. Een weggegooid profiel vertegenwoordigt iemand die niet in aanmerking komt om de reis binnen te gaan, bijvoorbeeld vanwege een onjuiste naamruimte of vanwege toegangsregels.

  >[!NOTE]
  >
  >Dit dashboard houdt rekening met de reizen met verkeer in de afgelopen 24 uur. Alleen de reizen waartoe u toegang hebt, worden weergegeven. De metriek worden verfrist om de 30 minuten en slechts wanneer de nieuwe gegevens beschikbaar zijn.

  ![](assets/journeys-dashboard.png)

* Op het tabblad **[!UICONTROL Browse]** wordt de lijst met bestaande reizen weergegeven. U kunt reizen zoeken, filters gebruiken en basishandelingen op elk element uitvoeren. U kunt bijvoorbeeld een item dupliceren of verwijderen.

  ![](assets/journeys-browse.png)

### Uw reizen filteren {#filter}

In de lijst met reizen kunt u verschillende filters gebruiken om de lijst met reizen te verfijnen, zodat u deze beter leesbaar kunt maken.

![](assets/filter-journeys.png)

Hier zijn de diverse het filtreren verrichtingen die u kunt uitvoeren:

De ritten van de filter op hun status, type, versie en toegewezen markeringen van **[!UICONTROL Status and version filters]**.

Het type kan zijn: **[!UICONTROL Unitary event]**, **[!UICONTROL Audience qualification]**, **[!UICONTROL Read audience]** of **[!UICONTROL Business event]** .

De status kan zijn:

* **Gesloten**: de reis is gesloten gebruikend **dicht aan nieuwe ingangen** knoop. De reis houdt in dat nieuwe individuen de reis kunnen betreden. Personen die al onderweg zijn, kunnen de reis normaal afmaken.
* **Ontwerp**: de reis is in zijn eerste stadium. Het is nog niet gepubliceerd.
* **Ontwerp (Test)**: de testwijze is geactiveerd gebruikend de **wijze van de Test** knoop.
* **Voltooid**: De reis schakelt automatisch aan deze status na de globale onderbreking 91 dag [ ](journey-properties.md#global_timeout). Profielen die al op reis zijn, worden normaal afgehandeld. Nieuwe profielen kunnen niet langer de reis betreden.
* **Levend**: de reis is gepubliceerd gebruikend **publiceer** knoop.
* **Gestopt**: de reis is uitgezet gebruikend de **3} knoop van het Einde {.** Alle individuen sluiten onmiddellijk de reis.

>[!NOTE]
>
>De publicatielevenscyclus van de Reis omvat ook een reeks tussenliggende statussen die niet beschikbaar zijn voor filtering: &quot;Publishing&quot; (tussen &quot;Draft&quot; en &quot;Live&quot;), &quot;Activating test mode&quot; of &quot;Deactivating test mode&quot; (tussen &quot;Draft&quot; en &quot;Draft (test)&quot;) en &quot;Stopping&quot; (tussen &quot;Live&quot; en &quot;Gestopt&quot;). Wanneer een reis in een tussenstadium is, is het read-only.

Gebruik **[!UICONTROL Creation filters]** om ritten te filteren op basis van de aanmaakdatum of de gebruiker die ze heeft gemaakt.

Geef ritten weer die een specifieke gebeurtenis, veldgroep of handeling van de **[!UICONTROL Activity filters]** en **[!UICONTROL Data filters]** gebruiken.

Gebruik **[!UICONTROL Publication filters]** om een publicatiedatum of een gebruiker te selecteren. U kunt bijvoorbeeld kiezen of u de nieuwste versies wilt weergeven van live reizen die gisteren zijn gepubliceerd.

Selecteer **[!UICONTROL Custom]** in de vervolgkeuzelijst **[!UICONTROL Published]** als u reizen wilt filteren op basis van een specifiek datumbereik.

Daarnaast wordt in het configuratievenster Gebeurtenis, Gegevensbron en Handeling in het veld **[!UICONTROL Used in]** het aantal ritten weergegeven dat die specifieke gebeurtenis, veldgroep of handeling gebruikt. U kunt klikken op de knop **[!UICONTROL View journeys]** om de lijst met corresponderende journey’s weer te geven.

![](assets/journey3bis.png)


## Journeyversies {#journey-versions}

In de reislijst, worden alle reisversies getoond met het versieaantal. Wanneer u een reis zoekt, verschijnen de nieuwste versies bij de eerste keer dat de toepassing wordt geopend boven aan de lijst. Vervolgens kunt u de gewenste sortering definiëren en wordt deze door de toepassing als gebruikervoorkeur behouden. De versie van de reis wordt ook weergegeven boven aan de interface van de reiseditie, boven het canvas.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Gewoonlijk kan een profiel niet meerdere keren op dezelfde reis tegelijk aanwezig zijn. Als de terugkeer wordt toegelaten, kan een profiel een reis opnieuw ingaan, maar kan het niet doen tot zij dat vorige geval van de reis volledig verlaten. [Meer informatie](end-journey.md).

Als u zich aan een levende reis moet aanpassen, creeer een nieuwe versie van uw reis.

1. Open de meest recente versie van uw livereis, klik op **[!UICONTROL Create a new version]** en bevestig deze.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >U kunt alleen een nieuwe versie maken van de meest recente versie van een reis.

1. Breng uw wijzigingen aan, klik op **[!UICONTROL Publish]** en bevestig de selectie.

Vanaf het moment dat de reis wordt gepubliceerd, zullen individuen naar de recentste versie van de reis gaan. Mensen die al een vorige versie hebben ingevoerd, blijven er totdat ze klaar zijn met de reis. Als ze later weer dezelfde reis maken, gaan ze naar de meest recente versie.

Reisversies kunnen afzonderlijk worden gestopt. Alle versies van reizen hebben dezelfde naam.

Wanneer u een nieuwe versie van een reis publiceert, beëindigt de vorige versie automatisch en schakelt aan de **Gesloten** status. Er kan geen toegang tot de reis plaatsvinden. Zelfs als u de laatste versie stopt, blijft de vorige versie gesloten.



## Een reis dupliceren {#duplicate-a-journey}

U kunt een bestaande reis van **dupliceren doorbladert** tabel. Alle objecten en instellingen worden gedupliceerd naar de reiskopie.

Volg onderstaande stappen om dit te doen:

1. Navigeer aan de reis u wilt kopiëren, **klikken Meer acties** pictogram (de drie punten naast de reisnaam).
1. Selecteer **Dupliceren**.

   ![ Dupliceer een reis ](assets/duplicate-jo.png)

1. Voer de naam van de reis in en bevestig deze. U kunt de naam ook wijzigen in het scherm met de reiseigenschappen. Standaard wordt de naam als volgt ingesteld: `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. De nieuwe reis wordt gecreeerd en beschikbaar in de reislijst.

