---
solution: Journey Optimizer
product: journey optimizer
title: Integreren met Adobe Campaign v7/v8
description: Leer hoe u Journey Optimizer kunt integreren met Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: campagne, acc, integratie
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Integreren met Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Handelingen voor Adobe Campaign v7/v8"
>abstract="Deze integratie is beschikbaar voor Adobe Campaign v7 en v8. Hiermee kunt u e-mails, pushberichten en SMS verzenden met de mogelijkheden van Adobe Campaign Transaction Messaging. De verbinding tussen de Journey Optimizer en de instanties van de Campagne is opstelling door Adobe bij leveringstijd."

Deze integratie is beschikbaar voor Adobe Campaign v7/v8 vanaf versie 7.1 en Adobe Campaign v8. Hiermee kunt u e-mails, pushberichten en SMS verzenden met de mogelijkheden van Adobe Campaign Transaction Messaging.

De verbinding tussen de Journey Optimizer en de instanties van de Campagne is opstelling door Adobe bij leveringstijd.

In dit hoofdstuk wordt een gebruiksgeval van begin tot eind weergegeven [sectie](../building-journeys/ajo-ac.md).

Voor elke gevormde actie, is een actieactiviteit beschikbaar in het palet van de reisontwerper. Zie dit [sectie](../building-journeys/using-adobe-campaign-v7-v8.md).

## Belangrijke opmerkingen {#important-notes}

* Er is geen vertraging van berichten. Het systeem kapt het aantal berichten die over aan 4000 per 5 minuten kunnen worden verzonden, die op huidige Campagne SLA worden gebaseerd. Om deze reden dient Journey Optimizer alleen te worden gebruikt in gevallen van eenmalig gebruik (individuele gebeurtenissen, niet het publiek).

* U moet één actie op het canvas per malplaatje vormen u wenst te gebruiken. U moet één actie in Journey Optimizer voor elke malplaatje vormen u om van Adobe Campaign wenst te gebruiken.

* Wij adviseren dat u een specifieke instantie van het Centrum van het Bericht gebruikt die voor deze integratie wordt ontvangen om het beïnvloeden van om het even welke andere verrichtingen van de Campagne te vermijden die u kunt hebben gaande. De marketingserver kan worden gehost of op locatie worden opgeslagen. De vereiste build is 21.1 Release Candidate of hoger.

* Er is geen bevestiging dat de lading of het bericht van de Campagne correct is.

* U kunt een Campagne-actie niet gebruiken met een kwalificatiegebeurtenis voor het publiek.

## Vereisten {#prerequisites}

In Campagne, moet u een transactiebericht en zijn bijbehorende gebeurtenis tot stand brengen en publiceren. Zie de [Adobe Campaign-documentatie](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target="_blank"}.

U kunt uw JSON-lading voor elk bericht samenstellen volgens het onderstaande patroon. U gaat deze payload vervolgens plakken tijdens het configureren van de handeling in Journey Optimizer (zie hieronder)

Hier volgt een voorbeeld:

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **kanaal**: het kanaal dat is gedefinieerd voor de transactiesjabloon van uw campagne
* **eventType**: de interne naam van uw Campagnegebeurtenis
* **ctx**: variabele die op de verpersoonlijking wordt gebaseerd u in uw bericht hebt.

## De handeling configureren {#configure-action}

In Journey Optimizer moet u één actie per transactiemelding configureren. Voer de volgende stappen uit:

1. Maak een nieuwe handeling. Zie dit [sectie](../action/action.md).
1. Voer een naam en beschrijving in.
1. In de **Type handeling** veld, selecteren **Adobe Campaign Classic**.
1. Klik in het dialoogvenster **Payload** veld en plak een voorbeeld van de JSON-payload die overeenkomt met het campagnebericht. Neem contact op met de Adobe voor deze lading.
1. Pas de verschillende velden aan op statisch of variabel, afhankelijk van de vraag of u ze wilt toewijzen op het canvas Reis. Bepaalde gebieden, zoals kanaalparameters voor e-mailadres en verpersoonlijkingsgebieden (ctx), wilt u waarschijnlijk bepaald als variabelen voor afbeelding in de context van de reis.
1. Klikken **Opslaan**.

![](assets/accintegration1.png)