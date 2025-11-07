---
solution: Journey Optimizer
product: journey optimizer
title: Typen e-mailfouten
description: Open de lijst met alle mogelijke e-mailfouten bij het verzenden van leveringen met Journey Optimizer.
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: opnieuw proberen, stuiteren, zacht, genegeerd, hard, optimaliseren, fout
hide: true
hidefromtoc: true
exl-id: a8908b11-2288-4d53-897c-3f99cb5ceab4
source-git-commit: 0cb73489981659c3f231b9def40e0e483ed3aef8
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 4%

---

# Typen e-mailfouten {#email-error-types}

Mogelijke oorzaken voor een leveringsmislukking zijn veelvoudige. In de onderstaande tabel staan alle fouten die kunnen optreden bij het verzenden van e-mailleveringen met [!DNL Journey Optimizer] , alsmede de beschrijving en het type fout.

Deze fouten kunnen in de [&#x200B; Dataset van de Gebeurtenis van de Terugkoppeling van het Bericht van AJO &#x200B;](../data/datasets-query-examples.md#message-feedback-event-dataset) worden gevonden die de logboeken van de berichtlevering, met inbegrip van informatie over alle berichtlevering van [!DNL Journey Optimizer] bevat, en terugkoppelt verslagen van e-mail ISPs op grenzen.

| Foutlabel | Fouttype | Technische waarde | Beschrijving |
| --- | --- | --- | --- |
| **Onbepaald** | Genegeerd | 1 | Onbekwaam om het SMTP stuitbericht te classificeren dat van ISP wordt ontvangen. |
| **Ongeldige Ontvanger** | Hard stuiteren | 10 | Het adres van de ontvanger is ongeldig. |
| **Ontvanger weigerde** | Hard stuiteren | 15 | ISP van de ontvanger heeft het bericht geweigerd, en ISP kan de afzender blokkeren als de ontvanger niet wordt onderdrukt. |
| **Zachte Stuiteren** | Zacht stuiteren | 20 | Het bericht ondervond een tijdelijke mislukking. Het kan slagen in toekomstige pogingen. |
| **DNS Mislukt** | Zacht stuiteren | 21 | De berichtlevering ondervond een tijdelijke DNS mislukking. Het kan slagen in toekomstige pogingen. |
| **Volledige Brievenbus** | Zacht stuiteren | 22 | Het bericht ondervond tijdelijke leveringsmislukking aangezien de brievenbus van de ontvanger volledig was. |
| **Te groot** | Genegeerd | 23 | Het bericht ondervond een tijdelijke leveringsmislukking omdat de berichtgrootte de grens van de ontvanger overschreed. |
| **Onderbreking** | Genegeerd | 24 | De berichtlevering ontbrak of omdat de berichtgeldigheid verliep, of het te lang duurde om naar ISP te verzenden. |
| **Mislukking Admin** | Beheerder | 25 | De levering is mislukt als gevolg van een beleidsconfiguratie in de infrastructuur voor het verzenden van e-mail. |
| **Algemene Stuiteren: GEEN RCPT** | Genegeerd | 30 | Het bericht kon niet worden afgeleverd omdat de ontvanger niet werd geïdentificeerd. |
| **Algemene Stuiteren** | Genegeerd | 40 | Het bericht ondervond een tijdelijke leveringsmislukking om niet gespecificeerde redenen. |
| **Blok van de Post** | Genegeerd | 50 | De levering ondervond tijdelijke mislukking toe te schrijven aan hoge volume of tariefgrenzen door ISP. |
| **Spam Blok** | Genegeerd | 51 | De levering ondervond tijdelijke mislukking omdat ISP de domeinen van de afzender of IPs een bekende spambron beschouwde. |
| **Inhoud Spam** | Genegeerd | 52 | De levering ondervond een tijdelijke mislukking omdat ISP de inhoud van e-mail als spam classificeerde. |
| **het opnieuw beginnen ontkend** | Zacht stuiteren | 54 | Het bericht kan niet worden geaccepteerd omdat het doeldomein niet is toegestaan voor opnieuw afspelen. |
| **auto-Antwoord** | Genegeerd | 60 | Deze berichten worden verworpen door [!DNL Journey Optimizer] wanneer ontvangen tenzij het door:sturen wordt toegelaten. |
| **Voorbijgaande Mislukking** | Genegeerd | 70 | De levering wordt opnieuw beproefd met een vertraagde snelheid of kan worden uitgesteld in geval van opschorting. |
| **uitdaging-Reactie** | Zacht stuiteren | 100 | De levering zou permanent kunnen ontbreken aangezien [!DNL Journey Optimizer] geen vraag-antwoord authentificatiemechanisme steunt. |
