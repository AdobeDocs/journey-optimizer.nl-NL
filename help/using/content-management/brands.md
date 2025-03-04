---
solution: Journey Optimizer
product: journey optimizer
title: Merk beheren
description: Leer hoe u richtlijnen voor uw merk kunt maken en beheren
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: b1b7abbe-8600-4a8d-b0b5-0dbd49abc275
source-git-commit: 7e354b5235aa6a6378ebc3d13a2c99017064379f
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Uw merken maken en beheren {#brands}

>[!CONTEXTUALHELP]
>id="ajo_brand_overview"
>title="Aan de slag met merken"
>abstract="Creëer en pas uw eigen merken aan om uw unieke visuele en verbale identiteit te bepalen terwijl het gemakkelijker wordt om inhoud te produceren die de stijl en de stem van uw merk aanpast."

>[!CONTEXTUALHELP]
>id="ajo_brand_ai_menu"
>title="Merk selecteren"
>abstract="Kies uw merk om ervoor te zorgen dat alle door AI gegenereerde inhoud is afgestemd op de specificaties en richtlijnen van uw merk."

>[!CONTEXTUALHELP]
>id="ajo_brand_score"
>title="Aanpassingsscore merk"
>abstract="Met uw merkuitlijningsscore wordt gemeten in hoeverre door AI gegenereerde inhoud voldoet aan de richtlijnen van uw merk. Zo bent u verzekerd van consistentie in kleuren, lettertypen, logo, beeldvorming en schrijfstijl."


>[!AVAILABILITY]
>
>Dit vermogen wordt vrijgegeven als privé bèta. Het zal in toekomstige versies geleidelijk beschikbaar zijn voor alle klanten.

Merkrichtlijnen zijn een gedetailleerde reeks regels en normen die de visuele en verbale identiteit van een merk bepalen. Zij fungeren als referentie om een consistente merkweergave te behouden op alle marketing- en communicatieplatforms.

<!--Upload feature currently behind feature flag--

In [!DNL Journey Optimizer], you now have the option to manually input and organize your brand details or upload brand guideline documents for automatic information extraction.-->

## Handelsmerken {#generative-access}

Gebruikers die het menu **[!UICONTROL Brands]** in [!DNL Adobe Journey Optimizer] willen openen, moeten de machtigingen **[!UICONTROL Managed brand kit]** of **[!UICONTROL Enable AI assistant]** hebben. [Meer informatie](../administration/permissions.md)

+++  Leer hoe u merkgerelateerde machtigingen kunt toewijzen

1. In het **product van Toestemmingen**, ga naar het **lusje van Rollen** en selecteer de gewenste **Rol**.

1. Klik **uitgeven** om de toestemmingen te wijzigen.

1. Voeg het **AI Medewerker** middel toe, dan uitgezocht **Beheerde merkuitrusting** of **[!UICONTROL Enable Ai assistant]** van het drop-down menu.

   **[!UICONTROL Enable Ai assistant]** geeft alleen alleen alleen-lezen toegang tot het menu **[!UICONTROL Brands]** .

   ![](assets/brands-permission.png){zoomable="yes"}

1. Klik **sparen** om veranderingen toe te passen.

   Voor alle gebruikers die al zijn toegewezen aan deze rol, worden hun machtigingen automatisch bijgewerkt.

1. Om deze rol aan nieuwe gebruikers toe te wijzen, navigeer aan het **lusje van Gebruikers** binnen het **dashboard van Rollen** en klik **toevoegen Gebruiker**.

1. Ga de naam van de gebruiker, e-mailadres in, of kies van de lijst, dan klik **sparen**.

1. Als de gebruiker niet eerder werd gecreeerd, verwijs naar [ deze documentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Uw merk maken {#create-brand-kit}

>[!CONTEXTUALHELP]
>id="ajo_brands_create"
>title="Uw merk maken"
>abstract="Voer uw merknaam in en upload het bestand met uw merkrichtlijnen. Met dit gereedschap worden automatisch belangrijke details opgehaald, zodat u de identiteit van uw merk eenvoudiger kunt behouden."

Volg onderstaande stappen om uw richtlijnen voor uw merk te maken en te beheren.

<!--Upload feature currently behind feature flag--

To create and manage your Brand guideline, you can either enter the details yourself, or upload your brand guidelines document to have the information extracted automatically:-->

1. Klik in het menu **[!UICONTROL Brands]** op **[!UICONTROL Create brand]** .

   ![](assets/brands-1.png)

1. Voer een **[!UICONTROL Name]** voor uw merk in <!--and a **[!UICONTROL Description]** to your brand guideline-->.

   ![](assets/brands-2-temp.png)

<!--Upload feature currently behind feature flag so hidden from doc - should be available again by EOM (Feb)--

1. Drag and drop or select your file to upload your brand guidelines and extract automatically relevant brand information. Click **[!UICONTROL Create brand]**.

    The information extraction process now begins. Note that it may take several minutes to complete.

    ![](assets/brands-2.png)

1. Your Content and visual creation standards are now automatically populated. Browse through the different tabs to adapt the information as needed.

-->

1. Klik op het tabblad **[!UICONTROL Writing Style]** op ![](assets/do-not-localize/Smock_Add_18_N.svg) om een hulplijn of uitsluiting toe te voegen, inclusief voorbeelden.

   ![](assets/brands-3.png)

1. Klik op het tabblad **[!UICONTROL Visual content]** op ![](assets/do-not-localize/Smock_Add_18_N.svg) om nog een hulplijn of uitsluiting toe te voegen.

1. Als u een afbeelding met het juiste gebruik wilt toevoegen, selecteert u **[!UICONTROL Example]** en klikt u op **[!UICONTROL Select image]** . U kunt ook een afbeelding toevoegen waarin onjuist gebruik wordt getoond als uitsluitingsvoorbeeld.

   ![](assets/brands-4.png)

1. Als u deze hebt geconfigureerd, klikt u op **[!UICONTROL Save]** en vervolgens op **[!UICONTROL Publish]** om uw merkenhulplijn beschikbaar te maken in de AI-assistent.

1. Klik op **[!UICONTROL Edit brand]** om wijzigingen aan te brengen in uw gepubliceerde merk.

   >[!NOTE]
   >
   >Er wordt dan een tijdelijke kopie gemaakt in de bewerkingsmodus, waarbij de live versie wordt vervangen nadat deze is gepubliceerd.

   ![](assets/brands-8.png)

1. Open het geavanceerde menu op het dashboard van **[!UICONTROL Brands]** door op het pictogram ![](assets/do-not-localize/Smock_More_18_N.svg) te klikken op:

   * Merk weergeven
   * Bewerken
   * Dupliceren
   * Publiceren
   * Publiceren ongedaan maken
   * Verwijderen

   ![](assets/brands-6.png)

De richtlijnen voor uw merk zijn nu beschikbaar via de vervolgkeuzelijst **[!UICONTROL Brand]** in het menu AI-assistent, zodat u inhoud en elementen kunt genereren die zijn afgestemd op uw specificaties. [ leer meer op de AI medewerker ](gs-generative.md)

![](assets/brands-7.png)
