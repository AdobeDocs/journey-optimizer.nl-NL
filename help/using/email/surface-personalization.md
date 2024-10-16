---
solution: Journey Optimizer
product: journey optimizer
title: Instellingen voor e-mailconfiguratie aanpassen
description: Leer hoe u persoonlijke waarden voor uw instellingen definieert op het niveau van de configuratie van het e-mailkanaal
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: instellingen, e-mail, configuratie, subdomein
badge: label="Beperkte beschikbaarheid"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: f8a6c2a3b27d5dca422dfdc868f802c6a10b001d
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Instellingen voor e-mailconfiguratie aanpassen {#surface-personalization}

Voor meer flexibiliteit en controle over uw e-mailmontages, [!DNL Journey Optimizer] staat u toe om gepersonaliseerde waarden voor subdomeinen en kopballen te bepalen <!--and URL tracking parameters--> wanneer het creëren van e-mailconfiguraties.

>[!AVAILABILITY]
>
>Aanpassing van de e-mailconfiguratie is momenteel alleen beschikbaar voor een aantal organisaties (beperkte beschikbaarheid). Neem contact op met uw Adobe als u toegang wilt.

## Dynamische subdomeinen toevoegen {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalization niet beschikbaar"
>abstract="Deze configuratie is gemaakt zonder personalisatiekenmerken. Raadpleeg de documentatie voor stappen die u kunt oplossen als personalisatie vereist is."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Dynamische subdomeinen inschakelen"
>abstract="Wanneer u een e-mailconfiguratie maakt, kunt u dynamische subdomeinen instellen op basis van voorwaarden die u met de verpersoonlijkingseditor definieert. U kunt maximaal 50 dynamische subdomeinen toevoegen."

Wanneer u een e-mailconfiguratie maakt, kunt u dynamische subdomeinen instellen op basis van specifieke voorwaarden.

Als u bijvoorbeeld juridische beperkingen hebt om berichten van een specifiek e-mailadres per land te verzenden, kunt u dynamische subdomeinen gebruiken. Dit staat u toe om één enkele configuratie met verscheidene verzendende subdomeinen te creëren die aan verschillende landen beantwoorden - in plaats van het creëren van veelvoudige configuraties voor elk land. Vervolgens kunt u zich richten op klanten die in verschillende landen zijn gevestigd en in één campagne zijn geconsolideerd.

Voer de onderstaande stappen uit om dynamische subdomeinen te definiëren in een configuratie van een e-mailkanaal.

1. Voordat u een configuratie maakt, stelt u de subdomeinen in die u wilt gebruiken voor het verzenden van e-mails volgens uw gebruiksscenario. [ leer hoe ](../configuration/about-subdomain-delegation.md)

   Stel bijvoorbeeld dat u verschillende subdomeinen wilt gebruiken voor verschillende landen: één subdomein instellen dat specifiek is voor de VS, één specifiek voor het Verenigd Koninkrijk, enzovoort.

1. Maak een kanaalconfiguratie. [ leer hoe ](../configuration/channel-surfaces.md)

1. Selecteer het kanaal **[!UICONTROL Email]** .

1. In de **Subdomain** sectie, laat de **[!UICONTROL Dynamic Subdomain]** optie toe.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Selecteer het pictogram Bewerken naast het eerste veld **[!UICONTROL Condition]** .

1. De [ verpersoonlijkingsredacteur ](../personalization/personalization-build-expressions.md) opent. In dit voorbeeld stelt u een voorwaarde in, bijvoorbeeld `Country` is gelijk aan `US` .

   ![](assets/surface-email-edit-condition.png)

1. Selecteer het subdomein dat u aan deze voorwaarde wilt koppelen. [ leer meer op subdomeinen ](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Bepaalde subdomeinen zijn momenteel niet beschikbaar voor selectie toe te schrijven aan hangende [ terugkoppel lijn ](../reports/deliverability.md#feedback-loops) registratie. Dit proces kan tot 10 werkdagen duren. Na voltooiing kunt u kiezen uit alle beschikbare subdomeinen. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Alle ontvangers die in de VS zijn gebaseerd, ontvangen berichten die het geselecteerde subdomein voor dat land gebruiken. Dit houdt in dat alle betrokken URL&#39;s (zoals spiegel, URL volgen of koppeling opzeggen) worden ingevuld op basis van dat subdomein.

1. Stel andere dynamische subdomeinen naar wens in. Je kunt maximaal 50 objecten toevoegen.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the configuration. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. Bepaal alle andere [ e-mailmontages ](email-settings.md) en [ voorleggen ](../configuration/channel-surfaces.md#create-channel-surface) uw configuratie.

Nadat u een of meer dynamische subdomeinen aan een configuratie hebt toegevoegd, worden de volgende items gevuld op basis van het opgeloste dynamische subdomein voor deze configuratie:

* Alle URL&#39;s (bron-URL, spiegel-URL en URL voor bijhouden)

* [ unsubscribe URL ](email-settings.md#list-unsubscribe)

* **van e-mail** en **E-mail van de Fout** achtervoegsels

>[!NOTE]
>
>Als u dynamische subdomeinen instelt en vervolgens de optie **[!UICONTROL Dynamic Subdomain]** uitschakelt, worden alle dynamische waarden verwijderd. Selecteer een subdomein en verzend de configuratie voor de veranderingen om van kracht te worden.

## De koptekst personaliseren {#personalize-header}

U kunt verpersoonlijking voor alle kopbalparameters ook gebruiken die in een configuratie worden bepaald.

Als u bijvoorbeeld meerdere merken hebt, kunt u één configuratie maken en gepersonaliseerde waarden gebruiken voor uw e-mailkopteksten. Dit staat u toe om ervoor te zorgen dat alle e-mails die van uw verschillende merken worden verzonden aan elk van uw klanten met het correcte **van** namen en e-mails worden gericht. Op dezelfde manier wanneer uw ontvangers de **knoop van het Antwoord** in hun software van de e-mailcliënt raken, wilt u **antwoorden aan** namen en e-mails beantwoorden aan het correcte merk voor de juiste gebruiker.

Volg onderstaande stappen om gepersonaliseerde variabelen voor de parameters van de configuratiekopbal te gebruiken.

>[!NOTE]
>
>U kunt alle **[!UICONTROL Header parameters]** -velden aanpassen, behalve het **[!UICONTROL Error email prefix]** -veld.


1. Definieer de headerparameters zoals u dat gewoonlijk doet. [ leer hoe ](email-settings.md#email-header)

1. Selecteer voor elk veld het pictogram Bewerken.

   ![](assets/surface-email-personalize-header.png)

1. De [ verpersoonlijkingsredacteur ](../personalization/personalization-build-expressions.md) opent. Bepaal uw voorwaarde zoals gewenst en sla uw wijzigingen op.

   Stel bijvoorbeeld een voorwaarde in, zodat elke ontvanger een e-mail ontvangt van zijn eigen merkvertegenwoordiger.

   >[!NOTE]
   >
   >U kunt alleen **[!UICONTROL Profile attributes]** en **[!UICONTROL Helper functions]** selecteren.

1. Herhaal bovenstaande stappen voor elke parameter waaraan u personalisatie wilt toevoegen.

>[!NOTE]
>
>Als u één of meerdere dynamische subdomeinen aan uw configuratie toevoegde, zullen **van e-mail** en **achtervoegsels van de Fout e-mail** worden bevolkt gebaseerd op het opgeloste [ dynamische subdomain ](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the personalization editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Configuratiedetails weergeven {#view-surface-details}

Wanneer het gebruiken van een configuratie met gepersonaliseerde montages in een campagne of een configuratie, kunt u de configuratiedetails direct binnen de campagne of de configuratie tonen. Voer de onderstaande stappen uit.

1. Creeer een e-mail [ campagne ](../campaigns/create-campaign.md) of [ reis ](../building-journeys/journey-gs.md).

1. Selecteer de knop **[!UICONTROL Edit content]**.

1. Klik op de knop **[!UICONTROL View configuration details]**.

   ![](assets/campaign-view-surface-details.png)

1. Het venster **[!UICONTROL Delivery settings]** wordt weergegeven. U kunt alle configuratiemontages, met inbegrip van dynamische subdomeinen en gepersonaliseerde kopbalparameters bekijken.

   >[!NOTE]
   >
   >Alle informatie op dit scherm is alleen-lezen.

1. Selecteer **[!UICONTROL Expand]** om de details van de dynamische subdomeinen weer te geven.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
