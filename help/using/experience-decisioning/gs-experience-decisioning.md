---
title: Aan de slag met beslissing
description: Meer informatie over beslissingen
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
version: Journey Orchestration
source-git-commit: 9ac3eaba0b4c6536c1c447df825eb5f5c0afc900
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 4%

---

# Aan de slag met beslissing {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="Wat is de beslissing?"
>abstract="Beslissing is een nieuw instrument naast het beheer van besluiten om de beste punten te kiezen uit de beslissingsmotor en aan elk individu te leveren. Er is aanvullende installatie nodig om deze te kunnen gebruiken."

## Wat is beslissend? {#about}

Beslissing vereenvoudigt personalisering met een gecentraliseerde catalogus van marketingaanbiedingen die gelden als &#39;beslissingspunten&#39; en een geavanceerde besluitvormingsengine. Deze motor hanteert regels en rangschikkingscriteria om de meest relevante beslissingsitems te selecteren en aan elk individu voor te leggen.

Deze besluitpunten zijn naadloos geïntegreerd in een brede waaier van binnenkomende oppervlakten door het [&#x200B; op code-gebaseerde ervaringskanaal &#x200B;](../code-based/get-started-code-based.md), toegankelijk binnen [!DNL Adobe Journey Optimizer] campagnes.

>[!IMPORTANT]
>
>Beslissingsbeleid is alleen beschikbaar voor gebruik in code-gebaseerde ervaring- en e-mailcampagnes.

➡️ [Ontdek deze functie in video](#video)

➡️ Een gebruiksgeval dat van begin tot eind toont hoe te om besluiten tot stand te brengen en hen te gebruiken in inhoudsexperimenten met het op code-gebaseerde ervaringskanaal wordt voorgesteld in [&#x200B; deze sectie &#x200B;](experience-decisioning-uc.md).

## Belangrijke stappen voor besluitvorming {#steps}

De belangrijkste stappen om met Beslissing te werken zijn als volgt:

1. **wijs juiste toestemmingen** toe. Beslissingen zijn alleen beschikbaar voor gebruikers met toegang tot een besluit dat betrekking heeft op **[!UICONTROL role]** , zoals Beslissingsmanagers. Als u geen toegang hebt tot Beslissing, moeten uw toestemmingen worden uitgebreid.

   +++Leer hoe u de rol van beslissingsmanagers toewijst

   1. Als u een rol wilt toewijzen aan een gebruiker in het [!DNL Permissions] -product, navigeert u naar het tabblad **[!UICONTROL Roles]** en selecteert u Beslissingsmanagers.

      ![](assets/decision_permission_1.png)

   1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

      ![](assets/decision_permission_2.png)

   1. Typ de naam of het e-mailadres van de gebruiker of selecteer de gebruiker in de lijst en klik op **[!UICONTROL Save]** .

      Als de gebruiker niet eerder werd gecreeerd, verwijs naar [&#x200B; gebruikersdocumentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/access-control/ui/users) toevoegen.

      ![](assets/decision_permission_3.png)

   Uw gebruiker moet dan een e-mail ontvangen die aan uw instantie opnieuw richt.

   +++

1. **vorm douanekenmerken**: Tailor de puntcatalogus aan uw specifieke vereisten door opstellingsdouaneattributen in het schema van de catalogus.

   ➡️ [&#x200B; Leer hoe te om de puntcatalogus &#x200B;](catalogs.md) te vormen

1. **creeer besluitpunten** om aan uw gericht publiek te tonen.

   ➡️ [&#x200B; Leer hoe te om besluitvormingspunten &#x200B;](items.md) in het gebruikersinterface (en in de [&#x200B; API documentatie &#x200B;](api-reference/decisions-items/create.md) tot stand te brengen)

1. **organiseert zich met inzamelingen**: De inzamelingen van het gebruik om besluitpunten te categoriseren die op op attribuut-gebaseerde regels worden gebaseerd. Neem inzamelingen in uw selectiestrategieën op om te bepalen welke inzameling van besluitvormingspunten zou moeten worden overwogen.

   ➡️ [&#x200B; Leer hoe te om puntinzamelingen &#x200B;](collections.md) in het gebruikersinterface (en in de [&#x200B; API documentatie &#x200B;](api-reference/items-collections/create.md) te beheren)

1. **creeer besluitvormingsregels**: De regels van het besluit worden gebruikt in besluitvormingspunten en/of selectiestrategieën om te bepalen aan wie een besluitpunt kan worden getoond.

   ➡️ [&#x200B; Leer hoe te om besluitvormingsregels tot stand te brengen &#x200B;](rules.md)

1. **voert het rangschikken methodes** uit: Creeer het rangschikken methodes en pas hen binnen selectiestrategieën toe om de prioritaire orde te bepalen om besluitpunten te selecteren.

   ➡️ [&#x200B; Leer hoe te om het rangschikken methodes &#x200B;](ranking/ranking.md) tot stand te brengen

1. **creeer selectiestrategieën**: Bouw selectiestrategieën die hefboominzamelingen, besluitvormingsregels, en het rangschikken methodes om de besluitpunten te identificeren geschikt voor het tonen aan profielen.

   ➡️ [&#x200B; Leer hoe te om selectiestrategieën in het gebruikersinterface &#x200B;](selection-strategies.md) in het gebruikersinterface (en in de [&#x200B; API documentatie &#x200B;](api-reference/selection-strategies/create.md) tot stand te brengen)

1. **creeer een besluitvormingsbeleid en bedt het in uw op code-gebaseerde of e-mailreis/campagne** in: Het beleid van het besluit combineert veelvoudige selectiestrategieën om de in aanmerking komende besluitpunten te bepalen aan vertoning aan het voorgenomen publiek.

   ➡️ [&#x200B; Leer hoe te met besluitvormingsbeleid &#x200B;](create-decision.md) te werken
➡️ om de aanbieding via op code-gebaseerd ervaringskanaal met succes te leveren, volg de implementatiestappen in [&#x200B; deze sectie &#x200B;](../code-based/code-based-implementation-samples.md).

## Aanvullende bronnen

* **[creeer besluitpunten](items.md)** - leer hoe te om besluitvormingspunten met inbegrip van aanbiedingen, inhoudsafwijkingen, en ervaringen tot stand te brengen en te beheren.
* **[vormt besluitcatalogi](catalogs.md)** - begrijp hoe te om besluitvormingspunten in catalogi voor beter beheer te organiseren.
* **[bepaal selectiestrategieën](selection-strategies.md)** - ontdek hoe te om selectiestrategieën met toelatingsregels en rangschikkende methodes tot stand te brengen.
* **[creeer besluitvormingsbeleid](create-decision-policy.md)** - leer hoe te om besluitvormingsbeleid te bouwen dat strategieën en beperkingen combineert.
* **[Rangschikkend en AI modellen](ranking/ranking.md)** - de Hoofd rangschikkende formules en AI modellen voor gepersonaliseerd besluit.
* **[Migreer van het beheer van Besluit](migrate-to-decisioning.md)** - begrijp de voordelen van het migreren aan Beslissing en gebruik migrerende tooling APIs.
* **[Beslissende gidsen](decisioning-guardrails.md)** - herzie belangrijke beperkingen en beste praktijken voor beslissingsimplementatie.
* **[het Beslissen leerprogramma&#39;s &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-learn/tutorials/decision-capabilities/decisioning/introduction-to-decisioning){target="_blank"}** - Onderzoek geleidelijke videoleerprogramma&#39;s op besluitvormingseigenschappen en beste praktijken.

## Hoe kan ik-video {#video}

Meer informatie over beslissingsmogelijkheden in Adobe Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3475869?captions=dut&quality=12)
