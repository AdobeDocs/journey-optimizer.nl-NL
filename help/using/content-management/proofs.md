---
title: E-mailproefdrukken verzenden
description: Leer hoe u proefdrukken per e-mail verzendt.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: f874456748a8bd7fce69c7ad2a7e69380d5336a6
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# Proefdrukken verzenden met gegevens van testprofielen {#send-proofs}

Een proef is een specifiek bericht dat u toestaat om een bericht te testen alvorens het naar het belangrijkste publiek te verzenden. Ontvangers van de proefdruk zijn verantwoordelijk voor het goedkeuren van het bericht: rendering, content, personalisatie-instellingen, configuratie.

>[!NOTE]
>
>Met [!DNL Journey Optimizer] kunt u ook verschillende varianten van uw inhoud testen door deze voor te vertonen en proefdrukken te verzenden met behulp van voorbeeldinvoergegevens die vanuit een CSV-/JSON-bestand zijn geüpload of handmatig zijn toegevoegd. [&#x200B; leer hoe te om inhoudvariaties &#x200B;](../test-approve/simulate-sample-input.md) te simuleren

## Meer lezen {#must-read}

**het Afbakenen van de Frequentie regels** - Alle bestaande frequentie die regels afschilderen is op proeven van toepassing. Als u [&#x200B; frequentie het begrenzen regels &#x200B;](../conflict-prioritization/channel-capping.md) hebt geplaatst (b.v., verzendt het maximum per profiel), zijn deze grenzen ook van toepassing wanneer het verzenden van proeven. Als een testprofiel de limiet voor de maximale frequentie al heeft bereikt, worden proefdrukken weergegeven als voltooid, maar wordt er geen e-mail verzonden. Voor herhaalde tests kunt u eventueel gebruikmaken van unieke testprofielen of frequentiecappen aanpassen om scenario&#39;s te testen.

**pagina van het Spiegel** - in de verzonden proef, is de verbinding aan de spiegelpagina niet actief. Deze wordt alleen geactiveerd in de laatste berichten.

**Assets** - Assets en de beelden hebben specifieke toegankelijkheidsregels:

* Assets/Images zijn maximaal 2 jaar (730 dagen) sinds de eerste publicatie ervan in een fragment/inline-bericht toegankelijk in geleverde inhoud of proefdrukinhoud.
* Na deze vervaldatum (op een willekeurig tijdstip na 730 dagen) moet de publicatie opnieuw worden gepubliceerd om deze twee jaar toegankelijk te houden.
* Bij elke herpublicatie die binnen 730 dagen na de eerste publicatie wordt uitgevoerd, wordt het vervallen van de middelen/afbeeldingen niet tot de volgende 730 dagen verlengd.

## Proefdrukken verzenden {#send-proofs-steps}

Om e-mailproeven te verzenden die de gegevens van testprofielen gebruiken, moet u [&#x200B; testprofielen &#x200B;](test-profiles.md) eerst selecteren. Voer vervolgens de volgende stappen uit:

1. Klik in het **[!UICONTROL Simulate]** -scherm op de knop **[!UICONTROL Send proof]** .

   ![&#x200B; verzendt proefdrukknoop in het simuleren scherm &#x200B;](../email/assets/send-proof-button.png)

1. Typ in het venster **[!UICONTROL Send proof]** de e-mail van de ontvanger en klik op **[!UICONTROL Add]** om de proef naar uzelf of naar leden van uw organisatie te verzenden.

   U kunt maximaal tien ontvangers toevoegen voor de proefaflevering.

   ![&#x200B; voegt ontvangers aan de proeflevering &#x200B;](../email/assets/send-proof-add.png) toe

1. Selecteer de **profielen van de Test** om de berichtinhoud te gebruiken te personaliseren.

   Elke ontvanger van de proefdruk ontvangt evenveel berichten als het aantal geselecteerde testprofielen. Als u bijvoorbeeld vijf e-mailberichten voor ontvangers hebt toegevoegd en tien testprofielen hebt geselecteerd, verzendt u vijftig proefdrukberichten. Elke ontvanger krijgt er tien.

1. U kunt desgewenst een voorvoegsel toevoegen aan de onderwerpregel van de proefdruk. Alleen alfanumerieke tekens en speciale tekens zoals . - _ ( ) [ ] zijn toegestaan als voorvoegsel voor de onderwerpregel.

1. Klik op **[!UICONTROL Send proof]**.

   ![&#x200B; selecteer testprofielen en verzend de proef &#x200B;](../email/assets/send-proof-select.png)

1. Klik weer in het **[!UICONTROL Simulate]** -scherm op de knop **[!UICONTROL View proofs]** om de status te controleren.

   ![&#x200B; knoop van de Beelden van de Mening om leveringsstatus te controleren &#x200B;](../email/assets/send-proof-view.png)

Het wordt aanbevolen om na elke wijziging proefdrukken naar de inhoud van het bericht te verzenden.
