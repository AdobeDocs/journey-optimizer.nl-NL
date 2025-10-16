---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met WhatsApp-berichten
description: Meer informatie over het maken en verzenden van WhatsApp-berichten in Journey Optimizer
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Aan de slag met WhatsApp-berichten {#get-started-whatsapp}

U kunt WhatsApp berichten direct door Journey Optimizer via Meta [&#x200B; Cloud API &#x200B;](https://developers.facebook.com/docs/whatsapp/cloud-api/) verzenden. Met deze functie kunt u whatsApp naadloos integreren in reizen en campagnes, waardoor de communicatie en de betrokkenheid met ontvangers wordt verbeterd.

* In a **Reis**. Creeer een reis, voeg a **WhatsApp** activiteit toe, en bepaal basismontages, dan doorblader aan de **[!UICONTROL Actions: WhatsApp]** juiste ruit om de inhoud voor het bericht te creëren WhatsApp. Leer hoe te om een reis op [&#x200B; tot stand te brengen deze pagina &#x200B;](../building-journeys/journey-gs.md).

* In a **Campagne**. Creeer een campagne, selecteer **WhatsApp** als uw actie en bepaal basismontages, dan geef de berichtinhoud uit om het te verzenden bericht te bepalen WhatsApp. Leer hoe te om een campagne op [&#x200B; tot stand te brengen deze pagina &#x200B;](../campaigns/create-campaign.md#configure).

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Voorwaarden {#prereq}

Voor de integratie van WhatsApp met Journey Optimizer is het volgende vereist:

* Meta Business Manager-account
* [&#x200B; WhatsApp BedrijfsRekening met geverifieerde afzendernaam en telefoonaantal &#x200B;](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [&#x200B; het toestemmingstoken van de Gebruiker met aangewezen toestemmingen &#x200B;](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [&#x200B; Goedgekeurde malplaatjes van Meta &#x200B;](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

U moet ook het volgende erkennen voordat u verdergaat met integratie:

* [&#x200B; WhatsApp inhoudsregels &#x200B;](https://www.whatsapp.com/legal/messaging-guidelines)
* [&#x200B; Naleving met het Beleid van Meta &#x200B;](https://www.whatsapp.com/legal)
* [&#x200B; 24 de gespreksgrenzen van het Uur &#x200B;](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Beperkingen {#limitations}

De volgende beperkingen gelden voor het WhatsApp-kanaal:

* Het WhatsApp-kanaal in Adobe Journey Optimizer is HIPAA-klaar, maar externe leveranciers vallen niet onder Adobe BAA. Klanten zijn verantwoordelijk voor hun eigen compatibiliteit en validatie van leveranciers.

* Merk op dat geautomatiseerde of vooraf bepaalde antwoordberichten nog niet worden gesteund.

* Vanaf april 2025 is de levering van alle berichten van het marketingmalplaatje aan gebruikers WhatsApp die een telefoonaantal van de Verenigde Staten (een aantal dat uit een +1 het draaien code en een het gebiedscode van de V.S. bestaat) tijdelijk opgeschort. [&#x200B; leer meer in de documentatie van Meta &#x200B;](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* De native integratiefunctionaliteit staat geen integratie met een externe Business Service Provider (BSP) toe.

## Hoe kan ik-video {#video}

In de onderstaande video ziet u hoe u WhatsApp kunt integreren als een native kanaal in Adobe Journey Optimizer om veilige, realtime, gepersonaliseerde berichten op schaal te leveren.

+++ Zie video

>[!VIDEO](https://video.tv.adobe.com/v/3470250?captions=dut&learn=on)

+++

