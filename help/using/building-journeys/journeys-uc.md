---
title: Dagboeken
description: Dagboeken
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 2%

---

# Multikanaalberichten verzenden

In deze sectie wordt een gebruiksscenario beschreven waarin een leessegment, een gebeurtenis, reactiegebeurtenissen en e-mail-/pushberichten worden gecombineerd.

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

Raadpleeg deze voor meer informatie over segmenten [page](../segment/about-segments.md).

1. Selecteer in de menusectie KLANT de optie **[!UICONTROL Segments]**.

1. Klik op de knop **[!UICONTROL Create segment]** knoop die bij het hoogste recht van de segmentlijst wordt gevestigd.

1. In de **[!UICONTROL Segment properties]** Voer een naam voor het segment in.

1. Sleep de gewenste velden vanuit het linkerdeelvenster naar de werkruimte in het midden en configureer ze op basis van uw behoeften. In dit voorbeeld gebruiken wij **Plaats** en **Geboortejaar** kenmerkvelden.

1. Klik op **[!UICONTROL Save]**.

   ![](../assets/add-attributes.png)

Het segment is nu gemaakt en klaar om in uw reis te worden gebruikt. Een **Segment lezen** activiteit, kunt u alle individuen van het segment tot de reis maken.

### De gebeurtenis configureren

U moet een gebeurtenis vormen die naar uw reis wordt verzonden wanneer een klant een aankoop maakt. Wanneer de reis de gebeurtenis ontvangt, brengt het het &quot;dank u&quot;bericht teweeg.

Hiervoor gebruiken we een op regels gebaseerde gebeurtenis. Raadpleeg deze voor meer informatie over gebeurtenissen [page](../event/about-events.md).

1. Selecteer in de sectie van het menu ADMINISTRATIE de optie **[!UICONTROL Configurations]** en klik vervolgens op **[!UICONTROL Events]**. Klik op **[!UICONTROL Create event]** om een nieuwe gebeurtenis te maken.

1. Voer de naam van de gebeurtenis in.

1. Selecteer in het veld **[!UICONTROL Event ID type]** de optie **[!UICONTROL Rule Based]**.

1. Definieer de **[!UICONTROL Schema]** en lading **[!UICONTROL Fields]**. U kunt verschillende velden gebruiken, zoals het aangeschafte product, de aankoopdatum en de aankoop-id.

1. In de **[!UICONTROL Event ID condition]** , definieert u de voorwaarde die door het systeem wordt gebruikt om de gebeurtenissen te identificeren die uw reis activeren. U kunt bijvoorbeeld een `purchaseMessage` en definieert de volgende regel: `purchaseMessage="thank you"`

1. Definieer de **[!UICONTROL Namespace]** en **[!UICONTROL Profile Identifier]**.

1. Klik op **[!UICONTROL Save]**.

   ![](../assets/jo-uc2.png)

De gebeurtenis is nu geconfigureerd en klaar om in uw reis te worden gebruikt. Met de bijbehorende gebeurtenisactiviteit kunt u een actie activeren telkens wanneer een klant een aankoop doet.

### Berichten maken

Voor dit gebruik, moeten wij drie berichten tot stand brengen:

* een eerste pushbericht en e-mailbericht
* een pushbericht &quot; dank u &quot;
* een e-mailvervolgbericht

![](../assets/jo-uc3.png)

Zie dit [sectie](../segment/about-segments.md) om te leren om deze berichten te ontwerpen en te publiceren.

## De reis ontwerpen

1. Begin de reis met een **Segment lezen** activiteit. Selecteer het eerder gemaakte segment. Alle personen die tot het segment behoren, komen de reis binnen.

   ![](../assets/jo-uc4.png)

1. Een neerzetten **Bericht** en selecteer het eerste pushbericht en e-mailbericht. Dit bericht wordt naar alle personen op de reis gestuurd.

   ![](../assets/jo-uc5.png)

1. Plaats de cursor op de berichtactiviteit en klik op het plusteken (+) om een nieuw pad te maken.

1. Voeg in het eerste pad een **Reactie** gebeurtenis en selecteer **Push geopend**. De gebeurtenis wordt geactiveerd wanneer een individu dat tot het segment behoort de pushversie van het eerste bericht opent.

1. Voeg in het tweede pad een **Reactie** gebeurtenis en selecteer **E-mail geopend**. De gebeurtenis wordt geactiveerd wanneer de persoon het e-mailbericht opent.

1. Controleer bij een van de reactieactiviteiten de **De time-out van gebeurtenissen definiëren** een duur definiëren (1 dag in ons voorbeeld) en controleren **Een time-outpad instellen**. Hiermee maakt u een ander pad voor personen die het eerste pushbericht of e-mailbericht niet openen.

   >[!NOTE]
   >
   >Wanneer u een time-out configureert voor meerdere gebeurtenissen (de twee reacties in dit geval), hoeft u de time-out alleen te configureren voor een van deze gebeurtenissen.

1. Plaats een **Bericht** en selecteer het e-mailvervolgbericht. Dit bericht wordt verzonden naar de personen die het e-mailbericht of het eerste pushbericht de volgende dag niet openen.

1. Sluit de drie paden aan op de eerder gemaakte aankoopgebeurtenis. De gebeurtenis wordt geactiveerd wanneer een individu een aankoop doet.

1. Na de gebeurtenis, laat vallen a **Bericht** en selecteer het e-mailbericht &quot;Bedankt&quot;.

1. Een **Einde** activiteit.

## De journey testen en publiceren

1. Controleer voordat u de reis test of deze geldig is en of er geen fout optreedt.

1. Klik op de knop **Testen** in de rechterbovenhoek wordt geschakeld om de testmodus te activeren. Bepaal hoe u testprofielen de test wilt ingaan: één profiel, of maximaal 100 tegelijk. Zie dit [sectie](testing-the-journey.md) om te leren hoe u de testmodus kunt gebruiken.

1. Als de reis klaar is, publiceert u deze met de **Publiceren** in de rechterbovenhoek.
