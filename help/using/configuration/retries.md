---
solution: Journey Optimizer
product: journey optimizer
title: Opnieuw
description: Leer hoe opnieuw proberen alvorens een adres naar de onderdrukkingslijst te verzenden
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: opnieuw proberen, stuiteren, zacht, optimaliseren, fout
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
source-git-commit: 0db7f514a2604ad09fbd9863a51d3c86d69eac41
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Opnieuw {#retries}

Wanneer een e-mailbericht wegens een tijdelijke **Zachte stuitfout** voor een bepaald adres ontbreekt, worden verscheidene pogingen uitgevoerd. Elke fout verhoogt een foutenteller. Wanneer deze teller de grensdrempel bereikt, wordt het e-mailadres toegevoegd aan de onderdrukkingslijst.

>[!NOTE]
>
>Leer meer over de types van fouten in de [ types van mislukkingen van de Levering ](../reports/suppression-list.md#delivery-failures) sectie.

In de standaardconfiguratie is de drempel ingesteld op 5 fouten.

* Voor de zelfde levering, bij de vijfde ondervond fout binnen de [ periode van de herprobeert tijd ](#retry-duration), wordt het adres onderdrukt.

* Als er verschillende leveringen zijn en twee fouten minstens 24 uur uit elkaar voorkomen, wordt de foutenteller verhoogd op elke fout en het adres wordt ook onderdrukt bij de vijfde poging. Fouten zijn cumulatief voor elk adres.

Als de levering succesvol is nadat opnieuw is geprobeerd, wordt de foutenteller van het adres opnieuw geïnitialiseerd.

Bijvoorbeeld:

* U verzendt een e-mail op Maandag met een herbestellingstijd die aan 24 uren wordt geplaatst. Het `emma.jones@mail.com` -adres kan niet worden bezorgd. Het e-mailbericht wordt tot drie keer opnieuw geprobeerd en probeert het niet meer tijdens de periode van 24 uur voor opnieuw proberen.

* U verzendt nog een e-mail op woensdag. De instructie `emma.jones@mail.com`, die al een telling met drie fouten bevat, is ook bedoeld en kan opnieuw niet worden afgeleverd - twee keer. Er zijn nog twee fouten.

Op voorwaarde dat tussen deze twee e-mails geen andere levering is geprobeerd en geen succes is, wordt het `emma.jones@mail.com` -adres toegevoegd aan de lijst met onderdrukking vanwege de cumulatieve impact van 3 + 2 fouten.

## Drempelwaarde voor opnieuw proberen {#edit-retry-threshold}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_bounces"
>title="De drempel voor opnieuw proberen bijwerken"
>abstract="Als de standaardwaarde niet aan uw behoeften voldoet, kunt u het toegestane aantal opeenvolgende zachte grenzen wijzigen. Wanneer de teller voor opnieuw proberen de foutendrempel voor een specifiek e-mailadres bereikt, wordt dit adres toegevoegd aan de onderdrukkingslijst."
<!--
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/reporting/deliverability/suppression-list.html" text="Understand the suppresion list"-->

Als de standaardwaarde 5 niet aan uw wensen voldoet, kunt u de foutdrempel wijzigen volgens de onderstaande stappen.

1. Ga naar **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** > **[!UICONTROL Suppression list]** .

1. Selecteer de knop **[!UICONTROL Edit suppression rules]**.

   ![](assets/suppression-list-edit-retries.png)

1. Pas het toegestane aantal opeenvolgende zachte grenzen aan uw wensen aan.

   ![](assets/suppression-list-edit-soft-bounces.png)

   U moet een geheel getal tussen 1 en 20 invoeren. Dit betekent dat het minimum aantal pogingen 1 is en het maximum aantal 20.

   >[!CAUTION]
   >
   >Om het even welke waarde hoger dan 10 kan de kwesties van de leveringsreputatie, evenals IP het vertragen of het voegend op lijst van gewenste personen door ISPs veroorzaken. [ Leer meer over leverbaarheid ](../reports/deliverability.md)

## Periode voor opnieuw proberen {#retry-duration}

De **periode van de herprobeer tijd** is timeframe waarin om het even welk e-mailbericht van de levering die een tijdelijke fout of zachte stuit ondervond opnieuw zal worden geprobeerd.

Door gebrek, zal het opnieuw proberen voor **3.5 dagen** (of **84 uren**) van de tijd worden uitgevoerd het bericht aan de e-mailrij werd toegevoegd.

Nochtans, om ervoor te zorgen dat de pogingen van het opnieuw proberen niet meer wanneer niet meer nodig worden uitgevoerd, kunt u dit het plaatsen volgens uw behoeften veranderen wanneer het creëren van of het uitgeven van a [ kanaalconfiguratie ](channel-surfaces.md) die op het e-mailkanaal van toepassing is.

U kunt bijvoorbeeld de periode voor het opnieuw proberen instellen op 24 uur voor een transactie-e-mail die betrekking heeft op het opnieuw instellen van wachtwoorden en die een koppeling bevat die slechts een dag geldig is. Op dezelfde manier kunt u voor een uitverkoop in middernacht een uitzetperiode van 6 uur definiëren.

>[!NOTE]
>
>De periode van opnieuw proberen mag niet langer zijn dan 84 uur. De minimumperiode voor het opnieuw proberen is 6 uur voor marketing e-mails en 10 minuten voor transactie e-mails.

Leer hoe te om e-mail aan te passen herprobeert parameters wanneer het creëren van een kanaalconfiguratie in [ deze sectie ](../email/email-settings.md#email-retry).

