---
title: Aan de slag met beslissing
description: Meer informatie over beslissingen
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 41563414b2118ae1fcde65874c56f38daf4fa9ab
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 4%

---

# Aan de slag met beslissing {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="Wat is de beslissing?"
>abstract="Beslissing is een nieuw instrument naast het beheer van besluiten om de beste punten te kiezen uit de beslissingsmotor en aan elk individu te leveren. Er is aanvullende installatie nodig om deze te kunnen gebruiken."

## Wat is beslissend? {#about}

Beslissing vereenvoudigt personalisering met een gecentraliseerde catalogus van marketingaanbiedingen die gelden als &#39;beslissingspunten&#39; en een geavanceerde besluitvormingsengine. Deze motor hanteert regels en rangschikkingscriteria om de meest relevante beslissingsitems te selecteren en aan elk individu voor te leggen.

Deze besluitpunten zijn naadloos geïntegreerd in een brede waaier van binnenkomende oppervlakten door het [ nieuwe code-gebaseerde ervaringskanaal ](../code-based/get-started-code-based.md), toegankelijk binnen de campagnes van Journey Optimizer.

>[!IMPORTANT]
>
>Beslissingsbeleid is alleen beschikbaar voor gebruik in code-gebaseerde ervaring- en e-mailcampagnes.

➡️ Een gebruiksgeval dat van begin tot eind toont hoe te om besluiten tot stand te brengen en hen te gebruiken in inhoudsexperimenten met het op code-gebaseerde ervaringskanaal wordt voorgesteld in [ deze sectie ](experience-decisioning-uc.md).

## Belangrijke stappen voor besluitvorming {#steps}

De belangrijkste stappen om met Beslissing te werken zijn als volgt:

1. **wijs juiste toestemmingen** toe. Beslissingen zijn alleen beschikbaar voor gebruikers met toegang tot een besluit dat betrekking heeft op **[!UICONTROL role]** , zoals Beslissingsmanagers. Als u geen toegang hebt tot Beslissing, moeten uw toestemmingen worden uitgebreid.

   +++Leer hoe u de rol van beslissingsmanagers toewijst

   1. Als u een rol wilt toewijzen aan een gebruiker in het [!DNL Permissions] -product, navigeert u naar het tabblad **[!UICONTROL Roles]** en selecteert u Beslissingsmanagers.

      ![](assets/decision_permission_1.png)

   1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

      ![](assets/decision_permission_2.png)

   1. Typ de naam of het e-mailadres van de gebruiker of selecteer de gebruiker in de lijst en klik op **[!UICONTROL Save]** .

      Als de gebruiker niet eerder werd gecreeerd, verwijs naar [ gebruikersdocumentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users) toevoegen.

      ![](assets/decision_permission_3.png)

   Uw gebruiker moet dan een e-mail ontvangen die aan uw instantie opnieuw richt.

+++

1. **vorm douanekenmerken**: Tailor de puntcatalogus aan uw specifieke vereisten door opstellingsdouaneattributen in het schema van de catalogus.

   ➡️ [ Leer hoe te om de puntcatalogus ](catalogs.md) te vormen

1. **creeer besluitpunten** om aan uw gericht publiek te tonen.

   ➡️ [ Leer hoe te om beslissende punten ](items.md) in het gebruikersinterface (en in de [ API documentatie ](api-reference/decisions-items/create.md) tot stand te brengen)

1. **organiseert zich met inzamelingen**: De inzamelingen van het gebruik om besluitpunten te categoriseren die op op attribuut-gebaseerde regels worden gebaseerd. Neem inzamelingen in uw selectiestrategieën op om te bepalen welke inzameling van besluitvormingspunten zou moeten worden overwogen.

   ➡️ [ Leer hoe te om puntinzamelingen ](collections.md) in het gebruikersinterface (en in de [ API documentatie ](api-reference/items-collections/create.md) te beheren)

1. **creeer besluitvormingsregels**: De regels van het besluit worden gebruikt in besluitvormingspunten en/of selectiestrategieën om te bepalen aan wie een besluitpunt kan worden getoond.

   ➡️ [ Leer hoe te om besluitvormingsregels tot stand te brengen ](rules.md)

1. **voert het rangschikken methodes** uit: Creeer het rangschikken methodes en pas hen binnen selectiestrategieën toe om de prioritaire orde te bepalen om besluitpunten te selecteren.

   ➡️ [ Leer hoe te om het rangschikken methodes ](ranking/ranking.md) tot stand te brengen

1. **creeer selectiestrategieën**: Bouw selectiestrategieën die hefboominzamelingen, besluitvormingsregels, en het rangschikken methodes om de besluitpunten te identificeren geschikt voor het tonen aan profielen.

   ➡️ [ Leer hoe te om selectiestrategieën in het gebruikersinterface ](selection-strategies.md) in het gebruikersinterface (en in de [ API documentatie ](api-reference/selection-strategies/create.md) tot stand te brengen)

1. **creeer een besluitvormingsbeleid en bedt het in uw op code-gebaseerde of e-mailreis/campagne** in: Het beleid van het besluit combineert veelvoudige selectiestrategieën om de in aanmerking komende besluitpunten te bepalen aan vertoning aan het voorgenomen publiek.

   ➡️ [ Leer hoe te met besluitvormingsbeleid ](create-decision.md) te werken
➡️ om de aanbieding via op code-gebaseerd ervaringskanaal met succes te leveren, volg de implementatiestappen in [ deze sectie ](../code-based/code-based-implementation-samples.md).

