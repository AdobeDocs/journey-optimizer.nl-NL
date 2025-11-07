---
solution: Journey Optimizer
product: journey optimizer
title: Paginaspecifieke inhoud definiëren
description: Leer hoe u landingspagina-specifieke inhoud ontwerpt in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: landing, landing page, creation, page, form, component
exl-id: 5bf023b4-4218-4110-b171-3e70e0507fca
source-git-commit: a5dd21377a26debb0aa3174fafb29c0532562c63
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 2%

---

# Paginaspecifieke inhoud definiëren {#lp-content}

>[!CONTEXTUALHELP]
>id="ac_lp_components"
>title="Inhoudscomponenten gebruiken"
>abstract="Inhoudscomponenten zijn lege plaatsaanduidingen voor inhoud die u kunt gebruiken om de lay-out van een bestemmingspagina te maken. Gebruik de formuliercomponent om specifieke inhoud te definiëren waarmee gebruikers hun keuzes kunnen selecteren en verzenden."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/email/design-email/add-content/content-components#add-content-components" text="Inhoudscomponenten toevoegen"

Als u de inhoud van de bestemmingspagina wilt ontwerpen, kunt u dezelfde onderdelen gebruiken als voor een e-mail. [Meer informatie](../email/content-components.md#add-content-components)

Om specifieke inhoud te ontwerpen die gebruikers zal toelaten om hun keuzen te selecteren en voor te leggen, [ gebruik de vormcomponent ](#use-form-component) en bepaal zijn [ landend pagina-specifieke stijlen ](#lp-form-styles).

>[!NOTE]
>
>U kunt ook een doorklikbestemmingspagina maken zonder een component **[!UICONTROL Form]** . In dat geval wordt de landingspagina weergegeven aan gebruikers, maar hoeven zij geen formulier in te dienen. Dit kan handig zijn als u alleen een bestemmingspagina wilt weergeven zonder dat u enige actie van uw ontvangers nodig hebt, zoals aanmelden of Weigeren, of informatie wilt opgeven waarvoor geen invoer van de gebruiker is vereist.

Met de landende pagina-inhoudontwerper kunt u ook contextuele gegevens gebruiken die afkomstig zijn van de primaire pagina in een subpagina. [Meer informatie](#use-primary-page-context)

>[!NOTE]
>
>De [ Europese toegankelijkheidshandeling ](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32019L0882){target="_blank"} verklaart dat alle digitale mededelingen toegankelijk zouden moeten zijn. Zorg ervoor u de specifieke richtlijnen volgt die op [ worden vermeld deze pagina ](../email/accessible-content.md) wanneer het ontwerpen van inhoud in [!DNL Journey Optimizer].

## De formuliercomponent gebruiken {#use-form-component}

>[!CONTEXTUALHELP]
>id="ac_lp_formfield"
>title="De velden voor formuliercomponenten instellen"
>abstract="Bepaal hoe de ontvangers hun keuzes vanaf de bestemmingspagina zien en verzenden."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/landing-pages/landing-pages-design/lp-content#lp-form-styles" text="Landingspagina-formulierstijlen definiëren"

>[!CONTEXTUALHELP]
>id="ac_lp_submission"
>title="Wat gebeurt er als u op de knop klikt"
>abstract="Bepaal wat er gebeurt wanneer gebruikers het formulier voor de landingspagina indienen."

Gebruik de component **[!UICONTROL Form]** om specifieke inhoud te definiëren waarmee gebruikers hun keuzes vanaf de landingspagina kunnen selecteren en verzenden. Volg de onderstaande stappen om dit te doen.

1. Sleep de landingspaginaspecifieke **[!UICONTROL Form]** component van het linkerpalet naar de hoofdwerkruimte.

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >De component **[!UICONTROL Form]** kan slechts eenmaal op dezelfde pagina worden gebruikt.

1. Selecteer het. Het tabblad **[!UICONTROL Form content]** wordt weergegeven in het rechterpalet, zodat u de verschillende velden van het formulier kunt bewerken.

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >Schakel op elk gewenst moment over naar het tabblad **[!UICONTROL Styles]** om de stijlen van de inhoud van de formuliercomponent te bewerken. [Meer informatie](#define-lp-styles)

1. Vanuit de sectie **[!UICONTROL Checkbox 1]** kunt u het label bewerken dat hoort bij dit selectievakje.

1. Definiëren of dit selectievakje gebruikers in- of uitchecken is: stemmen ze in met het ontvangen van communicatie of vragen ze niet meer contact met hen op te nemen?

   ![](assets/lp_designer-form-update.png)

   Kies een van de drie onderstaande opties:

   * **[!UICONTROL Opt in if checked]**: gebruikers moeten het selectievakje voor toestemming (opt-in) inschakelen.
   * **[!UICONTROL Opt out if checked]**: gebruikers moeten het selectievakje inschakelen om hun toestemming (opt-out) te verwijderen.
   * **[!UICONTROL Opt in if checked, opt out if unchecked]**: met deze optie kunt u één selectievakje voor opt-in/opt-out invoegen. Gebruikers moeten het selectievakje voor toestemming (opt-in) inschakelen en het selectievakje uitschakelen om hun toestemming (opt-out) te verwijderen.

1. Kies wat tussen de drie volgende opties wordt bijgewerkt:

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Subscription list]**: U moet de abonnementenlijst selecteren die wordt bijgewerkt als het profiel dit selectievakje selecteert. Leer meer over [ abonnementenlijsten ](subscription-list.md).

     <!--![](assets/lp_designer-form-subs-list.png)-->

   * **[!UICONTROL Channel (email)]**: De optie om te weigeren of te weigeren is van toepassing op het gehele kanaal. Als een profiel dat opteert bijvoorbeeld twee e-mailadressen heeft, worden beide adressen uitgesloten van al uw communicatie.

   * **[!UICONTROL Email identity]**: De optie om te weigeren of te weigeren is alleen van toepassing op het e-mailadres dat is gebruikt voor toegang tot de bestemmingspagina. Als een profiel bijvoorbeeld twee e-mailadressen heeft, ontvangt alleen het profiel dat is gebruikt om u aan te melden, communicatie van uw merk.

1. Klik op **[!UICONTROL Add field]** > **[!UICONTROL Checkbox]** om nog een selectievakje toe te voegen. Herhaal bovenstaande stappen om de eigenschappen ervan te definiëren.

   ![](assets/lp_designer-form-checkbox-2.png)

1. U kunt ook een **[!UICONTROL Text field]** toevoegen.

   ![](assets/lp_designer-form-add-text-field.png)

   * Voer de **[!UICONTROL Label]** in die boven op het veld in het formulier wordt weergegeven.

   * Voer een **[!UICONTROL Placeholder]** -tekst in. Het wordt in het veld weergegeven voordat de gebruiker het veld invult.

   * Schakel indien nodig de optie **[!UICONTROL Make form field mandatory]** in. In dat geval kan de landingspagina alleen worden verzonden als de gebruiker dit veld heeft ingevuld. Als een verplicht veld niet is ingevuld, wordt een foutbericht weergegeven wanneer de gebruiker de pagina verzendt.

   ![](assets/lp_designer-form-text-field.png)

1. Nadat u alle gewenste selectievakjes en/of tekstvelden hebt toegevoegd, klikt u op **[!UICONTROL Call to action]** om de bijbehorende sectie uit te vouwen. Hiermee kunt u het gedrag van de knop in de component **[!UICONTROL Form]** definiëren.

   ![](assets/lp_designer-form-call-to-action.png)

1. Bepaal wat er gebeurt wanneer u op de knop klikt:

   * **[!UICONTROL Redirect URL]**: voer de URL in van de pagina waarnaar de gebruikers worden omgeleid.
   * **[!UICONTROL Confirmation text]**: typ de bevestigingstekst die wordt weergegeven.
   * **[!UICONTROL Link to a subpage]**: Vorm a [ subpage ](create-lp.md#configure-subpages) en selecteer het van de drop-down lijst die toont.

   ![](assets/lp_designer-form-confirmation-action.png)

1. Definieer wat er gebeurt wanneer op de knop wordt geklikt in het geval een fout optreedt:

   * **[!UICONTROL Redirect URL]**: voer de URL in van de pagina waarnaar de gebruikers worden omgeleid.
   * **[!UICONTROL Error text]**: typ de fouttekst die wordt weergegeven. U kunt voorproef de foutentekst wanneer het bepalen van de [ vormstijlen ](#define-lp-styles).

   * **[!UICONTROL Link to a subpage]**: Vorm a [ subpage ](create-lp.md#configure-subpages) en selecteer het van de drop-down lijst die toont.

   ![](assets/lp_designer-form-error.png)

1. Als u aanvullende updates wilt uitvoeren wanneer u het formulier verzendt, selecteert u **[!UICONTROL Opt in]** of **[!UICONTROL Opt out]** en definieert u of u een abonnementenlijst, het kanaal of alleen het gebruikte e-mailadres wilt bijwerken.

   ![](assets/lp_designer-form-additionnal-update.png)

1. Sparen uw inhoud en klik de pijl naast de paginanaam om terug naar de [ het landen paginaeigenschappen ](create-lp.md#configure-primary-page) te gaan.

   ![](assets/lp_designer-form-save.png)

## Landingspagina-formulierstijlen definiëren {#lp-form-styles}

1. Als u de stijlen van de inhoud van een formuliercomponent wilt wijzigen, schakelt u op elk gewenst moment over naar het tabblad **[!UICONTROL Style]** .

   ![](assets/lp_designer-form-style.png)

1. De sectie **[!UICONTROL Fields]** wordt standaard uitgevouwen en biedt u de mogelijkheid om de weergave van het tekstveld te bewerken, zoals het lettertype van het label en de plaatsaanduiding, de positie van het label, de achtergrondkleur van het veld of de veldrand.

   ![](assets/lp_designer-form-style-fields.png)

1. Vouw de sectie **[!UICONTROL Checkboxes]** uit om de weergave van de selectievakjes en de bijbehorende tekst te definiëren. U kunt bijvoorbeeld de lettertypefamilie of -grootte of de randkleur van het selectievakje aanpassen.

   ![](assets/lp_designer-form-style-checkboxes.png)

1. Vouw de sectie **[!UICONTROL Buttons]** uit om de weergave van de knop in het deelformulier te wijzigen. U kunt bijvoorbeeld het lettertype wijzigen, een rand toevoegen, de labelkleur bewerken op de muisaanwijzer of de uitlijning van de knop aanpassen.

   ![](assets/lp_designer-form-style-buttons.png)

   Met de knop **[!UICONTROL Simulate content]** kunt u een voorbeeld van uw instellingen bekijken, zoals de kleur van knoplabels op de muisaanwijzer. Leer meer over het testen van het landen van pagina&#39;s [ hier ](create-lp.md#test-landing-page).

   <!--![](assets/lp_designer-form-style-buttons-preview.png)-->

1. Vouw de sectie **[!UICONTROL Form layout]** uit om de lay-outinstellingen zoals de achtergrondkleur, opvulling of marge te bewerken.

   ![](assets/lp_designer-form-style-layout.png)

1. Vouw de sectie **[!UICONTROL Form error]** uit om de weergave van het foutbericht aan te passen dat wordt weergegeven als zich een probleem voordoet. Schakel de desbetreffende optie in om een voorbeeld van de fouttekst op het formulier te bekijken.

   ![](assets/lp_designer-form-error-preview.png)

## De context van de primaire pagina gebruiken {#use-primary-page-context}

U kunt contextuele gegevens gebruiken die afkomstig zijn van een andere pagina binnen dezelfde landingspagina.

Bijvoorbeeld, als u checkbox <!-- or the submission of the page--> met a [ abonnementenlijst ](subscription-list.md) op de primaire het landen pagina verbindt, kunt u die abonnementenlijst op &quot;dank u&quot;subpage gebruiken.

Stel dat u twee selectievakjes op de primaire pagina koppelt aan twee verschillende abonnementlijsten. Als een gebruiker zich op een van deze machtigingen abonneert, wilt u bij het verzenden van het formulier een specifiek bericht weergeven, afhankelijk van het selectievakje dat de gebruiker heeft ingeschakeld.

Hiervoor voert u de volgende stappen uit:

1. Koppel op de primaire pagina elk selectievakje van de component **[!UICONTROL Form]** aan de betreffende abonnementenlijst. [Meer informatie](#use-form-component).

   ![](assets/lp_designer-form-luma-newsletter.png)

1. Plaats de muisaanwijzer op de subpagina waar u de tekst wilt invoegen en selecteer **[!UICONTROL Add personalization]** in de contextafhankelijke werkbalk.

   ![](assets/lp_designer-form-subpage-perso.png)

1. Selecteer in het **[!UICONTROL Edit personalization]** -venster **[!UICONTROL Contextual attributes]** > **[!UICONTROL Landing Pages]** > **[!UICONTROL Primary Page Context]** > **[!UICONTROL Subscription]** .

1. Alle abonnementenlijsten die u op de primaire pagina hebt geselecteerd, worden weergegeven. Selecteer de relevante items met het pictogram +.

   ![](assets/lp_designer-form-add-subscription.png)

1. Voeg de relevante voorwaarden toe gebruikend de hulpfuncties van de verpersoonlijkingsredacteur. [Meer informatie](../personalization/functions/functions.md)

   ![](assets/lp_designer-form-add-subscription-condition.png)

   >[!CAUTION]
   >
   >Als er een speciaal teken in de expressie staat, zoals een afbreekstreepje, moet u de tekst weglaten, inclusief het afbreekstreepje.

1. Sla uw wijzigingen op.

Nu wanneer gebruikers een van de selectievakjes selecteren,

![](assets/lp_designer-form-preview-checked-box.png)

het bericht dat overeenkomt met het geselecteerde selectievakje wordt weergegeven bij het verzenden van het formulier.

![](assets/lp_designer-form-thankyou-preview.png)

<!--![](assets/lp_designer-form-subscription-preview.png)-->

>[!NOTE]
>
>Als een gebruiker de twee selectievakjes selecteert, worden beide teksten weergegeven.

<!--
## Use landing page additional data {#use-additional-data}

When [configuring the primary page](create-lp.md#configure-primary-page), you can create additional data to enable storing information when the landing page is being submitted.

>[!NOTE]
>
>This data may not be visible to users who visit the page.

If you defined one or more keys with their corresponding values when [configuring the primary page](create-lp.md#configure-primary-page), you can leverage these keys in the content of your primary page and subpages using the [personalization editor](../personalization/personalization-build-expressions.md).

///When you reuse the same text on a page, this enables you to dynamically change that text if needed, without going through each occurrence.

For example, if you define the company name as a key, you can quickly update it everywhere (on all the pages of a given landing page) by changing it only once in the [primary page settings](create-lp.md#configure-primary-page).///

To leverage these keys in a landing page, follow the steps below:

1. When configuring the primary page, define a key and its corresponding value in the **[!UICONTROL Additional data]** section. [Learn more](create-lp.md#configure-primary-page)

    ![](assets/lp_create-lp-additional-data.png)

1. When editing your primary page with the designer, place the pointer of your mouse where you want to insert your key and select **[!UICONTROL Add personalization]** from the contextual toolbar.

    ![](assets/lp_designer-context-add-perso.png)

1. In the **[!UICONTROL Edit Personalization]** window, select **[!UICONTROL Contextual attributes]** > **[!UICONTROL Landing Pages]** > **[!UICONTROL Additional Context]**.

    ![](assets/lp_designer-contextual-attributes.png)

1. All the keys that you created when configuring the primary page are listed. Select the key of your choice using the + icon.

    ![](assets/lp_designer-context-select-key.png)

1. Save your changes and repeat the steps above as many times as needed.

    ![](assets/lp_designer-context-keys-inserted.png)

    You can see that the personalization item corresponding to your key is now displayed everywhere you inserted it.
-->