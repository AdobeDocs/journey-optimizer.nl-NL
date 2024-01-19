---
solution: Journey Optimizer
product: journey optimizer
title: DMARC-record
description: Leer hoe u DMARC-record instelt in Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: subdomein, domein, mail, dmarc, record
hide: true
hidefromtoc: true
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# DMARC-record belangrijke update{#dmarc-record}


>[!CAUTION]
>
>Na de recente Gmail en Yahoo aankondigingen voor bulkafzenders, steunt Journey Optimizer nu de DMARC authentificatietechnologie.

Google en Yahoo hebben als onderdeel van hun best practices in de branche hun best practices afgedwongen dat u een DMARC-record hebt voor elk domein dat u gebruikt om e-mail naar hen te verzenden. Deze nieuwe eis begint op **1 februari 2024**.

Meer informatie over Google en Yahoo&#39;s vereisten voor DMARC-record vindt u in [deze sectie](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Meer informatie over de aangekondigde wijzigingen vindt u op Google en Yahoo [deze pagina](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Vervolgens hebt u nog een actie of volgende stappen voor u sectie waarin wordt aangegeven:

U moet deze instellen voor al uw subdomeinen
* Als u het domein volledig aan ons hebt gedelegeerd, hebt u twee opties
   * Stel DMARC in op het bovenliggende domein van het gedelegeerde domein in uw hostoplossing, OF
   * Stel DMARC in op een gedelegeerd domein met onze volgende functie in de interface voor beheerders zonder extra werk voor het hosten van de oplossing
* Als u CNAME hebt ingesteld voor uw verzendende domeinen, hebt u twee opties
   * Stel DMARC in op het subdomein OF het bovenliggende domein van het subdomein in uw hostoplossing, OF
   * Stel DMARC in met onze aanstaande functie in de interface voor beheerders. Het vereist echter niet alleen onze gebruikersinterface, maar ook toegang tot de hostoplossing.

Binnenkort vindt u meer informatie over onze toekomstige functie.

Bovendien kunt u de impact opnemen als deze niet is ingesteld door de voor DMARC relevante sectie te kopiëren van de onderste sectie (gekopieerd van bovenstaande koppeling). Of we trekken alleen DMARC-gerelateerde dingen uit. Of hier kunt u aangeven dat de aankondiging voor DMARC is en één klik unsub en hier is de laatste tijdlijn voor beide functies.

Sinds de oorspronkelijke aankondiging in oktober zijn er actualiseringen van de tijdlijnen aangebracht.

De meest recente tijdlijnen zien er als volgt uit:

Gmail:

* Februari 2024 - Tijdelijke steunbedragen om te waarschuwen voor niet-naleving zullen beginnen. E-mails worden nog steeds als normaal bezorgd na een korte vertraging als je nog niet aan de voorwaarden voldoet. Als je volledig aan de regels voldoet, zullen er geen tijdelijke grenzen zijn en zal je niets merken.
* April 2024 - de Blokken zullen voor afzenders beginnen die niet in overeenstemming met alles behalve lijst-Unsubscribe 1-Klik zijn. In eerste instantie wordt slechts een gedeelte van de niet-compatibele e-mail geblokkeerd, waarbij het percentage geblokkeerde e-mail na verloop van tijd toeneemt.
* 1 juni 2024 - Elke afzender die niet aan de volledige vereisten voldoet, inclusief List-Unsubscribe 1-Click, krijgt te maken met blokkeren.

Yahoo:

Heeft geen precieze data verstrekt, maar heeft gezegd: &quot;De tenuitvoerlegging begint in februari 2024. De tenuitvoerlegging zal geleidelijk worden uitgevoerd.&quot;
