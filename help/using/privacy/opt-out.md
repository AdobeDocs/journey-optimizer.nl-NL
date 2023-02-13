---
solution: Journey Optimizer
product: journey optimizer
title: Weigeren beheren
description: Meer informatie over het beheren van opt-out en privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: e45c5d17e4758becdaaaa750c6fec488042ae2f7
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Weigeren beheren {#consent}

## Over opt-outbeheer {#about}

Het is een wettelijke vereiste dat ontvangers de mogelijkheid krijgen om zich af te melden voor het ontvangen van communicatie van een merk. Meer informatie over de toepasselijke wetgeving vindt u in het [Documentatie Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target="_blank"}.

**Waarom is het belangrijk?**

* Als u deze voorschriften niet naleeft, brengt u juridische risico&#39;s met zich mee voor uw merk.
* Het helpt u vermijden verzendend ongevraagde mededelingen naar uw ontvangers, die hen zouden kunnen maken uw berichten als spam merken en uw reputatie schaden.

## Afmelden in Journey Optimizer {#opt-out-ajo}

Wanneer het verzenden van berichten van reizen of campagnes, moet u altijd ervoor zorgen dat de klanten van toekomstige mededelingen kunnen opzeggen. Als u het abonnement opzegt, worden de profielen automatisch verwijderd uit het publiek van toekomstige marketingberichten.

while **[!DNL Journey Optimizer]** biedt manieren om de optie om te weigeren in e-mails en SMS-berichten te beheren. Voor pushberichten is geen actie aan uw kant vereist, omdat ontvangers hun abonnement zelf kunnen opzeggen via hun apparaten. Ze kunnen er bijvoorbeeld voor kiezen om meldingen te stoppen wanneer ze worden gedownload of wanneer ze uw app gebruiken. Op dezelfde manier kunnen ze de meldingsinstellingen wijzigen via het mobiele besturingssysteem.

In de volgende secties vindt u informatie over het beheren van opt-out in Journey Optimizer-berichten voor e-mail en SMS:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Lood" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>E-mailuitschakelbeheer</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Onfrequent" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>SMS-opt-out-beheer</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>In [!DNL Journey Optimizer], wordt de toestemming door het Experience Platform afgehandeld [Goedkeuringsschema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target="_blank"}.