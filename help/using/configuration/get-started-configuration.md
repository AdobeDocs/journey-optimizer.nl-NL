---
solution: Journey Optimizer
product: journey optimizer
title: Begonnen krijgen met  [!DNL Journey Optimizer]  configuratie
description: Leer meer over  [!DNL Journey Optimizer]  configuratie
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configuratie, configureren, berichten, kanaal, sandbox, optimaliseren
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 10%

---


# Aan de slag met [!DNL Journey Optimizer] -configuratie {#start-optimizer-configuration}

Wanneer u [!DNL Journey Optimizer] voor het eerst opent, beschikt u over een productiesandbox en kunt u een bepaald aantal IP&#39;s toewijzen, afhankelijk van uw contract.

Als u uw reizen wilt maken en berichten wilt verzenden, moet u de onderstaande configuratiestappen doorlopen.

## Berichten en kanalen configureren

1. Om berichten te kunnen tot stand brengen en verzenden, moet u specifieke configuraties afhankelijk van het kanaal uitvoeren.

   * Voor het **E-mail** kanaal, moet u subdomeinen aan Adobe delegeren en IP pools creëren om samen IP adressen te groeperen. [Meer informatie](../email/get-started-email-config.md)

   * Voor het **Push** kanaal, moet u duw berichten montages in zowel [!DNL Adobe Experience Platform] als [!DNL Adobe Experience Platform Launch] bepalen. [Meer informatie](../push/push-configuration.md)

   * Voor het **kanaal van SMS**, moet u uw instantie vormen om SMS te verzenden, met inbegrip van het integreren van de leveranciersmontages met [!DNL Journey Optimizer]. [Meer informatie](../sms/sms-configuration.md)

1. Zodra gedaan, moet u **kanaalconfiguraties** tot stand brengen om alle technische parameters te vormen die worden vereist om berichten te leveren. [Meer informatie](channel-surfaces.md)

1. U kunt ook het volgende doen:

   * Het aantal dagen beheren waarin opnieuw pogingen worden uitgevoerd voordat e-mailadressen naar de suppressielijst worden verzonden. [Meer informatie](manage-suppression-list.md)

   * Laat de **BBC e-mailoptie** toe om een exemplaar van berichten te houden die naar individuen worden verzonden. [Meer informatie](archiving-support.md#enable-bcc)

   * Vorm **bedrijfsregels** om te vermijden oversolicitating uw ontvangers. [Meer informatie](frequency-rules.md)

   * Bepaal welk e-mailadres en/of telefoonnummer als prioriteit voor uw ontvangers moet worden gebruikt wanneer er in Adobe Experience Platform verschillende adressen/nummers beschikbaar zijn. [Meer informatie](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>Deze stappen moeten door een [ het systeembeheerder van Adobe Journey Optimizer ](../start/path/administrator.md) worden uitgevoerd.

## Reizen configureren

Als u ritten wilt maken, moet u **[!UICONTROL Data Sources]** , **[!UICONTROL Events]** en **[!UICONTROL Actions]** configureren. [Meer informatie](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* De **gegevensbron** configuratie staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw reizen zal worden gebruikt. [Meer informatie](../datasource/about-data-sources.md)

* **Gebeurtenissen** staan u toe om uw reizen unitatically te teweegbrengen om berichten, in real time, naar het individu te verzenden dat in de reis stroomt. In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De data van binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen komen van de Streaming Ingestie-API&#39;s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). [Meer informatie](../event/about-events.md)

* [!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheden waarmee u uw inhoud kunt ontwerpen en verzenden. Als u een derdesysteem gebruikt om uw berichten te verzenden, creeer a **douaneactie**. [Meer informatie](../action/action.md)