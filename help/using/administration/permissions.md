---
title: Gebruikers en productprofielen beheren
description: Leer hoe u machtigingen beheert
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Controlegroepen
topic: Beheer
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 11%

---

# Gebruikers en productprofielen beheren {#manage-permissions}

>[!IMPORTANT]
>
> Elk van de hieronder beschreven procedures kan slechts door een **[!UICONTROL Product]** of **[!UICONTROL System]** beheerder worden uitgevoerd. Raadpleeg de documentatie [Admin-console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html) voor meer informatie hierover.

**[!UICONTROL Product profiles]** zijn reeksen gebruikers die de zelfde toestemmingen en zandbakken binnen uw organisatie delen.

Met het [!DNL Journey Optimizer]-product kunt u kiezen tussen verschillende &#39;out-of-the-box&#39; **[!UICONTROL Product profiles]** met verschillende machtigingsniveaus om toe te wijzen aan uw gebruikers. Raadpleeg deze [pagina](ootb-product-profiles.md) voor meer informatie over de beschikbare **[!UICONTROL Product profiles]**.

Elke gebruiker die tot een **[!UICONTROL Product profiles]** behoort, heeft recht op de Adobe-apps en -services in het product.

U kunt ook uw eigen **[!UICONTROL Product profiles]** maken als u de toegang van uw gebruikers tot bepaalde functies of objecten in de interface wilt verfijnen.

## Een productprofiel toewijzen {#assigning-product-profile}

U kunt verkiezen om uit-van-de-doos of douane **[!UICONTROL Product profile]** aan uw gebruikers toe te wijzen.

De lijst van elke uit-van-de-doos productprofielen met toegewezen toestemmingen kan in [Ingebouwde productprofielen](ootb-product-profiles.md) sectie worden gevonden.

Een **[!UICONTROL Product profile]** toewijzen:

1. Selecteer in [!DNL Admin Console] op het tabblad **[!UICONTROL Products]** het product **[!UICONTROL Experience Cloud - Platform powered applications]**.

1. Selecteer een **[!UICONTROL Product profile]**.

   ![](../assets/access_control_2.png)

1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

   ![](../assets/access_control_3.png)

1. Typ de naam of het e-mailadres van uw gebruiker en selecteer de gebruiker.

   Als de gebruiker niet eerder in [!DNL Admin Console] werd gecreeerd, verwijs naar [gebruikersdocumentatie toevoegen](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](../assets/access_control_4.png)

1. Voer dezelfde stappen uit als hierboven om andere gebruikers toe te voegen aan uw **[!UICONTROL Product profile]**. Klik vervolgens op **[!UICONTROL Save]**.

De gebruiker ontvangt vervolgens een e-mail met een doorverwijzing naar uw -instantie.

Raadpleeg de documentatie [Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html) voor meer informatie over gebruikersbeheer.

Wanneer de toegang tot van de instantie, zal uw gebruiker een specifieke mening afhankelijk van de toegewezen toestemmingen in **[!UICONTROL Product profile]** zien. Als de gebruiker niet de juiste toegang tot een eigenschap heeft, zal het volgende scherm verschijnen.

![](../assets/access_control_1.png)

## Een bestaand productprofiel bewerken {#edit-product-profile}

Voor uit-van-de-doos of douane **[!UICONTROL Product profiles]**, kunt u op elk ogenblik besluiten om toestemmingen toe te voegen of te schrappen.

In dit voorbeeld willen we **[!UICONTROL Permissions]** toevoegen met betrekking tot de **[!UICONTROL Message]**-functie voor gebruikers die zijn toegewezen aan de Journey-viewer **[!UICONTROL Product profile]**. De gebruikers zullen dan berichten kunnen publiceren.

Merk op dat als u een uit-van-de-doos of douane **[!UICONTROL Product profile]** wijzigt, het elke gebruiker zal beïnvloeden die aan dit **[!UICONTROL Product profile]** wordt toegewezen.

1. Selecteer in [!DNL Admin Console] op het tabblad **[!UICONTROL Products]** het product **[!UICONTROL Experience Cloud - Platform powered applications]**.

1. Selecteer de Journey-viewer **[!UICONTROL Product profile]**.

1. Selecteer het tabblad **[!UICONTROL Permissions]**. 

   Op het tabblad **[!UICONTROL Permissions]** wordt de lijst met mogelijkheden weergegeven die van toepassing zijn op het **[!UICONTROL Experience Cloud - Platform powered applications]**-product.

   ![](../assets/access_control_5.png)

1. Selecteer de **[!UICONTROL Messages]** mogelijkheid.

   ![](../assets/access_control_6.png)

1. Selecteer in de lijst **[!UICONTROL Available Permission Items]** de machtigingen die u aan uw **[!UICONTROL Product profile]** wilt toewijzen door op de plusknop (+) te klikken.

   Hier, voegen wij **[!UICONTROL Publish messages]** toestemming toe.

   ![](../assets/access_control_7.png)

1. Klik zo nodig onder **[!UICONTROL Included Permission Items]** op het X-pictogram om toestemmingen voor uw productprofiel te verwijderen.

1. Klik op **[!UICONTROL Save]** als u klaar bent.

   ![](../assets/access_control_8.png)

Indien nodig kunt u ook een nieuw productprofiel met specifieke machtigingen maken. Raadpleeg [Een productprofiel maken](#create-product-profile) voor meer informatie.

## Een productprofiel maken {#create-product-profile}

[!DNL Journey Optimizer] kunt u uw eigen machtigingen maken  **[!UICONTROL Product profiles]** en een set machtigingen en sandboxen aan uw gebruikers toewijzen. Met **[!UICONTROL Product profiles]**, kunt u toegang tot bepaalde functionaliteit of voorwerpen in de interface machtigen of ontkennen.

Raadpleeg [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html){target=&quot;_blank&quot;} voor meer informatie over het maken en beheren van sandboxen.

In dit voorbeeld maken we een productprofiel met de naam **Reizen alleen-lezen**, waarbij we alleen-lezen rechten geven aan de functie Reis. Gebruikers kunnen alleen reizen openen en bekijken en hebben geen toegang tot andere functies, zoals **[!UICONTROL Decision management]** of **[!UICONTROL Messages]** in [!DNL Journey Optimizer].

Om onze **Reis read-only** **[!UICONTROL product profiles]** te creëren:

1. Open [!DNL Admin Console].

1. Selecteer op het tabblad **[!UICONTROL Products]** het product **[!UICONTROL Experience Cloud - Platform powered applications]**.

1. Klik op **[!UICONTROL New Profile]**.

   ![](../assets/access_control_9.png)

1. Voeg een **[!UICONTROL Product Profile Name]**, **[!UICONTROL Display Name]** en **[!UICONTROL Description]** voor uw nieuwe **[!UICONTROL product profiles]** toe.

   ![](../assets/access_control_10.png)

1. Kies in de categorie **[!UICONTROL Notifications]** of gebruikers via e-mail op de hoogte worden gesteld wanneer ze aan dit productprofiel worden toegevoegd of eruit worden verwijderd.

1. Wanneer gebeëindigd, klik **[!UICONTROL Save]** en selecteer uw onlangs gecreeerd **[!UICONTROL product profiles]**.

1. Als u machtigingen voor gebruikers wilt toevoegen om toegang te krijgen tot verschillende functies, selecteert u het tabblad **[!UICONTROL Permissions]**.

1. Selecteer tussen de verschillende mogelijkheden zoals **[!UICONTROL Messages]**, **[!UICONTROL Segments]** of **[!UICONTROL Decision management]** beschikbaar in [!DNL Journey Optimizer] vermeld in het linkermenu.

   Hier selecteren we de **[!UICONTROL Journeys]** mogelijkheid.

   ![](../assets/access_control_11.png)

1. Selecteer in de lijst **[!UICONTROL Available Permission Items]** de machtigingen die u aan uw **[!UICONTROL Product profile]** wilt toewijzen door op de plusknop (+) te klikken.

   Hier selecteren we **[!UICONTROL View journeys]** en **[!UICONTROL View journeys event, data sources, actions]**.

   ![](../assets/access_control_12.png)

1. Selecteer de **[!UICONTROL Sandbox access]** mogelijkheid om te kiezen welke zandbak(en) u wilt toewijzen aan uw **[!UICONTROL Product profile]**.

   ![](../assets/access_control_13.png)

1. Klik onder **[!UICONTROL Available Permissions Items]** op het pluspictogram (+) om sandboxen aan uw profiel toe te wijzen. [Meer informatie over sandboxen](sandboxes.md).

1. Klik op **[!UICONTROL Save]** als u klaar bent.

Uw **[!UICONTROL Product profile]** wordt nu gecreeerd en gevormd. U moet deze nu aan gebruikers toewijzen.

Raadpleeg de documentatie [Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html) voor meer informatie over het maken en beheren van productprofielen.
