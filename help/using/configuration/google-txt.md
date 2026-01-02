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
source-git-commit: e89bec74f597185065b274d22740324a09e9319e
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 6%

---

# Een Google TXT-record toevoegen aan een subdomein {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT-records"
>abstract="Als u ervoor wilt zorgen dat e-mailberichten naar Gmail-adressen worden verzonden, kunt u speciale TXT-records voor de verificatie van de Google-site toevoegen aan uw subdomein om te controleren of deze is geverifieerd."

TXT-records zijn een type DNS-record dat wordt gebruikt om tekstinformatie over een domein te verstrekken en dat kan worden gelezen door externe bronnen.

Met [!DNL Journey Optimizer] kunt u speciale TXT-records voor de verificatie van de Google-site toevoegen aan uw subdomein om ervoor te zorgen dat deze worden geverifieerd, zodat u verzekerd bent van optimale leverbaarheid en een geslaagde verzending van e-mailberichten naar Gmail-adressen.

>[!CAUTION]
>
> Deze bewerking kan alleen worden uitgevoerd als een subdomein de status **[!UICONTROL Success]** heeft. Voor meer op de statussen van subdomeinen, verwijs naar [ deze sectie ](delegate-subdomain.md#access-delegated-subdomains).

Ga als volgt te werk om een Google TXT-record aan uw subdomein toe te voegen:

1. Open het subdomein via het menu **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** > **[!UICONTROL Subdomains]** .

1. In de **[!UICONTROL Google txt record]** sectie, ga de verificatiecode in die van [ Google Workspace ](https://support.google.com/a/answer/183895){target="_blank"} <!--G Suite Admin tools--> wordt geproduceerd, dan klik **[!UICONTROL Save]**.

   ![](assets/subdomain-google-txt.png)

1. Nadat de TXT-record is toegevoegd, moet u deze door Google laten verifiëren. Om dit te doen, navigeer aan [ Google Workspace ](https://support.google.com/a/answer/183895){target="_blank"} <!--G Suite Admin tools-->, dan lanceer de verificatiestap.

## Een Google TXT-record bijwerken {#update-google-txt-record}

Voer de volgende stappen uit om een bestaande Google TXT-record bij te werken:

1. Open het subdomein vanuit het menu **[!UICONTROL Subdomains]** .

1. Wis de bestaande waarde in het veld **[!UICONTROL Google txt record]** en klik op **[!UICONTROL Save]** . Deze stap vervangt de vorige Google TXT-recordwaarde door een lege tekenreeks.

1. Open nu hetzelfde subdomein en voer de nieuwe verificatiecode in.

1. Klik nogmaals op **[!UICONTROL Save]** .

1. Verifieer het bijgewerkte verslag door [ Google Workspace ](https://support.google.com/a/answer/183895){target="_blank"}.
