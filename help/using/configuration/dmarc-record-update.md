---
solution: Journey Optimizer
product: journey optimizer
title: Voldoen aan nieuwe DMARC-eis
description: Leer waarom en wanneer u een DMARC-record moet instellen in Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdomein, domein, mail, dmarc, record
exl-id: 15b10a61-6ecd-4ffa-b1c2-21e862263f6d
source-git-commit: da5b8d6c95e76af98b27ffcff11e75c26b90200a
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Voldoen aan nieuwe DMARC-eis {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Meer informatie over verplichte DMARC-update"
>abstract="Google en Yahoo hebben als onderdeel van hun afdwingbare best practices in de branche allebei de eis dat u een **DMARC-record** voor elk domein dat u gebruikt om e-mail naar hen te verzenden, vanaf **1 februari 2024**.<br>Daarom moet u ervoor zorgen dat u een DMARC-record hebt ingesteld voor alle subdomeinen die u hebt gedelegeerd aan Adobe in Journey Optimizer."

De op domein-gebaseerde Authentificatie van het Bericht, het Melden, en de Conformiteit (DMARC) is een methode van de e-mailauthentificatie die domeineigenaars toestaat om hun domein tegen onbevoegd gebruik te beschermen. Door een duidelijk beleid aan e-mailleveranciers/ISPs aan te bieden, helpt het kwaadwillige acteurs verhinderen e-mails te verzenden die beweren van uw domein te zijn. DMARC implementeren verkleint het risico dat legitieme e-mailberichten worden gemarkeerd als spam of afgewezen, en verbetert uw e-mailleverbaarheid.

Google en Yahoo zijn een onderdeel van hun best practices in de branche. beide een **DMARC-record** voor elk domein dat u gebruikt om e-mail naar hen te verzenden. Deze nieuwe eis geldt vanaf **1 februari 2024**.

>[!CAUTION]
>
>Gmail en Yahoo voldoen niet aan deze nieuwe eis! wordt verwacht dat e-mailberichten in de map spam zullen landen of geblokkeerd zullen raken.

Daarom raadt de Adobe u ten zeerste aan ervoor te zorgen dat u een DMARC-record hebt ingesteld voor alle subdomeinen die u hebt gedelegeerd aan Adobe in [!DNL Journey Optimizer]. Voer de onderstaande stappen uit die op je kwestie van toepassing zijn:

* Als u [volledig gedelegeerd](delegate-subdomain.md#full-subdomain-delegation) Voer een van de onderstaande opties uit om de subdomeinen die u verzendt naar de Adobe te verzenden:

   * DMARC instellen voor het bovenliggende domein van de gedelegeerde subdomeinen **in uw hostingoplossing**.
of
   * DMARC instellen op uw gedelegeerde subdomeinen **in de[!DNL Journey Optimizer]** gebruikersinterface van de configuratie - zonder extra werk aan uw het ontvangen oplossing. [Meer informatie](dmarc-record.md#implement-dmarc)

* Als u de verzendende subdomeinen hebt ingesteld met [CNAME](delegate-subdomain.md#cname-subdomain-delegation)Voer een van de volgende opties uit:

   * DMARC instellen op uw subdomeinen of op het bovenliggende domein van uw subdomeinen **in uw hostingoplossing**.
of
   * DMARC instellen op uw gedelegeerde subdomeinen **in de[!DNL Journey Optimizer]** gebruikersinterface voor configuratie. [Meer informatie](dmarc-record.md#implement-dmarc)

  Nochtans, vereist de opstelling CNAME ook één of andere extra ingang in uw het ontvangen oplossing. Zorg er daarom voor dat u coördineert met uw IT-afdeling, zodat deze de in [deze sectie](dmarc-record.md#implement-dmarc).

<!--The most recent timelines shared by Google and Yahoo! are as follows:

* Google:

    * **February 2024** – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you will not be affected.

    * **April 2024** – Blocks will begin for senders who are not in compliance with DMARC requirement. Only a portion of non-compliant email will be blocked at first, with the percentage blocked increasing over time.

    * **June 1st, 2024** – Any sender not in full compliance will experience blocking.

* Yahoo! has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".
-->

>[!NOTE]
>
>Als u vragen hebt of ondersteuning nodig hebt, neemt u contact op met uw Adobe of uw Adobe.

**Nuttige koppelingen**

* Meer informatie over DMARC in het dialoogvenster [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"}
* Lees de [Google Gmail-aankondiging](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Lees de [Yahoo! aankondiging](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
