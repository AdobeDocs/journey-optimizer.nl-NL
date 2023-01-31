---
solution: Journey Optimizer
product: journey optimizer
title: Inhoudssjablonen maken
description: Leer hoe u sjablonen maakt om inhoud te hergebruiken in Journey Optimizer-campagnes en -reizen
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 1%

---

# Inhoudssjablonen maken {#content-templates}

>[!CONTEXTUALHELP]
>id="ajo_content_templates"
>title="Inhoudssjablonen maken"
>abstract="Zelfstandige sjablonen maken om inhoud te hergebruiken voor reizen en campagnes."

Voor een geavanceerd en verbeterd ontwerpproces kunt u zelfstandige sjablonen maken om aangepaste inhoud eenvoudig te hergebruiken in [!DNL Journey Optimizer] campagnes en reizen.

Met deze functionaliteit kunnen gebruikers die op inhoud zijn gericht, aan sjablonen werken buiten campagnes of reizen. Marketing-gebruikers kunnen deze zelfstandige inhoudssjablonen vervolgens hergebruiken en aanpassen binnen hun eigen reizen of campagnes.

>[!CAUTION]
>
>Als u inhoudssjablonen wilt maken, bewerken en verwijderen, moet u beschikken over de **[!DNL Manage Library Items]** bevoegdheid opgenomen in de **[!DNL Content Library Manager]** productprofiel. [Meer informatie](../administration/ootb-product-profiles.md#content-library-manager)

Een gebruiker in uw bedrijf is bijvoorbeeld alleen verantwoordelijk voor inhoud en heeft daarom geen toegang tot campagnes of reizen. Deze gebruiker kan echter een e-mailsjabloon maken die de marketers van uw organisatie kunnen selecteren voor gebruik in alle e-mails als startpunt.

>[!NOTE]
>
>* Wijzigingen in inhoudssjablonen worden niet doorgegeven aan campagnes of reizen, of het nu live of conceptueel gaat.
>
>* En als sjablonen worden gebruikt in een campagne of een reis, hebben alle bewerkingen die u aanbrengt in uw campagne en inhoud van de reis geen invloed op de eerder gebruikte inhoudssjabloon.


➡️ [Leer hoe u in deze video sjablonen maakt en gebruikt](#video-templates)

Voer de onderstaande stappen uit om een inhoudssjabloon te maken.

1. Selecteer **[!UICONTROL Content Management]** > **[!UICONTROL Content Templates]** in het linkermenu.

   ![](assets/content-template-list.png)

1. Alle sjablonen die op de huidige sandbox zijn gemaakt - van een reis, een campagne of de **[!UICONTROL Content Templates]** menu - worden weergegeven.

   >[!NOTE]
   >
   >U kunt inhoudssjablonen sorteren op aanmaak- of wijzigingsdatum.

1. Selecteer **[!UICONTROL Create template]**.

1. Vul de sjabloondetails in.

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >Alleen de **E-mail** kanaal en **HTML** type worden ondersteund.

1. Selecteer **[!UICONTROL Manage access]**. [Leer meer op de Controle van de Toegang van het Niveau van Objecten (OLAC)](../administration/object-based-access.md).

1. Klikken **[!UICONTROL Create]** en kies hoe u uw e-mail van de volgende opties wilt ontwerpen:

   * **[!UICONTROL Design from scratch]**
   * **[!UICONTROL Code your own]**
   * **[!UICONTROL Import HTML]**
   * **[!UICONTROL Select design template]**

   ![](assets/content-template-design.png)

   >[!NOTE]
   >
   >Als u een sjabloon selecteert, kunt u kiezen tussen **[!UICONTROL Sample templates]**, die e-mailsjablonen zijn die buiten de box vallen, en **[!UICONTROL Saved templates]**, die ontstaan zijn door een reis, een campagne of **[!UICONTROL Content Templates]** -menu. [Meer informatie](email-templates.md#save-as-template)

1. In het dialoogvenster E-mailontwerper wordt weergegeven. Bewerk uw inhoud naar wens, net zoals u doet voor elke e-mail binnen een rit of campagne, afhankelijk van de optie die u hebt geselecteerd:

   * [Ontwerp uw e-mail helemaal zelf](content-from-scratch.md) via de interface van de ontwerper en met behulp van afbeeldingen [Adobe Experience Manager Assets Essentials](assets-essentials.md).

   * [Code of copy-paste onbewerkte HTML](code-content.md) rechtstreeks in de e-mailontwerper.

   * [Bestaande HTML-inhoud importeren](existing-content.md) uit een bestand of een ZIP-map.

   * [Bestaande inhoud gebruiken](email-templates.md) uit een lijst met ingebouwde of aangepaste sjablonen.

   ![](assets/content-template-designer.png)

1. Klikken **[!UICONTROL Simulate Content]** om de rendering van uw e-mail te controleren. U kunt kiezen voor de weergave Computer of Mobiel. [Meer informatie](preview.md)

   >[!CAUTION]
   >
   >Om inhoud te simuleren, moet u hebben **[!DNL Manage Simulate Content]** bevoegdheid opgenomen in de **[!DNL Content Library Manager]** productprofiel. [Meer informatie](../administration/ootb-product-profiles.md#content-library-manager)

   ![](assets/content-template-stimulate.png)

1. U kunt een bewijs verzenden om uw inhoud te testen en het door sommige interne gebruikers te laten goedkeuren alvorens het in een reis of een campagne te gebruiken.

   * Klik hiertoe op de knop **[!UICONTROL Send proof]** en voert u de in [deze sectie](preview.md#send-proofs).

   * Voordat u de proefdruk verzendt, moet u de optie [e-mailoppervlak](../configuration/channel-surfaces.md) die wordt gebruikt om uw inhoud te testen.

      ![](assets/content-template-stimulate-proof-surface.png)

1. Als de sjabloon gereed is, klikt u op **[!UICONTROL Save]**.

1. Klik zo nodig op de pijl naast de sjabloonnaam om terug te gaan naar de **[!UICONTROL Details]** het scherm en geeft uw malplaatje uit.

   ![](assets/content-template-designer-back.png)

1. U kunt deze inhoudssjabloon nu gebruiken wanneer u een [email](get-started-email-design.md) binnen [!DNL Journey Optimizer]. Meer informatie over [een opgeslagen sjabloon gebruiken](email-templates.md#use-saved-template).

   ![](assets/email_designer-saved-templates.png)

## Hoe kan ik-video{#video-templates}

Leer hoe u inhoudssjablonen kunt maken, bewerken en gebruiken in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)