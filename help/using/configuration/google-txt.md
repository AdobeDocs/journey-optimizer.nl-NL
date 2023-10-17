---
solution: Journey Optimizer
product: journey optimizer
title: Een Google TXT-record toevoegen aan een subdomein
description: Leer hoe u een Google TXT-record aan een subdomein kunt toevoegen
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: subdomein, google, txt, record, gmail, leverability
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 10%

---

# Een Google TXT-record toevoegen aan een subdomein {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT-records"
>abstract="Als u ervoor wilt zorgen dat e-mailberichten naar Gmail-adressen worden verzonden, kunt u speciale TXT-records voor de verificatie van de Google-site toevoegen aan uw subdomein om te controleren of deze is geverifieerd."

TXT-records zijn een type DNS-record dat wordt gebruikt om tekstinformatie over een domein te verstrekken en dat kan worden gelezen door externe bronnen.

Om ervoor te zorgen dat de e-mailadressen optimaal kunnen worden bezorgd en succesvol kunnen worden bezorgd, [!DNL Journey Optimizer] Hiermee kunt u speciale TXT-records voor verificatie van de Google-site toevoegen aan uw subdomein om te controleren of dit is geverifieerd.

>[!CAUTION]
>
> Deze bewerking kan alleen worden uitgevoerd als een subdomein het **[!UICONTROL Success]** status. Raadpleeg voor meer informatie over de status van subdomeinen [deze sectie](about-subdomain-delegation.md#access-delegated-subdomains).

Ga als volgt te werk om een Google TXT-record aan uw subdomein toe te voegen:

1. Het subdomein openen vanuit het dialoogvenster **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** -menu.

1. In de **[!UICONTROL Google txt record]** de verificatiecode invoeren die is gegenereerd op basis van [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->en klik vervolgens op **[!UICONTROL Save]**.

   ![](assets/subdomain-google-txt.png)

1. Nadat de TXT-record is toegevoegd, moet u deze door Google laten verifiëren. Navigeer naar [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->en start vervolgens de verificatiestap.
