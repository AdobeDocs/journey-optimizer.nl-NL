---
title: Sandboxbeheer
description: Leer hoe u sandboxen beheert
feature: Controlegroepen
topic: Beheer
role: Administrator
level: Intermediate
source-git-commit: 2c4a86f7beb10d1ce35e8fb5600a979164038e5f
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 28%

---

# Sandboxbeheer {#sandboxes}

## Sandboxen gebruiken {#using-sandbox}

In [!DNL Journey Optimizer] kunt u uw instantie partitioneren in afzonderlijke virtuele omgevingen, sandboxen genoemd.
Sandboxen worden toegewezen via productprofielen in de Admin Console. [Leer hoe u sandboxen](permissions.md#create-product-profile) toewijst.

[!DNL Journey Optimizer] weerspiegelt Adobe Experience Platform-sandboxen die voor een bepaalde organisatie zijn gemaakt.
U kunt Adobe Experience Platform-sandboxen maken of herstellen vanuit uw Adobe Experience Platform-instantie. [Meer informatie vindt u in de gebruikershandleiding](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html) van de sandbox.

U vindt de schakelfunctie voor sandboxen linksboven in het scherm. Als u van sandbox wilt wisselen, klikt u op de momenteel actieve sandbox in de schakelfunctie en selecteert u een andere sandbox in de vervolgkeuzelijst.

## Sandboxen toewijzen {#assign-sandboxes}

>[!IMPORTANT]
>
> Sandboxbeheer kan alleen worden uitgevoerd door een beheerder **[!UICONTROL Product]** of **[!UICONTROL System]**. Raadpleeg de documentatie [Admin-console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html) voor meer informatie hierover.

U kunt ervoor kiezen verschillende sandboxen toe te wijzen aan een uitgesneden of aangepaste **[!UICONTROL Product profiles]**.

Sandboxen toewijzen:

1. Selecteer in [!DNL Admin Console] op het tabblad **[!UICONTROL Products]** het product **[!UICONTROL Adobe Experience Platform Apps]**.

1. Selecteer een **[!UICONTROL Product profile]**.

   ![](../assets/sandbox_1.png)

1. Selecteer het tabblad **[!UICONTROL Permissions]**. 

1. Selecteer de **[!UICONTROL Sandboxes]** mogelijkheid.

   ![](../assets/sandbox_2.png)

1. Klik onder **[!UICONTROL Available Permissions Items]** op het pluspictogram (+) om sandboxen aan uw profiel toe te wijzen. [Meer informatie over sandboxen](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html).

   ![](../assets/sandbox_3.png)

1. Klik, indien nodig, onder **[!UICONTROL Included Permission Items]** op het X-pictogram naast het verwijderen van de toegang tot uw **[!UICONTROL Product profile]**-sandboxen.

   ![](../assets/sandbox_4.png)

1. Klik op **[!UICONTROL Save]**.

## Toegang tot inhoud {#content-access}

Als u de toegankelijkheid van uw inhoud wilt configureren, moet u een gedeelde inhoudsmap toewijzen aan elk van uw sandboxen. U kunt uw gedeelde omslag op **[!UICONTROL Storage]** tabel tot stand brengen en vormen die in [!DNL Admin Console] voor beheerders wordt getoond. Als u als systeembeheerder toegang tot [!DNL Admin Console] hebt, kunt u gedeelde omslagen tot stand brengen en afgevaardigden met verschillend toegangsniveau aan uw gedeelde omslagen toevoegen.

![](../assets/do-not-localize/content_access.png)

Houd er rekening mee dat voor synchronisatie van uw inhoud met de juiste sandbox dezelfde syntaxis moet worden gebruikt als de sandbox, bijvoorbeeld als de sandbox ontwikkeling wordt genoemd, moet uw gedeelde map dezelfde naam hebben.

[Leer hoe u gedeelde mappen](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html) beheert.
