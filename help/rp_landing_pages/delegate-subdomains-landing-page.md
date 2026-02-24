---
solution: Journey Optimizer
product: Journey Optimizer
title: E-mailsubdomeinen delegeren
description: E-mailsubdomeinen delegeren
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: bb50d06e86f9399dfd295b8091aa637abcaea4a8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# E-mailsubdomeinen delegeren{#section-overview}

Het delegeren van e-mailsubdomeinen is een kernstap in [&#x200B; kanaalconfiguratie &#x200B;](../using/configuration/get-started-configuration.md) - vereist alvorens u e-mails van Journey Optimizer kunt verzenden. Subdomeinen laten u verkeerstypes (b.v., marketing versus transactie) isoleren, de reputatie van uw belangrijkste domein beschermen, en versnellen [&#x200B; IP warmup &#x200B;](../using/configuration/ip-warmup-gs.md). Zij werken naast [&#x200B; configuratie van het e-mailkanaal &#x200B;](../using/email/get-started-email-config.md) en [&#x200B; leverbaarheidscontrole &#x200B;](../using/reports/deliverability.md) om berichten te verzekeren bereiken inboxes.

U kunt van verscheidene opstellingsmethodes kiezen: **volledige delegatie** (Adobe beheert DNS), **opstelling van de NAAM**, of **douanedelegatie** (u hebt certificaten en DNS). Als u met CNAME begint, kunt u later [&#x200B; aan douanedelegatie &#x200B;](../using/configuration/custom-subdomain-migration.md) voor striktere veiligheid migreren. Deze sectie gaat ook over DMARC- en PTR-records, Google TXT-records voor Gmail en IP-pools. Voor breder te leveren hulp, zie [&#x200B; begonnen met bevrediging &#x200B;](../using/reports/deliverability.md) en [&#x200B; de e-mailadressen van de Monitor &#x200B;](monitor-reputation-landing-page.md).

## E-mailsubdomeinen delegeren

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=nl-NL)

Aan de slag met subdomeindelegatie

Leer de voordelen, de configuratiemethodes, en de overwegingen voor het delegeren van subdomeinen in Adobe Journey Optimizer.

[Subdomeinen delegeren starten](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=nl-NL)

Een subdomein delegeren

De geleidelijke begeleiding voor het delegeren van subdomeinen aan Adobe, met inbegrip van volledige delegatie en opstelling CNAME.

[Leer hoe te om te delegeren](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/screwdriver-wrench.svg?lang=nl-NL)

Een aangepast subdomein instellen

Neem volledig eigendom van uw subdomeinen met douane delegatie-upload uw eigen SSL certificaten en handhaaf volledige controle over domeinconfiguratie.

[Een aangepast subdomein instellen](../using/configuration/delegate-custom-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=nl-NL)

Migreren van CNAME naar aangepaste delegatie

Migreer bestaande CNAME-gevormde subdomeinen aan douanedelegatie om veiligheidsbeleid te ontmoeten en volledige controle over certificaten te verkrijgen.

[Uw subdomein migreren](../using/configuration/custom-subdomain-migration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=nl-NL)

DMARC-records instellen

Configureer DMARC-records om de e-mailbeveiliging en de leverbaarheid voor gedelegeerde subdomeinen te verbeteren.

[DMARC nu instellen](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=nl-NL)

Een Google TXT-record toevoegen

Verifieer subdomeinen voor Gmail leverability door Google TXT- verslagen in Adobe Journey Optimizer toe te voegen.

[Google TXT-records toevoegen](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=nl-NL)

PTR-records openen en bewerken

PTR-records beheren voor gedelegeerde subdomeinen, waaronder het bewerken en begrijpen van updatestatus.

[PTR-records bewerken](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=nl-NL)

IP-pools maken

IP van de groep adressen voor betere e-mailleverbaarheid en beheer effectief subdomeinreputatie.

[IP-pools maken](../using/configuration/ip-pools.md)
:::

::::

## Aanvullende bronnen

- **[vormt het landen van pagina subdomeinen](../using/landing-pages/lp-subdomains.md)** - opstelling subdomeinen voor het landen van pagina&#39;s en abonnementvormen.
- **[vorm Websubdomeinen](../using/web/web-delegated-subdomains.md)** - Afgevaardigde subdomeinen voor Webervaringen en het volgen.
- **[wordt begonnen met kanaalconfiguratie](../using/configuration/get-started-configuration.md)** - Overzicht van alle stappen van de kanaalopstelling, met inbegrip van subdomain delegatie.
