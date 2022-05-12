---
solution: Journey Optimizer
title: Toestemming
description: Inhoud
feature: Actions
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 4b50dddd8cf00648b6a86ba523c6c8c8295712e1
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# Toegangsbeheer (bèta) {#consent-management}

Met Adobe Experience Platform kunt u eenvoudig marketingbeleid toepassen en afdwingen om de voorkeuren voor toestemming van uw klanten te respecteren. Beleid voor instemming wordt gedefinieerd in Adobe Experience Platform. Zie [deze documentatie](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=en#consent-policy).

In Journey Optimizer kunt u dit beleid voor toestemming toepassen op aangepaste handelingen. U kunt bijvoorbeeld regels voor toestemming definiëren om klanten uit te sluiten die niet hebben ingestemd met het ontvangen van e-mail, push- of SMS-berichten.

>[!NOTE]
>
>Deze functie wordt vrijgegeven als een persoonlijke bètaversie. Het is niet beschikbaar voor alle Journey Optimizer-klanten.

In Journey Optimizer wordt de toestemming op verschillende niveaus gedefinieerd:

* wanneer **een aangepaste handeling configureren** kunt u een kanaal- en marketingactie definiëren. Zie dit [sectie](../action/consent.md#consent-custom-action).
* bij het toevoegen van de **aangepaste actie op reis**, kunt u een extra marketingactie definiëren. Zie dit [sectie](../action/consent.md#consent-journey).

## Belangrijke opmerkingen {#important-notes}

In Journey Optimizer kan toestemming worden gebruikt voor aangepaste acties. Als u het met de ingebouwde berichtmogelijkheden wilt gebruiken, moet u een voorwaardenactiviteit gebruiken om klanten in uw reis te filtreren.

Met toestemmingsbeheer worden twee reisactiviteiten geanalyseerd:

* Leessegment: het opgehaalde segment wordt in aanmerking genomen.
* Aangepaste actie: bij het beheer van de toestemming wordt rekening gehouden met de gebruikte kenmerken ([actieparameters](../action/about-custom-action-configuration.md#define-the-message-parameters)) en de vastgestelde marketingactie(s) (vereiste marketingactie en aanvullende marketingactie).

Alle andere activiteiten die tijdens een reis worden gebruikt, worden niet in aanmerking genomen. Als u uw reis met een kwalificatie van het Segment begint, wordt het segment niet in aanmerking genomen.

Als tijdens een reis een profiel door een toestemmingsbeleid in een douaneactie wordt uitgesloten, wordt het bericht niet naar hem verzonden, maar hij gaat door met de reis. Het profiel gaat niet naar de time-out en het foutpad wanneer een voorwaarde wordt gebruikt.

Voordat u het beleid vernieuwt in een aangepaste handeling die op een reis wordt geplaatst, moet u ervoor zorgen dat er geen fouten optreden tijdens de reis.

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

## De aangepaste handeling configureren {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_admin"
>title="Een vereiste marketingactie definiëren"
>abstract="Met de actie &quot;Vereist op de markt brengen&quot; kunt u de marketingactie definiëren die betrekking heeft op uw aangepaste actie. Als u bijvoorbeeld die aangepaste handeling gebruikt om e-mailberichten te verzenden, kunt u de optie &#39;Doelstelling e-mail verzenden&#39; selecteren. Bij gebruik tijdens een reis worden alle toestemmingsbeleid dat met die marketingactie verband houdt, opgehaald en benut. Dit kan niet worden gewijzigd op het canvas."

Wanneer het vormen van een douaneactie, kunnen twee gebieden voor toestemmingsbeheer worden gebruikt.

De **Kanaal** in het veld kunt u het kanaal selecteren dat betrekking heeft op deze aangepaste handeling: **E-mail**, **SMS**, of **Pushmelding**. De voorinstelling wordt **Vereiste marketingactie** veld met de standaardmarketingactie voor het geselecteerde kanaal. Als u **overige**, wordt standaard geen marketingactie gedefinieerd.

![](assets/consent1.png)

De **Vereiste marketingactie** Hiermee kunt u de marketingactie definiëren die betrekking heeft op uw aangepaste handeling. Als u bijvoorbeeld die aangepaste handeling gebruikt om e-mailberichten te verzenden, kunt u **E-mailadres**. Bij gebruik tijdens een reis worden alle toestemmingsbeleid dat met die marketingactie verband houdt, opgehaald en benut. Er is een standaardmarketingactie geselecteerd, maar u kunt op de pijl-omlaag klikken om alle beschikbare marketingacties in de lijst te selecteren.

![](assets/consent2.png)

Voor bepaalde soorten belangrijke mededelingen, bijvoorbeeld een transactiebericht wordt verzonden om het wachtwoord van de cliënt terug te stellen die, kunt u geen toestemmingsbeleid willen toepassen. Vervolgens selecteert u **Geen** in de **Vereiste marketingactie** veld.

De andere stappen voor het configureren van een aangepaste handeling worden beschreven in [deze sectie](../action/about-custom-action-configuration.md#consent-management).

### Journey samenstellen {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="Vereiste marketingactie"
>abstract="Een vereiste marketingactie wordt gedefinieerd tijdens het maken van een aangepaste handeling. Deze vereiste marketingactie kan niet uit de actie worden verwijderd of gewijzigd."

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="Aanvullende marketingacties"
>abstract="Voeg nog een marketingactie toe naast de vereiste actie. Het beleid van de toestemming met betrekking tot beide marketing acties zal worden afgedwongen."

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="Beleid voor visualisatie van toestemmingen dat tijdens runtime wordt toegepast"
>abstract="Handelingen voor het in de handel brengen zorgen voor een toestemmingsbeleid waarin handelingsparameters en afzonderlijke waarden voor profieltoestemming worden gecombineerd om gebruikers uit te filteren. Haal de nieuwste definitie van dit beleid op door op de knop voor vernieuwen te klikken."

Wanneer u de aangepaste handeling tijdens een reis toevoegt, kunt u de toestemming op verschillende manieren beheren. Klik op de knop **Alleen-lezen velden tonen** om alle parameters weer te geven.

De **Kanaal** en **Vereiste marketingactie**, gedefinieerd tijdens het configureren van de aangepaste handeling, wordt boven in het scherm weergegeven. U kunt deze velden niet wijzigen.

![](assets/consent4.png)

U kunt een **Aanvullende marketingacties** om het type aangepaste handeling in te stellen. Hierdoor kunt u het doel van de aangepaste handeling in deze reis definiëren. Naast de vereiste marketingactie, die doorgaans specifiek is voor een kanaal, kunt u een aanvullende marketingactie definiëren die specifiek is voor de aangepaste actie op deze specifieke reis. Bijvoorbeeld: een workout-communicatie, een nieuwsbrief, een fitness-communicatie, enz. Zowel de vereiste marketingactie als de aanvullende marketingactie zijn van toepassing.

![](assets/consent3.png)

Klik op de knop **Beleid vernieuwen** onder aan het scherm om de lijst met beleidsregels bij te werken en te controleren die in aanmerking zijn genomen voor deze aangepaste handeling. Dit is uitsluitend bedoeld voor informatiedoeleinden, terwijl een reis wordt gemaakt. Bij live reizen wordt het beleid voor toestemming elke zes uur automatisch opgehaald en bijgewerkt.

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-segment.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

De andere stappen voor het vormen van een douaneactie in een reis zijn gedetailleerd in [deze sectie](../building-journeys/using-custom-actions.md).
