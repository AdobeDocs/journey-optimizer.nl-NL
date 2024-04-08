---
solution: Journey Optimizer
product: journey optimizer
title: Dynamische e-mailsubdomeinen configureren
description: Leer hoe te om dynamische subdomeinen op het oppervlakniveau van het e-mailkanaal te vormen
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: instellingen, e-mail, configuratie, subdomein
hide: true
hidefromtoc: true
source-git-commit: c082d9329949fd8dc68929e3934daf2d9dfdbd46
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Dynamische e-mailsubdomeinen configureren {#surface-personalization}

Voor meer flexibiliteit en controle over uw e-mailinstellingen bij het maken van e-mailoppervlakken [!DNL Journey Optimizer] Hiermee kunt u gepersonaliseerde waarden definiëren voor subdomeinen, kopteksten en URL-volgparameters.

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

Voer de onderstaande stappen uit om dynamische subdomeinen te definiëren.

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

   Alle ontvangers die in de Verenigde Staten zijn gebaseerd, ontvangen berichten die het geselecteerde subdomein voor dat land gebruiken. Dit houdt in dat alle betrokken URL&#39;s (zoals de spiegelpagina, de URL die wordt gevolgd of de koppeling die het abonnement opzegt) worden ingevuld op basis van dat subdomein.

1. Stel het andere dynamische subdomein naar wens in. Je kunt maximaal 50 objecten toevoegen.

   ![](assets/surface-email-add-dynamic-subdomain.png)

1. Selecteer de [IP-pool](../configuration/ip-pools.md) aan het oppervlak te koppelen. [Meer informatie](email-settings.md#subdomains-and-ip-pools)

Nadat u een of meer dynamische subdomeinen aan een oppervlak hebt toegevoegd, worden de volgende items gevuld op basis van het opgeloste dynamische subdomein voor dit oppervlak:

* Alle URL&#39;s (bron-URL, spiegel-URL en URL voor bijhouden)

* De [abonnement-URL opzeggen](email-settings.md#list-unsubscribe)

* De **Van e-mail** en **Foutbericht** achtervoegsels

## Uw header personaliseren (#personalize-header)

U kunt ook personalisatie gebruiken voor alle headerparameters die in een oppervlak zijn gedefinieerd.

Als u bijvoorbeeld meerdere merken hebt, kunt u één oppervlak maken en gepersonaliseerde waarden gebruiken voor uw e-mailkopteksten. Op deze manier kunt u ervoor zorgen dat alle e-mails die van uw verschillende merken worden verzonden, met de juiste naam naar elk van uw klanten worden verzonden **Van** namen en e-mails. Wanneer de ontvangers op dezelfde manier op de knop klikken **Antwoord** in hun e-mailclientsoftware wilt **Reageren op** namen en e-mails komen overeen met het juiste merk voor de juiste gebruiker.

Volg onderstaande stappen om gepersonaliseerde variabelen voor de parameters van de oppervlaktekop te gebruiken.

1. Definieer de headerparameters zoals u dat gewoonlijk doet. [Meer informatie](email-settings.md#email-header)

1. Selecteer voor elk veld het pictogram Bewerken.

   ![](assets/surface-email-personalize-header.png)

1. De [Expressieeditor](../personalization/personalization-build-expressions.md) wordt geopend. Bepaal uw voorwaarde zoals gewenst en sla uw wijzigingen op.<!--In this example, set a condition such as -->

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

select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->
