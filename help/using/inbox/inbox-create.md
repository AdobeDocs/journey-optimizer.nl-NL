---
title: Postvak IN maken
description: Leer hoe u een Postvak IN Adobe Journey Optimizer maakt en configureert voor het verzenden van permanente, niet-indringende berichten aan uw gebruikers.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
source-git-commit: d84cc0f4d9226876e55e37409a685550fe0c9050
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# Een Postvak IN maken {#inbox-create}

Voorafgaand aan het creëren van inbox, voltooi de stappen in [&#x200B; configuratie Inbox &#x200B;](inbox-configuration.md). De kanaalconfiguratie identificeert de doeltoepassing of website, de pagina of de regel, en de plaatsing waar inbox wordt teruggegeven.

Voer de volgende stappen uit om een bericht in een campagne te maken:

1. Maak een campagne. [Meer informatie](../campaigns/create-campaign.md)

1. Selecteer het type campagne dat u wilt uitvoeren:

   * **[!UICONTROL Scheduled - Marketing]** : voer de campagne onmiddellijk uit of op een opgegeven datum. De geplande campagnes zijn gericht op het verzenden van **marketing** berichten. Zij worden gevormd en uitgevoerd van het gebruikersinterface.

   * **[!UICONTROL API-triggered - Marketing/Transactional]** : voer de campagne uit met behulp van een API-aanroep. API-teweeggebrachte campagnes zijn gericht op het verzenden van of **marketing**, of **transactie** berichten, d.w.z. berichten die na een actie worden verzonden die door een individu wordt uitgevoerd: het terugstellen van het wachtwoord, het kartelaankoop enz. [&#x200B; Leer hoe te om een campagne teweeg te brengen gebruikend APIs &#x200B;](../campaigns/api-triggered-campaigns.md)

1. Geef op het tabblad **[!UICONTROL Properties]** een naam en een beschrijving voor de campagne op.

1. Selecteer op het tabblad **[!UICONTROL Action]** de handeling **[!UICONTROL Inbox]** .

   ![](assets/inbox-create-1.png)

1. Selecteer of creeer een nieuwe [&#x200B; configuratie Inbox &#x200B;](inbox-configuration.md).

   ![](assets/inbox-create-2.png)

1. Open het tabblad Inhoud om uw bericht te ontwerpen met de inhoudsontwerper. [Meer informatie](inbox-design.md)

1. Klik in het tabblad **[!UICONTROL Audience]** op de knop **[!UICONTROL Select audience]** om de lijst met beschikbare Adobe Experience Platform-soorten publiek weer te geven. [&#x200B; leer meer over publiek &#x200B;](../audience/about-audiences.md)

1. Kies in het veld **[!UICONTROL Identity namespace]** de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren. [&#x200B; Leer meer over namespaces &#x200B;](../event/about-creating.md#select-the-namespace)

1. U kunt uw campagne plannen aan een specifieke datum of reeks om met regelmatige intervallen opnieuw te komen. [Meer informatie](../campaigns/create-campaign.md#schedule)

1. Controleer en activeer uw campagne om berichten naar inbox te verzenden.

U kunt dit Inbox nu kiezen wanneer het creëren van uw [&#x200B; de kaartcampagne van de Inhoud &#x200B;](../content-card/create-content-card.md).
