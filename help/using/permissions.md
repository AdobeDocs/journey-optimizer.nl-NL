---
title: Machtigingen beheren
description: Leer hoe u machtigingen beheert
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 66%

---

# Machtigingen beheren {#manage-permissions}

![](assets/do-not-localize/badge.png)

## Toegang tot Journey Optimizer {#access-CJM}

Met [!DNL Journey Optimizer] kunt u een reeks toestemmingen aan uw gebruikers toewijzen om te definiëren tot welk deel van de interface ze toegang hebben.

Ze kunnen worden beheerd door beheerders met toegang tot de Admin Console. [Meer weten over Adobe Admin Console](https://helpx.adobe.com/nl/enterprise/managing/user-guide.html)?

Voor toegang tot [!DNL Journey Optimizer]moet een gebruiker:

* deel van een [!DNL Journey Optimizer]-**[!UICONTROL product profile]** zijn dat is gekoppeld aan [!DNL Journey Optimizer]-toestemmingen.

* deel van een [!DNL Adobe Experience Platform]-**[!UICONTROL product profile]** zijn. Er is geen verplichte toestemming. De gebruiker heeft de **[!UICONTROL profile management]**-toestemming nodig om platformsegmenten te maken en te bewerken vanuit de [!DNL Journey Optimizer]-interface. [Meer informatie over toegangsbeheer](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=en#adobe-admin-console).

In de Admin Console kunt u een van de volgende meegeleverde productprofielen aan uw gebruikers toewijzen:

* **[!UICONTROL Limited Access User]**: gebruiker met alleen-lezen toegang tot journey’s en rapporten. Dit productprofiel bevat de volgende toestemmingen:
   * Journey’s lezen
   * Rapporten lezen

* **[!UICONTROL Administrators]**: gebruiker met toegang tot de beheermenu’s met de mogelijkheid om journey’s, gebeurtenissen en rapporten te beheren. Dit productprofiel bevat de volgende toestemmingen:
   * Journey’s beheren
   * Journey’s publiceren
   * Gebeurtenissen, databronnen en acties beheren
   * Rapporten beheren

* **[!UICONTROL Standard User]**: gebruiker met basistoegang zoals journeybeheer. Dit productprofiel bevat de volgende toestemmingen:
   * Journey’s beheren
   * Journey’s publiceren
   * Rapporten beheren
   * Gebeurtenissen, gegevensbronnen en handelingen lezen

U kunt ook zelf productprofielen maken als de meegeleverde profielen niet voldoende zijn om uw gebruikers te beheren.
Gebruikers moeten altijd aan een productprofiel zijn gekoppeld zodat u specifieke ingebouwde toestemmingen aan hen kunt toewijzen, zoals:

* **[!UICONTROL Read journeys]**
* **[!UICONTROL Read reports]**
* **[!UICONTROL Manage events, data sources and actions]**
* **[!UICONTROL Read events, data sources and actions]**
* **[!UICONTROL Manage journeys]**
* **[!UICONTROL Publish journeys]**
* **[!UICONTROL Manage reports]**

>[!NOTE]
>
> Machtigingsbeheer omvat geen berichten: elke gebruiker kan berichten tot stand brengen of wijzigen.

### Een productprofiel maken {#create-product-profile}

Met [!DNL Journey Optimizer] kunt u zelf productprofielen maken en een reeks toestemmingen en sandboxen aan uw gebruikers toewijzen. Met productprofielen kunt u toegang tot bepaalde functies of objecten in de interface toestaan of weigeren.

Raadpleeg de [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html) voor informatie over het maken en beheren van sandboxen.

Een productprofiel maken en een reeks toestemmingen en sandboxen toewijzen:

1. Selecteer **[!UICONTROL Journey Orchestration]** in de Admin Console. Klik op het tabblad **[!UICONTROL Product profile]** op **[!UICONTROL New Profile]**.

   ![](assets/do-not-localize/user_management_5.png)

1. Voeg een **[!UICONTROL Profile Name]** en **[!UICONTROL Description]** toe voor uw nieuwe productprofiel. Als u voor uw profiel een andere **[!UICONTROL Display name]** wilt, schakelt u **[!UICONTROL Same as Profile Name]** uit en typt u uw **[!UICONTROL Display name]**.

1. Kies in de categorie **[!UICONTROL User Notifications]** of gebruikers via e-mail op de hoogte worden gesteld wanneer ze aan dit productprofiel worden toegevoegd of eruit worden verwijderd.

1. Klik op **[!UICONTROL Done]** als u klaar bent. Uw nieuwe productprofiel is nu gemaakt.

   ![](assets/do-not-localize/user_management_1.png)

1. Selecteer het nieuwe productprofiel om toestemmingen te beheren. Voeg op het tabblad **[!UICONTROL Users]** gebruikers toe aan uw productprofiel. [Leer hoe u productprofiel](permissions.md#assigning-product-profile) toewijst.

1. Voer dezelfde stappen uit als hierboven beschreven om **[!UICONTROL Admin]** aan uw productprofiel toe te voegen.

1. Selecteer op het tabblad **[!UICONTROL Permissions]** een van de twee categorieën **[!UICONTROL Sandbox]** of **[!UICONTROL Authoring]** om de pagina **[!UICONTROL Edit Permissions]** te openen en toestemmingen voor uw productprofiel toe te voegen of te verwijderen.

   ![](assets/do-not-localize/user_management_7.png)

1. Kies in de toestemmingencategorie **[!UICONTROL Sandboxes]** welke sandbox(en) aan uw productprofiel moeten worden toegewezen. Klik onder **[!UICONTROL Available Permissions Items]** op het pluspictogram (+) om sandboxen aan uw profiel toe te wijzen. [Meer informatie over sandboxen](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html).

   ![](assets/do-not-localize/user_management_8.png)

1. Klik zo nodig onder **[!UICONTROL Included Permission Items]** op het X-pictogram om toestemmingen voor uw productprofiel te verwijderen.

   ![](assets/do-not-localize/user_management_9.png)

1. Voer vanuit de toestemmingencategorie **[!UICONTROL Authoring]** dezelfde stappen uit als hierboven om toestemmingen toe te voegen aan uw productprofiel.

   ![](assets/do-not-localize/user_management_10.png)

1. Klik op **[!UICONTROL Save]** als u klaar bent.

Uw productprofiel is nu gemaakt en geconfigureerd. Gebruikers die aan dit profiel zijn gekoppeld, kunnen nu verbinding maken met [!DNL Journey Optimizer].

### Een productprofiel toewijzen {#assigning-product-profile}

Productprofielen worden toegewezen aan een reeks gebruikers die dezelfde toestemmingen hebben binnen uw organisatie.
In deze sectie vindt u de lijst van alle meegeleverde productprofielen met toegewezen toestemmingen.

Een productprofiel toewijzen aan een gebruiker voor toegang tot reizen:

1. Selecteer **[!UICONTROL Journey Orchestration]** in de Admin Console.

   ![](assets/do-not-localize/user_management.png)

1. Selecteer het productprofiel waaraan de nieuwe gebruiker wordt gekoppeld.

   ![](assets/do-not-localize/user_management_2.png)

1. Klik op **[!UICONTROL Add user]**.

   U kunt de nieuwe gebruiker ook toevoegen aan een gebruikersgroep om de gedeelde reeks toestemmingen te verfijnen. [Meer weten over gebruikersgroepen](https://helpx.adobe.com/nl/enterprise/using/user-groups.html)?

   ![](assets/do-not-localize/user_management_3.png)

1. Typ het e-mailadres van de nieuwe gebruiker en klik op **[!UICONTROL Save]**.

   ![](assets/do-not-localize/user_management_4.png)

De gebruiker ontvangt vervolgens een e-mail met een doorverwijzing naar uw -instantie.

## Sandboxen gebruiken {#sandboxes}

In [!DNL Journey Optimizer] kunt u uw instantie partitioneren in afzonderlijke virtuele omgevingen, sandboxen genoemd.
Sandboxen worden toegewezen via productprofielen in de Admin Console. [Leer hoe u sandboxen](permissions.md#create-product-profile) toewijst.

[!DNL Journey Optimizer] weerspiegelt Adobe Experience Platform-sandboxen die voor een bepaalde organisatie zijn gemaakt.
U kunt Adobe Experience Platform-sandboxen maken of herstellen vanuit uw Adobe Experience Platform-instantie. [Meer informatie vindt u in de gebruikershandleiding](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html) van de sandbox.

U vindt de schakelfunctie voor sandboxen linksboven in het scherm. Als u van sandbox wilt wisselen, klikt u op de momenteel actieve sandbox in de schakelfunctie en selecteert u een andere sandbox in de vervolgkeuzelijst.

## Toegang tot inhoud {#content-access}

Als u de toegankelijkheid van uw inhoud wilt configureren, moet u een gedeelde inhoudsmap toewijzen aan elk van uw sandboxen. U kunt uw gedeelde omslag op **[!UICONTROL Storage]** tabel tot stand brengen en vormen die in [!DNL Admin Console] voor beheerders wordt getoond. Als u als systeembeheerder toegang tot [!DNL Admin Console] hebt, kunt u gedeelde omslagen tot stand brengen en afgevaardigden met verschillend toegangsniveau aan uw gedeelde omslagen toevoegen.

![](assets/do-not-localize/content_access.png)

Houd er rekening mee dat voor synchronisatie van uw inhoud met de juiste sandbox dezelfde syntaxis moet worden gebruikt als de sandbox, bijvoorbeeld als de sandbox ontwikkeling wordt genoemd, moet uw gedeelde map dezelfde naam hebben.

[Leer hoe u gedeelde mappen](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html) beheert.

## Assets Essentials-machtigingen {#assets-permissions}

Adobe Experience Manager Assets Essentials biedt één gecentraliseerde opslagplaats voor middelen die u kunt gebruiken om uw berichten te vullen.
Elk element wordt opgeslagen in mappen of submappen. U kunt kiezen om uw mappen te delen en welk toegangsniveau u wilt toewijzen.

1. Navigeer op het tabblad **[!UICONTROL Assets]** door de mappen om te zoeken naar de map die u wilt delen.

1. Selecteer de map of het element en klik op **[!UICONTROL Share]**.

   ![](assets/share_media_1.png)

1. Voer het e-mailadres in van de andere persoon met wie u toegang tot uw map wilt delen.

1. Kies tussen de verschillende toegangsniveaus:

   * **[!UICONTROL Can view]**
   * **[!UICONTROL Can edit]**
   * **[!UICONTROL Has ownership (can share, edit, and delete)]**

   ![](assets/share_media_2.png)

1. Voeg zo nodig een bericht toe aan uw uitnodiging.

1. Klik op **[!UICONTROL Invite]**.

   ![](assets/share_media_3.png)
