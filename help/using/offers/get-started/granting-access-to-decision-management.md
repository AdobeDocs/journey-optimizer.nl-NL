---
product: experience platform
solution: Experience Platform
title: Toegang verlenen tot Offer Decisioning
description: Leer hoe u gebruikersmachtigingen voor de service Offers Decisioning via Adobe Admin Console beheert.
feature: Collections
role: User
level: Intermediate
exl-id: 2a2fece9-1ad5-498e-b0ee-5bb0b73a2cd5
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 7%

---

# Toegang tot het besluitvormingsbeheer verlenen {#granting-acess-to-decision-management}

De toestemmingen om tot de mogelijkheden van de offer decisioning toegang te hebben en te gebruiken worden beheerd gebruikend [Adobe Admin Console](https://helpx.adobe.com/nl/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

Om toegang tot de functionaliteit van het Beheer van het Besluit te verlenen, moet u tot een **[!UICONTROL Product profile]** en wijs de overeenkomstige toestemmingen aan uw gebruikers toe. Meer informatie over beheren [!DNL Journey Optimizer] gebruikers en machtigingen in [deze sectie](../../administration/permissions.md).

De machtigingen die specifiek zijn voor Beslissingsbeheer worden vermeld in [deze sectie](../../administration/high-low-permissions.md#manage-decisioning).

<!--If you are a [!DNL Journey Optimizer] user leveraging the **Decision Management** functionality, you need to have the [Decision management permissions](../../administration/high-low-permissions.md#decisions-permissions) enabled to acces all related capabilities. Learn more on managing [!DNL Journey Optimizer] users and permissions in [this section](../../administration/permissions.md).

If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service, follow the steps [below](#granting-acess-to-offer-decisioning) to grant access to [!DNL Offer Decisioning].

Grant access to Offer Decisioning

The steps below only apply to **Experience Platform users** leveraging the [!DNL Offer Decisioning] service.-->

1. Open de [Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html)selecteert u vervolgens **[!UICONTROL Adobe Experience Platform]**.

   <!--![](../../assets/offers_admin_console.png)-->

1. De productprofielen voor de de dienstvertoning. Als u een nieuw productprofiel wilt maken, klikt u op de knop **[!UICONTROL New Profile]** knop.

   ![](../../assets/offers_rights_productprofile.png)

   >[!NOTE]
   >
   >U kunt zo vele productprofielen hebben zoals gewenst, die aan de diverse rollen beantwoorden die u opstelling voor uw organisatie wilt.

1. Geef de naam en beschrijving van het productprofiel op en klik vervolgens op **[!UICONTROL Next]**.

   ![](../../assets/create-product-profile.png)

   <!--To access the product profile’s permissions, select the **[!UICONTROL Permissions]** line.-->

1. Selecteer de services die u wilt inschakelen voor het productprofiel. Standaard worden alle services geselecteerd. Dit wordt aanbevolen om ervoor te zorgen dat alle functies van het Experience Platform beschikbaar zijn.

   ![](../../assets/enable-services.png)

1. In de **[!UICONTROL Decision Management]** klikt u op de **+** om rechten toe te wijzen aan het productprofiel, klikt u vervolgens op **[!UICONTROL Save]**.

   ![](../../assets/configure-profile.png)

   Beschikbare machtigingen zijn:

   **[!UICONTROL Manage Decisioning Activities]**:

   * Aanbiedingen lezen, schrijven, verwijderen
   * Besluiten lezen, schrijven en verwijderen (voorheen bekend als aanbiedingsactiviteiten)
   * Plaatsen lezen, schrijven en verwijderen

   **[!UICONTROL Execute Decisioning Activities]**:

   * Aanbiedingen lezen
   * Besluiten lezen
   * Plaatsen lezen

   **[!UICONTROL Manage Decisioning Options]**:

   * Aanbiedingen lezen, schrijven, verwijderen
   * Besluiten lezen
   * Plaatsen lezen, schrijven en verwijderen



1. Er wordt een overzicht weergegeven van de machtigingen van het productprofiel. U kunt nu gebruikers toewijzen aan het productprofiel zodat ze deze machtigingen kunnen gebruiken.

   ![](../../assets/product-profile-created.png)

>[!NOTE]
>
>Raadpleeg voor meer informatie over het beheren van gebruikersmachtigingen de [Documentatie Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

