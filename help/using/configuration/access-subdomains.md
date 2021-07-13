---
title: Subdomeinen delegeren
description: Leer hoe u uw subdomeinen kunt delegeren
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
feature: Applicatie-instellingen
topic: Beheer
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---


# Gedelegeerde subdomeinen benaderen

Alle gedelegeerde subdomeinen worden weergegeven in het menu **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**. Er zijn filters beschikbaar waarmee u de lijst (datum van delegatie, gebruiker of status) kunt verfijnen.

![](../assets/subdomain-list.png)

De **[!UICONTROL Status]** kolom verstrekt informatie over het subdomain delegatieproces:

* **[!UICONTROL Draft]**: De subdomeindelegatie is opgeslagen als een concept. Klik op de subdomeinnaam om het delegatieproces te hervatten.
* **[!UICONTROL Processing]**: Het subdomein gaat door verscheidene configuratiecontroles alvorens het kan worden gebruikt,
* **[!UICONTROL Success]**: Het subdomein is door de controles met succes gegaan en kan worden gebruikt om berichten te leveren,
* **[!UICONTROL Failed]**: Een of meer controles zijn mislukt nadat de subdomeindelegatie is verzonden.

Als u toegang wilt tot gedetailleerde informatie over een subdomein, opent u het subdomein in de lijst. U kunt:

* Haal de subdomeinnaam (read-only) op die tijdens het delegatieproces wordt gevormd, evenals geproduceerde URLs (middelen, spiegelpagina&#39;s, het volgen URLs),

* Voeg een TXT-record voor Google-siteverificatie toe aan uw subdomein om te controleren of dit is geverifieerd (zie [Een Google TXT-record toevoegen aan een subdomein](google-txt.md)).

![](../assets/subdomain-delegated.png)
