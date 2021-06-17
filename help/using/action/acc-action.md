---
title: Integreren met Adobe Campaign v7/v8
description: Leer hoe u kunt integreren met Adobe Campaign v7/v8
feature: Acties
topic: Beheer
role: Administrator
level: Intermediate
source-git-commit: 9ca747c4f46fd7eb24dbbf12350d7bbe409b1617
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 1%

---

# Integreren met Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-classic}

Deze integratie is beschikbaar voor Adobe Campaign Classic v7 vanaf versie 21.1 en Adobe Campaign v8. Hiermee kunt u e-mails, pushberichten en SMS verzenden met de mogelijkheden van Adobe Campaign Transaction Messaging.

De verbinding tussen de Journey Optimizer en de instanties van de Campagne wordt opstelling door Adobe bij leveringstijd.

In deze [sectie](../building-journeys/campaign-classic-use-case.md) wordt een gebruiksgeval van begin tot eind weergegeven.

Voor elke gevormde actie, is een actieactiviteit beschikbaar in het palet van de reisontwerper. Zie deze [sectie](../building-journeys/using-adobe-campaign-classic.md).

## Belangrijke opmerkingen

* Er is geen vertraging van berichten. Wij begrenzen het aantal berichten die over aan 50.000/uur kunnen worden verzonden die op onze huidige Campagne SLA wordt gebaseerd. Daarom mag Journey Optimizer alleen worden gebruikt in gevallen van eenmalig gebruik (individuele gebeurtenissen, niet segmenten).

* U moet één actie op het canvas per malplaatje vormen u wenst te gebruiken. U moet één actie in Journey Optimizer voor elke malplaatje vormen u om van Adobe Campaign wenst te gebruiken.

* Wij adviseren dat u een specifieke instantie van het Centrum van het Bericht gebruikt die voor deze integratie wordt ontvangen om het beïnvloeden van om het even welke andere verrichtingen van de Campagne te vermijden die u kunt hebben gaande. De marketingserver kan worden gehost of op locatie worden opgeslagen. De vereiste build is 21.1 Release Candidate of hoger.

* Er is geen bevestiging dat de lading of het bericht van de Campagne correct is.

* U kunt geen actie van de Campagne met een gebeurtenis van de segmentkwalificatie gebruiken.

## Vereisten

In Campagne, moet u een transactiebericht en zijn bijbehorende gebeurtenis tot stand brengen en publiceren. Raadpleeg de [Adobe Campaign-documentatie](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging).

U kunt uw JSON-lading voor elk bericht samenstellen volgens het onderstaande patroon. U zult dan deze nuttige lading wanneer het vormen van de actie in Journey Orchestration (zie hieronder) kleven

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

* **kanaal**: het kanaal dat voor uw transactiemalplaatje van de Campagne wordt bepaald
* **eventType**: de interne naam van uw Campagnegebeurtenis
* **ctx**: variabele die op de verpersoonlijking wordt gebaseerd u in uw bericht hebt.

## De handeling configureren

In Journey Optimizer moet u één actie per transactiemelding configureren. Voer de volgende stappen uit:

1. Maak een nieuwe handeling. Zie deze [sectie](../action/action.md).
1. Voer een naam en beschrijving in.
1. Selecteer **Adobe Campaign Classic** in het veld **Actietype**.
1. Klik in het veld **Payload** en plak een voorbeeld van de JSON-lading die overeenkomt met het campagnebericht. Neem contact op met Adobe om deze lading op te halen.
1. Pas de verschillende velden aan op statisch of variabel, afhankelijk van de vraag of u ze wilt toewijzen op het canvas Reis. Bepaalde gebieden, zoals kanaalparameters voor e-mailadres en verpersoonlijkingsgebieden (ctx), wilt u waarschijnlijk bepaald als variabelen voor afbeelding in de context van de reis.
1. Klik **Opslaan**.

![](../assets/accintegration1.png)


