---
title: Toegangsbeheer op objectniveau
description: Meer informatie over toegangsbeheer op objectniveau
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 61293a2ad45d30d24e1b38d8a5df81534dc19b40
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 2%

---

# Toegangsbeheer op objectniveau {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Toegangsbeheer op objectniveau"
>abstract="Als u labels toepast waartoe u geen toegang hebt, wordt de toegang tot dit object ingetrokken."

>[!IMPORTANT]
>
>Het gebruik van de toegangscontrole van het niveau van Objecten is momenteel beperkt tot geselecteerde klanten, en zal aan alle milieu&#39;s in een toekomstige versie worden opgesteld.

Met toegangsbeheer op objectniveau (OLAC) kunt u machtigingen definiëren om gegevenstoegang tot een selectie objecten te beheren:

* Reis
* Campaign
* Landingspagina
* Aanbiedingen
* Verzameling voorstellen
* Offer decisioning

Het doel is gevoelige digitale activa te beschermen tegen ongeoorloofde gebruikers, zodat persoonsgegevens verder kunnen worden beschermd.

In Adobe Journey Optimizer, staat OLAC u toe om gegevens te beschermen en specifieke toegang tot specifieke voorwerpen te verlenen.

## Labels maken {#create-assign-labels}

>[!IMPORTANT]
>
>Als u labels wilt maken, moet u deel uitmaken van een rol met de **[!UICONTROL Manage usage labels]** toestemming.

**[!UICONTROL Labels]** staat u toe om datasets en gebieden volgens gebruiksbeleid te categoriseren die op die gegevens van toepassing zijn. **[!UICONTROL Labels]** kan op elk moment worden toegepast, zodat u op flexibele wijze gegevens kunt beheren.

U kunt labels maken in het dialoogvenster [!DNL Permissions] product. Raadpleeg [deze pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html) voor meer informatie.

**[!UICONTROL Labels]** kan ook rechtstreeks in Journey Optimizer worden gemaakt:

1. Van een Adobe Journey Optimizer-object, hier een nieuw gemaakt **[!UICONTROL Campaign]** klikt u op de knop **[!UICONTROL Manage access]** knop.

   ![](assets/olac_1.png)

1. Van de **[!UICONTROL Manage access]** venster, klikt u op **[!UICONTROL Create label]**.

   ![](assets/olac_2.png)

1. Vorm uw etiket, moet u specificeren:
   * **[!UICONTROL Name]**
   * **[!UICONTROL Friendly name]**
   * **[!UICONTROL Description]**

   ![](assets/olac_3.png)

1. Klikken **[!UICONTROL Create]** om uw **[!UICONTROL Label]**.

Uw nieuwe versie **[!UICONTROL Label]** is nu beschikbaar in de lijst. Indien nodig, kunt u het in [!DNL Permissions] product.

## Labels toewijzen {#assign-labels}

>[!IMPORTANT]
>
>Als u labels wilt kunnen toewijzen, moet u deel uitmaken van een rol met een machtiging Beheren, dat wil zeggen: [!DNL Manage journeys], [!DNL Manage Campaigns] of [!DNL Manage decisions]. Zonder deze toestemming, **[!UICONTROL Manage access]** wordt grijs weergegeven.

Aangepaste labels of basislabels voor gegevensgebruik toewijzen aan Journey Optimizer-objecten:

1. Van een Adobe Journey Optimizer-object, hier een nieuw gemaakt **[!UICONTROL Campaign]** klikt u op de knop **[!UICONTROL Manage access]** knop.

   ![](assets/olac_1.png)

1. Van de **[!UICONTROL Manage access]** selecteert u de aangepaste of basislabels voor gegevensgebruik om de toegang tot dit object te beheren.

   Voor meer informatie over de basislabels voor gegevensgebruik raadpleegt u [deze pagina](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. Klikken **[!UICONTROL Save]** om deze labelbeperking toe te passen.

Als gebruikers toegang tot dit object willen hebben, moeten ze beschikken over de specifieke **[!UICONTROL Label]** opgenomen in hun **[!UICONTROL Roles]**.
Bijvoorbeeld, zal een gebruiker met het C1 etiket slechts toegang tot C1 geëtiketteerde of unlabel voorwerpen hebben.

Voor meer informatie over hoe u kunt toewijzen **[!UICONTROL Label]** een **[!UICONTROL Role]**, zie [deze pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).



