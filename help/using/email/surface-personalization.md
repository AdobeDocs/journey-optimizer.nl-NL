---
solution: Journey Optimizer
product: journey optimizer
title: Instellingen van e-mailoppervlak aanpassen
description: Leer hoe u gepersonaliseerde waarden voor uw instellingen definieert op het oppervlakniveau van het e-mailkanaal
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: instellingen, e-mail, configuratie, subdomein
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: 513fddf21eaf7958df45d97f028103519c77ec44
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Instellingen van e-mailoppervlak aanpassen {#surface-personalization}

Voor meer flexibiliteit en controle over uw e-mailinstellingen [!DNL Journey Optimizer] kunt u gepersonaliseerde waarden voor subdomeinen en kopballen bepalen<!--and URL tracking parameters--> bij het maken van e-mailoppervlakken.

>[!AVAILABILITY]
>
>Deze mogelijkheid is momenteel beschikbaar als een bètaversie om alleen gebruikers te selecteren. <!--To join the beta program, contact Adobe Customer Care.-->

## Dynamische subdomeinen toevoegen {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalisatie niet beschikbaar"
>abstract="Dit oppervlak is gemaakt zonder personalisatiekenmerken. Raadpleeg de documentatie voor stappen die u kunt oplossen als personalisatie vereist is."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Dynamische subdomeinen inschakelen"
>abstract="Wanneer u een e-mailoppervlak maakt, kunt u dynamische subdomeinen instellen op basis van voorwaarden die u definieert met de Expressieeditor. U kunt maximaal 50 dynamische subdomeinen toevoegen."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Sommige subdomeinen zijn mogelijk niet beschikbaar"
>abstract="Bepaalde subdomeinen zijn momenteel niet beschikbaar voor selectie vanwege de registratie van de feedbacklus die in behandeling is. Dit proces kan tot 10 werkdagen duren. Na voltooiing kunt u kiezen uit alle beschikbare subdomeinen."

Wanneer u een e-mailoppervlak maakt, kunt u dynamische subdomeinen instellen op basis van specifieke voorwaarden.

Als u bijvoorbeeld juridische beperkingen hebt om berichten van een specifiek e-mailadres per land te verzenden, kunt u dynamische subdomeinen gebruiken. Hierdoor kunt u één oppervlak maken met verschillende verzendende subdomeinen die overeenkomen met verschillende landen, in plaats van meerdere oppervlakken voor elk land te maken. Vervolgens kunt u zich richten op klanten die in verschillende landen zijn gevestigd en in één campagne zijn geconsolideerd.

Voer de onderstaande stappen uit om dynamische subdomeinen in een oppervlak van een e-mailkanaal te definiëren.

1. Voordat u een oppervlak maakt, stelt u de subdomeinen in die u wilt gebruiken voor het verzenden van e-mails volgens uw gebruiksscenario. [Meer informatie](../configuration/about-subdomain-delegation.md)

   Stel bijvoorbeeld dat u verschillende subdomeinen wilt gebruiken voor verschillende landen: één subdomein instellen dat specifiek is voor de VS, één specifiek voor het Verenigd Koninkrijk, enzovoort.

1. Maak een kanaaloppervlak. [Meer informatie](../configuration/channel-surfaces.md)

1. Selecteer de **[!UICONTROL Email]** kanaal.

1. In de **Subdomein** in, schakelt u de **[!UICONTROL Dynamic Subdomain]** -optie.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Selecteer het pictogram Bewerken naast de eerste **[!UICONTROL Condition]** veld.

1. De [Expressieeditor](../personalization/personalization-build-expressions.md) wordt geopend. In dit voorbeeld stelt u een voorwaarde in, zoals `Country` equals `US`.

   ![](assets/surface-email-edit-condition.png)

1. Selecteer het subdomein dat u aan deze voorwaarde wilt koppelen. [Meer informatie over subdomeinen](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Bepaalde subdomeinen zijn momenteel niet beschikbaar voor selectie vanwege hangende [feedbacklus](../reports/deliverability.md#feedback-loops) registratie. Dit proces kan tot 10 werkdagen duren. Na voltooiing kunt u kiezen uit alle beschikbare subdomeinen. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Alle ontvangers die in de VS zijn gebaseerd, ontvangen berichten die het geselecteerde subdomein voor dat land gebruiken. Dit houdt in dat alle betrokken URL&#39;s (zoals spiegel, URL volgen of koppeling opzeggen) worden ingevuld op basis van dat subdomein.

1. Stel andere dynamische subdomeinen naar wens in. Je kunt maximaal 50 objecten toevoegen.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the surface. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. Alle andere definiëren [e-mailinstellingen](email-settings.md) en [indienen](../configuration/channel-surfaces.md#create-channel-surface) uw oppervlak.

Nadat u een of meer dynamische subdomeinen aan een oppervlak hebt toegevoegd, worden de volgende items gevuld op basis van het opgeloste dynamische subdomein voor dit oppervlak:

* Alle URL&#39;s (bron-URL, spiegel-URL en URL voor bijhouden)

* De [abonnement-URL opzeggen](email-settings.md#list-unsubscribe)

* De **Van e-mail** en **Foutbericht** achtervoegsels

>[!NOTE]
>
>Als u dynamische subdomeinen instelt en vervolgens de optie **[!UICONTROL Dynamic Subdomain]** worden alle dynamische waarden verwijderd. Selecteer een subdomein en verzend het oppervlak waarop de wijzigingen van kracht moeten worden.

## De koptekst personaliseren {#personalize-header}

U kunt ook personalisatie gebruiken voor alle headerparameters die in een oppervlak zijn gedefinieerd.

Als u bijvoorbeeld meerdere merken hebt, kunt u één oppervlak maken en gepersonaliseerde waarden gebruiken voor uw e-mailkopteksten. Op deze manier kunt u ervoor zorgen dat alle e-mails die van uw verschillende merken worden verzonden, met de juiste naam naar elk van uw klanten worden verzonden **Van** namen en e-mails. Wanneer de ontvangers op dezelfde manier op de knop klikken **Antwoord** in hun e-mailclientsoftware wilt **Reageren op** namen en e-mails komen overeen met het juiste merk voor de juiste gebruiker.

Volg onderstaande stappen om gepersonaliseerde variabelen voor de parameters van de oppervlaktekop te gebruiken.

>[!NOTE]
>
>U kunt alles personaliseren **[!UICONTROL Header parameters]** velden, behalve de **[!UICONTROL Error email prefix]** veld.


1. Definieer de headerparameters zoals u dat gewoonlijk doet. [Meer informatie](email-settings.md#email-header)

1. Selecteer voor elk veld het pictogram Bewerken.

   ![](assets/surface-email-personalize-header.png)

1. De [Expressieeditor](../personalization/personalization-build-expressions.md) wordt geopend. Bepaal uw voorwaarde zoals gewenst en sla uw wijzigingen op.

   Stel bijvoorbeeld een voorwaarde in, zodat elke ontvanger een e-mail ontvangt van zijn eigen merkvertegenwoordiger.

   >[!NOTE]
   >
   >U kunt alleen **[!UICONTROL Profile attributes]** en **[!UICONTROL Helper functions]**.

1. Herhaal bovenstaande stappen voor elke parameter waaraan u personalisatie wilt toevoegen.

>[!NOTE]
>
>Als u een of meer dynamische subdomeinen aan uw oppervlak hebt toegevoegd, **Van e-mail** en **Foutbericht** achtervoegsels worden gevuld op basis van de oplossing [dynamisch subdomein](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Details oppervlak weergeven {#view-surface-details}

Wanneer u een oppervlak gebruikt met gepersonaliseerde instellingen in een campagne of een oppervlak, kunt u de oppervlakdetails direct weergeven binnen de campagne of het oppervlak. Voer de onderstaande stappen uit.

1. Een e-mail maken [campagne](../campaigns/create-campaign.md) of [reis](../building-journeys/journey-gs.md).

1. Selecteer de knop **[!UICONTROL Edit content]**.

1. Klik op de knop **[!UICONTROL View surface details]**.

   ![](assets/campaign-view-surface-details.png)

1. De **[!UICONTROL Delivery settings]** wordt weergegeven. U kunt alle oppervlakmontages, met inbegrip van dynamische subdomeinen en gepersonaliseerde kopbalparameters bekijken.

   >[!NOTE]
   >
   >Alle informatie op dit scherm is alleen-lezen.

1. Selecteren **[!UICONTROL Expand]** om de details van de dynamische subdomeinen weer te geven.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
