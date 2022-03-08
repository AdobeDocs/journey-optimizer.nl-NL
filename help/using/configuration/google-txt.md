---
title: Een Google TXT-record toevoegen aan een subdomein
description: Leer hoe u een Google TXT-record aan een subdomein kunt toevoegen
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 26%

---

# Een Google TXT-record toevoegen aan een subdomein {#google-txt-record}

TXT-records zijn DNS-records die worden gebruikt om tekstgegevens over een domein te verstrekken en die kunnen worden gelezen door externe bronnen.

Om ervoor te zorgen dat de e-mails naar Gmail-adressen goed kunnen worden afgeleverd en succesvol kunnen worden verzonden, [!DNL Journey Optimizer] Hiermee kunt u speciale TXT-records voor verificatie van de Google-site toevoegen aan uw subdomeinen om te controleren of deze zijn geverifieerd.

>[!CAUTION]
>
> Deze bewerking kan alleen worden uitgevoerd als een subdomein het **[!UICONTROL Success]** status. Raadpleeg voor meer informatie over de status van subdomeinen [deze sectie](access-subdomains.md).

Ga als volgt te werk om een Google TXT-record aan uw subdomein toe te voegen:

1. Het subdomein openen vanuit het dialoogvenster **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** -menu.

1. In de **[!UICONTROL Google txt record]** de verificatiecode invoeren die is gegenereerd op basis van [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->en klik vervolgens op **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. Nadat de TXT-record is toegevoegd, moet u deze door Google laten verifiëren. Navigeer om dit te doen naar [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->en start vervolgens de verificatiestap.
