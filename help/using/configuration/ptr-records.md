---
title: PTR-records
description: '"Leer hoe u ptr-records beheert"'
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
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 1%

---


# PTR-records

## PTR-records

Een wijzerverslag (PTR) is een type van het verslag van het Systeem van de Naam van het Domein (DNS) dat de domeinnaam verbonden aan een IP adres verstrekt.

Met PTR verslagen, kunnen het ontvangen van postservers de authenticiteit van het verzenden van postservers controleren door te identificeren of hun IP adressen aan de namen beantwoorden waarmee de servers verbinden.

## De PTR-records van uw subdomeinen openen

Zodra een subdomein in het Beheer van de Reis van de Klant wordt gedelegeerd, wordt een PTR- verslag automatisch gecreeerd en met dit subdomein geassocieerd. U hebt toegang tot dit bestand via het menu **[!UICONTROL Channels]** / **[!UICONTROL PTR records]**.

![](../assets/ptr-records.png)

In de lijst worden de PTR-records weergegeven die voor elk gedelegeerd subdomein zijn gegenereerd. Hierbij wordt de volgende syntaxis gebruikt:

* &quot;r&quot; voor opnamen,
* &quot;xx&quot; voor de twee laatste cijfers van het IP-adres,
* subdomeinnaam.

U kunt een PTR-record in de lijst openen om de bijbehorende subdomeinnaam en het IP-adres weer te geven.

>[!NOTE]
>
>Merk op dat de PTR- verslagen read-only zijn en dat u subdomain niet kunt wijzigen verbonden aan een IP adres.
