---
solution: Journey Optimizer
product: journey optimizer
title: Gebruikers en rollen beheren
description: Leer hoe u gebruikers en rollen beheert
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: product, profielen, sandbox
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 1%

---

# Gebruikers en rollen beheren {#manage-permissions}

>[!IMPORTANT]
>
> Elke hieronder beschreven procedure kan alleen worden uitgevoerd door een **[!UICONTROL Product]** - of **[!UICONTROL System]** -beheerder.

**[!UICONTROL Roles]** verwijst naar een verzameling gebruikers die dezelfde machtigingen en sandboxen delen. Deze rollen staan u toe om toegang en toestemmingen voor verschillende groepen gebruikers binnen uw organisatie gemakkelijk te beheren.

Met het [!DNL Journey Optimizer] -product kunt u kiezen uit een bereik van vooraf bestaande **[!UICONTROL Roles]** , elk met verschillende machtigingsniveaus, om toe te wijzen aan uw gebruikers. Voor meer informatie over beschikbare **[!UICONTROL Roles]**, verwijs naar deze [ pagina ](ootb-product-profiles.md).

Wanneer een gebruiker tot een **[!UICONTROL Role]** behoort, krijgt hij of zij toegang tot de Adobe-apps en -services in het product.

Als de reeds bestaande rollen niet aan de specifieke behoeften van uw organisatie voldoen, kunt u douane **[!UICONTROL Roles]** ook tot stand brengen om toegang tot bepaalde functionaliteit of voorwerpen in de interface te verfijnen. Op deze manier kunt u ervoor zorgen dat elke gebruiker alleen toegang heeft tot de bronnen en gereedschappen die nodig zijn om zijn taken efficiënt uit te voeren.

## Rollen toewijzen {#assigning-role}

U kunt desgewenst een uitwendige of aangepaste **[!UICONTROL Role]** aan uw gebruikers toewijzen.

De lijst van elke uit-van-de-doos rollen met toegewezen toestemmingen kan in de [ ingebouwde rollen ](ootb-product-profiles.md) sectie worden gevonden.

Een **[!UICONTROL Role]** toewijzen:

1. Als u een rol wilt toewijzen aan een gebruiker in het [!DNL Permissions] -product, navigeert u naar het tabblad **[!UICONTROL Roles]** en selecteert u de gewenste rol.

   ![](assets/do-not-localize/access_control_2.png)

1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Typ de naam of het e-mailadres van de gebruiker of selecteer de gebruiker in de lijst en klik op **[!UICONTROL Save]** .

   Als de gebruiker niet eerder in [!DNL Admin Console] werd gecreeerd, verwijs naar [ gebruikersdocumentatie ](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/users.html) toevoegen.

   ![](assets/do-not-localize/access_control_4.png)

Uw gebruiker moet dan een e-mail ontvangen die aan uw instantie opnieuw richt.

Voor meer informatie over gebruikersbeheer, verwijs naar de [ documentatie van het Toegangsbeheer ](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html).

Wanneer u de instantie opent, ziet uw gebruiker een specifieke weergave, afhankelijk van de toegewezen machtigingen in de **[!UICONTROL Role]** . Als de gebruiker niet de juiste toegang tot een eigenschap heeft, zal het volgende bericht verschijnen:

`You don't have permission to access this feature. Permission needed: XX.`

## Een bestaande rol bewerken {#edit-product-profile}

Voor instructies die niet in de doos of op maat **[!UICONTROL Roles]** zijn, kunt u op elk moment beslissen om machtigingen toe te voegen of te verwijderen.

In dit voorbeeld willen we **[!UICONTROL Permissions]** toevoegen met betrekking tot de **[!UICONTROL Journeys]** -bron voor gebruikers die zijn toegewezen aan de Journey-viewer **[!UICONTROL Role]** . De gebruikers kunnen dan reizen publiceren.

Houd er rekening mee dat als u een uit-de-box of aangepaste **[!UICONTROL Role]** aanpast, dit gevolgen heeft voor elke gebruiker die aan deze **[!UICONTROL Role]** is toegewezen.

1. Als u een rol wilt toewijzen aan een gebruiker in het [!DNL Permissions] -product, navigeert u naar het tabblad **[!UICONTROL Roles]** en selecteert u de gewenste rol, hier in de Journey-viewer **[!UICONTROL Role]** .
   ![](assets/do-not-localize/access_control_5.png)

1. Klik op het dashboard van **[!UICONTROL Role]** **[!UICONTROL Edit]** .

   ![](assets/do-not-localize/access_control_6.png)

1. In het menu **[!UICONTROL Resources]** wordt de lijst met bronnen weergegeven die van toepassing zijn op het **[!UICONTROL Experience Cloud - Platform powered applications]** -product. Sleep bronnen om machtigingen toe te wijzen.

   In de vervolgkeuzelijst met **[!UICONTROL Journeys]** bronnen kiezen we hier de publicatietraject **[!UICONTROL Permission]** .

   ![](assets/do-not-localize/access_control_14.png)

1. Klik, indien nodig, onder **[!UICONTROL Included Permission Items]** op het X-pictogram naast het verwijderen van machtigingen of bronnen voor uw rol.

1. Klik op **[!UICONTROL Save]** als u klaar bent.

Indien nodig kunt u ook een nieuwe rol maken met specifieke machtigingen. Voor meer op dit, verwijs naar [ creeer een nieuwe rol ](#create-product-profile).

## Een nieuwe rol maken {#create-product-profile}

Met [!DNL Journey Optimizer] kunt u uw eigen **[!UICONTROL Roles]** maken en een set machtigingen en sandboxen aan uw gebruikers toewijzen. Met **[!UICONTROL Roles]** kunt u toegang tot bepaalde functies of objecten in de interface autoriseren of weigeren.

Voor meer informatie over om zandbakken tot stand te brengen en te beheren, verwijs naar [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html){target="_blank"} .

In dit voorbeeld, zullen wij een rol tot stand brengen genoemd **Reis read-only** waar wij read-only rechten op de eigenschap van de Reis zullen verlenen. Gebruikers kunnen alleen reizen openen en bekijken en hebben geen toegang tot andere functies, zoals **[!DNL &#x200B; Decision management]** in [!DNL Journey Optimizer] .

Om onze **Reizen read-only** **[!UICONTROL Role]** te creëren:

1. Als u een rol wilt toewijzen aan een gebruiker in het [!DNL Permissions] -product, navigeert u naar de tab **[!UICONTROL Roles]** en klikt u op **[!UICONTROL Create role]** .

   ![](assets/do-not-localize/access_control_9.png)

1. Voeg een **[!UICONTROL Name]** en **[!UICONTROL Description]** voor uw nieuwe **[!UICONTROL Role]** toe. Klik vervolgens op **[!UICONTROL Confirm]** .

   ![](assets/do-not-localize/access_control_10.png)

1. Kies in de vervolgkeuzelijst met bronnen van **[!UICONTROL Sandbox]** welke sandbox(s) u wilt toewijzen aan uw **[!UICONTROL Role]** . [ leer meer over zandbakken ](sandboxes.md).

   ![](assets/do-not-localize/access_control_13.png)

1. Selecteer een van de verschillende bronnen, zoals **[!DNL Journeys]** , **[!DNL Segments]** of **[!DNL Decision management]** , die beschikbaar zijn in [!DNL Journey Optimizer] .

   Hier selecteren we de **[!UICONTROL Journeys]** -bron.

   ![](assets/do-not-localize/access_control_11.png)

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Journeys]** de machtigingen die u wilt toewijzen aan uw **[!UICONTROL Role]** .

   Hier selecteren we **[!DNL View journeys]** , **[!DNL View journeys report]** en **[!DNL View journeys event, data sources, actions]** .

   ![](assets/do-not-localize/access_control_12.png)

1. Klik op **[!UICONTROL Save]** als u klaar bent.

Uw **[!UICONTROL Role]** wordt nu gecreeerd en gevormd. U moet deze nu aan gebruikers toewijzen.

Voor meer informatie over rolverwezenlijking en beheer, verwijs naar de [ documentatie van Admin Console ](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html).
