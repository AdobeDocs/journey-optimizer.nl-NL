---
title: Aan de slag met beleidsbeslissingen
description: Leer hoe u met beleidsbeslissingen werkt om aanbiedingen te leveren.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: fc741db8db2ca9c05dbb87a41712e90a62a18c13
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Aan de slag met beleidsbeslissingen {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Wat is een beslissing?"
>abstract="Het beslissingsbeleid bevat alle selectielogica waarmee de beslissingsengine de beste inhoud kan kiezen. Het besluitvormingsbeleid is specifiek voor de campagne. Hun doel is de beste aanbiedingen voor elk profiel te selecteren terwijl het campagneontwerp u toestaat om erop te wijzen hoe de geselecteerde besluitvormingspunten zouden moeten worden voorgesteld, met inbegrip van welke puntattributen om in het bericht worden omvat."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Informatie over beslissen"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="Een beslissingsbeleid definiëren"
>abstract="Een besluitvormingsbeleid staat u toe om de beste punten van de motor van Beslissing te kiezen en hen aan het juiste publiek te leveren."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Informatie over beslissen"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="Beslissingsbeleid"
>abstract="Met een beslissingsbeleid kunt u de beste items kiezen uit de beslissingsengine en leveren aan elk publiek."

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="Plaatsing"
>abstract="Een plaatsing bepaalt waar de teruggekeerde punten van de besluitvormingsmotor in een bericht verschijnen. U kunt de prestaties van de verschillende locaties in de rapportage bijhouden."

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="Beslissingskenmerken selecteren uit catalogus"
>abstract="Beslissingskenmerken worden opgeslagen in het schema van de catalogus. Selecteer een kenmerk dat u hier wilt gebruiken in de geselecteerde catalogus."

Beslissingsbeleid is containers voor uw aanbiedingen die de beslissingsengine gebruiken om dynamisch de beste inhoud te retourneren die voor elk publiekslid kan worden geleverd. Hun doel is de beste aanbiedingen voor elk profiel te selecteren, terwijl het campagne/reis auteursrecht u toestaat om te wijzen op hoe de geselecteerde besluitvormingspunten, met inbegrip van welke puntattributen in het bericht moeten worden omvat.

>[!AVAILABILITY]
>
>Momenteel, zijn het besluitvormingsbeleid beschikbaar aan alle klanten voor het op code-gebaseerde kanaal van de Ervaring. Ze zijn beschikbaar voor het e-mailkanaal als een beperkte beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

## Belangrijkste stappen {#key}

De belangrijkste stappen voor hefboomwerking beslissingsbeleid in berichten zijn als volgt:

1. [Beslissingsbeleid maken](../experience-decisioning/create-decision-policy.md)

   Opstelling een besluitvormingsbeleid in uw bericht door het aantal punten te kiezen om terug te keren, vormend selectiestrategieën, reserveopties, en evaluatieorde.

1. [Het beslissingsbeleid in uw inhoud gebruiken](../experience-decisioning/use-decision-policy.md)

   Pas uw inhoud met de output van het besluitvormingsbeleid en attributen van de besluitvormingspunten aan u in het bericht wilt tonen.

1. [Rapportagedashboards maken](cja-reporting.md)

   Bouw aangepaste Customer Journey Analytics dashboards om prestaties te meten en inzicht te krijgen in hoe je besluitvormingsbeleid en aanbiedingen worden geleverd en waarmee je werkt.

## Afbeeldingen en beperkingen

* **E-mail spiegelpagina&#39;s** - voor nu, geven de besluitvormingspunten niet in e-mailspiegelpagina&#39;s terug.
* **het Volgen &amp; het type van verbindingen** - om verbindingen te volgen die door besluit worden geproduceerd, bepaal hen in het schema als &quot;Beslissende Assets&quot;. Op kenmerken gebaseerde koppelingen kunnen niet worden gevolgd.
* **beleid dat van het Besluit in e-mail** negeert - u kunt geen veelvoudige besluitvormingsbeleid binnen een ouder e-mailcomponent nesten die reeds een bijbehorend besluitvormingsbeleid heeft.
* **Gedupliceerde reizen/campagnes met besluit** - als u een reis of een campagne dupliceert die een besluitvormingsbeleid omvat, verwijst de gedupliceerde versie naar de originele e-mail of op code-gebaseerde ervaring, veroorzakend fouten. Configureer het beslissingsbeleid altijd na duplicatie.
* **het beleid van de Goedkeuring** - de Updates aan toestemmingsbeleid nemen tot 48 uren om van kracht te worden. Als in een besluitvormingsbeleid wordt verwezen naar een kenmerk dat is gekoppeld aan een onlangs bijgewerkt beleid voor toestemming, worden de wijzigingen niet onmiddellijk toegepast.

  Op dezelfde manier als nieuwe profielattributen die aan een toestemmingsbeleid onderworpen zijn aan een besluitvormingsbeleid worden toegevoegd, zullen zij bruikbaar zijn, maar het toestemmingsbeleid verbonden aan hen zal niet worden afgedwongen tot de vertraging is overgegaan.

  Beleid met toestemming is alleen beschikbaar voor organisaties met de invoegtoepassing Adobe Healthcare Shield of Privacy and Security Shield.

* **AI het Rangschikken** - voor nu, wordt AI het rangschikken niet gesteund voor het E-mailkanaal in reizen met besluit.

## Volgende stappen {#next-steps}

Nu u begrijpt hoe beleidsbeslissingen werken en hoe u persoonlijke aanbiedingen kunt aanbieden, bent u klaar om uw eerste beslissingsbeleid te maken.

➡️ [ Leer hoe te om een besluitvormingsbeleid ](../experience-decisioning/create-decision-policy.md) tot stand te brengen

