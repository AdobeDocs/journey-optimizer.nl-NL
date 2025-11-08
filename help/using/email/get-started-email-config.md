---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met e-mailconfiguratie
description: Meer informatie over e-mailconfiguratie in  [!DNL Journey Optimizer]
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: e-mail, configuratie, oppervlak, subdomeinen
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 7%

---

# Aan de slag met e-mailconfiguratie {#get-starte-email-config}

Als u e-mailberichten wilt verzenden via reizen en campagnes in [!DNL Journey Optimizer] , moet u een aantal configuratiestappen doorlopen.

1. Om optimale leverbaarheid te verzekeren en uw reputatie te beschermen, begin door **te delegeren aan Adobe subdomain** u gaat gebruiken om uw e-mails met [!DNL Journey Optimizer] te verzenden. Deze subdomeinen bepalen elementen zoals de webpagina&#39;s die moeten worden bijgehouden en de URL&#39;s van de spiegelpagina. [Meer informatie](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Creeer IP pools aan **groep samen IP adressen** provisioned met uw instantie. [Meer informatie](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Creeer **kanaalconfiguraties** en selecteer het **[!UICONTROL Email]** kanaal. [Meer informatie](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. In elke configuratie van het e-mailkanaal, vorm alle **technische parameters** die worden vereist om e-mails te leveren. [Meer informatie](email-settings.md)

   * Hier selecteert u het subdomein dat u wilt gebruiken om de e-mails en de IP-pools te verzenden die u aan de configuratie wilt koppelen. [Meer informatie](email-settings.md#ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * De adressen **[!UICONTROL Sender email]** en **[!UICONTROL Error email]** moeten het geselecteerde gedelegeerde subdomein gebruiken. [Meer informatie](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Bepaal welke **uitvoeringsgebieden** om in prioriteit voor uw ontvangers te gebruiken wanneer verscheidene adressen in Adobe Experience Platform beschikbaar zijn. [Meer informatie](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Beheer het aantal dagen waarin **opnieuw probeert** alvorens e-mailadressen naar de onderdrukkingslijst te verzenden wordt uitgevoerd. [Meer informatie](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
