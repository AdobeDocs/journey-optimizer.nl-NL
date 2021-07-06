---
title: Beheer en instellingen
description: Meer informatie over richtlijnen voor beheer en instellingen
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Applicatie-instellingen
topic: Beheer
role: Administrator
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 36%

---

# Reizen configureren

Als u berichten wilt verzenden met ritten, moet u **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** en **[!UICONTROL Actions]** configureren.

![](../assets/admin-menu.png)

## Databronnen

De configuratie van de Gegevensbron staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw reizen zal worden gebruikt. [Meer informatie](../../using/datasource/about-data-sources.md)

## Gebeurtenissen

Gebeurtenissen stellen u in staat om uw reizen tijdelijk te activeren en berichten in real-time te verzenden aan de persoon die de reis maakt.

In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De gegevens van de binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen zijn afkomstig van de streamingopname-API’s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). [Meer informatie](../../using/event/about-events.md)

## Acties

Journey Optimizer-berichtmogelijkheden zijn ingebouwd: u hoeft alleen uw inhoud te ontwerpen en uw bericht te publiceren. Als u berichten verzendt met een systeem van derden, kunt u een aangepaste handeling maken. [Meer informatie](../../using/action/action.md)

## Bladeren door Adobe Experience Platform-velden {#friendly-names-display}

Wanneer het bepalen van [gebeurtenislading](../event/about-creating.md#define-the-payload-fields), [gebiedsgroeplading](../datasource/configure-data-sources.md#define-field-groups) en het selecteren van gebieden in [expression redacteur](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html){target=&quot;_blank&quot;}, wordt de vertoningsnaam getoond naast de gebiedsnaam. Deze informatie wordt opgehaald uit de schemadefinitie in het Gegevenservaringmodel.

Als er beschrijvingen als xdm:alternateDisplayInfo worden opgegeven tijdens het instellen van schema’s, worden de weergavenamen vervangen door de gebruikersvriendelijke namen. Dit is vooral handig wanneer u werkt met &quot;eVars&quot; en algemene velden. U kunt beschrijvers van vriendschappelijke namen via een API vraag vormen. Voor meer informatie, zie [de ontwikkelaarsgids ](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html){target= &quot;_blank&quot;} van de Registratie van het Schema.

![](../assets/xdm-from-descriptors.png)

Als een beschrijvende naam beschikbaar is, wordt het veld weergegeven als `<friendly-name>(<name>)`. Als er geen beschrijvende naam beschikbaar is, wordt de weergavenaam weergegeven, bijvoorbeeld `<display-name>(<name>)`. Als geen van deze waarden is gedefinieerd, wordt alleen de technische naam van het veld weergegeven: `<name>`.

>[!NOTE]
>
>De beschrijvende namen worden niet opgehaald wanneer u velden selecteert uit een samenvoeging van schema’s.