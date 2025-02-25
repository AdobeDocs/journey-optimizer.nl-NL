---
solution: Journey Optimizer
product: journey optimizer
title: Reizen configureren
description: Leer hoe te om Gegevensbronnen, Gebeurtenissen en Acties te vormen
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: configuratie, reis, dashboard, gegevensbronnen, gebeurtenissen, acties
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 30%

---

# Gegevensbronnen, gebeurtenissen en handelingen configureren {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="Informatie over reisconfiguratie"
>abstract="Om berichten met reizen te verzenden, moet u Gegevensbronnen, Gebeurtenissen en Acties vormen. Met behulp van gegevensbronnen kunt u een verbinding met een systeem definiëren om aanvullende informatie op te halen die tijdens uw reizen wordt gebruikt, bijvoorbeeld onder uw omstandigheden. Met gebeurtenissen kunt u uw reizen starten wanneer een gebeurtenis wordt ontvangen. Met aangepaste acties kunt u verbinding maken met een systeem van derden om uw berichten te verzenden. Als u ingebouwde berichtmogelijkheden van Journey Optimizer gebruikt, hoeft u geen actie te configureren."

Als u berichten met ritten wilt verzenden, moet u **[!UICONTROL Data Sources]** , **[!UICONTROL Events]** en **[!UICONTROL Actions]** configureren.

![](assets/admin-menu.png)

## Gegevensbronnen {#data-sources}

Met de configuratie Data Source kunt u een verbinding met een systeem definiëren om aanvullende informatie op te halen die tijdens uw reizen wordt gebruikt. [Meer informatie](../../using/datasource/about-data-sources.md)

## Gebeurtenissen {#events}

Gebeurtenissen stellen u in staat om uw reizen tijdelijk te activeren en berichten in real-time te verzenden aan de persoon die de reis maakt.

In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De gegevens van de binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen komen van de Streaming Ingestie-API&#39;s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). [Meer informatie](../../using/event/about-events.md)

## Acties {#actions}

Journey Optimizer-berichtmogelijkheden zijn ingebouwd: u hoeft alleen een kanaalactie-activiteit aan uw reis toe te voegen. Als u berichten verzendt met een systeem van derden, kunt u een aangepaste handeling maken. [Meer informatie](../../using/action/action.md)

## Bladeren door Adobe Experience Platform-velden {#friendly-names-display}

Bij het definiëren van een [gebeurtenispayload](../event/about-creating.md#define-the-payload-fields), een [veldengroep-payload](../datasource/configure-data-sources.md#define-field-groups) en het selecteren van velden in de [expressie-editor](../building-journeys/expression/expressionadvanced.md) wordt naast de veldnaam ook de weergavenaam weergegeven. Deze informatie wordt opgehaald uit de schemadefinitie in het Gegevenservaringmodel.

Als er beschrijvingen als xdm:alternateDisplayInfo worden opgegeven tijdens het instellen van schema’s, worden de weergavenamen vervangen door de gebruikersvriendelijke namen. Dit is vooral handig wanneer u werkt met &quot;eVars&quot; en algemene velden. U kunt beschrijvers van vriendschappelijke namen via een API vraag vormen. Voor meer informatie, zie de [ gids van de de ontwikkelaar van de Registratie van het Schema ](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html) {target="_blank"}.

![](assets/xdm-from-descriptors.png)

Als een beschrijvende naam beschikbaar is, wordt het veld weergegeven als `<friendly-name>(<name>)`. Als er geen beschrijvende naam beschikbaar is, wordt de weergavenaam weergegeven, bijvoorbeeld `<display-name>(<name>)`. Als geen van deze waarden is gedefinieerd, wordt alleen de technische naam van het veld weergegeven: `<name>`.

>[!NOTE]
>
>De beschrijvende namen worden niet opgehaald wanneer u velden selecteert uit een samenvoeging van schema’s.
