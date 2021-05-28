---
title: Technische instellingen
description: Meer informatie over richtlijnen voor beheer en instellingen
hidefromtoc: true
hide: true
source-git-commit: 8a94c63b4a0cba1014e9778caa24720fb975ae52
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 6%

---

# Technische instellingen

![](../assets/do-not-localize/badge.png)

## Brandingparameters instellen{#cjm-branding}

Elk bedrijf heeft visuele en technische richtlijnen voor de merkidentiteit. U kunt een reeks specificaties bepalen om een verenigbaar merk aan uw klanten, van logo&#39;s aan technische aspecten, zoals e-mailafzender, het domein van de URL van de spiegelpagina&#39;s, of de montages van het berichtvolgen voor te stellen.
Merken kunnen niet door eindgebruikers worden gemaakt of gewijzigd: deze configuratie wordt beheerd door Adobe.

Als u brandingparameters wilt instellen voor uw [!DNL Journey Optimizer]-instantie, moet u contact opnemen met Adobe en de volgende gegevens delen:

* Bedrijfsnaam

* E-mailadres van afzender (Van)

* Naam afzender (Van)

* Reageren op adres

Zodra branding parameters zijn gevormd, zult u hen kunnen selecteren wanneer het creëren van berichten.

Zodra branding parameters zijn gevormd, zult u hen kunnen selecteren wanneer het creëren van berichten van de **[!UICONTROL Presets]** lijst. [Meer weten over het maken](../create-message.md) van inhoud?

## Het pushmeldingskanaal configureren

Leer hoe te om drukkanaal in dit [sectie](../create-push.md) te vormen.

## Subdomeindelegatie

Voor om het even welk nieuw subdomain dat in [!DNL Journey Optimizer] moet worden gebruikt, zal de eerste stap zijn het te delegeren. Je moet contact opnemen met je Adobe technische contact.

Bij het implementeren van een oplossing gelden er vereisten voor naar buiten gerichte onderdelen: het gaat hierbij onder andere om het instellen van koppelingen en webpagina&#39;s die moeten worden bijgehouden, het weergeven van spiegelpagina&#39;s, enz.

Hoewel deze vereisten worden beheerd via componenten die door zowel Adobe als de klant worden gehost, bevatten ze URL&#39;s die door de ontvangers van de e-mails kunnen worden bekeken.  Om te voorkomen dat URL&#39;s de onderliggende technische oplossing of hostingprovider aangeven, kunnen subdomeinen worden ingesteld om dit transparant te maken voor de ontvangers van de e-mails.

Na deze delegaties zorgt de infrastructuur die door Adobe wordt opgezet ervoor dat de volgende diensten voor elk gedelegeerd of CNAME-aliased verzendend domein worden uitgevoerd:

* Maken van postmaster@ en misbruik@-postvakken

* Opstelling van terugkoppellijnen voor het gedelegeerde domein

* Basic DMARC-recordconfiguratie

De parameters door Adobe worden bepaald zijn slechts geldig vanaf het tijdstip dat de delegatie werd voltooid en dan door Adobe werd geverifieerd, en blijven functioneel.

[Meer informatie over domeindelegatie](https://helpx.adobe.com/nl/campaign/kb/domain-name-delegation.html).


## Gegevensbronnen, gebeurtenissen en handelingen maken

Met de sectie **[!UICONTROL Admin]** kunt u **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** en **[!UICONTROL Actions]** beheren.

![](../assets/admin-menu.png)

### Databronnen

De configuratie van de Gegevensbron staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw reizen zal worden gebruikt.

Meer informatie over gegevensbronnen vindt u in deze [sectie](../datasource/about-data-sources.md)

### Gebeurtenissen

Gebeurtenissen stellen u in staat om uw reizen tijdelijk te activeren en berichten in real-time te verzenden aan de persoon die de reis maakt.

In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De gegevens van de binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen zijn afkomstig van de streamingopname-API’s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen).

Meer informatie over gebeurtenissen in deze [sectie](../event/about-events.md)

### Acties

[!DNL Journey Optimizer] berichtmogelijkheden zijn ingebouwd: u hoeft alleen uw inhoud te ontwerpen en uw bericht te publiceren. Als u berichten verzendt met een systeem van derden, kunt u een aangepaste handeling maken.

Meer informatie over handelingen in deze [sectie](../action/action.md)
