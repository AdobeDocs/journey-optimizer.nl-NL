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
source-wordcount: '168'
ht-degree: 26%

---


# Een Google TXT-record toevoegen aan een subdomein

TXT-records zijn DNS-records die worden gebruikt om tekstgegevens over een domein te verstrekken en die kunnen worden gelezen door externe bronnen.

Met het beheer van de reizen van de klant kunt u speciale TXT-records voor de verificatie van de Google-site toevoegen aan uw subdomeinen om ervoor te zorgen dat deze worden geverifieerd, zodat u zeker bent van een goede leverantie en e-mailadressen.

>[!NOTE]
>
> Deze bewerking kan alleen worden uitgevoerd wanneer een subdomein de status **[!UICONTROL Success]** heeft. Raadpleeg [deze sectie](access-subdomains.md) voor meer informatie over de status van subdomeinen.

Ga als volgt te werk om een Google TXT-record aan uw subdomein toe te voegen:

1. Open het subdomein vanuit het menu **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**.

1. Voer in de sectie met de Google-tekstrecord de verificatiecode in die wordt gegenereerd in [G Suite Admin Tools](https://support.google.com/a/answer/183895) en klik vervolgens op **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. Nadat de TXT-record is toegevoegd, moet u deze door Google laten verifiëren. Navigeer hiertoe naar de G Suite Admin-hulpprogramma&#39;s en start vervolgens de verificatiestap.
