---
solution: Journey Optimizer
product: journey optimizer
title: Toegangsbeheer op basis van kenmerken
description: Op attributen-gebaseerde toegangsbeheer (ABAC) laat u toestemmingen bepalen om gegevenstoegang voor specifieke teams of groepen gebruikers te beheren.
feature: Access Management
topic: Administration
role: Admin,Leader
level: Intermediate
keywords: abac, attribute, Authorizations, data, access, sensitive, assets
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: fbcd5ae83c024d672d608d5f5aefc6a4252ec8c0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Toegangsbeheer op basis van kenmerken {#attribute-based-access}

Met de ABAC-functie (Attribuut-based Access Control) kunt u machtigingen definiëren voor het beheren van gegevenstoegang voor specifieke teams of groepen gebruikers. Het doel is gevoelige digitale activa te beschermen tegen ongeoorloofde gebruikers, zodat persoonsgegevens verder kunnen worden beschermd.

In Adobe Journey Optimizer, staat ABAC u toe om gegevens te beschermen en specifieke toegang tot specifieke gebiedselementen met inbegrip van de schema&#39;s van de Gegevens van de Ervaring (XDM), de attributen van het Profiel, en publiek te verlenen.

Voor een meer gedetailleerde lijst van de terminologie die met ABAC wordt gebruikt, verwijs naar [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html).

In dit voorbeeld, willen wij een etiket aan het **het schemagebied van de Nationaliteit** toevoegen om onbevoegde gebruikers van het te beperken gebruiken. Dit werkt alleen als u de volgende stappen uitvoert:

1. Maak een nieuwe **[!UICONTROL Role]** en wijs deze met de bijbehorende **[!UICONTROL Label]** toe zodat gebruikers het schemaveld kunnen openen en gebruiken.

1. Wijs a **[!UICONTROL Label]** aan het **Nationaliteit** schemagebied in Adobe Experience Platform toe.

1. Gebruik **[!UICONTROL Schema field]** in Adobe Journey Optimizer.

**[!UICONTROL Roles]** , **[!UICONTROL Policies]** en **[!UICONTROL Products]** kunnen ook worden benaderd met de op kenmerken gebaseerde API voor toegangsbeheer. Voor meer op dit, verwijs naar deze [ documentatie ](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html).

## Een rol maken en labels toewijzen {#assign-role}

>[!IMPORTANT]
>
>Voordat u machtigingen voor een rol beheert, moet u eerst een beleid maken. Voor meer op dit, verwijs naar [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html).

**[!UICONTROL Roles]** is een reeks gebruikers die dezelfde machtigingen, labels en sandboxen binnen uw organisatie hebben. Elke gebruiker die tot een **[!UICONTROL Role]** behoort, heeft recht op de Adobe-apps en -services in het product.
U kunt ook uw eigen **[!UICONTROL Roles]** maken als u de toegang van uw gebruikers tot bepaalde functies of objecten in de interface wilt verfijnen.

Wij willen nu geselecteerde gebruikers toegang tot het **gebied van de Nationaliteit** verlenen, geëtiketteerd C2. Om dit te doen, moeten wij nieuw **[!UICONTROL Role]** met een specifieke reeks gebruikers tot stand brengen en hen het etiket C2 verlenen die hen toestaat om de **Nationaliteit** details in a **[!UICONTROL Journey]** te gebruiken.

1. Selecteer in het product [!DNL Permissions] de optie **[!UICONTROL Role]** in het menu van het linkerdeelvenster en klik op **[!UICONTROL Create role]** . U kunt ook **[!UICONTROL Label]** toevoegen aan ingebouwde rollen.

   ![](assets/role_1.png)

1. Voeg hier een **[!UICONTROL Name]** en **[!UICONTROL Description]** toe aan uw nieuwe **[!UICONTROL Role]** . Dit is een demografische beperking voor de rol.

1. Selecteer in de vervolgkeuzelijst de **[!UICONTROL Sandbox]** .

   ![](assets/role_2.png)

1. Klik in het menu **[!UICONTROL Resources]** op **[!UICONTROL Adobe Experience Platform]** om de verschillende mogelijkheden te openen. Hier selecteren we **[!UICONTROL Journeys]** .

   ![](assets/role_3.png)

1. Selecteer in de vervolgkeuzelijst de **[!UICONTROL Permissions]** die aan de geselecteerde functie, zoals **[!UICONTROL View journeys]** of **[!UICONTROL Publish journeys]** , is gekoppeld.

   ![](assets/role_6.png)

1. Nadat u het zojuist gemaakte bestand hebt opgeslagen **[!UICONTROL Role]** , klikt u op **[!UICONTROL Properties]** om de toegang tot uw rol verder te configureren.

   ![](assets/role_7.png)

1. Klik op het tabblad **[!UICONTROL Users]** op **[!UICONTROL Add users]**.

   ![](assets/role_8.png)

1. Selecteer op het tabblad **[!UICONTROL Labels]** de optie **[!UICONTROL Add label]**.

   ![](assets/role_9.png)

1. Selecteer **[!UICONTROL Labels]** u aan uw rol wilt toevoegen en **[!UICONTROL Save]** klikken. Voor dit voorbeeld, verlenen wij het etiket C2 voor gebruikers om toegang tot het eerder beperkte gebied van het schema te hebben.

   ![](assets/role_4.png)

De gebruikers in de **Beperkte rol demografische** rol hebben nu toegang tot de C2 geëtiketteerde voorwerpen.

## Labels toewijzen aan een object in Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>Onjuist labelgebruik kan de toegang tot personen verbreken en beleidsovertredingen veroorzaken.

**[!UICONTROL Labels]** kan worden gebruikt om specifieke eigenschapgebieden toe te wijzen gebruikend op Attributen-Gebaseerd toegangsbeheer.
In dit voorbeeld, willen wij toegang tot het **gebied van de Nationaliteit** beperken. Dit veld is alleen toegankelijk voor gebruikers met de bijbehorende **[!UICONTROL Label]** voor hun **[!UICONTROL Role]** .

U kunt ook **[!UICONTROL Label]** toevoegen aan **[!UICONTROL Schema]** , **[!UICONTROL Datasets]** en **[!UICONTROL Audiences]** .

1. Maak uw **[!UICONTROL Schema]** . Voor meer op dit, verwijs naar [ deze documentatie ](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html).

   ![](assets/label_1.png)

1. In onlangs gecreeerd **[!UICONTROL Schema]**, voegen wij eerst de **[!UICONTROL Demographic details]** gebiedsgroep toe die het **gebied van de Nationaliteit** bevat.

   ![](assets/label_2.png)

1. Van het **[!UICONTROL Labels]** lusje, controleer de beperkte gebiedsnaam, hier **Nationaliteit**. Selecteer vervolgens **[!UICONTROL Edit governance labels]** in het menu van het rechterdeelvenster.

   ![](assets/label_3.png)

1. Selecteer de corresponderende **[!UICONTROL Label]**, in dit geval de C2 - Gegevens kunnen niet naar een derde worden geëxporteerd. Voor de gedetailleerde lijst van beschikbare etiketten, verwijs naar [ deze pagina ](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. Pas verder uw schema aan als nodig dan laat het toe. Voor de gedetailleerde stappen op hoe te om uw schema toe te laten, verwijs naar deze [ pagina ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

Het veld van uw schema is nu alleen zichtbaar en kan nu alleen worden gebruikt door gebruikers die deel uitmaken van een rolset met het label C2.
Door a **[!UICONTROL Label]** op uw **[!UICONTROL Field name]** toe te passen, merk op dat **[!UICONTROL Label]** automatisch op het **gebied van de Nationaliteit** in elk gecreeerd schema zal worden toegepast.

![](assets/label_5.png)

## Benoemde objecten openen in Adobe Journey Optimizer {#attribute-access-ajo}

Na het etiketteren van onze **het gebiedsnaam van de Nationaliteit** in een nieuw schema en onze nieuwe rol, kunnen wij nu het effect van deze beperking in Adobe Journey Optimizer zien.
Een eerste gebruiker X met toegang tot objecten met het label C2 zal bijvoorbeeld een reis maken met een voorwaarde die gericht is op de beperkte **[!UICONTROL Field name]** . Een tweede gebruiker Y zonder toegang tot voorwerpen geëtiketteerd C2 zal dan de Reis moeten publiceren.

1. Vanuit Adobe Journey Optimizer moet u de **[!UICONTROL Data source]** eerst configureren met uw nieuwe schema.

   ![](assets/journey_1.png)

1. Voeg een nieuwe **[!UICONTROL Field group]** van de nieuwe **[!UICONTROL Schema]** toe aan de ingebouwde **[!UICONTROL Data source]** . U kunt ook een nieuwe externe **[!UICONTROL data source]** en gekoppelde **[!UICONTROL Field groups]** maken.

   ![](assets/journey_2.png)

1. Na het selecteren van de eerder gemaakte **[!UICONTROL Schema]** klikt u op **[!UICONTROL Edit]** in de categorie **[!UICONTROL Fields]** .

   ![](assets/journey_3.png)

1. Selecteer de **[!UICONTROL Field name]** die u als doel wilt instellen. Hier selecteren wij het beperkte **gebied van de Nationaliteit**.

   ![](assets/journey_4.png)

1. Maak vervolgens een Reis die een e-mail stuurt naar gebruikers met een specifieke nationaliteit. Voeg een **[!UICONTROL Event]** dan een **[!UICONTROL Condition]** toe.

   ![](assets/journey_5.png)

1. Selecteer het beperkte **gebied van de Nationaliteit** beginnen uw uitdrukking te bouwen.

   ![](assets/journey_6.png)

1. Bewerk uw **[!UICONTROL Condition]** om een specifieke bevolking met het beperkte **gebied van de Nationaliteit** te richten.

   ![](assets/journey_7.png)

1. Pas uw reis waar nodig aan, hier voegen we een **[!UICONTROL Email]** actie toe.

   ![](assets/journey_8.png)

Als de Gebruiker Y zonder toegang tot etiket C2 voorwerpen tot deze reis met dit beperkte gebied moet toegang hebben:

* Gebruiker Y kan de beperkte veldnaam niet gebruiken omdat deze niet zichtbaar is.

* Gebruiker Y kan de uitdrukking met de beperkte gebiedsnaam niet op Geavanceerde wijze uitgeven. De volgende fout wordt weergegeven `The expression is invalid. Field is no longer available or you don't have enough permission to see it` .

* Gebruiker Y kan de uitdrukking verwijderen.

* Gebruiker Y kan de Reis niet testen.

* Gebruiker Y kan de Reis niet publiceren.
