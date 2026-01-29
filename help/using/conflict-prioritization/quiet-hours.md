---
solution: Journey Optimizer
product: journey optimizer
title: Stille uren instellen
description: Leer hoe u rustige uren maakt en toepast
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: bericht, frequentie, regels, druk
source-git-commit: a7d2557790054e7c6e28ca3ffa937f454c4b004c
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 0%

---


# Stille uren instellen {#quiet-hours}

## Wat zijn stille uren

**Stil uren** laat u op tijd-gebaseerde uitsluitingen voor **E-mail**, **SMS**, **Duw**, en **WhatsApp** kanalen bepalen. Zij zorgen ervoor dat geen berichten tijdens specifieke periodes worden verzonden, die u helpen klantenvoorkeur en nalevingsvereisten respecteren.

U kunt stille uren door **regelreeksen** toepassen, die aan individuele acties in campagnes of reizen voor nauwkeurige controle kunnen worden toegewezen.

Door deze processen te stroomlijnen, kunt u klantenervaring verbeteren, tijd besparen, en naleving van communicatie regels verzekeren:

* **wordt niet wakker uw klant** - *de juiste klant, het juiste kanaal, de juiste tijd* is mantra van vele marketers, zodat het steek houdt dat de timing een kritiek deel van de klantenreis is. Door een regel voor stille uren in te stellen, hebben merken meer controle over het tijdstip waarop contactpersonen berichten ontvangen, zodat ze deze ontvangen wanneer ze waarschijnlijk actie zullen ondernemen op uw bericht.
* **Handigheid** - onderschept gemakkelijk mededelingen over campagnes &amp; reizen wanneer u een publiek moet verhinderen een bericht te ontvangen zonder de volledige reis of de campagne te moeten tegenhouden.
* **Tijd die** bespaart - beheer uitsluitingen op één plaats door a **op tijd-gebaseerde regel** te creëren, in plaats van het toevoegen van veelvoudige voorwaardenknopen met douaneuitdrukkingen.\
  <!--* **Extra Safeguard** - Benefit from an extra safeguard in case audience criteria or time-window configurations were incorrectly set, ensuring individuals are still excluded when they should be.-->

➡️ [Ontdek deze functie in video](#video)

## Afbeeldingen en beperkingen

* **Gesteunde kanalen** - E-mail, SMS, Duw, en WhatsApp.
* **Geordende campagnes** - de stille uren worden niet gesteund voor Geordende campagnes.
* {de vertraging van de Verspreiding 0} **- de Updates aan een stille urenregel kunnen tot 12 uren vergen om op kanaalacties worden toegepast die reeds die regel gebruiken.**
* **Hoog-volumelatentie** - in gevallen van hoog-volumemededelingen, kan het systeem extra tijd nemen beginnen met het met succes afdwingen van stille uuronderdrukking.

<!--* **Custom actions** – For custom actions, only quiet hours rules are enforced. If a rule set also includes other rules (e.g., frequency capping), those rules are ignored.-->
<!--* **Pre-suppression window** – The system begins suppressing communications 30 minutes before quiet hours start, ensuring that no messages are delivered once the quiet period begins.-->

## Regels voor stille uren maken

Om stille uren te plaatsen, creeer een regel binnen een reeks van de douaneregel. [&#x200B; Leer hoe te om regelreeksen &#x200B;](../conflict-prioritization/rule-sets.md#Create) tot stand te brengen. Voer de volgende stappen uit:

1. Navigeer naar **[!UICONTROL Business rules]** om toegang te krijgen tot het overzicht van regelsets.

1. Kies een bestaande aangepaste regelset of maak een nieuwe set:

   +++Creeer een stille urenregel in een bestaande regelreeks

   Selecteer de regelset in het overzicht. De stille urenregels kunnen slechts aan regelreeksen met het &quot;kanaal&quot;domein worden toegevoegd. U kunt deze informatie controleren in de kolom **[!UICONTROL Domain]** .

   ![](assets/journey-capping-list.png)

   +++

   +++Creeer een stille urenregel in een nieuwe regelreeks

   Klik op **[!UICONTROL Create rule set]** , voer een unieke naam in en selecteer Kanaal in de vervolgkeuzelijst **[!UICONTROL Rule Set Domain]** .

   ![](assets/rule-sets-create.png)

   +++

   >[!NOTE]
   >
   >De stille uren kunnen slechts in **reeksen van de douaneregel** worden bepaald. De globale regelreeks steunt rustige uurconfiguratie niet.

1. Klik in het scherm met regelsets op **[!UICONTROL Add Rule]** en geef een unieke naam voor de regel op.

1. Het **gebied van de Categorie** specificeert de categorie van bericht de regel op van toepassing is. Momenteel is dit veld alleen-lezen en standaard ingesteld op **[!UICONTROL Marketing]** .

1. Selecteer **[!UICONTROL Rule type]** in de vervolgkeuzelijst **[!UICONTROL Quiet hours]** .

   ![](assets/quiet-hours-type.png)

1. Definieer in de sectie **[!UICONTROL Dates & times]** wanneer u stille uren wilt toepassen:

   1. Pas in de vervolgkeuzelijst **[!UICONTROL Time zone]** een standaardtijdzone toe op alle ontvangers in het publiek, ongeacht hun afzonderlijke tijdzones.

      Selecteer **[!UICONTROL Use recipients local time zone]** als u het tijdzoneveld van elk profiel wilt gebruiken. [&#x200B; leer meer op het beheer van de tijdzone in reizen &#x200B;](../building-journeys/timezone-management.md#timezone-from-profiles)

      >[!IMPORTANT]
      >
      >Als een profiel geen tijdzone heeft, worden de stille uren niet afgedwongen voor dat profiel.

   1. Geef de periode op waarop de stille uren moeten worden toegepast.

      * **[!UICONTROL Weekly]** - Kies specifieke dagen van de week en een tijdreeks. U kunt de regel ook afdwingen **[!UICONTROL All day]** .

        ![](assets/quiet-hours-weekly.png)

      * **[!UICONTROL Custom date]** - Kies specifieke datums in de kalender en een tijdspad. U kunt de regel ook afdwingen **[!UICONTROL All day]** .

        ![](assets/quiet-hours-custom.png)

   1. Klik op de knop **[!UICONTROL Add more dates]** om maximaal vijf afzonderlijke punten toe te voegen.

      ![](assets/quiet-hours-date.png)

1. Kies in de sectie **[!UICONTROL Handling actions during quiet hours]** hoe berichten tijdens de geselecteerde periode worden behandeld:

   ![](assets/quiet-hours-queue.png)

   * **[!UICONTROL Queue message]** - Berichten worden verzonden wanneer de stille tijdsperiode is voltooid, tenzij de status Gepauzeerd is.

     >[!NOTE]
     >
     >Als een bericht langer dan 7 dagen in een wachtrij voor een profiel blijft staan, wordt het bericht genegeerd.

   * **[!UICONTROL Discard message]** - Berichten worden nooit verzonden.

     >[!NOTE]
     >
     >Als u **[!UICONTROL Discard]** selecteert en deze regel op een reisactie toepast, wordt het profiel verwijderd uit de berichtlevering en van de reis verlaten.

De regel wordt nu weergegeven in de regelset. U kunt het selecteren om zijn details in de eigenschappen ruit te tonen.

![](assets/quiet-hours-preview.png)

Als uw regel klaar is, activeer het en voltooi de configuratie van uw regelreeks. [&#x200B; leer hoe te om regelreeksen tot stand te brengen en te activeren &#x200B;](../conflict-prioritization/rule-sets.md#Create)

## Stil uur toepassen op reizen en campagnes {#apply}

Nadat u de regel hebt opgeslagen en de regelset hebt geactiveerd, kunt u deze toepassen op handelingen tijdens reizen en campagnes. Ondersteunde kanalen: **E-mail, SMS, Duw, WhatsApp**. Blader op de onderstaande tabbladen voor meer informatie.

>[!BEGINTABS]

>[!TAB  pas de acties van het het urenkanaal van de stilte in reizen toe ]

1. Open uw reis, selecteer de actie van het a [&#x200B; kanaal &#x200B;](../building-journeys/journeys-message.md) en geef de inhoud van uw bericht uit.
1. Klik op de knop **[!UICONTROL Add Business Rule]** en selecteer de regelset die de regel voor stille uren bevat.

   ![](assets/quiet-hours-apply.png)

   >[!NOTE]
   >
   >Slechts [&#x200B; geactiveerde &#x200B;](#activate-rule) regelreeksen tonen in de lijst.

1. Activeer je reis.

>[!TAB  pas stille uren op campagneacties toe ]

1. Bewerk uw campagne en open het tabblad **[!UICONTROL Actions]** .
1. Selecteer in de sectie **[!UICONTROL Business rules]** de regelset die de regel voor stille uren bevat.

   ![](assets/quiet-hours-campaign.png)

   >[!NOTE]
   >
   >Slechts [&#x200B; geactiveerde &#x200B;](#activate-rule) regelreeksen tonen in de lijst.

1. Activeer uw campagne.

>[!ENDTABS]

## Volgende stappen

Zodra uw reis of campagnes zijn geactiveerd en uitgevoerd, kunt u het aantal profielen bekijken die van de mededeling in het [&#x200B; rapport van Customer Journey Analytics &#x200B;](../reports/report-gs-cja.md) worden uitgesloten, en in het [&#x200B; Levende rapport &#x200B;](../reports/live-report.md), waar de de urenregels van de Quiet als mogelijke reden voor gebruikers die van levering worden uitgesloten zullen worden vermeld.

![](assets/quiet-hours-report.png)





<!--

>[!TAB Apply Quiet hours to custom actions]

1. Open your journey and add or select a custom action in the canvas.

1. In the **[!UICONTROL Business rules]** section, select the rule set containing the Quiet hours rule.

   ![](assets/quiet-hours-custom-action.png)

   >[!NOTE]
   >
   >Only [activated](#activate-rule) rule sets display in the list.

1. Activate your journey.

-->


## Hoe kan ik-video {#video}

Leer hoe u de functie voor stille uren in Adobe Journey Optimizer kunt gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/3475858?captions=dut&quality=12)
