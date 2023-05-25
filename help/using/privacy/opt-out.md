---
solution: Journey Optimizer
product: journey optimizer
title: Weigeren beheren
description: Meer informatie over het beheren van opt-out en privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 8b459f71852d031dc650b77725bdc693325cdb1d
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 1%

---

# Weigeren beheren {#consent}

Het is een wettelijke vereiste om ontvangers de mogelijkheid te bieden zich niet langer te abonneren op het ontvangen van communicatie van een merk, en om ervoor te zorgen dat deze keuze wordt nagekomen. Meer informatie over de toepasselijke wetgeving vindt u in het [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target="_blank"}.

**Waarom is het belangrijk?**

* Als u deze voorschriften niet naleeft, brengt u juridische risico&#39;s met zich mee voor uw merk.
* Het helpt u vermijden verzendend ongevraagde mededelingen naar uw ontvangers, die hen zouden kunnen maken uw berichten als spam merken en uw reputatie schaden.

## Abonnementen beheren tijdens reizen en campagnes {#opt-out-ajo}

Wanneer het verzenden van berichten van reizen of campagnes, moet u altijd ervoor zorgen dat de klanten van toekomstige mededelingen kunnen opzeggen. Als u het abonnement opzegt, worden de profielen automatisch verwijderd uit het publiek van toekomstige marketingberichten.

while **[!DNL Journey Optimizer]** biedt manieren om de optie om te weigeren in e-mails en SMS-berichten te beheren. Voor pushberichten is geen actie aan uw kant vereist, omdat ontvangers hun abonnement zelf kunnen opzeggen via hun apparaten. Ze kunnen er bijvoorbeeld voor kiezen om meldingen te stoppen wanneer ze worden gedownload of wanneer ze uw app gebruiken. Op dezelfde manier kunnen ze de meldingsinstellingen wijzigen via het mobiele besturingssysteem.

In de volgende secties vindt u informatie over het beheren van opt-out in Journey Optimizer-berichten voor e-mail en SMS:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Lood" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>E-mailuitschakelbeheer</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Onfrequent" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>SMS-opt-out-beheer</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>In [!DNL Journey Optimizer], wordt de toestemming door het Experience Platform afgehandeld [Goedkeuringsschema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target="_blank"}.

## Persoonlijkheidsgoedkeuring implementeren {#opt-out-personalization}

Uw klanten kunnen er ook voor kiezen om geen persoonlijke inhoud te presenteren. Zodra een profiel uit verpersoonlijking heeft gekozen, moet u ervoor zorgen dat hun gegevens niet voor verpersoonlijking worden gebruikt en u moet om het even welke gepersonaliseerde inhoud met een fallback variant vervangen.

### In beslissingsbeheer

Als u aanbiedingen gebruikt, worden de voorkeuren voor personalisatie niet automatisch geïmplementeerd in [beslissingsbereik](../offers/offer-activities/create-offer-activities.md#add-decision-scopes) gebruikt uit een [beslissing](../offers/api-reference/offer-delivery-api/decisioning-api.md) API-verzoek of [randdefinitie](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md) API-verzoek. In dit geval, moet u verpersoonlijkingstoestemming manueel afdwingen. Hiervoor voert u de volgende stappen uit.

>[!NOTE]
>
>Beslissingsbereik gebruikt in [!DNL Journey Optimizer] authored kanalen voldoen aan deze eis van de reis of de campagne waartoe zij behoren.



1. Een [Adobe Experience Platform-segment](../segment/about-segments.md) een profielkenmerk gebruiken, zoals: *&quot;Consents to Personalization = True&quot;* om gebruikers aan te wijzen die met personalisatie hebben ingestemd.

1. Wanneer u een [beslissing](../offers/offer-activities/create-offer-activities.md), voegt u een beslissingsbereik toe en definieert u een subsidiabiliteitsbeperking op basis van dit segment voor elke verzameling evaluatiecriteria die gepersonaliseerde aanbiedingen bevat.

1. Een [fallback-aanbieding](../offers/offer-library/creating-fallback-offers.md) dat geen gepersonaliseerde inhoud omvat.

1. [Toewijzen](../offers/offer-activities/create-offer-activities.md#add-fallback) het niet-persoonlijke fallback-aanbod aan het besluit.

1. [Controleren en opslaan](../offers/offer-activities/create-offer-activities.md#review) de beschikking.

Als een gebruiker:

* met toestemming voor personalisatie zal het beslissingsbereik het beste aanbod voor dat profiel bepalen .

* zonder toestemming voor personalisatie, komt het desbetreffende profiel niet in aanmerking voor een van de aanbiedingen die in de evaluatiecriteria zijn opgenomen en zal daarom het niet-persoonlijke fallback-aanbod ontvangen.

>[!NOTE]
>
>Toestemming voor het gebruik van profielgegevens in [gegevensmodellering](../offers/ranking/ai-models.md) wordt nog niet ondersteund in [!DNL Journey Optimizer].

