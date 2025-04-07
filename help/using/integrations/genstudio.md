---
solution: Journey Optimizer
product: journey optimizer
title: Ga aan de slag met de GenStudio-integratie in Journey Optimizer
description: Leren werken met GenStudio in Journey Optimizer
feature: Content Assistant, Integrations
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: c22a44a8-e4e2-453a-9ca2-b80f7c0edc19
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 1%

---

# Aan de slag met de GenStudio-integratie {#gs-genstudio}

>[!CONTEXTUALHELP]
>id="ajo_genstudio_button"
>title="Een sjabloon gebruiken die is gebouwd met GenStudio"
>abstract="Dankzij de naadloze integratie met Adobe GenStudio for Performance Marketing kunt u eenvoudig een GenStudio-sjabloon importeren die is verbeterd met de Adobe AI-technologie."

>[!AVAILABILITY]
>
>De integratie van GenStudio in [!DNL Adobe Journey Optimizer] is momenteel niet beschikbaar voor gebruik met het **Schild van de Gezondheidszorg** of **Privacy en het 4} toe:voegen-op dienstenaanbod van het Schild van de Veiligheid.**
>
>Deze functie is alleen beschikbaar voor het e-mailkanaal.

[ Adobe GenStudio for Performance Marketing ](https://business.adobe.com/products/genstudio-for-performance-marketing.html) {target="_blank"} is een generatieve AI-eerste toepassing die marketing teams hun eigen advertenties en e-mails laat creëren om impactful, gepersonaliseerde marketing campagnes te drijven die aan uw merknormen voldoen en aan uw ondernemingsbeleid voldoet. Door gebruik te maken van Adobe AI-technologie, biedt deze technologie een uitgebreide reeks hulpmiddelen die de complexiteit van het maken en beheren van content vereenvoudigen, zodat creatieve mensen zich kunnen richten op innovatie.

Leer meer over [!DNL GenStudio for Performance Marketing] in de specifieke [ documentatie ](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) {target="_blank"}.

>[!INFO]
>
>Om verder te gaan, controleer dit [ overzicht ](https://business.adobe.com/products/genstudio-for-performance-marketing.html#watch-overview) {target="_blank"} en a [ demo ](https://business.adobe.com/products/genstudio-for-performance-marketing.html#demo) {target="_blank"} van [!DNL Adobe GenStudio for Performance Marketing].

<!--To access the GenStudio integration in [!DNL Adobe Journey Optimizer] feature, users need to be granted the **xxx** permission. [Learn more](../administration/permissions.md)

>[!IMPORTANT]
>
>* Before starting using this capability, read out related [Guardrails and Limitations](#generative-guardrails).-->

Om marketing efficiency te verbeteren en merkconsistentie te handhaven, kunt u [!DNL **GenStudio for Performance Marketing**] ervaringen met [!DNL **Adobe Journey Optimizer**] foutloos integreren. Zo kunt u de AI-kracht van [!DNL GenStudio] gebruiken om inhoud te maken, naast de geavanceerde orchestratiemogelijkheden van [!DNL Journey Optimizer] .

<!--![](../rn/assets/do-not-localize/genstudio.gif)-->

<!--Guardrails and limitations {#genstudio-guardrails}

General guidelines for using the GenStudio integration in [!DNL Adobe Journey Optimizer] for email generation are listed below:

See if guidelines/limitations such as the ones listed [here](gs-generative.md#generative-guardrails) for the AI Assistant can apply.

The following limitations apply to GenStudio integration in [!DNL Adobe Journey Optimizer]:-->

## De GenStudio-mogelijkheden in Journey Optimizer benutten {#use-genstudio}

Dankzij de [!DNL GenStudio for Performance Marketing] - en [!DNL Journey Optimizer] -integratie kunt u marketers van uw bedrijf beter laten samenwerken om processen te stroomlijnen.

Een technische markeerteken, die [!DNL Journey Optimizer] bijvoorbeeld gebruikt om e-mailcampagnes te ontwikkelen en te automatiseren, kan samenwerken met een prestatiemarkering die inhoud maakt met [!DNL GenStudio] .

Met deze integratie kunnen beide toepassingen samenwerken om on-brand-inhoud van [!DNL GenStudio] in [!DNL Journey Optimizer] eenvoudig te integreren, waardoor aantrekkelijke e-mails worden geleverd die gericht zijn op specifieke klantsegmenten en de verkoop stimuleren.

### Een HTML-sjabloon exporteren van Journey Optimizer naar GenStudio {#export-from-ajo-to-genstudio}

Eerst kunt u een [!DNL Journey Optimizer] HTML-sjabloon met instructies van uw merk exporteren naar [!DNL GenStudio for Performance Marketing] . Voer de onderstaande stappen uit.

1. In [!DNL Journey Optimizer] opent u de inhoud van uw e-mail via een reis of campagne. [ leer hoe ](../email/get-started-email-design.md#key-steps)

1. Selecteer in de Designer-mailtoepassing **[!UICONTROL Export HTML]** op de knop **[!UICONTROL More]** .

   ![](assets/genstudio-export-template.png){zoomable="yes"}

1. Upload deze geëxporteerde HTML-sjabloon naar [!DNL GenStudio for Performance Marketing] . <!--Make sure you detect the fields that the generative AI uses to insert content in order to create an actionable template.-->

   >[!NOTE]
   >
   >Leer hoe te om een malplaatje van HTML in [!DNL GenStudio] in de [ Gids van de Gebruiker van Adobe GenStudio for Performance Marketing ](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#templates-from-ajo-and-marketo) te uploaden {target="_blank"} specifieke sectie.

1. In GenStudio gebruikt u deze sjabloon om verschillende e-mailvariaties te maken met AI-herinneringen en deze op te slaan.

   >[!NOTE]
   >
   >Leer hoe te om e-mailervaringen in GenStudio te creëren specifieke [ sectie ](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience) {target="_blank"}.

### GenStudio-ervaringen in Journey Optimizer benutten {#leverage-genstudio-experiences}

Volg onderstaande stappen om de e-mailvariaties die u zojuist hebt gemaakt door deze te importeren in [!DNL Journey Optimizer] , te benutten.[!DNL GenStudio]

1. In [!DNL Journey Optimizer], [ voeg een e-mail ](../email/create-email.md) aan een campagne toe.

1. Van het scherm van de campagneconfiguratie, ga door [ geef inhoudsscherm ](../email/create-email.md#define-email-content) uit en klik **[!UICONTROL Edit email body]** om e-mail Designer te openen. [ leer hoe ](../email/get-started-email-design.md#key-steps)

1. Selecteer **[!UICONTROL Import HTML]** op de startpagina van e-mail Designer en klik op de knop **[!UICONTROL Adobe GenStudio for Performance Marketing]** .

   ![](assets/genstudio-pem-import-email.png){zoomable="yes"}

1. Blader naar de ervaringen van GenStudio om uw inhoud te gaan samenstellen. U kunt de ervaringen filteren op verschillende criteria, zoals producten, personen, merken of zelfs kleuren.

   <!--![](assets/genstudio-filter-experiences.png){zoomable="yes"}-->

1. Selecteer een ervaring en klik op **[!UICONTROL Use]** .

   ![](assets/genstudio-use-experience.png){zoomable="yes"}

1. Selecteer de map waarin u de GenStudio-ervaring wilt importeren.

   ![](assets/genstudio-choose-destination.png){zoomable="yes"}

1. De geselecteerde inhoud wordt weergegeven in de e-mailtoepassing van de Designer.

   ![](assets/genstudio-email-content.png){zoomable="yes"}

   >[!NOTE]
   >
   >De ervaringen van GenStudio [ die van a  [!DNL Journey Optimizer]  worden gecreeerd malplaatje ](#export-from-ajo-to-genstudio) worden direct ingevoerd in E-mailDesigner. De ervaringen van GenStudio die zonder a [!DNL Journey Optimizer] malplaatje worden gecreeerd worden ingevoerd in [ verenigbaarheidswijze ](../email/existing-content.md).

   Gebruik de [ e-mailinhoud het uitgeven hulpmiddelen ](../email/content-from-scratch.md) en [ verpersoonlijkingsgebieden ](../personalization/personalize.md) om uw e-mail uit te geven zoals gewenst. Sla uw inhoud op.

1. Ga terug naar de pagina met het campagneresamenvatting en klik op **[!UICONTROL Create experiment]** om te experimenteren. [ leer hoe te om een inhoudexperiment tot stand te brengen ](../content-management/content-experiment.md)

   <!--![](assets/genstudio-create-experiment.png){zoomable="yes"}-->

1. Maak verschillende behandelingen en herhaal de bovenstaande stappen om te importeren en gebruik snel de andere variaties in de e-mailervaring die u hebt gemaakt in [!DNL GenStudio] .

   ![](assets/genstudio-define-treatments.png){zoomable="yes"}

1. Sparen uw veranderingen en [ activeer ](../campaigns/review-activate-campaign.md) de campagne.

Na het in werking stellen van het experiment, spoor hoe uw campagnebehandelingen met het [ experimentatiecampagnerapport ](../reports/campaign-global-report-cja-experimentation.md) presteren. U kunt dan de resultaten van uw experiment interpreteren. [ leer hoe ](../content-management/get-started-experiment.md#interpret-results)
