---
title: Journey Optimizer-instellingen en configuratierichtlijnen
description: Leer bericht en reis configuratierichtlijnen
audience: administrators
content-type: reference
role: Administrator
level: Intermediate
product: Adobe Journey Optimizer
solution: Journey Optimizer
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Applicatie-instellingen
topic: Beheer
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 10%

---


# Aan de slag met [!DNL Journey Optimizer]-configuratie

Wanneer het toegang tot van [!DNL Journey Optimizer] voor het eerst, bent u provisioned een productiesandbox en toegewezen een bepaald aantal IPs afhankelijk van uw contract.

Om uw reizen te kunnen tot stand brengen en berichten te verzenden, moet u door deze configuratiestappen gaan:

1. **Berichten en kanalen** configureren: voorinstellingen definiëren, e-mail- en pushberichten aanpassen en aanpassen

   * Definieer instellingen voor pushmeldingen in zowel [!DNL Adobe Experience Platform] als [!DNL Adobe Experience Platform Launch]. [Meer informatie](../push-gs.md)

   * Maak voorinstellingen voor berichten om alle technische parameters te configureren die vereist zijn voor e-mail- en pushberichten. [Meer informatie](message-presets.md)

   * Bepaal welk e-mailadres u als prioriteit voor uw ontvangers wilt gebruiken wanneer in Adobe Experience Platform verschillende adressen beschikbaar zijn. [Meer informatie](primary-email-addresses.md)

   * Het aantal dagen beheren waarin opnieuw pogingen worden uitgevoerd voordat e-mailadressen naar de suppressielijst worden verzonden. [Meer informatie](manage-suppression-list.md)

   <!--
    * Understand push notification flow. [Learn more](../push-gs.md)
    -->

1. **Subdomeinen** delegeren: voor om het even welk nieuw subdomain dat in Journey Optimizer moet worden gebruikt, zal de eerste stap het delegeren zijn. [Meer informatie](about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **IP-pools** maken: Verbeter uw e-mailleverbaarheid en reputatie door IP adressen te groeperen die aan uw instantie worden geleverd. [Meer informatie](ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Reizen** configureren: om reizen te bouwen, moet u vormen  **[!UICONTROL Data Sources]**,  **[!UICONTROL Events]** en  **[!UICONTROL Actions]**. [Meer informatie](about-data-sources-events-actions.md)

   ![](../assets/admin-menu.png)

   * Met de configuratie **Gegevensbron** kunt u een verbinding met een systeem definiëren om aanvullende informatie op te halen die in uw reizen wordt gebruikt. Meer informatie over gegevensbronnen vindt u in deze [sectie](../datasource/about-data-sources.md)

   * **** Eventsallow je om je reizen te activeren en in real-time berichten te sturen naar de persoon die de reis binnenkomt. In de gebeurtenisconfiguratie, vormt u de gebeurtenissen die in de reizen worden verwacht. De gegevens van de binnenkomende gebeurtenissen worden genormaliseerd volgens het Adobe Experience Data Model (XDM). Gebeurtenissen zijn afkomstig van de streamingopname-API’s voor geverifieerde en niet-geverifieerde gebeurtenissen (zoals Adobe Mobile SDK-gebeurtenissen). Meer informatie over gebeurtenissen in deze [sectie](../event/about-events.md)

   * [!DNL Journey Optimizer] wordt geleverd met ingebouwde berichtmogelijkheden: u kunt uw inhoud ontwerpen en uw bericht publiceren. Als u een derdesysteem gebruikt om uw berichten te verzenden, creeer een **douaneactie**. Meer informatie over handelingen in deze [sectie](../action/action.md)