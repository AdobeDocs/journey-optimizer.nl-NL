---
solution: Journey Optimizer
product: journey optimizer
title: Toegangsbeheer op objectniveau
description: Meer informatie over toegangsbeheer op objectniveau waarmee u machtigingen kunt definiëren voor het beheren van gegevenstoegang tot een selectie objecten
feature: Access Management
topic: Administration
role: Admin, Developer
level: Experienced
keywords: voorwerp, niveau, toegang, controle, etiketten, olc, vergunning
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Toegangsbeheer op objectniveau {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Toegangsbeheerlabels"
>abstract="U kunt de toegang tot een object beperken op basis van toegangslabels. Deze aanpak beschermt gevoelige digitale middelen tegen onbevoegde gebruikers en zorgt voor een verdere bescherming van persoonsgegevens. **zorg ervoor om slechts etiketten te selecteren u toestemming voor hebt.**"

U kunt de toegang tot een object beperken op basis van toegangslabels. Deze aanpak beschermt gevoelige digitale middelen tegen onbevoegde gebruikers en zorgt voor een verdere bescherming van persoonsgegevens.

Met de mogelijkheid voor toegangsbeheer op objectniveau (OLAC) kunt u machtigingen definiëren voor het beheren van gegevenstoegang voor een selectie van objecten:

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


## Vereisten {#prereq-labels}

Om [ etiketten ](#create-labels) te kunnen tot stand brengen, moet u tot een rol met de **[!UICONTROL Manage usage labels]** toestemming behoren.

Om [ etiketten ](#assign-labels) toe te wijzen, moet u tot een rol met a **behoren leidt** toestemming i.e., [!DNL Manage journeys], [!DNL Manage Campaigns], of [!DNL Manage decisions]. Zonder deze machtiging wordt de knop **[!UICONTROL Manage access]** grijs weergegeven.

Leer meer over toestemmingen in [ deze sectie ](../administration/permissions.md).

## Labels maken {#create-labels}

**[!UICONTROL Labels]** staat u toe om datasets en gebieden volgens gebruiksbeleid te categoriseren die op die gegevens van toepassing zijn. **[!UICONTROL Labels]** kan op elk gewenst moment worden toegepast, zodat u flexibel kunt bepalen hoe gegevens worden beheerd.

Gebruik labels om toegang tot gebruikers te bieden en om het beheer van gegevens en het toestemmingsbeleid af te dwingen. Deze bestuurslabels kunnen downstreamconsumptie beïnvloeden.

U kunt labels maken in het [!DNL Permissions] -product. Voor meer details, verwijs naar [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html){target="_blank"}.

U kunt **[!UICONTROL Labels]** ook rechtstreeks in Journey Optimizer maken. Voer de volgende stappen uit om een label te maken:

1. Klik op de knop **[!UICONTROL Campaign]** van een Adobe Journey Optimizer-object, zoals een nieuw gemaakt **[!UICONTROL Manage access]** .

   ![ beheert toegangsknoop in Adobe Journey Optimizer ](assets/olac_1.png)

1. Klik in het **[!UICONTROL Manage access]** -venster op **[!UICONTROL Create label]** .

   ![](assets/olac_2.png)

1. Configureer uw label. U moet opgeven:

   * **[!UICONTROL Name]**
   * **[!UICONTROL Friendly name]**
   * **[!UICONTROL Description]**

   ![ de configuratiegebieden van het Etiket ](assets/olac_3.png)

1. Klik op **[!UICONTROL Create]** om de **[!UICONTROL Label]** op te slaan.

Het nieuwe **[!UICONTROL Label]** is nu beschikbaar in de lijst. Indien nodig, kunt u deze wijzigen in het [!DNL Permissions] -product.

## Labels toewijzen {#assign-labels}

Aangepaste labels of basislabels voor gegevensgebruik toewijzen aan Journey Optimizer-objecten:

1. Klik op de knop **[!UICONTROL Campaign]** van een Adobe Journey Optimizer-object, zoals een nieuw gemaakt **[!UICONTROL Manage access]** .

   ![ beheert toegangsknoop in Adobe Journey Optimizer ](assets/olac_1.png)

1. Selecteer in het venster **[!UICONTROL Manage access]** uw aangepaste label(s) of basislabel(en) voor gegevensgebruik om de toegang tot dit object te beheren.

   Voor meer informatie over de etiketten van het kerngegevensgebruik, verwijs naar [ deze pagina ](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html){target="_blank"}.

   ![](assets/olac_4.png)

1. Klik op **[!UICONTROL Save]** om deze labelbeperking toe te passen.

Gebruikers moeten de specifieke **[!UICONTROL Label]** -code in hun **[!UICONTROL Roles]** hebben opgenomen om toegang te krijgen tot dit object. Bijvoorbeeld, zal een gebruiker met het C1 etiket slechts toegang tot C1-geëtiketteerde of unlabel voorwerpen hebben.

Voor meer details op hoe te om a **[!UICONTROL Label]** aan a **[!UICONTROL Role]** toe te wijzen, verwijs naar [ deze pagina ](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role){target="_blank"}.
