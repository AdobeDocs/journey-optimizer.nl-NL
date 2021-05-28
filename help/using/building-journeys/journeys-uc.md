---
title: Dagboeken
description: Dagboeken
source-git-commit: 4464ea7169424c1ec6212394b8bda79a9bec1913
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 2%

---

# Reisgebruik

![](../assets/do-not-localize/badge.png)

In deze sectie wordt een gebruiksscenario beschreven waarin een Read-segment, een gebeurtenis, reactiegebeurtenissen en e-mail-/pushberichten worden gecombineerd.

![](../assets/jo-uc1.png)

## Beschrijving van het gebruiksgeval

In dit geval, willen wij een eerste bericht (e-mail en duw) naar alle klanten verzenden die tot een specifiek segment behoren.

Op basis van hun reactie op het eerste bericht willen we specifieke berichten verzenden.

Na het eerste bericht wachten we op een dag totdat klanten de push of e-mail kunnen openen. Als er geen reactie is, sturen we ze een vervolgmail.

Vervolgens wachten we op een aankoop en sturen we een pushbericht om de klant te bedanken.

## Vereisten

Voor dit gebruiksgeval om te werken, moet u het volgende vormen:

* een segment voor alle klanten die in Atlanta, San Francisco of Seattle wonen en na 1980 geboren zijn.
* een aankoopgebeurtenis
* drie berichten

### Het segment maken

In onze reis, willen wij hefboomwerking een specifiek segment van klanten. Alle personen die tot het segment behoren, nemen de reis over en volgen de verschillende stappen. In ons voorbeeld hebben we een segment nodig dat gericht is op alle klanten die in Atlanta, San Francisco of Seattle wonen en na 1980 geboren zijn.

Voor meer informatie over segmenten, verwijs naar deze [pagina](../segment/about-segments.md).

1. Klik in het menu **[!UICONTROL Segments]** op **[!UICONTROL Create segment]**.

1. Voer in het deelvenster **[!UICONTROL Segment properties]** een naam in voor het segment.

1. Sleep de gewenste velden vanuit het linkerdeelvenster naar de werkruimte in het midden en configureer ze op basis van uw behoeften. In dit voorbeeld gebruiken we de velden **City** en **Geboortejaar**.

1. Klik op **[!UICONTROL Save]**.

   ![](../assets/add-attributes.png)

Het segment is nu gemaakt en klaar om in uw reis te worden gebruikt. Met een **Leessegment** activiteit, kunt u alle individuen die tot het segment behoren tot de reis maken.

### De gebeurtenis configureren

U moet een gebeurtenis vormen die naar uw reis wordt verzonden wanneer een klant een aankoop maakt. Wanneer de reis de gebeurtenis ontvangt, brengt het het &quot;dank u&quot;bericht teweeg.

Hiervoor gebruiken we een op regels gebaseerde gebeurtenis. Raadpleeg deze [pagina](../event/about-events.md) voor meer informatie over gebeurtenissen.

1. Blader in de sectie BEHEER naar **[!UICONTROL Configurations]** en klik vervolgens op **[!UICONTROL Events]**. Klik op **[!UICONTROL Add]** om een nieuwe gebeurtenis te maken.

1. Voer de naam van de gebeurtenis in.

1. Selecteer in het veld **[!UICONTROL Event ID type]** de optie **[!UICONTROL Rule Based]**.

1. Definieer **[!UICONTROL Schema]** en payload **[!UICONTROL Fields]**. U kunt verschillende velden gebruiken, zoals het aangeschafte product, de aankoopdatum en de aankoop-id.

1. Definieer in het veld **[!UICONTROL Event ID condition]** de voorwaarde die door het systeem wordt gebruikt om de gebeurtenissen te identificeren die de reis activeren. U kunt bijvoorbeeld een veld `purchaseMessage` toevoegen en de volgende regel definiëren: `purchaseMessage="thank you"`

1. Definieer **[!UICONTROL Namespace]** en **[!UICONTROL Key]**.

1. Klik op **[!UICONTROL Save]**.

   ![](../assets/jo-uc2.png)

De gebeurtenis is nu geconfigureerd en klaar om in uw reis te worden gebruikt. Met de bijbehorende gebeurtenisactiviteit kunt u een actie activeren telkens wanneer een klant een aankoop doet.

### Berichten maken

Voor dit gebruik, moeten wij drie berichten tot stand brengen:

* een eerste pushbericht en e-mailbericht
* een pushbericht &quot; dank u &quot;
* een e-mailvervolgbericht

![](../assets/jo-uc3.png)

Raadpleeg deze [sectie](../segment/about-segments.md) voor meer informatie over het ontwerpen en publiceren van deze berichten.

## De reis ontwerpen

1. Begin de reis met een **Read segment** activiteit. Selecteer het eerder gemaakte segment. Alle personen die tot het segment behoren, komen de reis binnen.

   ![](../assets/jo-uc4.png)

1. Zet een **Bericht** activiteit neer en selecteer duw en e-mail eerste bericht. Dit bericht wordt naar alle personen op de reis gestuurd.

   ![](../assets/jo-uc5.png)

1. Plaats de cursor op de berichtactiviteit en klik op het plusteken (+) om een nieuw pad te maken.

1. Voeg in het eerste pad een **Reactie**-gebeurtenis toe en selecteer **Push opened**. De gebeurtenis wordt geactiveerd wanneer een individu dat tot het segment behoort de pushversie van het eerste bericht opent.

1. Voeg in het tweede pad een gebeurtenis **Reaction** toe en selecteer **Geopende e-mail**. De gebeurtenis wordt geactiveerd wanneer de persoon het e-mailbericht opent.

1. Schakel in een van de reactieactiviteiten het selectievakje **De time-out van de gebeurtenis definiëren** in, definieer een duur (1 dag in ons voorbeeld) en schakel **Een time-outpad instellen** in. Hiermee maakt u een ander pad voor personen die het eerste pushbericht of e-mailbericht niet openen.

   >[!NOTE]
   >
   >Wanneer u een time-out configureert voor meerdere gebeurtenissen (de twee reacties in dit geval), hoeft u de time-out alleen te configureren voor een van deze gebeurtenissen.

1. Plaats in het time-outpad een **Message**-activiteit en selecteer het e-mailvervolgbericht. Dit bericht wordt verzonden naar de personen die het e-mailbericht of het eerste pushbericht de volgende dag niet openen.

1. Sluit de drie paden aan op de eerder gemaakte aankoopgebeurtenis. De gebeurtenis wordt geactiveerd wanneer een individu een aankoop doet.

1. Na de gebeurtenis, laat vallen een **Bericht** activiteit en selecteert e-mail &quot;dank u&quot;bericht.

1. Voeg een **End** activiteit toe.

## De journey testen en publiceren

1. Controleer voordat u de reis test of deze geldig is en of er geen fout optreedt.

1. Klik op de **Test**-schakeloptie in de rechterbovenhoek om de testmodus te activeren. Bepaal hoe u testprofielen de test wilt ingaan: één profiel, of maximaal 100 tegelijk. Raadpleeg deze [sectie](testing-the-journey.md) voor meer informatie over het gebruik van de testmodus.

1. Wanneer de reis klaar is, publiceer het gebruikend **Publish** knoop, die in de hoogste juiste hoek wordt gevestigd.
