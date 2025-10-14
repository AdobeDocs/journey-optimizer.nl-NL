---
solution: Journey Optimizer
product: journey optimizer
title: E-mailheaderparameters configureren
description: Leer hoe u de parameters van de e-mailkoptekst instelt op het niveau van de kanaalconfiguratie
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: instellingen, e-mail, configuratie
exl-id: e1556c25-9c79-4362-a5a9-0a46425fa8d9
source-git-commit: 1b4ab451ed9e2315ffe4850c6ab4b8ad20223ac3
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Parameters koptekst {#email-header}

Wanneer het vormen van een nieuwe [&#x200B; configuratie van het e-mailkanaal &#x200B;](email-settings.md), in de **[!UICONTROL Header parameters]** sectie, ga de afzendernamen en e-mailadressen verbonden aan het type van e-mail in die configuratie wordt verzonden.

>[!NOTE]
>
>Voor meer controle over de e-mailinstellingen kunt u de headerparameters aanpassen. [Meer informatie](../email/surface-personalization.md#personalize-header)

* **[!UICONTROL From name]**: De naam van de afzender, zoals de naam van uw merk.
* **[!UICONTROL From email prefix]**: Het e-mailadres dat u voor uw communicatie wilt gebruiken.
* **[!UICONTROL Reply to name]**: De naam die zal worden gebruikt wanneer de ontvanger de **antwoordknoop** in hun e-mailcliëntsoftware klikt.
* **[!UICONTROL Reply to email]**: Het e-mailadres dat zal worden gebruikt wanneer de ontvanger de **antwoordknoop** in hun e-mailcliëntsoftware klikt. [Meer informatie](#reply-to-email)
* **[!UICONTROL Error email prefix]**: Alle fouten die door ISPs na een paar dagen van post worden geproduceerd die (asynchrone stuitingen) worden ontvangen op dit adres. De out-of-office berichten en de uitdagingsreacties worden ook ontvangen op dit adres.

  Als u de uit-van-bureauberichten en uitdagingsreacties op een specifiek e-mailadres wilt ontvangen dat niet aan Adobe wordt gedelegeerd, moet u a [&#x200B; door:sturen proces &#x200B;](#forward-email) opstelling. Zorg er in dat geval voor dat u een handmatige of geautomatiseerde oplossing hebt waarmee de e-mailberichten die in deze Postvak IN worden geplaatst, kunnen worden verwerkt.

>[!NOTE]
>
>De **[!UICONTROL From email prefix]** en **[!UICONTROL Error email prefix]** adressen gebruiken huidige geselecteerde [&#x200B; gedelegeerde subdomain &#x200B;](../configuration/about-subdomain-delegation.md) om e-mail te verzenden. Bijvoorbeeld, als gedelegeerde subdomain *marketing.luma.com* is:
>* Ga *contact* als **[!UICONTROL From email prefix]** in - de afzender e-mail is *contact@marketing.luma.com*.
>* Ga *fout* als **[!UICONTROL Error email prefix]** in - het foutenadres is *error@marketing.luma.com*.

![](assets/preset-header.png){width="80%"}

>[!NOTE]
>
>Adressen moeten beginnen met een letter (A-Z) en mogen alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, punt `.` - en afbreekstreepjes `-` gebruiken.

## E-mail beantwoorden {#reply-to-email}

Wanneer u het **[!UICONTROL Reply to email]** -adres definieert, kunt u elk e-mailadres opgeven, op voorwaarde dat het een geldig adres is, in de juiste notatie en zonder enige typefout.

Inbox gebruikt voor antwoorden zal alle antwoorde-mails, behalve uit-van-bureauberichten en uitdagingsreacties ontvangen, die op het **E-mailadres van de Fout** worden ontvangen.

Volg onderstaande aanbevelingen om te zorgen voor een goed antwoordbeheer:

* Zorg ervoor dat de toegewezen Postvak IN voldoende ontvangstcapaciteit heeft om alle e-mailberichten te ontvangen die via de e-mailconfiguratie worden verzonden. Als het postvak &#39;Bounces&#39; retourneert, worden sommige reacties van uw klanten mogelijk niet ontvangen.

* De reacties moeten worden verwerkt met inachtneming van de verplichtingen inzake privacy en naleving, aangezien zij persoonlijk identificeerbare informatie (PII) kunnen bevatten.

* Merk geen berichten als spam in antwoordinbox, aangezien het alle andere reacties zal beïnvloeden die naar dit adres worden verzonden.

Wanneer u bovendien het **[!UICONTROL Reply to email]** -adres definieert, moet u ervoor zorgen dat u een subdomein gebruikt dat een geldige MX-recordconfiguratie heeft, anders mislukt de verwerking van de e-mailconfiguratie.

Als u een fout bij het voorleggen van de e-mailconfiguratie krijgt, betekent het dat het MX- verslag niet voor subdomain van het adres wordt gevormd u inging. Contacteer uw beheerder voor het vormen van het overeenkomstige MX verslag of gebruik een ander adres met een geldige MX verslagconfiguratie.

>[!NOTE]
>
>Als subdomain van het adres u inging een domein is dat [&#x200B; volledig &#x200B;](../configuration/delegate-subdomain.md#full-subdomain-delegation) aan Adobe werd gedelegeerd, contacteer uw vertegenwoordiger van Adobe.

## E-mail doorsturen {#forward-email}

Neem contact op met de klantenservice van Adobe als u alle e-mailberichten die [!DNL Journey Optimizer] voor het gedelegeerde subdomein heeft ontvangen, wilt doorsturen naar een specifiek e-mailadres.

>[!NOTE]
>
>Als het subdomein dat voor het **[!UICONTROL Reply to email]** adres wordt gebruikt niet aan Adobe wordt afgevaardigd, door:sturen kan niet voor dit adres werken.

U moet het volgende opgeven:

* Het e-mailadres van uw keuze. Het domein van het voorwaartse e-mailadres kan niet overeenkomen met een subdomein dat aan Adobe is gedelegeerd.
* De naam van uw sandbox.
* De configuratienaam of het subdomein waarvoor het voorwaartse e-mailadres zal worden gebruikt.
  <!--* The current **[!UICONTROL Reply to (email)]** address or **[!UICONTROL Error email]** address set at the channel configuration level.-->

>[!NOTE]
>
>Per subdomein kan slechts één voorwaarts e-mailadres aanwezig zijn. Daarom als de veelvoudige configuraties zelfde subdomain gebruiken, moet het zelfde voorwaartse e-mailadres voor elk van hen worden gebruikt.

Adobe stelt het e-mailadres voor verzending in. Dit kan 3 tot 4 dagen duren.

Zodra gedaan, worden alle berichten ontvangen op **[!UICONTROL Reply to email]** en **E-mail van de Fout** adressen, evenals alle e-mails die naar **van e-mail** adres worden verzonden, door:sturen aan het specifieke e-mailadres u verstrekte.

>[!NOTE]
>
>Door gebrek, als het door:sturen niet wordt toegelaten, worden de e-mails die rechtstreeks naar **van e-mail** adres worden verzonden verworpen.
