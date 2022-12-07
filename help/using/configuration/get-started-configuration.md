---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met [!DNL Journey Optimizer] configuratie
description: Meer informatie over [!DNL Journey Optimizer] configuratie
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 15%

---


# Aan de slag met [!DNL Journey Optimizer] configuratie {#start-optimizer-configuration}

Bij toegang [!DNL Journey Optimizer] voor het eerst, bent u provisioned een productiesandbox en toegewezen een bepaald aantal IPs afhankelijk van uw contract.

Als u uw reizen wilt maken en berichten wilt verzenden, moet u de onderstaande configuratiestappen doorlopen.

## Berichten en kanalen configureren

Bepaal kanaaloppervlakken, pas de berichten aan en pas deze aan.

* [Delegeren naar de Adobe van de subdomeinen](about-subdomain-delegation.md) je wilt e-mails verzenden en [IP-pools maken](ip-pools.md) om IP adressen te groeperen die aan uw instantie worden geleverd.

* Het aantal dagen beheren waarin opnieuw pogingen worden uitgevoerd voordat e-mailadressen naar de suppressielijst worden verzonden. [Meer informatie](manage-suppression-list.md)

* Instellingen voor pushmeldingen definiëren in beide [!DNL Adobe Experience Platform] en [!DNL Adobe Experience Platform Launch]. [Meer informatie](../push/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

* Configureer uw instantie voor het verzenden van SMS (momenteel alleen beschikbaar voor een set organisaties - Beperkte beschikbaarheid). [Meer informatie](../sms/sms-configuration.md)

* Creeer kanaaloppervlakten om alle technische parameters te vormen die worden vereist om berichten te leveren. [Meer informatie](channel-surfaces.md)

* Bepaal welk e-mailadres en/of telefoonnummer als prioriteit voor uw ontvangers moet worden gebruikt wanneer er in Adobe Experience Platform verschillende adressen/nummers beschikbaar zijn. [Meer informatie](primary-email-addresses.md)

## Journey&#39;s configureren

Om ritten te bouwen, moet u vormen **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** en **[!UICONTROL Actions]**. [Meer informatie](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* De **gegevensbron** De configuratie staat u toe om een verbinding aan een systeem te bepalen om extra informatie terug te winnen die in uw reizen zal worden gebruikt. [Meer informatie](../datasource/about-data-sources.md)

* **Gebeurtenissen** u toestaan om uw reizen te activeren om berichten, in real time, naar het individu te verzenden dat de reis overgaat. In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De data van binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen zijn afkomstig van de streamingopname-API’s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). [Meer informatie](../event/about-events.md)

* [!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheden waarmee u uw inhoud kunt ontwerpen en verzenden. Als u een systeem van derden gebruikt om uw berichten te verzenden, maakt u een **aangepaste handeling**. [Meer informatie](../action/action.md)