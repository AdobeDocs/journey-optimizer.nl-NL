---
title: Simulaties maken
description: Leer hoe u simulaties maakt
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: 899b8b47d6c6121c19e485376de368358049c05f
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# Simulaties maken

## Informatie over simulatie

Om uw beslissingslogica te bevestigen, kunt u simuleren welke aanbiedingen aan een testprofiel voor een bepaalde plaatsing zullen worden geleverd.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Hierdoor kunt u verschillende versies van uw aanbiedingen testen en verfijnen, zonder dat dit gevolgen heeft voor de beoogde ontvangers.

>[!NOTE]
>
>Deze mogelijkheid simuleert één verzoek aan de [!DNL Decisions] API. Meer informatie over [Aanbiedingen leveren met behulp van de Besluiten-API](../api-reference/decisions-api/deliver-offers.md).

Als u deze functie wilt openen, selecteert u de optie **[!UICONTROL Simulation]** van de **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** -menu.

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## Testprofielen selecteren

Eerst moet u de testprofielen selecteren die u voor simulatie gaat gebruiken.

1. Klik op **[!UICONTROL Manage profile]**.

   ![](../../assets/offers_simulation-manage-profile.png)

1. Selecteer de naamruimte voor de identiteit die u wilt gebruiken om testprofielen te identificeren. In dit voorbeeld gebruiken we de **E-mail** naamruimte.

   >[!NOTE]
   >
   >Een naamruimte voor identiteiten definieert de context van een id, zoals een e-mailadres of CRM-id. Meer informatie over naamruimten in Adobe Experience Platform [in deze sectie](../../get-started-identity.md){target=&quot;_blank&quot;}.

1. Voer de identiteitswaarde in en klik op **[!UICONTROL View]** om de beschikbare profielen weer te geven.

   ![](../../assets/offers_simulation-add-profile.png)

1. Voeg andere profielen toe als u andere profielgegevens wilt testen en sla uw selectie op.

   ![](../../assets/offers_simulation-save-profiles.png)

1. Na toevoeging worden alle profielen vermeld in de vervolgkeuzelijst onder **[!UICONTROL Test profile]**. U kunt schakelen tussen de opgeslagen testprofielen om de resultaten voor elk geselecteerd profiel weer te geven.

   ![](../../assets/offers_simulation-saved-profiles.png)

1. U kunt op de knop **[!UICONTROL Profile details]** koppeling gebruiken om de geselecteerde profielgegevens weer te geven.

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## Beslissingsbereik toevoegen

Selecteer nu de aanbiedingsbesluiten die u op uw testprofielen wilt simuleren.

1. Selecteer **[!UICONTROL Add decision scope]**.

   ![](../../assets/offers_simulation-add-decision.png)

1. Selecteer een plaatsing in de lijst.

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. De beschikbare beslissingen worden weergegeven.

   * U kunt het zoekveld gebruiken om de selectie te verfijnen.
   * U kunt op de knop **[!UICONTROL Open offer decisions]** Hiermee opent u de lijst met alle beslissingen die u hebt gemaakt. Meer informatie over [besluiten](create-offer-activities.md).

   Selecteer de gewenste beslissing en klik op **[!UICONTROL Add]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. Het beslissingsbereik dat u zojuist hebt gedefinieerd, wordt weergegeven in de hoofdwerkruimte.

   U kunt het aantal voorstellen aanpassen dat u wilt verzoeken. Als u bijvoorbeeld 2 selecteert, worden de beste 2 aanbiedingen weergegeven voor dit beslissingsbereik.

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Je kunt maximaal 30 voorstellen aanvragen.

1. Herhaal bovenstaande stappen om zoveel beslissingen toe te voegen als u nodig hebt.

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Zelfs als u verschillende beslissingsbereiken definieert, wordt slechts één API-aanvraag gesimuleerd.
   >
   >Alle markeringen voor deduplicatie worden standaard ingeschakeld voor simulatie, wat betekent dat de besluitvormingsengine duplicaten toestaat en dus dezelfde voorstelling kan maken voor meerdere beslissingen. Meer informatie over de [!DNL Decisions] Eigenschappen voor API-aanvragen in [deze sectie](../api-reference/decisions-api/deliver-offers.md).

## Simulatieresultaten weergeven

Nadat u een beslissingsbereik hebt toegevoegd en een testprofiel hebt geselecteerd, kunt u de resultaten bekijken.

1. Klik op **[!UICONTROL View results]**.

   ![](../../assets/offers_simulation-view-results.png)

1. De beste beschikbare aanbiedingen worden weergegeven volgens het geselecteerde profiel voor elke beslissing.

   Selecteer een voorstel om de details ervan weer te geven.

   ![](../../assets/offers_simulation-offer-details.png)

1. Selecteer een ander profiel in de lijst om de resultaten van de biedingsbesluiten voor een ander testprofiel weer te geven.

1. U kunt het beslissingsbereik zo vaak als nodig toevoegen, verwijderen of bijwerken.

>[!NOTE]
>
>Elke keer dat u profielen wijzigt of beslissingsbereik bijwerkt, moet u de resultaten vernieuwen met de opdracht **[!UICONTROL View results]** knop.

<!--Questions

* Is it recommended to first select profiles or first add decision scopes?
* What does Request offer changes?
* Nothing displays when I click View results? Can't see any score...
* What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
* What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
* Is there a way to create relevant test profiles?
* Error on Profile details link.
* Is there a tutorial planned to be released?
* Why still a big red frame when no profile is found?

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->