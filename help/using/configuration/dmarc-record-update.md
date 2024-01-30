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
source-git-commit: e1fda25bb16f6d1e304d600dfce39df07fc570b0
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Voldoen aan nieuwe DMARC-eis {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Meer informatie over verplichte DMARC-update"
>abstract="Google en Yahoo zullen als onderdeel van hun afdwingbare best practices in de branche eisen dat u een **DMARC-record** voor elk domein dat u gebruikt om e-mail naar hen te verzenden, vanaf **1 februari 2024**.<br>Daarom moet u ervoor zorgen dat u een DMARC-record hebt ingesteld voor alle subdomeinen die u hebt gedelegeerd aan Adobe in Journey Optimizer."

De op domein-gebaseerde Authentificatie van het Bericht, het Melden, en de Conformiteit (DMARC) is een methode van de e-mailauthentificatie die domeineigenaars toestaat om hun domein tegen onbevoegd gebruik te beschermen. Door een duidelijk beleid aan e-mailleveranciers/ISPs aan te bieden, helpt het kwaadwillige acteurs verhinderen e-mails te verzenden die beweren van uw domein te zijn. DMARC implementeren verkleint het risico dat legitieme e-mailberichten worden gemarkeerd als spam of afgewezen, en verbetert uw e-mailleverbaarheid.


Google en Yahoo zijn een onderdeel van hun best practices in de branche. beide vereisen dat een **DMARC-record** voor elk domein dat u gebruikt om e-mail naar hen te verzenden. Deze nieuwe eis geldt vanaf **1 februari 2024**. [Meer informatie](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#dmarc){target="_blank"}.

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

     Nochtans, met de delegatie van CNAME zal het ook ingang in uw het ontvangen oplossing vereisen. Daarom moet u ervoor zorgen dat u uw IT-afdeling coördineert, zodat deze de update kan uitvoeren zodra de [!DNL Journey Optimizer] is beschikbaar (op 30 januari). [Meer informatie](dmarc-record.md#implement-dmarc)

**Een zelfbedieningsinterface voor implementatie DMARC zal beschikbaar zijn aan u die Jan, 30 begint. Meer informatie in [deze sectie](dmarc-record.md#implement-dmarc).**

De meest recente tijdlijnen die door Google en Yahoo worden gedeeld, zijn als volgt:

* Google:

   * **februari 2024** - Er zullen tijdelijke boetes worden ingesteld om te waarschuwen voor niet-naleving. E-mails worden nog steeds als normaal bezorgd na een korte vertraging als je nog niet aan de voorwaarden voldoet. Als u zich volledig aan de voorschriften houdt, zullen er geen tijdelijke steunbedragen zijn en zult u niet worden beïnvloed.

   * **april 2024** - Blokken beginnen voor afzenders die niet voldoen aan de DMARC-vereisten. Slechts een gedeelte van niet-compatibele e-mail wordt eerst geblokkeerd, waarbij het percentage geblokkeerde e-mail na verloop van tijd toeneemt.

   * **1 juni 2024** - Elke afzender die niet volledig aan de voorschriften voldoet, zal last krijgen van blokkering.

* Yahoo heeft geen precieze data verstrekt, maar heeft gezegd: &quot;de tenuitvoerlegging begint in februari 2024. De tenuitvoerlegging zal geleidelijk worden uitgevoerd.&quot;

>[!NOTE]
>
>Als u vragen hebt of ondersteuning nodig hebt, neemt u contact op met uw Adobe of uw Adobe.

**Nuttige koppelingen**

* Meer informatie over DMARC in het dialoogvenster [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"}
* Meer informatie over deze wijzigingen vindt u in het dialoogvenster [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html){target="_blank"}
* Uitlezen [Google Gmail-aankondiging](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Uitlezen [Yahoo! aankondiging](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}
