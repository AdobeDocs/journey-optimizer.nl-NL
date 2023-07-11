---
solution: Journey Optimizer
product: journey optimizer
title: Sandboxbeheer
description: Leer hoe u sandboxen beheert
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: sandboxen, virtueel, omgevingen, organisatie, platform
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 6a81760170e53ed9c34142f3b0b367bd62c3464c
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 21%

---

# Sandboxbeheer {#sandboxes}

## Sandboxen gebruiken {#using-sandbox}

In [!DNL Journey Optimizer] kunt u uw instantie partitioneren in afzonderlijke virtuele omgevingen, sandboxen genoemd.
Sandboxen worden toegewezen via rollen in Machtigingen. [Leer hoe u sandboxen toewijst](permissions.md#create-product-profile).

[!DNL Journey Optimizer] weerspiegelt Adobe Experience Platform-sandboxen die voor een bepaalde organisatie zijn gemaakt.
U kunt Adobe Experience Platform-sandboxen maken of herstellen vanuit uw Adobe Experience Platform-instantie. [Meer informatie in de gebruikershandleiding voor de sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html){target="_blank"}.

U kunt het besturingselement voor de sandboxswitch rechtsboven in het scherm vinden naast de naam van uw organisatie. Als u van sandbox wilt wisselen, klikt u op de momenteel actieve sandbox in de schakelfunctie en selecteert u een andere sandbox in de vervolgkeuzelijst.

![](assets/sandbox_5.png)

➡️ [Meer informatie over sandboxen in deze video](#video)

## Sandboxen toewijzen {#assign-sandboxes}

>[!IMPORTANT]
>
> Sandboxbeheer kan alleen worden uitgevoerd door een **[!UICONTROL Product]** of **[!UICONTROL System]** beheerder. Raadpleeg voor meer informatie hierover de [Documentatie beheerconsole](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target="_blank"}.

U kunt desgewenst verschillende sandboxen toewijzen **[!UICONTROL Roles]**.

Sandboxen toewijzen:

1. In [!DNL Permissions]van de **[!UICONTROL Roles]** selecteert u een **[!UICONTROL Role]**.

   ![](assets/sandbox_1.png)

1. Klik op **[!UICONTROL Edit]**.

1. Van de **[!UICONTROL Sandboxes]** bron drop-down, selecteer de zandbak die aan uw rol zal worden toegewezen.

   ![](assets/sandbox_3.png)

1. Klik indien nodig op het X-pictogram naast het verwijderen van sandboxen die toegang hebben tot uw **[!UICONTROL Role]**.

   ![](assets/sandbox_4.png)

1. Klik op **[!UICONTROL Save]**.

## Toegang tot inhoud {#content-access}

Als u de toegankelijkheid van uw inhoud wilt configureren, moet u een gedeelde inhoudsmap toewijzen aan elk van uw sandboxen. U kunt uw gedeelde map maken en configureren in het dialoogvenster **[!UICONTROL Storage]** weergegeven in het dialoogvenster [!DNL Admin Console] voor beheerders. Als u toegang hebt tot [!DNL Admin Console] als systeembeheerder, kunt u gedeelde omslagen tot stand brengen en afgevaardigden met verschillend toegangsniveau toevoegen aan uw gedeelde omslagen.

![](assets/do-not-localize/content_access.png)

Houd er rekening mee dat voor synchronisatie van uw inhoud met de juiste sandbox dezelfde syntaxis moet worden gebruikt als de sandbox, bijvoorbeeld als de sandbox ontwikkeling wordt genoemd, moet uw gedeelde map dezelfde naam hebben.

[Leer hoe u gedeelde mappen kunt beheren](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## Hoe kan ik-video{#video}

Begrijp wat sandboxen zijn en hoe u onderscheid kunt maken tussen ontwikkelings- en productiesandboxen. Leer hoe u sandboxen kunt maken, herstellen en verwijderen.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)
