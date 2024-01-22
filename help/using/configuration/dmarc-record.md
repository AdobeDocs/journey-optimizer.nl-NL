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
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# DMARC-record {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="De DMARC-record instellen"
>abstract="Plaats DMARC verslag om leveringskwesties met ISPs te vermijden. Google en Yahoo vereisen als onderdeel van hun afdwingbare best practices in de branche dat u een DMARC-record hebt voor elk domein dat u gebruikt om e-mail naar hen te verzenden."

>[!CAUTION]
>
>Na de recente Gmail en Yahoo aankondigingen voor bulkafzenders, steunt Journey Optimizer nu de DMARC authentificatietechnologie.

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

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
>Meer informatie over het implementeren van DMARC in het dialoogvenster [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} om beter inzicht te krijgen in de gevolgen voor de e-mailleverbaarheid.

## Wat is DMARC?

DMARC, die staat voor **Op domein-gebaseerde Authentificatie van het Bericht, Rapportering, en Conformiteit**, is een methode/protocol voor e-mailverificatie waarmee domeineigenaars hun domein kunnen beschermen tegen ongeoorloofd gebruik.

Met een manier om het domein van de afzender voor authentiek te verklaren, helpt het kwaadwillige acteurs verhinderen e-mails te verzenden die om van uw domein schijnen te komen.

DMARC biedt ook feedback over de status van e-mailverificatie en biedt afzenders de mogelijkheid om te bepalen wat er gebeurt met e-mails waarvoor verificatie mislukt. Dit omvat opties om post te controleren, in quarantaine te plaatsen of te verwerpen afhankelijk van welk beleid DMARC is uitgevoerd.

<!--Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.-->

DMARC heeft drie beleidsopties:

* Monitor (p=none): instrueert de postbusprovider/ISP om te doen wat zij normaal aan het bericht zouden doen.
* Quarantine (p=quarantaine): Instrueert de brievenbusleverancier/ISP om post te leveren die geen DMARC tot spam of junk omslag van de ontvanger overgaat.
* Weigeren (p=weiger): Instrueert de brievenbusleverancier/ISP om post te blokkeren die DMARC niet overgaat resulterend in een stuit.

## Hoe werkt DMARC?

SPF en DKIM worden allebei gebruikt om een e-mail met een domein te associëren en samen te werken om e-mail voor authentiek te verklaren. DMARC neemt deze één stap verder en helpt spoofing te verhinderen door het domein aan te passen dat door DKIM en SPF wordt gecontroleerd. Om DMARC over te gaan, moet een bericht SPF of DKIM overgaan. Als deze beide niet worden geverifieerd, mislukt DMARC en wordt het e-mailbericht verzonden volgens het geselecteerde DMARC-beleid.

* SPF (het Kader van het Beleid van de Afzender): DMARC baseert zich op SPF om de identiteit van de verzendende postserver voor authentiek te verklaren. SPF helpt verifiëren dat het e-mailbericht uit een erkende bron door het IP van de verzendende server adres tegen een lijst van erkende IP adressen voor het domein te controleren komt.
* DKIM (DomainKeys Identified Mail): DMARC gebruikt DKIM ook om een digitale handtekening toe te voegen aan e-mailberichten, zodat de ontvanger de integriteit en authenticiteit van het bericht kan verifiëren.

>[!NOTE]
>
>DMARC vereist groepering tussen het &quot;van&quot;en &quot;terugkeer-Weg&quot;adres.


<!--

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

-->


## DMARC implementeren {#implement-dmarc}

Volg onderstaande stappen voor het implementeren van DMARC.

* Als u geen DMARC toevoegt, zult u (minstens) in quarantaine worden geplaatst.

### Volledig gedelegeerde subdomeinen

Plaats de actie die de ontvankelijke server zal uitvoeren als DMARC ontbreekt.

DMARC heeft drie beleidsopties:

* Monitor (p=none): instrueert de postbusprovider/ISP om te doen wat zij normaal aan het bericht zouden doen. Dit is de standaardwaarde.
* Quarantine (p=quarantaine): Instrueert de brievenbusleverancier/ISP om post te leveren die geen DMARC tot spam of junk omslag van de ontvanger overgaat.
* Weigeren (p=weiger): Instrueert de brievenbusleverancier/ISP om post te blokkeren die DMARC niet overgaat resulterend in een stuit.

E-mails om samengevoegde DMARC-rapporten en forensische DMARC-mislukkingsrapporten te ontvangen: u kunt maximaal vijf adressen toevoegen.

* Zorg ervoor dat u een echte inbox hebt waar u in uw controle kunt ontvangen - u beheert dit inbox (zou geen Adobe inbox moeten zijn)

Toepasselijk percentage van e-mails dat DMARC moet worden toegepast:

Meldend interval: De aanbeveling is 24 omdat over het algemeen dit is wat ISPs heeft.
als minder, evalueer uw capaciteit / controleer uw > praatje GPT

Als een DMARC-record wordt gedetecteerd, kunt u dezelfde waarden kopiëren en plakken als in de lijst staan of deze waarden indien nodig wijzigen.

Als u niets plaatst, worden standaardwaarden gebruikt.

### Subdomeinen die zijn gedelegeerd met CNAME

voor CNAME in de versiestroom moet u het CSV-bestand opnieuw downloaden (niet voor volledig gedelegeerde versie)





