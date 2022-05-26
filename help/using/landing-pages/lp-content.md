---
title: Paginaspecifieke inhoud definiëren
description: Leer hoe u landingspagina-specifieke inhoud ontwerpt in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
source-git-commit: f4b3a9de47e724f7b23df8a02b8106c131cf1b12
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 1%

---

# Paginaspecifieke inhoud definiëren {#lp-content}

Als u specifieke inhoud wilt definiëren waarmee gebruikers hun keuzes vanaf de bestemmingspagina kunnen selecteren en verzenden, gebruikt u de optie **[!UICONTROL Form]** component. Hiervoor voert u de volgende stappen uit.

>[!NOTE]
>
>U kunt ook een doorklikingspagina zonder een **[!UICONTROL Form]** component. In dat geval wordt de landingspagina weergegeven aan gebruikers, maar hoeven zij geen formulier in te dienen. Dit kan handig zijn als u alleen een bestemmingspagina wilt weergeven zonder dat u enige actie van uw ontvangers nodig hebt, zoals aanmelden of Weigeren, of als u informatie wilt opgeven waarvoor geen invoer van de gebruiker is vereist.

## De formuliercomponent gebruiken {#use-form-component}

1. De landingspagina-specifiek slepen en neerzetten **[!UICONTROL Form]** van het linkerpalet naar de hoofdwerkruimte.

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >De **[!UICONTROL Form]** kan slechts eenmaal op dezelfde pagina worden gebruikt.

1. Selecteer het. De **[!UICONTROL Form content]** wordt weergegeven in het rechterpalet, zodat u de verschillende velden van het formulier kunt bewerken.

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >Naar de **[!UICONTROL Form style]** kunt u op elk gewenst moment de stijlen van de inhoud van uw formuliercomponent bewerken. [Meer informatie](#define-lp-styles)

1. Van de **[!UICONTROL Checkbox 1]** kunt u het label bewerken dat overeenkomt met dit selectievakje.

1. Bepaal als dit checkbox gebruikers binnen of uit moet kiezen: gaan zij ermee akkoord om mededelingen te ontvangen of vragen zij geen contact meer op te nemen ?

   ![](assets/lp_designer-form-update.png)

   Kies een van de drie onderstaande opties:

   * **[!UICONTROL Opt in if checked]**: gebruikers moeten het selectievakje voor toestemming (opt-in) inschakelen.
   * **[!UICONTROL Opt out if checked]**: gebruikers moeten het selectievakje inschakelen om hun toestemming te verwijderen (opt-out).
   * **[!UICONTROL Opt in if checked, opt out if unchecked]**: Met deze optie kunt u één selectievakje voor opt-in/opt-out invoegen. Gebruikers moeten het selectievakje voor toestemming (opt-in) inschakelen en het selectievakje uitschakelen om hun toestemming (opt-out) te verwijderen.

1. Kies wat tussen de drie volgende opties wordt bijgewerkt:

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Subscription list]**: U moet de abonnementenlijst selecteren die wordt bijgewerkt als het profiel dit selectievakje selecteert. Meer informatie over [abonnementenlijsten](subscription-list.md).

      ![](assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL Channel (email)]**: De opt-in of opt-out geldt voor het gehele kanaal. Als een profiel dat opteert bijvoorbeeld twee e-mailadressen heeft, worden beide adressen uitgesloten van al uw communicatie.

   * **[!UICONTROL Email identity]**: De opt-in of opt-out is alleen van toepassing op het e-mailadres dat is gebruikt voor toegang tot de bestemmingspagina. Als een profiel bijvoorbeeld twee e-mailadressen heeft, ontvangt alleen het profiel dat is gebruikt om u aan te melden, communicatie van uw merk.

1. Klikken **[!UICONTROL Add field]** > **[!UICONTROL Checkbox]** om nog een selectievakje toe te voegen. Herhaal bovenstaande stappen om de eigenschappen ervan te definiëren.

   ![](assets/lp_designer-form-checkbox-2.png)

1. Nadat u alle gewenste selectievakjes hebt toegevoegd, klikt u op **[!UICONTROL Call to action]** om de corresponderende sectie uit te vouwen. Hiermee kunt u het gedrag van de knop in het dialoogvenster **[!UICONTROL Form]** component.

   ![](assets/lp_designer-form-call-to-action.png)

1. Bepaal wat er gebeurt wanneer u op de knop klikt:

   * **[!UICONTROL Redirect URL]**: Voer de URL in van de pagina waarnaar de gebruikers worden omgeleid.
   * **[!UICONTROL Confirmation text]**: Typ de bevestigingstekst die wordt weergegeven.
   * **[!UICONTROL Link to a subpage]**: Een [subpagina](create-lp.md#configure-subpages) en selecteert u deze in de vervolgkeuzelijst die wordt weergegeven.

   ![](assets/lp_designer-form-confirmation-action.png)

1. Definieer wat er gebeurt wanneer op de knop wordt geklikt in het geval een fout optreedt:

   * **[!UICONTROL Redirect URL]**: Voer de URL in van de pagina waarnaar de gebruikers worden omgeleid.
   * **[!UICONTROL Error text]**: Typ de fouttekst die wordt weergegeven. U kunt de fouttekst voorvertonen bij het definiëren van de [formulierstijlen](#define-lp-styles).

   * **[!UICONTROL Link to a subpage]**: Een [subpagina](create-lp.md#configure-subpages) en selecteert u deze in de vervolgkeuzelijst die wordt weergegeven.

   ![](assets/lp_designer-form-error.png)

1. Als u aanvullende updates wilt uitvoeren wanneer u het formulier verzendt, selecteert u **[!UICONTROL Opt in]** of **[!UICONTROL Opt out]** en definieer of u een abonnementenlijst, het kanaal of alleen het gebruikte e-mailadres wilt bijwerken.

   ![](assets/lp_designer-form-additionnal-update.png)

1. Sla de inhoud op en klik op de pijl naast de paginanaam om terug te gaan naar de map [eigenschappen van bestemmingspagina](create-lp.md#configure-primary-page).

   ![](assets/lp_designer-form-save.png)

<!--Will the name Email Designer be kept if you can also design LP with the same tool? > To modify in Messages section > content designer or Designer-->

## Landingspagina-formulierstijlen definiëren {#lp-form-styles}

1. Als u de stijlen van de inhoud van een formuliercomponent wilt wijzigen, schakelt u op elk gewenst moment over naar de **[!UICONTROL Form style]** tab.

   ![](assets/lp_designer-form-style.png)

1. Breid uit **[!UICONTROL Checkboxes]** om de vormgeving van de selectievakjes en de bijbehorende tekst te definiëren. U kunt bijvoorbeeld de lettertypefamilie of -grootte en de randkleur van het selectievakje aanpassen.

   ![](assets/lp_designer-form-style-checkboxes.png)

1. Breid uit **[!UICONTROL Buttons]** om de weergave van de knop in het deelformulier te wijzigen. U kunt bijvoorbeeld een rand toevoegen, de labelkleur bij aanwijzen bewerken of de uitlijning van de knop aanpassen.

   ![](assets/lp_designer-form-style-buttons.png)

   U kunt een voorvertoning van bepaalde instellingen, zoals de kleur van knoplabels op de muisaanwijzer, weergeven met de opdracht **[!UICONTROL Preview]** knop. Meer informatie over het testen van bestemmingspagina&#39;s [hier](create-lp.md#test-landing-page).

   ![](assets/lp_designer-form-style-buttons-preview.png)

1. Breid uit **[!UICONTROL Form layout]** om de layoutinstellingen zoals de achtergrondkleur, opvulling of marge te bewerken.

   ![](assets/lp_designer-form-style-layout.png)

1. Breid uit **[!UICONTROL Form error]** om de weergave aan te passen van het foutbericht dat wordt weergegeven wanneer zich een probleem voordoet. Schakel de desbetreffende optie in om een voorbeeld van de fouttekst op het formulier te bekijken.

   ![](assets/lp_designer-form-error-preview.png)

