---
solution: Journey Optimizer
product: journey optimizer
title: Merk beheren
description: Leer hoe u richtlijnen voor uw merk kunt maken en beheren
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: b1ccacd30acb886e06a3305f0c7046d85f558357
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Uw merken maken en beheren {#brands}

>[!AVAILABILITY]
>
>Dit vermogen wordt vrijgegeven als privé bèta. Het zal in toekomstige versies geleidelijk beschikbaar zijn voor alle klanten.

Merkrichtlijnen zijn een gedetailleerde reeks regels en normen die de visuele en verbale identiteit van een merk bepalen. Zij fungeren als referentie om een consistente merkweergave te behouden op alle marketing- en communicatieplatforms.

In [!DNL Journey Optimizer] hebt u nu de optie om uw merkdetails handmatig in te voeren en in te delen of documenten met brandrichtlijnen te uploaden voor automatische informatie-extractie.

## Toegangsmerken {#generative-access}

Gebruikers die het menu **[!UICONTROL Brands]** in [!DNL Adobe Journey Optimizer] willen openen, moeten de machtigingen **[!UICONTROL Managed brand kit]** of **[!UICONTROL Enable AI assistant]** hebben. [Meer informatie](../administration/permissions.md)

+++  Leer hoe u merkgerelateerde machtigingen kunt toewijzen

1. In het **product van Toestemmingen**, ga naar het **lusje van Rollen** en selecteer de gewenste **Rol**.

1. Klik **uitgeven** om de toestemmingen te wijzigen.

1. Voeg het **AI Medewerker** middel toe, dan uitgezocht **Beheerde merkuitrusting** of **[!UICONTROL Enable Ai assistant]** van het drop-down menu.

   **[!UICONTROL Enable Ai assistant]** biedt alleen alleen alleen-lezen toegang tot het menu Groepen.

   ![](assets/brands-permission.png){zoomable="yes"}

1. Klik **sparen** om veranderingen toe te passen.

   Voor alle gebruikers die al zijn toegewezen aan deze rol, worden hun machtigingen automatisch bijgewerkt.

1. Om deze rol aan nieuwe gebruikers toe te wijzen, navigeer aan het **lusje van Gebruikers** binnen het **dashboard van Rollen** en klik **toevoegen Gebruiker**.

1. Ga de naam van de gebruiker, e-mailadres in, of kies van de lijst, dan klik **sparen**.

1. Als de gebruiker niet eerder werd gecreeerd, verwijs naar [ deze documentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Uw merk maken {#create-brand-kit}

Als u uw merkenrichtlijn wilt maken en beheren, kunt u de details zelf invoeren of het document met uw merkenrichtlijnen uploaden om de informatie automatisch te laten uitnemen:

1. Klik in het menu **[!UICONTROL Brands]** op **[!UICONTROL Create brand]** .

   ![](assets/brands-1.png)

1. Voer een **[!UICONTROL Name]** voor uw merk in <!--and a **[!UICONTROL Description]** to your brand guideline-->.

   ![](assets/brands-2-temp.png)

<!--

[Upload feature currently behind feature flag so hidden from doc - should be available again by EOM (Feb)]

1. Drag and drop or select your file to upload your brand guidelines and extract automatically relevant brand information. Click **[!UICONTROL Create brand]**.

    The information extraction process now begins. Note that it may take several minutes to complete.

    ![](assets/brands-2.png)

1. Your Content and visual creation standards are now automatically populated. Browse through the different tabs to adapt the information as needed.

-->

1. Klik op het tabblad **[!UICONTROL Writing Style]** op ![](assets/do-not-localize/Smock_Add_18_N.svg) om een hulplijn of uitsluiting toe te voegen. U kunt ook voorbeelden toevoegen.

   ![](assets/brands-3.png)

1. Klik op het tabblad **[!UICONTROL Visual content]** op ![](assets/do-not-localize/Smock_Add_18_N.svg) om nog een hulplijn of uitsluiting toe te voegen.

1. Klik op **[!UICONTROL Select image]** om een voorbeeld van een afbeelding toe te voegen. U kunt ook een afbeelding toevoegen waarin onjuist gebruik wordt getoond als uitsluitingsvoorbeeld.

   ![](assets/brands-4.png)

1. Zodra gevormd, klik **[!UICONTROL Save]** toen **[!UICONTROL Publish]** om uw richtlijnen van Merken in de AI medewerker beschikbaar te maken.

1. Klik op **[!UICONTROL Edit brand]** om wijzigingen aan te brengen in uw gepubliceerde merk. Op deze manier wordt een tijdelijke kopie gemaakt in de bewerkingsmodus, waarbij de live versie wordt vervangen nadat deze is gepubliceerd.

   ![](assets/brands-8.png)

1. Open het geavanceerde menu op het dashboard van **[!UICONTROL Brands]** door op het pictogram ![](assets/do-not-localize/Smock_More_18_N.svg) te klikken op:

   * Merk weergeven
   * Bewerken
   * Dupliceren
   * Publiceren
   * Publiceren ongedaan maken
   * Verwijderen

   ![](assets/brands-6.png)

De richtlijnen voor merken zijn nu toegankelijk via de vervolgkeuzelijst Brands in het menu AI-assistent, zodat inhoud en elementen kunnen worden gegenereerd die zijn uitgelijnd op uw specificaties. [ leer meer op de AI medewerker ](gs-generative.md)

![](assets/brands-7.png)
