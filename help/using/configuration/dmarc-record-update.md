---
solution: Journey Optimizer
product: journey optimizer
title: Verplichte DMARC-update
description: Leer waarom en wanneer u een DMARC-record moet instellen in Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: subdomein, domein, mail, dmarc, record
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Verplichte DMARC-update {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Meer informatie over verplichte DMARC-update"
>abstract="Google en Yahoo zullen als onderdeel van hun afdwingbare best practices in de branche eisen dat u een **DMARC-record** voor elk domein dat u gebruikt om e-mail naar hen te verzenden, vanaf **1 februari 2024**. <br>Daarom moet u ervoor zorgen dat u een DMARC-record hebt ingesteld voor alle subdomeinen die u hebt gedelegeerd aan Adobe in Journey Optimizer."

Google en Yahoo zullen als onderdeel van hun afdwingbare best practices in de branche eisen dat u een **DMARC-record** voor elk domein dat u gebruikt om e-mail naar hen te verzenden. Deze nieuwe eis begint op **1 februari 2024**.

Meer informatie over Google en Yahoo&#39;s vereisten in [deze sectie](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Als Gmail en Yahoo niet aan deze nieuwe eis voldoen, zullen e-mails naar de map spam landen of geblokkeerd raken.

Daarom raadt de Adobe u ten zeerste aan ervoor te zorgen dat u een DMARC-record hebt ingesteld voor alle subdomeinen die u hebt gedelegeerd aan Adobe in [!DNL Journey Optimizer]. Voer de onderstaande stappen uit die op je kwestie van toepassing zijn:

* Als u [volledig gedelegeerd](delegate-subdomain.md#full-subdomain-delegation) Voer een van de volgende twee opties uit om de subdomeinen die u verzendt naar de Adobe te verzenden:

   * DMARC instellen voor het bovenliggende domein van de gedelegeerde subdomeinen **in uw hostingoplossing**.

   * DMARC instellen op uw gedelegeerde subdomeinen **de volgende functie gebruiken in het dialoogvenster [!DNL Journey Optimizer] beheer-interface** - zonder extra werk voor uw hostingoplossing.

* Als u hebt ingesteld [CNAME-delegatie](delegate-subdomain.md#cname-subdomain-delegation) Voor uw verzendende subdomeinen, volg één van beide hieronder opties:
   * DMARC instellen op uw subdomeinen of op het bovenliggende domein van uw subdomeinen **in uw hostingoplossing**.
   * DMARC instellen op uw gedelegeerde subdomeinen **de volgende functie gebruiken in het dialoogvenster [!DNL Journey Optimizer] beheer-interface**. Nochtans, zal het ook ingang in uw het ontvangen oplossing vereisen. Daarom moet u ervoor zorgen dat u uw IT-afdeling coördineert, zodat deze de update kan uitvoeren zodra de [!DNL Journey Optimizer] is beschikbaar (op 30 januari). <!--and be ready on February 1st, 2024-->

**Meer informatie over de [!DNL Journey Optimizer] De aanstaande functie DMARC zal binnenkort verschijnen.**

>[!NOTE]
>
>Als u vragen hebt of ondersteuning nodig hebt, neemt u contact op met uw Adobe of uw Adobe.

De meest recente tijdlijnen die door Google en Yahoo worden gedeeld, zijn als volgt:

* Google:

   * **februari 2024** - Er zullen tijdelijke boetes worden ingesteld om te waarschuwen voor niet-naleving. E-mails worden nog steeds als normaal bezorgd na een korte vertraging als je nog niet aan de voorwaarden voldoet. Als u zich volledig aan de voorschriften houdt, zullen er geen tijdelijke steunbedragen zijn en zult u niet worden beïnvloed.

   * **april 2024** - Blokken beginnen voor afzenders die niet voldoen aan de DMARC-vereisten. Slechts een gedeelte van niet-compatibele e-mail wordt eerst geblokkeerd, waarbij het percentage geblokkeerde e-mail na verloop van tijd toeneemt.

   * **1 juni 2024** - Elke afzender die niet volledig aan de voorschriften voldoet, zal last krijgen van blokkering.

* Yahoo heeft geen precieze data verstrekt, maar heeft gezegd: &quot;de tenuitvoerlegging begint in februari 2024. De tenuitvoerlegging zal geleidelijk worden uitgevoerd.&quot;

>[!NOTE]
>
>Meer informatie over het implementeren van DMARC in het dialoogvenster [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} om beter inzicht te krijgen in de gevolgen voor de e-mailleverbaarheid.
