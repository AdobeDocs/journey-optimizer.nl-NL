---
solution: Journey Optimizer
product: journey optimizer
title: Begonnen om met  [!DNL Journey Optimizer]  kanaalconfiguratie
description: Leer meer over  [!DNL Journey Optimizer]  kanaalconfiguratie
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configuratie, configureren, berichten, kanaal, sandbox, optimaliseren
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 4%

---


# Aan de slag met kanaalconfiguratie {#start-optimizer-configuration}

>[!CONTEXTUALHELP]
>id="ajo_channels_rate_controls"
>title="Snelheidbesturingselementen voor kanalen"
>abstract="Snelheidbesturingselementen voor kanalen"

Wanneer u [!DNL Journey Optimizer] voor het eerst opent, beschikt u over een productiesandbox en kunt u een bepaald aantal IP&#39;s toewijzen, afhankelijk van uw contract.

Om berichten te kunnen verzenden, moet u door de hieronder vermelde configuratiestappen gaan:

1. Als [ het systeembeheerder van Adobe Journey Optimizer ](../start/path/administrator.md), bepaal uw kanaal-specifieke configuraties. Leer hoe u deze configuraties instelt op de volgende pagina&#39;s:

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../email/get-started-email-config.md"><img alt="email" src="../channels/assets/do-not-localize/email.png"></a>
    <div align="center"><a href="../email/get-started-email-config.md"><strong> E-mail </strong></a></div></td>
    <td><a href="../sms/sms-configuration.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
    <div align="center"><a href="../sms/sms-configuration.md"><strong> SMS </strong></a></div></td>
    <td><a href="../push/push-configuration.md"><img alt="duwen" src="../channels/assets/do-not-localize/push.png"></a>
    <div align="center"><a href="../push/push-configuration.md"><strong> Push bericht </strong></a></div></td>
    <td><a href="../direct-mail/direct-mail-configuration.md"><img alt="direct mail" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
    <div align="center"><a href="../direct-mail/direct-mail-configuration.md"><strong>Direct mail</strong></a></div></td>
    </tr></table>

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../in-app/inapp-configuration.md"><img alt="in-app" src="../channels/assets/do-not-localize/inapp.jpg"></a>
    <div align="center"><a href="../in-app/inapp-configuration.md"><strong> In-app </strong></a></div></td>
    <td><a href="../web/web-configuration.md"><img alt="web" src="../channels/assets/do-not-localize/web.jpg"></a>
    <div align="center"><a href="../web/web-configuration.md"><strong> Web </strong></a></div></td>
    <td><a href="../code-based/code-based-configuration.md"><img alt="code-gebaseerde ervaring" src="../channels/assets/do-not-localize/code.png"></a>
    <div align="center"><a href="../code-based/code-based-configuration.md"><strong> op code-gebaseerde ervaring </strong></a></div></td>
    <td><a href="../content-card/content-card-configuration-prereq.md"><img alt="inhoudskaarten" src="../channels/assets/do-not-localize/cards.png"></a>
    <div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong> kaarten van de Inhoud </strong></a></div></td>
    </tr></table>

   >[!NOTE]
   >
   >Voor mobiele kanalen, vergemakkelijkt de [ Geleide kanaalopstelling ](set-mobile-config.md) de snelle configuratie van marketing kanalen, die alle vereiste middelen verzekeren gemakkelijk beschikbaar binnen Experience Platform, Journey Optimizer, en de Inzameling van Gegevens zijn. Hierdoor kan uw marketingteam beginnen met campagne en het creëren van reizen.

1. Zodra gedaan, moet u alle technische parameters vormen die worden vereist om berichten te leveren door **kanaalconfiguraties** te creëren. [ leer meer over kanaalconfiguraties ](channel-surfaces.md)

1. Afhankelijk van de kanalen die u gebruikt, uw milieu&#39;s en uw behoeften, moet u ook de volgende stappen uitvoeren:

   * Subdomain configuratie en delegatie voor uw kanalen, zoals [ e-mails ](about-subdomain-delegation.md), [ SMS ](../sms/sms-subdomains.md), [ het landen pagina&#39;s ](../landing-pages/lp-subdomains.md), en [ Webervaringen ](../web/web-delegated-subdomains.md).

   * IP van de opstelling warmup plannen voor optimale leverbaarheid. [Meer informatie](ip-warmup-gs.md)

   * Definieer een lijst van gewenste personen voor het verzenden van e-mail. [Meer informatie](allow-list.md)

   * Het aantal dagen beheren waarin opnieuw pogingen worden uitgevoerd voordat e-mailadressen naar de suppressielijst worden verzonden. [Meer informatie](manage-suppression-list.md)

   * Laat de **BCC e-mailoptie** toe om een exemplaar van berichten te houden die naar individuen worden verzonden. [Meer informatie](archiving-support.md#enable-bcc)

   * Vorm **bedrijfsregels** om te vermijden oversolicitating uw ontvangers. [Meer informatie](../conflict-prioritization/rule-sets.md)

   * Bepaal welk e-mailadres en/of telefoonnummer als prioriteit voor uw ontvangers moet worden gebruikt wanneer er in Adobe Experience Platform verschillende adressen/nummers beschikbaar zijn. [Meer informatie](primary-email-addresses.md)
