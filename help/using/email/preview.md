---
solution: Journey Optimizer
product: journey optimizer
title: Berichten voorvertonen en proefdrukken verzenden
description: Leer hoe u berichten kunt bekijken en testen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: f2c2a360-a4b2-4416-bbd0-e27dd014e4ac
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 1%

---

# Berichten voorvertonen en testen {#preview-and-proof}

Nadat u de e-mailinhoud hebt gedefinieerd, kunt u testprofielen gebruiken om deze voor te vertonen en te testen. Als u [persoonlijke inhoud](../personalization/personalize.md)kunt u met testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

Om mogelijke fouten in e-mailinhoud of verpersoonlijkingsmontages te ontdekken, verzend proefdrukken naar testprofielen. Telkens wanneer een wijziging wordt aangebracht, moet een bewijs worden verzonden om de meest recente inhoud te valideren.

>[!CAUTION]
>
>U hebt testprofielen nodig om uw berichten te kunnen bekijken en proefdrukken te kunnen verzenden.
>
>Leer hoe u testprofielen maakt in [deze pagina](../segment/creating-test-profiles.md).

Als u uw e-mailinhoud wilt testen, moet u:

* [Testprofielen selecteren](#select-test-profiles)
* [De voorvertoning van het bericht controleren](#preview-your-messages)

Dan kunt u [proefdrukken verzenden](#send-proofs) naar uw testprofielen.

Bovendien kunt u uw **Litmus** account [!DNL Journey Optimizer] om direct een voorvertoning van uw **e-mailrendering** in populaire e-mailclients. U kunt er dan voor zorgen dat uw e-mailinhoud er goed uitziet en goed werkt in elk Postvak IN. Leer hoe u e-mailvoorvertoningen in Lightroom kunt ontgrendelen [deze sectie](#email-rendering).

>[!CAUTION]
>
>Wanneer u een bericht voorvertoont of proefdrukken verzendt, worden alleen profielverpersoonlijkingsgegevens weergegeven. Personalisatie op basis van contextgegevens, zoals gebeurtenisinformatie, kan alleen worden getest in het kader van een reis. Leer hoe u personalisatie kunt testen in [dit geval gebruiken](../personalization/personalization-use-case.md).

➡️ [Leer hoe u uw e-mail in deze video kunt voorvertonen en controleren](#video-preview)

## Testprofielen selecteren {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Berichten voorvertonen en testen"
>abstract="Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/validate/preview.html?lang=en#email-rendering" text="E-mailweergave"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/validate/preview.html?lang=en#preview-your-messages" text="Voorvertoning"

Gebruiken [Testprofielen](../segment/creating-test-profiles.md) om extra ontvangers te richten die niet de bepaalde het richten criteria aanpassen.

Volg onderstaande stappen om testprofielen te selecteren:

1. In de [Inhoud bewerken](create-email.md#define-email-content) of in de e-mailontwerper klikt u op de knop **[!UICONTROL Simulate content]** om de selectie van het testprofiel te openen.

   ![](assets/email-preview-button.png)

1. Selecteer **[!UICONTROL Manage test profiles]**.

   ![](assets/email-preview_manage-test-profiles.png)

1. Selecteer de naamruimte die u wilt gebruiken om testprofielen te identificeren door op de knop **[!UICONTROL Identity namespace]** selectiepictogram.

   ![](assets/previewselect-namespace.png)

   Meer informatie over naamruimten in Adobe Experience Platform [in deze sectie](../segment/get-started-identity.md).

   In het onderstaande voorbeeld gebruiken we de **E-mail** naamruimte.

1. Gebruik het zoekveld om de naamruimte te zoeken, selecteer deze en klik op **[!UICONTROL Select]**

   ![](assets/preview-email-namespace.png)

1. In de **[!UICONTROL Identity value]** -veld, voer de waarde in (hier het e-mailadres) om het testprofiel te identificeren en klik op **[!UICONTROL Add profile]**.

   <!--![](assets/preview-identity-value.png)-->

1. Als u personalisatie aan uw bericht toevoegde, voeg andere profielen toe zodat u verschillende varianten van het bericht afhankelijk van profielgegevens kunt testen. Als profielen eenmaal zijn toegevoegd, worden deze weergegeven onder de geselecteerde velden.

   ![](assets/preview-profile-list.png)

   Gebaseerd op de elementen van de berichtverpersoonlijking, toont deze lijst gegevens voor elk testprofiel in de verwante kolommen.

### E-mailvoorbeeld {#preview-email}

Eenmaal [testprofielen](#select-test-profiles) geselecteerd, kunt u een voorbeeld van uw e-mailinhoud bekijken. Voer de onderstaande stappen uit:

1. In de [Inhoud bewerken](create-email.md#define-email-content) of in de e-mailontwerper klikt u op de knop **[!UICONTROL Simulate content]** knop.

1. Selecteer een testprofiel. U kunt de waarden controleren die beschikbaar zijn in de kolommen. Gebruik de pijl-rechts/pijl-links om door gegevens te bladeren.

   ![](assets/preview-select-profile.png)

   >[!NOTE]
   >
   >Als u meer testprofielen wilt toevoegen, selecteert u **[!UICONTROL Manage test profiles]**. [Meer informatie](#select-test-profiles)

1. Klik op de knop **[!UICONTROL Select data]** boven de lijst om kolommen toe te voegen of te verwijderen.

   ![](assets/preview-select-data.png)

   U kunt de gebieden van de verpersoonlijking voor het huidige bericht aan het eind van de lijst zien. In dit voorbeeld worden stad, voornaam en achternaam van het profiel weergegeven. Selecteer deze velden en zorg ervoor dat deze waarden worden ingevuld in uw testprofielen.

1. In de voorvertoning van het bericht worden gepersonaliseerde elementen vervangen door de geselecteerde gegevens van het testprofiel.

   Voor dit bericht zijn bijvoorbeeld zowel de e-mailinhoud als het onderwerp van de e-mail gepersonaliseerd:

   ![](assets/preview-test-profile.png)

1. Selecteer andere testprofielen voor een voorvertoning van de e-mailrendering voor elke variant van uw bericht.

## Verzend proeven {#send-proofs}

Een proef is een specifiek bericht dat u toestaat om een bericht te testen alvorens het naar het belangrijkste publiek te verzenden. Ontvangers van het bewijs zijn belast met de goedkeuring van het bericht: renderen, inhoud, instellingen voor personalisatie, configuratie.

Eenmaal [testprofielen](#select-test-profiles) zijn geselecteerd, kunt u proefdrukken verzenden.

1. In de **[!UICONTROL Simulate]** scherm, klik **[!UICONTROL Send proof]** knop.

   ![](assets/send-proof-button.png)

1. Van de **[!UICONTROL Send proof]** venster, typt u de e-mail van de ontvanger en klikt u op **[!UICONTROL Add]** om het bewijs naar uzelf of leden van uw organisaties te sturen.

   U kunt maximaal tien ontvangers toevoegen voor de proefaflevering.

   ![](assets/send-proof-add.png)

1. Selecteer vervolgens de **Testprofielen** die wordt gebruikt om de inhoud van het bericht aan te passen.

   Elke ontvanger van de proefdruk ontvangt evenveel berichten als het aantal geselecteerde testprofielen. Als u bijvoorbeeld vijf e-mailberichten voor ontvangers hebt toegevoegd en tien testprofielen hebt geselecteerd, verzendt u vijftig proefdrukberichten en ontvangt elke ontvanger er tien.

1. U kunt desgewenst een voorvoegsel toevoegen aan de onderwerpregel van de proefdruk. Alleen alfanumerieke tekens en speciale tekens zoals . - _ ( ) [ ] zijn toegestaan als voorvoegsel bij de onderwerpregel.

1. Klik op **[!UICONTROL Send proof]**.

   ![](assets/send-proof-select.png)

1. Terug in de  **[!UICONTROL Simulate]** scherm, klik  **[!UICONTROL View proofs]** om de status te controleren.

   ![](assets/send-proof-view.png)

Het wordt aanbevolen om na elke wijziging proefdrukken naar de inhoud van het bericht te verzenden.

>[!NOTE]
>
>In de verzonden proefdruk is de verbinding aan de spiegelpagina niet actief. Deze wordt alleen geactiveerd in de laatste berichten.

## E-mailrendering gebruiken {#email-rendering}

U kunt uw **Litmus** account [!DNL Journey Optimizer] om direct een voorvertoning van uw **e-mailrendering** in populaire e-mailclients.

Voor toegang tot de rendermogelijkheden via e-mail moet u:

* Een Litmus-account hebben
* [Testprofielen selecteren](#select-test-profiles)

Voer vervolgens de onderstaande stappen uit:

1. In de [Inhoud bewerken](create-email.md#define-email-content) of in de e-mailontwerper klikt u op de knop **[!UICONTROL Simulate content]** knop.

1. Selecteer de knop **[!UICONTROL Render email]**.

   ![](assets/email-rendering-button.png)

1. Klikken **Sluit uw Litmus-account aan** in de rechterbovenhoek.

   ![](assets/email-rendering-litmus.png)

1. Voer uw gegevens in en meld u aan.

   ![](assets/email-rendering-credentials.png)

1. Klik op de knop **Test uitvoeren** om e-mailvoorvertoningen te genereren.

1. Controleer uw e-mailinhoud in populaire desktops, mobiele en webclients.

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>Wanneer u verbinding maakt met uw **Litmus** account met [!DNL Journey Optimizer], gaat u ermee akkoord dat testberichten naar Litmus worden verzonden: nadat deze e-mails zijn verzonden , worden deze niet meer beheerd door Adobe . Dientengevolge, is het beleid van de het bewaare-mail van het Litmus- gegevens van toepassing op deze e-mail, met inbegrip van verpersoonlijkingsgegevens die in deze testberichten kunnen worden omvat.

## Hoe kan ik-video {#video-preview}

Leer hoe u het renderen van e-mailberichten in verschillende postvakken kunt testen, hoe u een voorvertoning van uw persoonlijke e-mails kunt weergeven op basis van testprofielen en proefdrukken kunt verzenden.

>[!VIDEO](https://video.tv.adobe.com/v/334239?quality=12)