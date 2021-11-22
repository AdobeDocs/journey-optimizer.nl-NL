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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 24%

---

# Een Google TXT-record toevoegen aan een subdomein

TXT-records zijn DNS-records die worden gebruikt om tekstgegevens over een domein te verstrekken en die kunnen worden gelezen door externe bronnen.

Met het beheer van de reizen van de klant kunt u speciale TXT-records voor de verificatie van de Google-site toevoegen aan uw subdomeinen om ervoor te zorgen dat deze worden geverifieerd, zodat u zeker bent van een goede leverantie en e-mail naar de Gmail-adressen.

>[!NOTE]
>
> Deze bewerking kan alleen worden uitgevoerd als een subdomein het **[!UICONTROL Success]** status. Raadpleeg voor meer informatie over de status van subdomeinen [deze sectie](access-subdomains.md).

Ga als volgt te werk om een Google TXT-record aan uw subdomein toe te voegen:

1. Het subdomein openen vanuit het dialoogvenster **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** -menu.

1. Voer in de sectie TXT-record van Google de verificatiecode in die is gegenereerd in [G Suite-beheerprogramma&#39;s](https://support.google.com/a/answer/183895)en klik vervolgens op **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. Nadat de TXT-record is toegevoegd, moet u deze door Google laten verifiëren. Navigeer hiertoe naar de G Suite Admin-hulpprogramma&#39;s en start vervolgens de verificatiestap.
