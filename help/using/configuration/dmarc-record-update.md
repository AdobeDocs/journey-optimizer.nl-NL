---
solution: Journey Optimizer
product: journey optimizer
title: Voldoen aan de nieuwe DMARC-eis
description: Meer weten waarom en wanneer u DMARC-record moet instellen in Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdomein, domein, mail, dmarc, record
exl-id: 15b10a61-6ecd-4ffa-b1c2-21e862263f6d
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Voldoen aan de nieuwe DMARC-eis {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Meer informatie over verplichte DMARC-update"
>abstract="Als deel van hun het afdwingen industrie beste praktijken, Google en Yahoo allebei vereisen dat u het verslag van a **DMARC** voor om het even welk domein hebt u gebruikt om e-mail naar hen te verzenden, die op **1 februari, 2024** beginnen.<br> dientengevolge, moet u ervoor zorgen dat u het verslagopstelling van DMARC voor alle subdomeinen hebt die u aan Adobe in Journey Optimizer hebt gedelegeerd."

De op domein-gebaseerde Authentificatie van het Bericht, het Melden, en de Conformiteit (DMARC) is een methode van de e-mailauthentificatie die domeineigenaars toestaat om hun domein tegen onbevoegd gebruik te beschermen. Door een duidelijk beleid aan e-mailleveranciers/ISPs aan te bieden, helpt het kwaadwillige acteurs verhinderen e-mails te verzenden die beweren van uw domein te zijn. Als u DMARC implementeert, verkleint u het risico dat legitieme e-mailberichten worden gemarkeerd als spam of afgewezen, en verbetert u de e-mailleverbaarheid.

Google en Yahoo zijn een onderdeel van hun best practices in de branche. allebei vereisen het verslag van a **DMARC** voor om het even welk domein u gebruikt om e-mail naar hen te verzenden. Dit nieuwe vereiste is beginnend **Februari 1st, 2024** van toepassing.

>[!CAUTION]
>
>Gmail en Yahoo voldoen niet aan deze nieuwe eis! wordt verwacht dat e-mailberichten in de map spam zullen landen of geblokkeerd zullen raken.

Daarom raadt Adobe u ten zeerste aan ervoor te zorgen dat DMARC-record is ingesteld voor alle subdomeinen die u in [!DNL Journey Optimizer] hebt gedelegeerd aan Adobe. Voer de onderstaande stappen uit die op je kwestie van toepassing zijn:

* Als u [&#x200B; volledig &#x200B;](delegate-subdomain.md#set-up-subdomain) uw verzendende subdomeinen aan Adobe hebt gedelegeerd, volg één van de hieronder opties:

   * Opstelling DMARC op het ouderdomein van uw gedelegeerde subdomeinen **in uw het ontvangen oplossing**.
of
   * Stel DMARC in op de gedelegeerde subdomeinen **in de gebruikersinterface van de[!DNL Journey Optimizer]** -configuratie, zonder extra werk voor de hostoplossing. [&#x200B; leer hoe &#x200B;](dmarc-record.md#implement-dmarc)

* Als u opstelling uw verzendende subdomeinen met [&#x200B; CNAME &#x200B;](delegate-subdomain.md#cname-subdomain-setup) hebt, volg één van de hieronder opties:

   * Opstelling DMARC op uw subdomeinen of op het ouderdomein van uw subdomeinen **in uw het ontvangen oplossing**.
of
   * Stel DMARC in op de gedelegeerde subdomeinen **in de gebruikersinterface van de[!DNL Journey Optimizer]** -configuratie. [&#x200B; leer hoe &#x200B;](dmarc-record.md#implement-dmarc)

  Nochtans, vereist de opstelling CNAME ook één of andere extra ingang in uw het ontvangen oplossing. Derhalve zorg ervoor u met uw afdeling van IT coördineert zodat zij de update kunnen uitvoeren die in [&#x200B; wordt gedetailleerd deze sectie &#x200B;](dmarc-record.md#implement-dmarc).

<!--The most recent timelines shared by Google and Yahoo! are as follows:

* Google:

    * **February 2024** – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you will not be affected.

    * **April 2024** – Blocks will begin for senders who are not in compliance with DMARC requirement. Only a portion of non-compliant email will be blocked at first, with the percentage blocked increasing over time.

    * **June 1st, 2024** – Any sender not in full compliance will experience blocking.

* Yahoo! has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".
-->

>[!NOTE]
>
>Als u vragen hebt of ondersteuning nodig hebt, neemt u contact op met uw Adobe Deliverability Consultant of uw Adobe-vertegenwoordiger.

**Nuttige verbindingen**

* Leer meer over DMARC in de [&#x200B; Gids van de Beste praktijken van de Levering &#x200B;](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=nl-NL#about){target="_blank"}
* Lees uit de [&#x200B; aankondiging van Google Gmail &#x200B;](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Lees uit [&#x200B; Yahoo! aankondiging &#x200B;](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
