---
solution: Journey Optimizer
product: journey optimizer
title: Reisgevallen
description: Reisgevallen
feature: Journeys, Use Cases, Email, Push
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: use case, multi-channel, messages, trip, channel, events, push
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 1%

---

# Multikanaalberichten verzenden {#send-multi-channel-messages}

In deze sectie wordt een gebruiksscenario beschreven waarin een leespubliek, een gebeurtenis, reactiegebeurtenissen en e-mail-/pushberichten worden gecombineerd.

![](assets/jo-uc1.png)

## Beschrijving van het gebruiksgeval

In dit geval, is het doel een eerste e-mailbericht naar alle klanten te verzenden die tot een specifiek publiek behoren.

Op basis van hun reactie op het eerste bericht worden specifieke vervolgberichten verzonden.

Als de klant de e-mail opent, wacht het systeem op een aankoop en verzendt het een pushbericht om de klant te bedanken.

Als er geen reactie is, wordt een vervolgbericht verzonden.

## Vereisten

Voor dit gebruiksgeval om te werken, vorm het volgende:

* Een publiek voor alle klanten die in Atlanta, San Francisco of Seattle wonen en na 1980 geboren zijn
* Een aankoopgebeurtenis

### Het publiek maken

In deze reis, wordt een specifiek publiek van klanten leveraged. Alle personen die tot het publiek behoren, reizen de reis en volgen de verschillende stappen. In dit voorbeeld richt het publiek zich op alle klanten die in Atlanta, San Francisco of Seattle wonen en na 1980 geboren zijn.

Voor meer informatie over publiek, [ verwijs naar deze pagina ](../audience/about-audiences.md).

1. Selecteer **[!UICONTROL Audiences]** in de menusectie KLANT.
1. Klik op de knop **[!UICONTROL Create audience]** rechtsboven in de lijst met doelgroepen.
1. Voer in het deelvenster **[!UICONTROL Audience properties]** een naam in voor het publiek.
1. Sleep de gewenste velden vanuit het linkerdeelvenster naar de werkruimte in het midden en configureer ze naar wens. In dit voorbeeld, gebruik de **Woonplaats** en **het jaar** attributengebieden van de Geboorteplaats.
1. Klik op **[!UICONTROL Save]**.

   ![](assets/add-attributes.png)

Het publiek is nu gemaakt en klaar om te worden gebruikt in de reis. Gebruikend a **Gelezen de activiteit van het publiek**, kunnen alle individuen die tot het publiek behoren de reis ingaan.

### De gebeurtenis configureren

Vorm een gebeurtenis die naar de reis wordt verzonden wanneer een klant een aankoop maakt. Wanneer de reis de gebeurtenis ontvangt, brengt het het &quot;dank u&quot;bericht teweeg.

Voor dit, gebruik a [ regel-gebaseerde gebeurtenis ](../event/about-events.md).

1. Selecteer **[!UICONTROL Configurations]** in de sectie van het menu BEHEER en klik vervolgens op **[!UICONTROL Events]** . Klik op **[!UICONTROL Create event]** om een nieuwe gebeurtenis te maken.

1. Voer de naam van de gebeurtenis in.

1. Selecteer in het veld **[!UICONTROL Event ID type]** de optie **[!UICONTROL Rule Based]**.

1. Definieer de waarden **[!UICONTROL Schema]** en payload **[!UICONTROL Fields]** . Gebruik verschillende velden, zoals het aangeschafte product, de aankoopdatum en de aankoop-id.

1. Definieer in het veld **[!UICONTROL Event ID condition]** de voorwaarde die door het systeem wordt gebruikt om de gebeurtenissen te identificeren die de rit activeren. Voeg bijvoorbeeld een veld `purchaseMessage` toe en definieer de volgende regel: `purchaseMessage="thank you"`

1. Definieer de **[!UICONTROL Namespace]** en **[!UICONTROL Profile Identifier]** .

1. Klik op **[!UICONTROL Save]**.

   ![](assets/jo-uc2.png)

De gebeurtenis is nu geconfigureerd en klaar om in de reis te worden gebruikt. Met behulp van de bijbehorende gebeurtenisactiviteit kan een actie worden geactiveerd telkens wanneer een klant een aankoop doet.

## De reis ontwerpen

1. Begin de reis met a **Gelezen de activiteit van het Publiek**. Selecteer het publiek dat eerder is gemaakt. Alle personen die tot het publiek behoren, nemen de reis in.

   ![](assets/jo-uc4.png)

1. Daling een **e-mail** actieactiviteit en bepaal de inhoud van het &quot;eerste bericht.&quot; Dit bericht wordt naar alle personen op de reis gestuurd. Verwijs naar deze [ sectie ](../email/create-email.md) om te leren hoe te om een e-mail te vormen en te ontwerpen.

   ![](assets/jo-uc5.png)

1. Voeg de gebeurtenis van de Reactie van de a **** toe en selecteer **Geopende E-mail**. De gebeurtenis wordt geactiveerd wanneer een persoon die tot het publiek behoort, het e-mailbericht opent.

1. Controle **bepaalt de gebeurtenisonderbreking** doos, bepaalt een duur (1 dag in dit voorbeeld), en controle **plaatste een onderbrekingspad**. Hiermee maakt u een ander pad voor personen die het eerste pushbericht of e-mailbericht niet openen.

1. In de onderbrekingspad, laat vallen een **E-mail** actieactiviteit en bepaalt de inhoud van het &quot;follow-up&quot;bericht. Dit bericht wordt verzonden naar de personen die het e-mailbericht of het eerste pushbericht niet binnen de volgende dag openen. [ Leer hoe te om een e-mail ](../email/create-email.md) te vormen en te ontwerpen.

1. Voeg in het eerste pad de eerder gemaakte aankoopgebeurtenis toe. De gebeurtenis wordt geactiveerd wanneer een individu een aankoop doet.

1. Na de gebeurtenis, laat vallen a **duw** actieactiviteit en bepaal de inhoud van het &quot;dank u&quot;bericht. Verwijs naar deze [ sectie ](../push/create-push.md) om te leren hoe te om een duw te vormen en te ontwerpen.

## De reis testen en publiceren

1. Controleer vóór het testen van de rit of deze geldig is en of er geen fout optreedt.

1. Gebruik de **knevel van de Test**, die in de hoogste juiste hoek wordt gevestigd, om de testwijze te activeren. Verwijs naar deze [ sectie ](testing-the-journey.md) om te leren hoe te om de testwijze te gebruiken.

1. Wanneer de reis klaar is, publiceer het gebruikend **publiceer** knoop, die in de hoogste juiste hoek wordt gevestigd.
