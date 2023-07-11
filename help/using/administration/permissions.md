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
source-git-commit: 6a81760170e53ed9c34142f3b0b367bd62c3464c
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 2%

---

# Gebruikers en rollen beheren {#manage-permissions}

>[!IMPORTANT]
>
> Elk van de onderstaande procedures kan alleen worden uitgevoerd door een **[!UICONTROL Product]** of **[!UICONTROL System]** beheerder. Raadpleeg voor meer informatie hierover de [Documentatie beheerconsole](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Roles]** verwijzen naar een verzameling gebruikers die dezelfde machtigingen en sandboxen delen. Deze rollen staan u toe om toegang en toestemmingen voor verschillende groepen gebruikers binnen uw organisatie gemakkelijk te beheren.

Met de [!DNL Journey Optimizer] product, kunt u kiezen uit een reeks van reeds bestaande **[!UICONTROL Roles]**, elk met verschillende machtigingsniveaus, om toe te wijzen aan uw gebruikers. Voor meer informatie over de beschikbare **[!UICONTROL Roles]**, verwijzen naar [page](ootb-product-profiles.md).

Wanneer een gebruiker tot een **[!UICONTROL Role]**, krijgen zij toegang tot de Adobe-apps en -services in het product.

Als de reeds bestaande rollen niet aan de specifieke behoeften van uw organisatie voldoen, kunt u douane ook tot stand brengen **[!UICONTROL Roles]** om de toegang tot bepaalde functies of objecten in de interface te verfijnen. Op deze manier kunt u ervoor zorgen dat elke gebruiker alleen toegang heeft tot de bronnen en gereedschappen die nodig zijn om zijn taken efficiënt uit te voeren.

## Rollen toewijzen {#assigning-role}

U kunt ervoor kiezen een uit-de-doos of een douane toe te wijzen **[!UICONTROL Role]** aan uw gebruikers.

De lijst van elke uit-van-de-doos rollen met toegewezen toestemmingen kan in worden gevonden [Ingebouwde rollen](ootb-product-profiles.md) sectie.

Om een **[!UICONTROL Role]**:

1. Om een rol aan een gebruiker in toe te wijzen [!DNL Permissions] product, navigeer naar de **[!UICONTROL Roles]** en selecteert u de gewenste rol.

   ![](assets/do-not-localize/access_control_2.png)

1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Typ de naam of het e-mailadres van uw gebruiker of selecteer de gebruiker in de lijst en klik op **[!UICONTROL Save]**.

   Als de gebruiker niet eerder in [!DNL Admin Console], verwijst u naar de [Gebruikersdocumentatie toevoegen](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

De gebruiker ontvangt vervolgens een e-mail met een doorverwijzing naar uw -instantie.

Raadpleeg voor meer informatie over gebruikersbeheer de [Documentatie Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Wanneer de gebruiker tot de instantie toegang heeft, zal uw gebruiker een specifieke mening afhankelijk van de toegewezen toestemmingen in zien **[!UICONTROL Role]**. Als de gebruiker niet de juiste toegang tot een eigenschap heeft, zal het volgende bericht verschijnen:

`You don't have permission to access this feature. Permission needed: XX.`

## Een bestaande rol bewerken {#edit-product-profile}

Voor uitpakken of aanpassen **[!UICONTROL Roles]** kunt u op elk gewenst moment besluiten machtigingen toe te voegen of te verwijderen.

In dit voorbeeld willen we toevoegen **[!UICONTROL Permissions]** in verband met de **[!UICONTROL Journeys]** bron voor gebruikers die zijn toegewezen aan de Journey-viewer **[!UICONTROL Role]**. De gebruikers kunnen dan reizen publiceren.

Let op: als u een uit-van-de-doos of aangepast **[!UICONTROL Role]**, heeft dit gevolgen voor elke gebruiker die aan deze **[!UICONTROL Role]**.

1. Om een rol aan een gebruiker in toe te wijzen [!DNL Permissions] product, navigeer naar de **[!UICONTROL Roles]** en selecteer de gewenste rol, hier in de Journey-viewer **[!UICONTROL Role]**.
   ![](assets/do-not-localize/access_control_5.png)

1. Van uw **[!UICONTROL Role]** dashboard, klik **[!UICONTROL Edit]**.

   ![](assets/do-not-localize/access_control_6.png)

1. De **[!UICONTROL Resources]** wordt de lijst met bronnen weergegeven die van toepassing zijn op de **[!UICONTROL Experience Cloud - Platform powered applications]** product. Sleep bronnen om machtigingen toe te wijzen.

   Van de **[!UICONTROL Journeys]** bron drop-down, kiezen wij hier de Publish reis **[!UICONTROL Permission]**.

   ![](assets/do-not-localize/access_control_14.png)

1. Indien nodig, onder **[!UICONTROL Included Permission Items]** klikt u op het X-pictogram naast het verwijderen van machtigingen of bronnen voor uw rol.

1. Klik op **[!UICONTROL Save]** als u klaar bent.

Indien nodig kunt u ook een nieuwe rol maken met specifieke machtigingen. Raadpleeg voor meer informatie hierover [Een nieuwe rol maken](#create-product-profile).

## Een nieuwe rol maken {#create-product-profile}

[!DNL Journey Optimizer] staat u toe om uw te creëren **[!UICONTROL Roles]** en wijs een reeks toestemmingen en zandbakken aan uw gebruikers toe. Met **[!UICONTROL Roles]** kunt u toegang tot bepaalde functies of objecten in de interface toestaan of weigeren.

Voor meer informatie over het maken en beheren van sandboxen raadpleegt u [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html){target="_blank"}.

In dit voorbeeld maken we een rol met de naam **Reizen, alleen-lezen** waar wij read-only rechten op de eigenschap van de Reis zullen verlenen. Gebruikers kunnen alleen reizen openen en bekijken en hebben geen toegang tot andere functies, zoals **[!DNL  Decision management]** in [!DNL Journey Optimizer].

Als u onze **Reizen, alleen-lezen** **[!UICONTROL Role]**:

1. Om een rol aan een gebruiker in toe te wijzen [!DNL Permissions] product, navigeer naar de **[!UICONTROL Roles]** en klik op **[!UICONTROL Create role]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Voeg een **[!UICONTROL Name]** en **[!UICONTROL Description]** voor uw nieuwe **[!UICONTROL Role]**. Klik vervolgens op **[!UICONTROL Confirm]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Van de **[!UICONTROL Sandbox]** bron drop-down, kies welke zandbak(en) aan uw **[!UICONTROL Role]**. [Meer informatie over sandboxen](sandboxes.md).

   ![](assets/do-not-localize/access_control_13.png)

1. Selecteren tussen verschillende bronnen, zoals **[!DNL Journeys]**, **[!DNL Segments]** of **[!DNL Decision management]** beschikbaar in [!DNL Journey Optimizer] in het linkermenu.

   Hier selecteren we de **[!UICONTROL Journeys]** resource.

   ![](assets/do-not-localize/access_control_11.png)

1. Van de **[!UICONTROL Journeys]** drop-down, selecteer de toestemmingen aan uw toe te wijzen **[!UICONTROL Role]**.

   Hier selecteren we **[!DNL View journeys]**, **[!DNL View journeys report]**  en **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Klik op **[!UICONTROL Save]** als u klaar bent.

Uw **[!UICONTROL Role]** wordt nu gecreeerd en gevormd. U moet deze nu aan gebruikers toewijzen.

Raadpleeg voor meer informatie over het maken en beheren van rollen de [Documentatie Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=en).
