---
solution: Journey Optimizer
product: journey optimizer
title: Toegangsbeheer op objectniveau
description: Meer informatie over toegangsbeheer op objectniveau waarmee u machtigingen kunt definiëren voor het beheren van gegevenstoegang tot een selectie objecten
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: voorwerp, niveau, toegang, controle, etiketten, olc, vergunning
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 2%

---

# Toegangsbeheer op objectniveau {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Toegangsbeheer op objectniveau"
>abstract="Als u toegang tot dit object wilt behouden, past u alleen labels toe waarvoor u machtigingen hebt."

Met toegangsbeheer op objectniveau (OLAC) kunt u machtigingen definiëren voor het beheren van gegevenstoegang tot een selectie objecten:

* Reis
* Campaign
* Sjabloon
* Fragment
* Openingspagina
* Voorstel
* Statische aanbiedingenverzameling
* Offertebeslissing
* Kanaalconfiguratie
* IP-opwarmingsplan

Het doel is gevoelige digitale activa te beschermen tegen ongeoorloofde gebruikers, zodat persoonsgegevens verder kunnen worden beschermd.

In Adobe Journey Optimizer, staat OLAC u toe om gegevens te beschermen en specifieke toegang tot specifieke voorwerpen te verlenen.

## Labels maken {#create-assign-labels}

>[!IMPORTANT]
>
>Als u labels wilt maken, moet u deel uitmaken van een rol met de machtiging **[!UICONTROL Manage usage labels]** .

**[!UICONTROL Labels]** staat u toe om datasets en gebieden volgens gebruiksbeleid te categoriseren die op die gegevens van toepassing zijn. **[!UICONTROL Labels]** kan op elk gewenst moment worden toegepast, zodat u op flexibele wijze gegevens kunt beheren.

U kunt labels maken in het [!DNL Permissions] -product. Raadpleeg [deze pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html) voor meer informatie.

**[!UICONTROL Labels]** kan ook rechtstreeks in Journey Optimizer worden gemaakt:

1. Klik vanuit een Adobe Journey Optimizer-object, hier een nieuw gemaakt **[!UICONTROL Campaign]** , op de knop **[!UICONTROL Manage access]** .

   ![](assets/olac_1.png)

1. Klik in het **[!UICONTROL Manage access]** -venster op **[!UICONTROL Create label]** .

   ![](assets/olac_2.png)

1. Vorm uw etiket, moet u specificeren:
   * **[!UICONTROL Name]**
   * **[!UICONTROL Friendly name]**
   * **[!UICONTROL Description]**

   ![](assets/olac_3.png)

1. Klik op **[!UICONTROL Create]** om de **[!UICONTROL Label]** op te slaan.

Het nieuwe **[!UICONTROL Label]** is nu beschikbaar in de lijst. Indien nodig, kunt u deze wijzigen in het [!DNL Permissions] -product.

## Labels toewijzen {#assign-labels}

>[!IMPORTANT]
>
>Als u labels wilt toewijzen, moet u deel uitmaken van een rol met een machtiging Beheren, dat wil zeggen [!DNL Manage journeys], [!DNL Manage Campaigns] of [!DNL Manage decisions] . Zonder deze machtiging wordt de knop **[!UICONTROL Manage access]** grijs weergegeven.

Aangepaste labels of basislabels voor gegevensgebruik toewijzen aan Journey Optimizer-objecten:

1. Klik vanuit een Adobe Journey Optimizer-object, hier een nieuw gemaakt **[!UICONTROL Campaign]** , op de knop **[!UICONTROL Manage access]** .

   ![](assets/olac_1.png)

1. Selecteer in het venster **[!UICONTROL Manage access]** uw aangepaste label(s) of basislabel(en) voor gegevensgebruik om de toegang tot dit object te beheren.

   Voor meer informatie over de etiketten van het kerngegevensgebruik, verwijs naar [ deze pagina ](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. Klik op **[!UICONTROL Save]** om deze labelbeperking toe te passen.

Als gebruikers toegang tot dit object willen hebben, moeten ze de specifieke **[!UICONTROL Label]** voor hun **[!UICONTROL Roles]** opnemen.
Bijvoorbeeld, zal een gebruiker met het C1 etiket slechts toegang tot C1 geëtiketteerde of unlabel voorwerpen hebben.

Voor meer informatie over hoe te om **[!UICONTROL Label]** aan a **[!UICONTROL Role]** toe te wijzen, verwijs naar [ deze pagina ](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role).