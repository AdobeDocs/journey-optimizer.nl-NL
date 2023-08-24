---
solution: Journey Optimizer
product: journey optimizer
title: Websubdomeinen configureren
description: Leer hoe u websubdomeinen instelt met Journey Optimizer
role: Admin
level: Intermediate
keywords: web, subdomeinen, configuratie
exl-id: 6503d9e6-6c6c-4a6d-ad3d-1d81eb3b4698
source-git-commit: 39953bb09a699ed4fd07db26a3f2e54f4e2cacd7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Websubdomeinen configureren {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Een websubdomein delegeren"
>abstract="U stelt het subdomein in voor gebruik met een webkanaal. Maak een keuze uit de subdomeinen die al zijn gedelegeerd aan de Adobe."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Een websubdomein delegeren"
>abstract="Als u inhoud van de Adobe Experience Manager Assets Essentials toevoegt aan uw webervaringen, moet u het subdomein instellen dat wordt gebruikt om deze inhoud te publiceren. Selecteer een van de subdomeinen die al zijn gedelegeerd aan de Adobe."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Een websubdomein instellen"
>abstract="Selecteer een subdomein in de lijst met subdomeinen die zijn gedelegeerd aan de Adobe. U kunt dit websubdomein instellen als het standaardsubdomein, maar er kan slechts één standaardsubdomein tegelijk worden gebruikt."

Als u tijdens het ontwerpen van een webversie inhoud toevoegt die afkomstig is van de [Adobe Experience Manager Assets Essentials](../content-management/assets-essentials.md) moet u het subdomein instellen dat wordt gebruikt om deze inhoud te publiceren.

Hiervoor moet u kiezen uit de lijst met subdomeinen die al zijn gedelegeerd aan de Adobe. Meer informatie over het delegeren van subdomeinen naar Adobe in [deze sectie](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>De subdomeinconfiguratie van het Web is gemeenschappelijk voor alle milieu&#39;s. Daarom geldt het volgende:
>
>* Als u websubdomeinen wilt openen en bewerken, moet u beschikken over **[!UICONTROL Manage Web Subdomains]** toestemming voor de productiesandbox.
>
> * Elke wijziging aan een websubdomein heeft ook invloed op de productiesandboxen.

U kunt meerdere subdomeinen voor het web maken, maar alleen de subdomeinen **default** subdomein wordt gebruikt. U kunt het standaardwebsubdomein wijzigen, maar u kunt slechts één subdomein tegelijk gebruiken.

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** menu, selecteert u vervolgens **[!UICONTROL Web configuration]** > **[!UICONTROL Web subdomains]**.

   ![](assets/web-access-subdomains.png)

1. Klik op **[!UICONTROL Set up subdomain]**.

1. Selecteer een gedelegeerd subdomein in de lijst.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >U kunt geen subdomein selecteren dat al als websubdomein wordt gebruikt.

1. Het voorvoegsel dat wordt weergegeven in de URL wordt automatisch toegevoegd. U kunt dit niet wijzigen.

1. Als u dit subdomein als standaard wilt instellen, selecteert u de bijbehorende optie.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >Alleen de **default** subdomein wordt gebruikt.

1. Klik op **[!UICONTROL Submit]**. Het subdomein krijgt de **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt voor uw webervaringen.

   >[!NOTE]
   >
   >In zeer zeldzame gevallen, kon een subdomain opstelling ontbreken. In dit geval kunt u de opdracht **[!UICONTROL Failed]** subdomein om de lijst op te schonen met de opdracht **[!UICONTROL Delete]** van de knop **[!UICONTROL More actions]** pictogram.

1. De **[!UICONTROL Default]** badge wordt weergegeven naast het subdomein dat momenteel als standaard wordt gebruikt. Als u het standaardsubdomein wilt wijzigen, selecteert u **[!UICONTROL Set as default]** van de **[!UICONTROL More actions]** naast het gewenste subdomein.

   ![](assets/web-subdomain-default.png)

   >[!NOTE]
   >
   >U kunt het standaardwebsubdomein wijzigen, maar u kunt slechts één subdomein tegelijk gebruiken.

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.

    You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->
