---
title: E-mailproefdrukken verzenden
description: Leer hoe u proefdrukken per e-mail verzendt.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: 10eaebc1d24eae4a0a149822d31ff92509d1e6f8
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Proefdrukken verzenden met gegevens van testprofielen {#send-proofs}

Een proef is een specifiek bericht dat u toestaat om een bericht te testen alvorens het naar het belangrijkste publiek te verzenden. Ontvangers van de proefdruk zijn verantwoordelijk voor het goedkeuren van het bericht: rendering, content, personalisatie-instellingen, configuratie.

>[!NOTE]
>
>Met [!DNL Journey optimizer] kunt u ook verschillende varianten van uw inhoud testen door deze voor te vertonen en proefdrukken te verzenden met behulp van voorbeeldinvoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of handmatig zijn toegevoegd. [&#x200B; leer hoe te om inhoudvariaties &#x200B;](../test-approve/simulate-sample-input.md) te simuleren

Om e-mailproeven te verzenden die de gegevens van testprofielen gebruiken, moet u [&#x200B; testprofielen &#x200B;](test-profiles.md) eerst selecteren. Voer vervolgens de volgende stappen uit:

1. Klik in het **[!UICONTROL Simulate]** -scherm op de knop **[!UICONTROL Send proof]** .

   ![](../email/assets/send-proof-button.png)

1. Typ in het venster **[!UICONTROL Send proof]** de e-mail van de ontvanger en klik op **[!UICONTROL Add]** om de proefdruk naar uzelf of leden van uw organisaties te verzenden.

   U kunt maximaal tien ontvangers toevoegen voor de proefaflevering.

   ![](../email/assets/send-proof-add.png)

1. Selecteer de **profielen van de Test** om de berichtinhoud te gebruiken te personaliseren.

   Elke ontvanger van de proefdruk ontvangt evenveel berichten als het aantal geselecteerde testprofielen. Als u bijvoorbeeld vijf e-mailberichten voor ontvangers hebt toegevoegd en tien testprofielen hebt geselecteerd, verzendt u vijftig proefdrukberichten en ontvangt elke ontvanger er tien.

1. U kunt desgewenst een voorvoegsel toevoegen aan de onderwerpregel van de proefdruk. Alleen alfanumerieke tekens en speciale tekens zoals . - _ ( ) [ ] zijn toegestaan als voorvoegsel voor de onderwerpregel.

1. Klik op **[!UICONTROL Send proof]**.

   ![](../email/assets/send-proof-select.png)

1. Klik weer in het **[!UICONTROL Simulate]** -scherm op de knop **[!UICONTROL View proofs]** om de status te controleren.

   ![](../email/assets/send-proof-view.png)

Het wordt aanbevolen om na elke wijziging proefdrukken naar de inhoud van het bericht te verzenden.

>[!NOTE]
>
>In de verzonden proefdruk is de verbinding aan de spiegelpagina niet actief. Deze wordt alleen geactiveerd in de laatste berichten.
>
>Assets/Images zijn maximaal 2 jaar (730 dagen) sinds de eerste publicatie ervan in een fragment/inline-bericht toegankelijk in geleverde inhoud of proefdrukinhoud. Na deze vervaldatum (op een willekeurig tijdstip na 730 dagen) moet de publicatie opnieuw worden gepubliceerd om deze twee jaar toegankelijk te houden. Bij elke herpublicatie die binnen 730 dagen na de eerste publicatie wordt uitgevoerd, wordt het vervallen van de middelen/afbeeldingen niet tot de volgende 730 dagen verlengd.
