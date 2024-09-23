---
solution: Journey Optimizer
product: journey optimizer
title: Inhoud testen met aangepaste profielen
description: Leer hoe u een voorvertoning van uw inhoud kunt weergeven en proefdrukken kunt verzenden met behulp van aangepaste profielen.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6229f295b961b0535139b64928216e40c3759947
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---


# Inhoud testen met aangepaste profielen {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simuleren met aangepaste profielen"
>abstract="In dit scherm kunt u een voorvertoning van uw inhoud weergeven en proefdrukken verzenden terwijl u aangepaste profielen imiteert die u vanuit een CSV-bestand kunt uploaden of handmatig vanuit dit scherm kunt toevoegen."

>[!AVAILABILITY]
>
>Deze functies zijn momenteel alleen beschikbaar als bètaversie voor geselecteerde gebruikers.
>
>Inbox rendering en spamrapporten zijn niet beschikbaar in de huidige ervaring. Als u deze functies wilt gebruiken, selecteert u de knop **[!UICONTROL Simulate content]** in de inhoud om toegang te krijgen tot de oudere gebruikersinterface.

Met Reis optimizer kunt u uw inhoud voorvertonen en testen met behulp van aangepaste profielen die u kunt uploaden vanuit een CSV-bestand of handmatig kunt toevoegen wanneer u de inhoud simuleert.

Klik op de knop **[!UICONTROL Simulate content]** en kies **[!UICONTROL Simulate with CSV(Beta)]** voor toegang tot deze ervaring.

In dit scherm kunt u profielen selecteren waarmee u een voorvertoning van uw inhoud kunt weergeven en proefdrukken kunt verzenden. Alle kenmerken die in de inhoud voor personalisatie worden gebruikt, worden automatisch door het systeem gedetecteerd en kunnen voor uw tests worden gebruikt.

De belangrijkste stappen om uw inhoud te testen zijn als volgt:

1. Voeg aangepaste profielen toe door een CSV-bestand te uploaden of door deze handmatig toe te voegen. [ leer hoe te om douaneprofielen toe te voegen ](#profiles)
1. Controleer de voorvertoning van uw inhoud met de toegevoegde profielen. [ Leer hoe te om uw inhoud ](#preview) voor te vertonen
1. U kunt maximaal 10 proefdrukken naar de e-mailadressen verzenden en tegelijkertijd de gewenste aangepaste profielen nastreven. [ Leer hoe te om proefdrukken ](#proofs) te verzenden


## Aangepaste profielen toevoegen {#profiles}

U kunt aangepaste profielen toevoegen om de inhoud te testen met behulp van een CSV-bestand of handmatig:

* Als u profielen wilt uploaden vanuit een CSV-bestand, klikt u op de koppeling **[!UICONTROL Download template]** om een CSV-bestandssjabloon op te halen. Deze sjablonen bevatten een kolom voor elk personalisatiekenmerk dat in uw inhoud wordt gebruikt.

  Vul het CSV-bestand in en klik op **[!UICONTROL Upload sample profiles]** om het te laden om de inhoud te testen.

* Als u handmatig een profiel wilt toevoegen, klikt u op de knop **[!UICONTROL Create sample profile]** en vult u de gegevens voor het profiel in. Er wordt één veld weergegeven voor elk personalisatiekenmerk dat in de inhoud wordt gebruikt.

  ![](assets/simulate-custom-add.png)

Nadat de profielen zijn geselecteerd, verschijnt er één vak voor elk profiel aan de linkerkant van het scherm. U kunt deze profielen gebruiken om een voorvertoning van uw inhoud weer te geven en proefdrukken te verzenden.

## Inhoud voorvertonen met aangepaste profielen {#preview}

Als u een voorvertoning van de inhoud wilt weergeven met een van de profielen, schakelt u het desbetreffende vak in om de voorvertoning van de inhoud in de rechtersectie bij te werken met de informatie die u voor dit profiel hebt ingevoerd.

U kunt een vak op elk gewenst moment verwijderen met de ellipknop in de rechterbovenhoek en door **[!UICONTROL Remove]** te selecteren. Als u informatie voor een profiel wilt bewerken, klikt u op de knop voor weglatingsteken en selecteert u **[!UICONTROL Edit]** .

![](assets/simulate-custom-boxes.png)

## Proefdrukken verzenden {#proofs}

Met Journey Optimizer kunt u proefdrukken naar e-mailadressen verzenden en tegelijkertijd een of meerdere aangepaste profielen nabootsen die u in het simulatiescherm hebt toegevoegd. De stappen zijn als volgt:

1. Controleer of er aangepaste profielen zijn toegevoegd om de inhoud te testen en klik op de knop **[!UICONTROL Send Proof]** .

1. Voer in het veld **[!UICONTROL Recipients]** het e-mailadres in waarnaar u de proefdruk wilt verzenden en klik vervolgens op **[!UICONTROL Add]** . Herhaal de bewerking om de proefdruk naar extra e-mailadressen te verzenden. U kunt maximaal tien proefontvangers toevoegen.

1. Selecteer in het onderste gedeelte van het scherm de aangepaste profielen die u wilt weergeven in de proefdruk. U kunt meerdere profielen selecteren. In dat geval bevat de e-mail evenveel proefdrukken als geselecteerde profielen.

   ![](assets/simulate-custom-proofs.png)

1. Klik op de knop **[!UICONTROL Send Proof]** om de proefdruk te verzenden.

U kunt het verzenden op elk gewenst moment volgen door op de knop **[!UICONTROL View proofs]** in het scherm met gesimuleerde inhoud te klikken.

![](assets/simulate-custom-sent-proofs.png)
