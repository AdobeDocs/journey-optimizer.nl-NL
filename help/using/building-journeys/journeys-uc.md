---
solution: Journey Optimizer
product: journey optimizer
title: Reisgevallen
description: Reisgevallen
feature: Journeys, Use Cases, Email, Push
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: use case, multi-channel, messages, trip, channel, events, push
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 2%

---

# Hoofdlettergebruik: berichten met meerdere kanalen verzenden{#send-multi-channel-messages}

In deze sectie wordt een gebruiksscenario beschreven waarin een leespubliek, een gebeurtenis, reactiegebeurtenissen en e-mail-/pushberichten worden gecombineerd.

![](assets/jo-uc1.png)

## Beschrijving van het gebruiksgeval

In dit geval, willen wij een eerste e-mailbericht naar alle klanten verzenden die tot een specifiek publiek behoren.

Op basis van hun reactie op het eerste bericht willen we specifieke berichten verzenden.

Als de klant het e-mailbericht opent, wachten we op een aankoop en sturen we een pushbericht om de klant te bedanken.

Als er geen reactie is, sturen we ze een vervolgmail.

## Vereisten

Voor dit gebruiksgeval om te werken, moet u het volgende vormen:

* een publiek voor alle klanten die in Atlanta, San Francisco of Seattle wonen en na 1980 geboren zijn.
* een aankoopgebeurtenis

### Het publiek maken

In onze reis, willen wij hefboomwerking een specifiek publiek van klanten. Alle personen die tot het publiek behoren, reizen de reis en volgen de verschillende stappen. In ons voorbeeld hebben we een publiek nodig dat gericht is op alle klanten die in Atlanta, San Francisco of Seattle wonen en na 1980 geboren zijn.

Raadpleeg de volgende secties voor meer informatie over het publiek [page](../audience/about-audiences.md).

1. Selecteer in de menusectie KLANT de optie **[!UICONTROL Audiences]**.

1. Klik op de knop **[!UICONTROL Create audience]** knoop die bij het hoogste recht van de publiekslijst wordt gevestigd.

1. In de **[!UICONTROL Audience properties]** voert u een naam in voor het publiek.

1. Sleep de gewenste velden vanuit het linkerdeelvenster naar de werkruimte in het midden en configureer ze op basis van uw behoeften. In dit voorbeeld gebruiken wij **Plaats** en **Geboortejaar** kenmerkvelden.

1. Klik op **[!UICONTROL Save]**.

   ![](assets/add-attributes.png)

Het publiek is nu gemaakt en klaar om te worden gebruikt op uw reis. Een **Publiek lezen** activiteit, kunt u alle individuen die tot het publiek behoren tot de reis maken.

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

   ![](assets/jo-uc2.png)

De gebeurtenis is nu geconfigureerd en klaar om in uw reis te worden gebruikt. Met de bijbehorende gebeurtenisactiviteit kunt u een actie activeren telkens wanneer een klant een aankoop doet.

## De reis ontwerpen

1. Begin de reis met een **Publiek lezen** activiteit. Selecteer het publiek dat eerder is gemaakt. Alle personen die tot het publiek behoren, nemen de reis in.

   ![](assets/jo-uc4.png)

1. Een dropknop **E-mail** en definieert de inhoud van het eerste bericht. Dit bericht wordt naar alle personen op de reis gestuurd. Zie dit [sectie](../email/create-email.md) leren hoe u een e-mail kunt configureren en ontwerpen.

   ![](assets/jo-uc5.png)

1. Voeg een **Reactie** gebeurtenis en selecteer **E-mail geopend**. De gebeurtenis wordt geactiveerd wanneer een persoon die tot het publiek behoort, het e-mailbericht opent.

1. Controleer de **De time-out van gebeurtenissen definiëren** een duur definiëren (1 dag in ons voorbeeld) en controleren **Een time-outpad instellen**. Hiermee maakt u een ander pad voor personen die het eerste pushbericht of e-mailbericht niet openen.

1. Zet een **E-mail** en definieert de inhoud van het vervolgbericht. Dit bericht wordt verzonden naar de personen die het e-mailbericht of het eerste pushbericht de volgende dag niet openen. Zie dit [sectie](../email/create-email.md) leren hoe u een e-mail kunt configureren en ontwerpen.

1. Voeg in het eerste pad de eerder gemaakte aankoopgebeurtenis toe. De gebeurtenis wordt geactiveerd wanneer een individu een aankoop doet.

1. Na de gebeurtenis, laat vallen a **Push** actie en definieer de inhoud van het &#39;&#39;bedankt&#39;&#39;-bericht. Zie dit [sectie](../push/create-push.md) leren hoe u een push kunt configureren en ontwerpen.

## De journey testen en publiceren

1. Controleer voordat u de reis test of deze geldig is en of er geen fout optreedt.

1. Klik op de knop **Testen** in de rechterbovenhoek wordt geschakeld om de testmodus te activeren. Zie dit [sectie](testing-the-journey.md) om te leren hoe u de testmodus kunt gebruiken.

1. Als de reis klaar is, publiceert u deze met de **Publiceren** in de rechterbovenhoek.
