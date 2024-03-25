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
source-git-commit: 334527cbad3363b77d14dd447e06d4e8da79daec
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---

# Werken met toestemmingsbeleid {#consent-management}

Uw gegevens zijn mogelijk onderworpen aan gebruiksbeperkingen die zijn gedefinieerd door uw organisatie of door wettelijke voorschriften. Het is daarom belangrijk ervoor te zorgen dat uw gegevensbewerkingen in Journey Optimizer voldoen aan de [beleid voor gegevensgebruik](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html){target="_blank"}. These policies are Adobe Experience Platform rules defining which [marketing actions](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html#marketing-actions){target="_blank"} u mag gegevens bewerken.

Eén type beleid voor gegevensgebruik is beschikbaar **toestemmingsbeleid**. Met deze services kunt u eenvoudig marketingbeleid toepassen en afdwingen om de voorkeuren voor machtigingen van uw klanten te respecteren. [Meer informatie over beleidshandhaving](https://experienceleague.adobe.com/docs/experience-platform/data-governance/enforcement/auto-enforcement.html){target="_blank"}

>[!IMPORTANT]
>
>Beleid voor toestemming is momenteel alleen beschikbaar voor organisaties die de Adobe hebben aangeschaft **Gezondheidsschild** of **Privacy- en beveiligingsschild** add-on aanbiedingen.

U kunt bijvoorbeeld [beleid voor instemming maken](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#consent-policy){target="_blank"} in Experience Platform om klanten uit te sluiten die niet hebben ingestemd met het ontvangen van e-mail-, push- of SMS-berichten.

<!--* For the native outbound channels (Email, Push, SMS, Direct mail), the logic is as follows:

    * By default, if a profile has opted out from receiving communications from you, the corresponding profile is excluded from subsequent deliveries.

    * If you have the Adobe **Healthcare Shield** or **Privacy and Security Shield**, you can create a custom consent policy that overrides the default logic. For example, you can define a policy to only send email messages to all individuals who have opted in. In the absence of a custom policy, the default policy applies.
    
    To apply a custom policy, you need to define a marketing action in that policy and associate it to a channel surface. [Learn more](#marketing-actions)-->

Op het niveau van de reis, kunt u toestemmingsbeleid op uw douaneacties toepassen:

* Wanneer **een aangepaste handeling configureren** kunt u een kanaal- en marketingactie definiëren. [Meer informatie](#consent-custom-action)
* Wanneer u het gereedschap **aangepaste actie op reis**, kunt u een extra marketingactie definiëren. [Meer informatie](#consent-journey)

<!--

## Leverage consent policies through channel surfaces {#marketing-actions}

In [!DNL Journey Optimizer], consent is handled by the Experience Platform [Consent schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target="_blank"}.

To modify the consent field value, you can create a custom consent policy in which you define a marketing action and the conditions under which that action is performed. [Learn more on marketing actions](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html#marketing-actions){target="_blank"}

For example, if you want to create a consent policy to target only profiles who have consented to receive email communications, follow the steps below.

1. Make sure your organization has purchased the Adobe **Healthcare Shield** or **Privacy and Security Shield** add-on offerings. [Learn more](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html){target="_blank"}

1. In Adobe Experience Platform, create a custom policy (from the **[!UICONTROL Privacy]** > **[!UICONTROL Policies]** menu). [Learn how](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-policy){target="_blank"}

    ![](assets/consent-policy-create.png)

1. Choose the **[!UICONTROL Consent policy]** type and configure a condition as follows. [Learn how to configure consent policies](https://experienceleague-review.corp.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#consent-policy){target="_blank"}

    1. Under the **[!UICONTROL If]** section, select the **[!UICONTROL Email Targeting]** default marketing action.

        ![](assets/consent-policy-marketing-action.png)

        >[!NOTE]
        >
        >The core marketing actions provided out-of-the-box by Adobe are listed in [this table](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=en#core-actions){target="_blank"}. The steps to create a custom marketing action are listed in [this section](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#create-marketing-action){target="_blank"}.

    1. Select what happens when the marketing action applies. In this example, select **[!UICONTROL Email Marketing Consent]**.

    ![](assets/consent-policy-then.png)

1. Save and [enable](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#enable){target="_blank"} this policy.

1. In Journey Optimizer, create an email surface. [Learn how](../configuration/channel-surfaces.md#create-channel-surface)

1. In the email surface details, select the **[!UICONTROL Email Targeting]** marketing action.

    ![](assets/surface-marketing-action.png)

All consent policies associated with that marketing action are automatically leveraged in order to respect the preferences of your customers.

Therefore, in this example, any [email](../email/create-email.md) using that surface in a campaign or a journey is only sent to the profiles who have consented to receive emails from you. Profiles who have not consented to receive email communications are excluded.-->

## Gebruikmaken van beleid voor toestemming via aangepaste handelingen {#journey-custom-actions}

### Belangrijke opmerkingen {#important-notes}

In Journey Optimizer kan toestemming <!--also -->worden gebruikt in aangepaste handelingen. Als u het met de ingebouwde berichtmogelijkheden wilt gebruiken, moet u een voorwaardenactiviteit gebruiken om klanten in uw reis te filtreren.

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

### De aangepaste handeling configureren {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action"
>title="Een vereiste marketingactie definiëren"
>abstract="Met de marketingactie Vereist kunt u de marketingactie definiëren die betrekking heeft op uw aangepaste actie. Als u bijvoorbeeld die aangepaste handeling gebruikt om e-mailberichten te verzenden, kunt u de optie E-mailadres selecteren. Bij gebruik tijdens een reis worden alle toestemmingsbeleid dat met die marketingactie verband houdt, opgehaald en benut. Dit kan niet worden gewijzigd op het canvas."

Wanneer het vormen van een douaneactie, kunnen twee gebieden voor toestemmingsbeheer worden gebruikt.

De **Kanaal** in het veld kunt u het kanaal selecteren dat betrekking heeft op deze aangepaste handeling: **E-mail**, **SMS**, of **Pushmelding**. De voorinstelling is **Vereiste marketingactie** veld met de standaardmarketingactie voor het geselecteerde kanaal. Als u **overige**, wordt er standaard geen marketingactie gedefinieerd.

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
