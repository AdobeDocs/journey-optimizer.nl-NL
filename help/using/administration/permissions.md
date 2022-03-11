---
title: Gebruikers en productprofielen beheren
description: Leer hoe u machtigingen beheert
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 11%

---

# Gebruikers en productprofielen beheren {#manage-permissions}

>[!IMPORTANT]
>
> Elk van de onderstaande procedures kan alleen worden uitgevoerd door een **[!UICONTROL Product]** of **[!UICONTROL System]** beheerder. Raadpleeg voor meer informatie hierover de [Documentatie beheerconsole](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Product profiles]** zijn reeksen gebruikers die de zelfde toestemmingen en zandbakken binnen uw organisatie delen.

The [!DNL Journey Optimizer] product allows you to select between different out-of-the-box **[!UICONTROL Product profiles]** with different levels of permissions to assign to your users. For more information on the available **[!UICONTROL Product profiles]**, refer to this [page](ootb-product-profiles.md).

Elke gebruiker die tot een **[!UICONTROL Product profiles]** heeft recht op de Adobe-apps en -services in het product.

U kunt ook uw eigen **[!UICONTROL Product profiles]** als u de toegang van uw gebruikers tot bepaalde functies of voorwerpen in de interface wilt verfijnen.

## Een productprofiel toewijzen {#assigning-product-profile}

U kunt ervoor kiezen een uit-de-doos of een douane toe te wijzen **[!UICONTROL Product profile]** aan uw gebruikers.

De lijst met alle out-of-the-box productprofielen met toegewezen machtigingen vindt u in de [Geïntegreerde productprofielen](ootb-product-profiles.md) sectie.

Om een **[!UICONTROL Product profile]**:

1. In the [!DNL Admin Console], from the **[!UICONTROL Products]** tab, select the **[!UICONTROL Experience Cloud - Platform powered applications]** product.

1. Selecteer een **[!UICONTROL Product profile]**.

   ![](assets/do-not-localize/access_control_2.png)

1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add user]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Type in your user&#39;s name or email address and select the user.

   Als de gebruiker niet eerder in [!DNL Admin Console], verwijst u naar de [Gebruikersdocumentatie toevoegen](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

1. Voer dezelfde stappen uit als hierboven om andere gebruikers toe te voegen aan uw **[!UICONTROL Product profile]**. Klik vervolgens op **[!UICONTROL Save]**.

De gebruiker ontvangt vervolgens een e-mail met een doorverwijzing naar uw -instantie.

Raadpleeg voor meer informatie over gebruikersbeheer de [Documentatie Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Wanneer de gebruiker tot de instantie toegang heeft, zal uw gebruiker een specifieke mening afhankelijk van de toegewezen toestemmingen in zien **[!UICONTROL Product profile]**. Als de gebruiker niet de juiste toegang tot een eigenschap heeft, zal het volgende scherm verschijnen.

![](assets/do-not-localize/access_control_1.png)

## Een bestaand productprofiel bewerken {#edit-product-profile}

For out-of-the-box or custom **[!UICONTROL Product profiles]**, you can decide at any time to add or delete permissions.

In this example, we want to add **[!UICONTROL Permissions]** related to the **[!UICONTROL Message]** capability for users assigned to the Journey viewer **[!UICONTROL Product profile]**. De gebruikers zullen dan berichten kunnen publiceren.

Let op: als u een uit-van-de-doos of aangepast **[!UICONTROL Product profile]**, heeft dit gevolgen voor elke gebruiker die aan deze **[!UICONTROL Product profile]**.

1. In de [!DNL Admin Console]van de **[!UICONTROL Products]** selecteert u de **[!UICONTROL Experience Cloud - Platform powered applications]** product.

1. Selecteer de Journey-viewer **[!UICONTROL Product profile]**.

1. Selecteer het tabblad **[!UICONTROL Permissions]**. 

   De **[!UICONTROL Permissions]** wordt de lijst weergegeven met mogelijkheden die van toepassing zijn op de **[!UICONTROL Experience Cloud - Platform powered applications]** product.

   ![](assets/do-not-localize/access_control_5.png)

1. Selecteer **[!UICONTROL Messages]** capaciteit.

   ![](assets/do-not-localize/access_control_6.png)

1. Van de **[!UICONTROL Available Permission Items]** Selecteer de machtigingen die aan uw **[!UICONTROL Product profile]** door op de plusknop (+) te klikken.

   Here, we add the **[!UICONTROL Publish messages]** permission.

   ![](assets/do-not-localize/access_control_7.png)

1. Klik zo nodig onder **[!UICONTROL Included Permission Items]** op het X-pictogram om toestemmingen voor uw productprofiel te verwijderen.

1. Klik op **[!UICONTROL Save]** als u klaar bent.

   ![](assets/do-not-localize/access_control_8.png)

Indien nodig kunt u ook een nieuw productprofiel met specifieke machtigingen maken. Raadpleeg voor meer informatie hierover [Een productprofiel maken](#create-product-profile).

## Een productprofiel maken {#create-product-profile}

[!DNL Journey Optimizer] staat u toe om uw te creëren **[!UICONTROL Product profiles]** en wijs een reeks toestemmingen en zandbakken aan uw gebruikers toe. Met **[!UICONTROL Product profiles]** kunt u toegang tot bepaalde functies of objecten in de interface toestaan of weigeren.

Voor meer informatie over het maken en beheren van sandboxen raadpleegt u [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html){target=&quot;_blank&quot;}.

In dit voorbeeld maken we een productprofiel met de naam **Reizen, alleen-lezen** waar wij read-only rechten op de eigenschap van de Reis zullen verlenen. Gebruikers kunnen alleen reizen openen en bekijken en hebben geen toegang tot andere functies, zoals **[!DNL  Decision management]** of **[!DNL Messages]** in [!DNL Journey Optimizer].

Als u onze **Reizen, alleen-lezen** **[!UICONTROL product profiles]**:

1. Toegang krijgen tot [!DNL Admin Console].

1. Van de **[!UICONTROL Products]** selecteert u de **[!UICONTROL Experience Cloud - Platform powered applications]** product.

1. Klik op **[!UICONTROL New Profile]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Voeg een **[!UICONTROL Product Profile Name]**, **[!UICONTROL Display Name]** en **[!UICONTROL Description]** voor uw nieuwe **[!UICONTROL product profiles]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Kies in de categorie **[!UICONTROL Notifications]** of gebruikers via e-mail op de hoogte worden gesteld wanneer ze aan dit productprofiel worden toegevoegd of eruit worden verwijderd.

1. Als u klaar bent, klikt u op **[!UICONTROL Save]** en selecteer de nieuwe **[!UICONTROL product profiles]**.

1. To add permissions for users to access different features, select the **[!UICONTROL Permissions]** tab.

1. Selecteren tussen de verschillende mogelijkheden, zoals **[!DNL Messages]**, **[!DNL Segments]** of **[!DNL Decision management]** beschikbaar in [!DNL Journey Optimizer] in het linkermenu.

   Here we select the **[!UICONTROL Journeys]** capability.

   ![](assets/do-not-localize/access_control_11.png)

1. Van de **[!UICONTROL Available Permission Items]** Selecteer de machtigingen die aan uw **[!UICONTROL Product profile]** door op de plusknop (+) te klikken.

   Here we select **[!DNL View journeys]** and **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Selecteer **[!UICONTROL Sandbox access]** mogelijkheid om te kiezen welke sandbox(en) u wilt toewijzen aan uw **[!UICONTROL Product profile]**.

   ![](assets/do-not-localize/access_control_13.png)

1. Klik onder **[!UICONTROL Available Permissions Items]** op het pluspictogram (+) om sandboxen aan uw profiel toe te wijzen. [Meer informatie over sandboxen](sandboxes.md).

1. Klik op **[!UICONTROL Save]** als u klaar bent.

Uw **[!UICONTROL Product profile]** wordt nu gecreeerd en gevormd. U moet deze nu aan gebruikers toewijzen.

Raadpleeg voor meer informatie over het maken en beheren van productprofielen de [Documentatie Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
