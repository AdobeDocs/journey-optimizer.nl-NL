---
title: Gedelegeerde subdomeinen benaderen
description: Leer hoe u gedelegeerde subdomeinen kunt openen.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# Gedelegeerde subdomeinen benaderen {#access-delegated-subdomains}

Alle gedelegeerde subdomeinen worden weergegeven in het dialoogvenster **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** -menu. Er zijn filters beschikbaar waarmee u de lijst (datum van delegatie, gebruiker of status) kunt verfijnen.

![](assets/subdomain-list.png)

De **[!UICONTROL Status]** de kolom verstrekt informatie over het subdomain delegatieproces:

* **[!UICONTROL Draft]**: De subdomeindelegatie is opgeslagen als een concept. Klik op de subdomeinnaam om het delegatieproces te hervatten.
* **[!UICONTROL Processing]**: Het subdomein gaat door verscheidene configuratiecontroles alvorens het kan worden gebruikt,
* **[!UICONTROL Success]**: Het subdomein is door de controles met succes gegaan en kan worden gebruikt om berichten te leveren,
* **[!UICONTROL Failed]**: Een of meer controles zijn mislukt nadat de subdomeindelegatie is verzonden.

Als u toegang wilt tot gedetailleerde informatie over een subdomein, opent u het subdomein in de lijst. U kunt:

* Haal de subdomeinnaam (read-only) op die tijdens het delegatieproces wordt gevormd, evenals geproduceerde URLs (middelen, spiegelpagina&#39;s, het volgen URLs),

* Voeg een TXT-record voor verificatie van de Google-site toe aan uw subdomein om te controleren of deze is geverifieerd (zie [Een Google TXT-record toevoegen aan een subdomein](google-txt.md)).

![](assets/subdomain-delegated.png)
