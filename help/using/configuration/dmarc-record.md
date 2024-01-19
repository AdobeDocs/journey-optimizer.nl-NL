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
source-git-commit: f9d3234a64ad659660c2d2c4ad24ab5c240cb857
workflow-type: tm+mt
source-wordcount: '680'
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

Daarom raadt de Adobe u ten zeerste aan ervoor te zorgen dat u een DMARC-record hebt ingesteld voor alle subdomeinen die u hebt gedelegeerd aan Adobe in [!DNL Journey Optimizer]. Voer een van de volgende twee opties uit:

* Stel DMARC in op uw subdomeinen of op het bovenliggende domein van uw subdomeinen. **in uw hostingoplossing**.

* DMARC instellen op uw gedelegeerde subdomeinen **met de nieuwe functie in het dialoogvenster [!DNL Journey Optimizer] beheer-interface** - zonder extra werk voor uw hostingoplossing. [Meer informatie](#implement-dmarc)

  >[!CAUTION]
  >
  >Als u hebt ingesteld [CNAME-delegatie](delegate-subdomain.md#cname-subdomain-delegation) voor uw verzendende subdomeinen, zal het ook wat ingang in uw het ontvangen oplossing vereisen. Zorg ervoor dat u coördineert met uw IT-afdeling zodat deze de update kan uitvoeren zodra de [!DNL Journey Optimizer] is beschikbaar (30 januari 2024). <!--and be ready on February 1st, 2024-->

>[!NOTE]
>
>Meer informatie over het implementeren van DMARC in het dialoogvenster [Handleiding voor best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} om beter inzicht te krijgen in de gevolgen voor de e-mailleverbaarheid.

## Wat is DMARC?

DMARC, die staat voor **Op domein-gebaseerde Authentificatie van het Bericht, Rapportering, en Conformiteit**, is een e-mailverificatieprotocol dat bescherming biedt tegen spoofing, phishing en andere frauduleuze activiteiten.

* E-mailverificatie:

   * SPF (het Kader van het Beleid van de Afzender): DMARC baseert zich op SPF om de identiteit van de verzendende postserver voor authentiek te verklaren. SPF helpt verifiëren dat het e-mailbericht uit een erkende bron door het IP van de verzendende server adres tegen een lijst van erkende IP adressen voor het domein te controleren komt.
   * DKIM (DomainKeys Identified Mail): DMARC gebruikt DKIM ook om een digitale handtekening toe te voegen aan e-mailberichten, zodat de ontvanger de integriteit en authenticiteit van het bericht kan verifiëren.

* DMARC helpt te voorkomen dat kwaadaardige acteurs e-mails verzenden die van uw domein lijken te komen. Door DMARC in te stellen, kunt u opgeven hoe e-mailproviders berichten moeten afhandelen die verificatiecontroles niet doorstaan, waardoor de kans kleiner is dat phishinge-mails ontvangers bereiken.

* DMARC helpt de e-mailleverbaarheid te verbeteren door een duidelijk beleid te bieden dat e-mailproviders kunnen volgen bij het ontvangen van berichten die beweren dat ze afkomstig zijn van uw domein. Dit kan de kans verkleinen dat legitieme e-mailberichten als spam worden gemarkeerd of worden afgewezen.

* Door DMARC te implementeren, kunt u uw merkreputatie beschermen door ervoor te zorgen dat onbevoegde partijen uw domein niet kunnen misbruiken voor phishing of andere schadelijke activiteiten. Dit is met name belangrijk voor bedrijven en organisaties die vertrouwen op e-mailcommunicatie met klanten en partners.

Het vestigen van een DMARC- verslag impliceert het toevoegen van een DNS TXT- verslag aan DNS van uw domein montages. Dit verslag specificeert uw beleid DMARC, zoals of aan quarantaine of verwerpt berichten die authentificatie ontbreken. Het uitvoeren van DMARC is een pro-actieve stap om e-mailveiligheid te verbeteren en zowel uw organisatie als uw ontvangers tegen e-mailgebaseerde bedreigingen te beschermen.

## DMARC implementeren {#implement-dmarc}

* Als u geen DMARC toevoegt, zult u (minstens) in quarantaine worden geplaatst.

* Zorg ervoor dat u een echte inbox hebt waar u in uw controle kunt ontvangen - u beheert dit inbox (zou geen Adobe inbox moeten zijn)

De aanbeveling is 24 omdat over het algemeen dit is wat ISPs heeft.
als minder, evalueer uw capaciteit / controleer uw > praatje GPT

Als een DMARC-record wordt gedetecteerd, kunt u dezelfde waarden kopiëren en plakken als in de lijst staan of deze waarden indien nodig wijzigen.

Als u niets plaatst, worden standaardwaarden gebruikt.

### Volledig gedelegeerde subdomeinen

### Subdomeinen die zijn gedelegeerd met CNAME

voor CNAME in de versiestroom moet u het CSV-bestand opnieuw downloaden (niet voor volledig gedelegeerde versie)





