---
title: Beslissingsbeleid gebruiken in berichten
description: Leer hoe u beleidsregels voor beslissingen gebruikt in uw berichten.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
version: Journey Orchestration
exl-id: 35fc3cf2-1b91-4f30-ad71-f9d7d2a0291c
source-git-commit: be4c0453630388d898d53feeb5f9dcfe57ad5934
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# Beslissingsbeleid gebruiken in berichten {#create-decision}

Nadat u een beslissingsbeleid aan de inhoud hebt toegevoegd, kunt u kenmerken van geretourneerde beslissingsitems gebruiken voor personalisatie. Om dit te doen, neem eerst de code van het besluitvormingsbeleid in uw inhoud op.

>[!CAUTION]
>
>Het beleid van het besluit is beschikbaar aan alle klanten voor de **op code-gebaseerde Ervaring**, **SMS**, en **Push bericht** kanalen.
>
>Het besluit voor het **E-mail** kanaal is beschikbaar in Beperkte Beschikbaarheid slechts. Neem contact op met uw Adobe-vertegenwoordiger als u toegang wilt aanvragen. Leer meer over [&#x200B; beschikbaarheidslabels &#x200B;](../rn/releases.md#availability-labels).

## De beleidscode voor beslissingen invoegen {#insert}

>[!BEGINTABS]

>[!TAB  op code-gebaseerde Ervaring ]

1. Bewerk uw op code gebaseerde ervaring en navigeer naar **[!UICONTROL Decision policy]** .

2. Selecteer **[!UICONTROL Insert policy]** om de code voor het beslissingsbeleid toe te voegen.

   ![](assets/decision-code-based-add-decision.png)

>[!NOTE]
>
>Voor op code-gebaseerde ervaringen, als uw besluitvormingsbeleid besluitpunten met inbegrip van fragmenten bevat, kunt u deze fragmenten in de code van het besluitvormingsbeleid hefboomwerking. [&#x200B; leer hoe te hefboomfragmenten &#x200B;](../experience-decisioning/fragments-decision-policies.md)

>[!TAB  E-mail ]

1. Open de **Redacteur van Personalization** en navigeer aan **[!UICONTROL Decision policies]**.

2. Selecteer **[!UICONTROL Insert syntax]** om de code voor uw beslissingsbeleid toe te voegen.

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >Als de invoegoptie niet wordt weergegeven, is er mogelijk al een beslissingsbeleid geconfigureerd voor de bovenliggende component.

3. Als er nog geen plaatsing aan de component is toegewezen, selecteert u een plaatsing in de lijst en klikt u op **[!UICONTROL Assign]** .

   ![](assets/decision-policy-placement.png)

>[!TAB  SMS ]

1. Open de **Redacteur van Personalization** en navigeer aan **[!UICONTROL Decision policies]**.

2. Selecteer **[!UICONTROL Insert syntax]** om de code voor uw beslissingsbeleid toe te voegen.

   ![](assets/decision-policy-add-sms-insert-syntax.png)

>[!TAB  Duw ]

1. Open de **Redacteur van Personalization** en navigeer aan **[!UICONTROL Decision policies]**.

2. Selecteer **[!UICONTROL Insert syntax]** om de code voor uw beslissingsbeleid toe te voegen.

   ![](assets/decision-policy-add-push-insert-syntax.png)

>[!IMPORTANT]
>
>Voor het bepalen van de ervaring met pushmeldingen is een specifieke versie van de Mobile SDK vereist. Alvorens deze eigenschap uit te voeren, controleer de [&#x200B; versienota&#39;s &#x200B;](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"} om de vereiste versie te identificeren en u te verzekeren dienovereenkomstig hebt bevorderd. U kunt alle beschikbare versies van SDK voor uw platform in [&#x200B; ook bekijken deze sectie &#x200B;](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}.

>[!ENDTABS]

De code van het besluitvormingsbeleid wordt toegevoegd. U kunt nu kenmerken van de geretourneerde beslissingsitems gebruiken om de inhoud aan te passen.

>[!NOTE]
>
>Voor code-gebaseerde ervaring en e-mailkanalen, herhaal deze opeenvolging eens per besluitpunt u teruggekeerd wilt. Bijvoorbeeld, als u verkoos om 2 punten terug te keren wanneer [&#x200B; creërend het besluit &#x200B;](create-decision-policy.md), herhaal tweemaal de opeenvolging. Voor SMS- en pushkanalen kan slechts één beslissingsitem worden geretourneerd.

## Persoonlijk maken met kenmerken van een keuze-item {#attributes}

Nadat u de code voor een beslissingsbeleid in uw inhoud hebt toegevoegd, worden alle kenmerken van de geretourneerde beslissingsitems beschikbaar voor personalisatie. [&#x200B; Leer hoe te met verpersoonlijking &#x200B;](../personalization/personalize.md) te werken.

De attributen worden opgeslagen in het &quot;Aanbiedingen&quot; [&#x200B; catalogusschema &#x200B;](catalogs.md). Zij tonen in de volgende omslagen van de verpersoonlijkingsredacteur:
* **de attributen van de Douane**: `_\<imsOrg\>` omslag
* **Standaard attributen**: `_experience` omslag

Kenmerken van beslissingsitems en contextafhankelijke kenmerken worden standaard niet ondersteund in [!DNL Journey Optimizer] -fragmenten. In plaats daarvan kunt u echter algemene variabelen gebruiken, zoals hieronder beschreven.

![](assets/decision-code-based-decision-attributes.png)

Als u een kenmerk wilt toevoegen, klikt u op het pictogram **`+`** naast het kenmerk. U kunt zoveel kenmerken toevoegen als u nodig hebt. U kunt ook andere personalisatiekenmerken opnemen, zoals profielgegevens.

* Voor **E-mail** en **code-Gebaseerde** kanalen, verpak de attributen binnen de `#each` lijn gebruikend vierkante steunen `[ ]`, en voeg een komma vóór de sluitende `/each` markering toe.

  +++Zie voorbeeld

  ![](assets/decision-code-based-wrap-code.png)

  +++

* Voor **SMS** en **duw** kanalen, zorg ervoor u attributen na de syntaxiscode voor het besluitvormingsbeleid opneemt. Deze syntaxis moet altijd op regel 1 staan.

  +++Zie voorbeeld

  ![](assets/decision-added-sms.png)

  +++

  >[!NOTE]
  >Als u een kenmerk van een afbeeldingselement invoegt in SMS of Push-inhoud (bijvoorbeeld in de titel of de hoofdtekst), wordt de kenmerkwaarde weergegeven als een URL. De afbeelding zelf wordt niet gerenderd in deze velden.

* Als u het bijhouden van beslissingsitems wilt inschakelen, voegt u het attribuut `trackingToken` toe: `trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

## Inhoud voorvertonen en testen

Nadat u de inhoud hebt gemaakt, kunt u deze voorvertonen en testen voordat u uw reis of campagne activeert. De punten van het besluit geven terug gebaseerd op geselecteerde profielen in de simulatieinterface. [&#x200B; Leer hoe te om inhoud &#x200B;](../content-management/preview-test.md) voor te vertonen en te testen.

## Volgende stappen {#final-steps}

Als uw inhoud klaar is, kunt u uw campagne of reis beoordelen en publiceren:

* [Een journey publiceren](../building-journeys/publish-journey.md)
* [Een campagne bekijken en activeren](../campaigns/review-activate-campaign.md)

Voor code-gebaseerde ervaringen, zodra uw ontwikkelaar een API of SDK vraag om inhoud voor de oppervlakte te halen die in uw kanaalconfiguratie wordt bepaald, zullen de veranderingen op uw Web-pagina of app worden toegepast.

>[!NOTE]
>
>U kunt momenteel geen op besluit-gebaseerde inhoud voor [&#x200B; op code-gebaseerde ervaring &#x200B;](../code-based/create-code-based.md) campagnes of reizen simuleren. Een alternerende actie is beschikbaar [&#x200B; hier &#x200B;](../code-based/code-based-decisioning-implementations.md).

## Rapporterende dashboards gebruiken

Om te zien hoe uw besluiten presteren, kunt u uit-van-de-doos beslissingsmetriek in de campagne of het reisrapport bekijken, of douane Customer Journey Analytics dashboards bouwen om prestaties te meten en inzicht in te winnen hoe uw besluitvormingsbeleid en aanbiedingen worden geleverd en met geëngageerd. [&#x200B; Leer meer over Beslissing die &#x200B;](cja-reporting.md) rapporteert.

![](../reports/assets/cja-decisioning-item-performance.png)
