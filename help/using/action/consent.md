---
solution: Journey Optimizer
product: journey optimizer
title: Werken met toestemmingsbeleid
description: Meer informatie over het werken met het instemmingsbeleid van Adobe Experience Platform
feature: Journeys, Actions, Custom Actions, Privacy, Consent Management
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: beleid, bestuur, platform, gezondheidsschild, toestemming
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: d549e4fdb7cd71e450cd00e4fa8707ae03ce0aff
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 0%

---

# Werken met toestemmingsbeleid {#consent-management}

<!--Adobe Experience Platform allows you to easily adopt and enforce marketing policies to respect the consent preferences of your customers. Consent policies are defined in Adobe Experience Platform. Refer to [this documentation](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#consent-policy).

In Journey Optimizer, you can apply these consent policies to your custom actions. For example, you can define consent policies to exclude customers who have not consented to receive email, push or SMS communication.-->

Uw gegevens zijn mogelijk onderworpen aan gebruiksbeperkingen die zijn gedefinieerd door uw organisatie of door wettelijke voorschriften. Het is daarom belangrijk ervoor te zorgen dat uw gegevensbewerkingen in Journey Optimizer voldoen aan de [beleid voor gegevensgebruik](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html){target="_blank"}. These policies are Adobe Experience Platform rules defining which [marketing actions](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html#marketing-actions){target="_blank"} u mag gegevens bewerken.

Eén type beleid voor gegevensgebruik is beschikbaar **toestemmingsbeleid**. Met deze services kunt u eenvoudig marketingbeleid toepassen en afdwingen om de voorkeuren voor machtigingen van uw klanten te respecteren. [Meer informatie over beleidshandhaving](https://experienceleague.adobe.com/docs/experience-platform/data-governance/enforcement/auto-enforcement.html){target="_blank"}

>[!IMPORTANT]
>
>Beleid voor toestemming is momenteel alleen beschikbaar voor organisaties die de Adobe hebben aangeschaft **Gezondheidsschild** of **Privacy- en beveiligingsschild** add-on aanbiedingen.

U kunt bijvoorbeeld [beleid voor instemming maken](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#consent-policy){target="_blank"} in Experience Platform om klanten uit te sluiten die niet hebben ingestemd met het ontvangen van e-mail-, push- of SMS-berichten.

In Journey Optimizer wordt de toestemming op verschillende niveaus gedefinieerd. U kunt toestemmingsbeleid op uw reis douaneacties toepassen:

* Wanneer **een aangepaste handeling configureren** kunt u een kanaal- en marketingactie definiëren. [Meer informatie](#consent-custom-action)
* Wanneer u het gereedschap **aangepaste actie op reis**, kunt u een extra marketingactie definiëren. [Meer informatie](#consent-journey)

## Belangrijke opmerkingen {#important-notes}

In Journey Optimizer kan toestemming worden gebruikt voor aangepaste acties. Als u het met de ingebouwde berichtmogelijkheden wilt gebruiken, moet u een voorwaardenactiviteit gebruiken om klanten in uw reis te filtreren.

Met toestemmingsbeheer worden twee reisactiviteiten geanalyseerd:

* Leespubliek: er wordt rekening gehouden met het opgehaalde publiek.
* Aangepaste actie: bij het beheer van de toestemming wordt rekening gehouden met de gebruikte kenmerken ([actieparameters](../action/about-custom-action-configuration.md#define-the-message-parameters)) en de vastgestelde marketingactie(s) (vereiste marketingactie en aanvullende marketingactie).
* Kenmerken die deel uitmaken van een veldgroep die het uit-van-de-doos Schema van de Unie gebruikt, worden niet gesteund. Deze kenmerken worden verborgen in de interface. U moet een andere veldgroep maken met een ander schema.
* Het beleid voor toestemming is alleen van toepassing wanneer een (vereiste of aanvullende) marketingactie is ingesteld op het niveau van de aangepaste actie.

Alle andere activiteiten die tijdens een reis worden gebruikt, worden niet in aanmerking genomen. Als u uw reis met een kwalificatie van het Publiek begint, wordt het publiek niet in aanmerking genomen.

Als tijdens een reis een profiel door een toestemmingsbeleid in een douaneactie wordt uitgesloten, wordt het bericht niet naar hem verzonden, maar hij gaat door met de reis. Het profiel gaat niet naar de time-out en het foutpad wanneer een voorwaarde wordt gebruikt.

Voordat u het beleid vernieuwt in een aangepaste handeling die op een reis wordt geplaatst, moet u ervoor zorgen dat er geen fouten optreden tijdens de reis.

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

## De aangepaste handeling configureren {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action"
>title="Een vereiste marketingactie definiëren"
>abstract="Met de marketingactie Vereist kunt u de marketingactie definiëren die betrekking heeft op uw aangepaste actie. Als u bijvoorbeeld die aangepaste handeling gebruikt om e-mailberichten te verzenden, kunt u de optie E-mailadres selecteren. Bij gebruik tijdens een reis worden alle toestemmingsbeleid dat met die marketingactie verband houdt, opgehaald en benut. Dit kan niet worden gewijzigd op het canvas."

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

Wanneer u de aangepaste handeling tijdens een reis toevoegt, kunt u de toestemming op verschillende manieren beheren. Klik op de knop **Alleen-lezen velden tonen** alle parameters weergeven.

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
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-audience.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

De andere stappen voor het vormen van een douaneactie in een reis zijn gedetailleerd in [deze sectie](../building-journeys/using-custom-actions.md).
