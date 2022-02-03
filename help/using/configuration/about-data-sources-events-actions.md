---
title: Beheer en instellingen
description: Meer informatie over richtlijnen voor beheer en instellingen
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 45%

---

# Reizen configureren {#configure-journeys}

Om berichten met reizen te verzenden, moet u vormen **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** en **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

## Gegevensbronnen

De configuratie van de Gegevensbron staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw reizen zal worden gebruikt. [Meer informatie](../../using/datasource/about-data-sources.md)

## Gebeurtenissen

Gebeurtenissen stellen u in staat om uw reizen tijdelijk te activeren en berichten in real-time te verzenden aan de persoon die de reis maakt.

In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De gegevens van de binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen zijn afkomstig van de streamingopname-API’s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). [Meer informatie](../../using/event/about-events.md)

## Acties

Journey Optimizer-berichtmogelijkheden zijn ingebouwd: u hoeft alleen uw inhoud te ontwerpen en uw bericht te publiceren. Als u berichten verzendt met een systeem van derden, kunt u een aangepaste handeling maken. [Meer informatie](../../using/action/action.md)

## Bladeren door Adobe Experience Platform-velden {#friendly-names-display}

Bij het definiëren van een [gebeurtenispayload](../event/about-creating.md#define-the-payload-fields), een [veldengroep-payload](../datasource/configure-data-sources.md#define-field-groups) en het selecteren van velden in de [expressie-editor](../building-journeys/expression/expressionadvanced.md) wordt naast de veldnaam ook de weergavenaam weergegeven. Deze informatie wordt opgehaald uit de schemadefinitie in het Gegevenservaringmodel.

Als er beschrijvingen als xdm:alternateDisplayInfo worden opgegeven tijdens het instellen van schema’s, worden de weergavenamen vervangen door de gebruikersvriendelijke namen. Dit is vooral handig wanneer u werkt met &quot;eVars&quot; en algemene velden. U kunt beschrijvers van vriendschappelijke namen via een API vraag vormen. Zie voor meer informatie de [Handleiding voor ontwikkelaars van het schema Register](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html){target=&quot;_blank&quot;}.

![](../assets/xdm-from-descriptors.png)

Als een beschrijvende naam beschikbaar is, wordt het veld weergegeven als `<friendly-name>(<name>)`. Als er geen beschrijvende naam beschikbaar is, wordt de weergavenaam weergegeven, bijvoorbeeld `<display-name>(<name>)`. Als geen van deze waarden is gedefinieerd, wordt alleen de technische naam van het veld weergegeven: `<name>`.

>[!NOTE]
>
>De beschrijvende namen worden niet opgehaald wanneer u velden selecteert uit een samenvoeging van schema’s.
