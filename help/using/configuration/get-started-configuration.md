---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met [!DNL Journey Optimizer] configuratie
description: Meer informatie over [!DNL Journey Optimizer] configuratie
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configuratie, configureren, berichten, kanaal, sandbox, optimaliseren
source-git-commit: 970fef96b6fa04f2b5ce1a8d10f89802f513b373
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 6%

---


# Aan de slag met [!DNL Journey Optimizer] configuratie {#start-optimizer-configuration}

Bij toegang [!DNL Journey Optimizer] voor het eerst, bent u provisioned een productiesandbox en toegewezen een bepaald aantal IPs afhankelijk van uw contract.

Als u uw reizen wilt maken en berichten wilt verzenden, moet u de onderstaande configuratiestappen doorlopen.

## Berichten en kanalen configureren

1. Om berichten te kunnen tot stand brengen en verzenden, moet u specifieke configuraties afhankelijk van het kanaal uitvoeren.

   * Voor de **E-mail** kanaal, moet u subdomeinen aan Adobe delegeren en IP pools creëren om IP adressen samen te groeperen. [Meer informatie](../email/get-started-email-config.md)

   * Voor de **Push** kanaal, moet u dupberichten montages in allebei bepalen [!DNL Adobe Experience Platform] en [!DNL Adobe Experience Platform Launch]. [Meer informatie](../push/push-configuration.md)

   * Voor de **SMS** kanaal, moet u uw instantie vormen om SMS te verzenden, met inbegrip van het integreren van de leveranciersmontages met [!DNL Journey Optimizer]. [Meer informatie](../sms/sms-configuration.md)

1. Als u klaar bent, moet u **kanaaloppervlakken** om alle technische parameters te vormen die worden vereist om berichten te leveren. [Meer informatie](channel-surfaces.md)

1. U kunt ook:

   * Het aantal dagen beheren waarin opnieuw pogingen worden uitgevoerd voordat e-mailadressen naar de suppressielijst worden verzonden. [Meer informatie](manage-suppression-list.md)

   * De optie **BBC-e-mailoptie** om een kopie van de berichten te bewaren die aan individuen worden verzonden. [Meer informatie](archiving-support.md#enable-bcc)

   * Configureren **bedrijfsvoorschriften** om te voorkomen dat uw ontvangers te veel vragen. [Meer informatie](frequency-rules.md)

   * Bepaal welk e-mailadres en/of telefoonnummer als prioriteit voor uw ontvangers moet worden gebruikt wanneer er in Adobe Experience Platform verschillende adressen/nummers beschikbaar zijn. [Meer informatie](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>Deze stappen moeten worden uitgevoerd door [Adobe Journey Optimizer-systeembeheerder](../start/path/administrator.md).

## Reizen configureren

Om ritten te bouwen, moet u vormen **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** en **[!UICONTROL Actions]**. [Meer informatie](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* De **gegevensbron** De configuratie staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw reizen zal worden gebruikt. [Meer informatie](../datasource/about-data-sources.md)

* **Gebeurtenissen** u toestaan om uw reizen te activeren om berichten, in real time, naar het individu te verzenden dat de reis overgaat. In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De gegevens van inkomende gebeurtenissen worden genormaliseerd na het Model van de Gegevens van de Ervaring van de Adobe (XDM). Gebeurtenissen komen van de Streaming Ingestie-API&#39;s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). [Meer informatie](../event/about-events.md)

* [!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheden waarmee u uw inhoud kunt ontwerpen en verzenden. Als u uw berichten verzendt met een systeem van derden, maakt u een **aangepaste handeling**. [Meer informatie](../action/action.md)