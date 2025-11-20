---
solution: Journey Optimizer
product: journey optimizer
title: Integreren met Adobe Campaign v7/v8
description: Leer hoe u Journey Optimizer kunt integreren met Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: campagne, acc, integratie
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: ee1b6808d3247c7549e82990113d0d496c31b2a9
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 1%

---

# Integreren met Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Handelingen voor Adobe Campaign v7/v8"
>abstract="Deze integratie is beschikbaar voor Adobe Campaign v7 en v8. Hiermee kunt u e-mails, pushberichten en SMS verzenden met de mogelijkheden van Adobe Campaign Transaction Messaging. De verbinding tussen de Journey Optimizer- en Campagneinstanties wordt door Adobe tijdens de levering ingesteld."

Als u Adobe Campaign Classic v7 of Campaign v8 hebt, kunt u op uw reizen een specifieke aangepaste actie uitvoeren om Adobe Journey Optimizer en Adobe Campaign te integreren. Dankzij deze integratie kunt u e-mails, pushberichten en SMS verzenden via de mogelijkheden van Adobe Campaign Transaction Messaging. Leer meer in dit [&#x200B; gebruiksgeval van begin tot eind &#x200B;](../building-journeys/ajo-ac.md).

Voor elke gevormde actie, is de actie van de a [&#x200B; Campagne activiteit &#x200B;](../building-journeys/using-adobe-campaign-v7-v8.md) beschikbaar in het palet van de reisontwerper.

## Activering {#access}

Op verzoek wordt de verbinding tussen de Journey Optimizer- en Adobe Campaign-omgevingen door Adobe tijdens de provisioning ingesteld. Als u de verbinding niet op het tijdstip van de levering hebt aangevraagd, neemt u contact op met de ondersteuning van Adobe Journey Optimizer om de activering aan te vragen. U dient de volgende gegevens op te geven:

>[!BEGINTABS]

>[!TAB  voor Adobe Journey Optimizer ]

* Organisatie-id (Adobe OrgID)
* Naam sandbox

>[!TAB  voor Adobe Campaign ]

* URL campagneserver
* Real-Time Server-URL
* Uw Adobe Campaign-versie

>[!ENDTABS]


## Afvoerkanalen en beperkingen {#important-notes}

* Er is geen vertraging van berichten. Het systeem kapt het aantal berichten in dat naar 4.000 per 5 minuten kan worden verzonden, die op de huidige Campagne SLA wordt gebaseerd. Om deze reden dient Journey Optimizer alleen te worden gebruikt in gevallen van eenmalig gebruik (individuele gebeurtenissen, niet het publiek).

* U moet één actie op het canvas per malplaatje vormen om te gebruiken. U moet één actie in Journey Optimizer voor elke malplaatje vormen u om van Adobe Campaign wenst te gebruiken.

* Wij adviseren dat u een specifiek Centrum van het Bericht voor deze integratie wordt ontvangen of instantie van Managed Services gebruikt om het beïnvloeden van om het even welke andere verrichtingen van de Campagne te vermijden die u kunt hebben gaande. De marketing server kan worden ontvangen of op-gebouw.<!--The build required is 21.1 Release Candidate or greater. -->

* Er is geen bevestiging dat de lading of het bericht van de Campagne correct is.

* U kunt een Campagne-actie niet gebruiken met een kwalificatiegebeurtenis voor het publiek.

## Vereisten {#prerequisites}

In Adobe Campaign moet u een transactiemelding en de bijbehorende gebeurtenis maken en publiceren. Verwijs naar de [&#x200B; documentatie van Adobe Campaign &#x200B;](https://experienceleague.adobe.com/nl/docs/campaign/campaign-v8/send/real-time/transactional){target="_blank"}.

U kunt uw JSON-lading voor elk bericht samenstellen volgens het onderstaande patroon. U gaat deze lading dan kleven wanneer het vormen van de actie in Journey Optimizer (zie hieronder).

+++ Voorbeeld

```json
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **kanaal**: het kanaal dat voor uw het transactiemalplaatje van de Campagne wordt bepaald
* **eventType**: de interne naam van uw gebeurtenis van de Campagne
* **ctx**: variabele die op de verpersoonlijking wordt gebaseerd u in uw bericht hebt

+++

## De handeling configureren {#configure-action}

In Journey Optimizer moet u één actie per transactiemelding configureren.

Ga als volgt te werk om een Campagne te maken:

1. Maak een nieuwe handeling. [&#x200B; Leer hoe te om douaneacties &#x200B;](../action/action.md) tot stand te brengen.
1. Voer een naam en beschrijving in.
1. Selecteer in het veld **[!UICONTROL Action type]** de optie **[!UICONTROL Adobe Campaign Classic]**.
   ![](assets/accintegration1.png)
1. Klik in het veld **[!UICONTROL Payload]** en plak een voorbeeld van de JSON-payload die overeenkomt met het campagnebericht. Neem contact op met Adobe voor deze lading.
1. Stel elk veld in op statisch of variabel op basis van de vraag of u het wilt toewijzen op het canvas Journey. Bijvoorbeeld, zouden de gebieden zoals de parameters van het e-mailkanaal en verpersoonlijkingsgebieden (`ctx`) typisch als variabelen moeten worden geplaatst zodat kunnen zij zich dynamisch binnen de reis aanpassen.
1. Klik op **[!UICONTROL Save]**.

## Een bestaande handeling bijwerken {#update-action}

Als u een bestaande aangepaste actie van Campagne v7/v8 moet bijwerken, bijvoorbeeld wanneer het eindpunt Real-Time (RT) na de eerste installatie verandert, voert u de volgende stappen uit:

1. Selecteer **[!UICONTROL Administration]** in het menu **[!UICONTROL Configurations]** en ga vervolgens naar **[!UICONTROL Actions]** .
1. Zoek en selecteer de actie Campagne die u wilt bijwerken in de lijst met acties.
1. Klik op **[!UICONTROL Edit]** om de actieconfiguratie te openen.
1. Werk het **[!UICONTROL URL]** gebied met het nieuwe eindpunt URL van RT bij. Verzeker het eindpuntformaat correct en bereikbaar is.
1. Werk indien nodig de configuratie van **[!UICONTROL Payload]** bij zodat deze overeenkomt met eventuele wijzigingen in de structuur van het transactiebericht van de campagne.
1. Klik **[!UICONTROL Test]** om de verbinding aan het nieuwe eindpunt te bevestigen. Verifieer dat de test een succesvolle reactie alvorens te werk te gaan terugkeert.
1. Nadat de wijzigingen zijn gevalideerd, klikt u op **[!UICONTROL Save]** om de wijzigingen toe te passen.

>[!NOTE]
>
>Voor elke reis die deze handeling gebruikt, wordt automatisch de bijgewerkte configuratie gebruikt. Als u levende reizen gebruikend deze actie hebt, controleer hen na het bijwerken van het eindpunt nauwkeurig om correcte berichtlevering te verzekeren.

