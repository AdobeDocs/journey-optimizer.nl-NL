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
source-git-commit: 49cb9734d66dc1aa2a3531c71a687aac00834d82
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# DMARC-record {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="De DMARC-record instellen"
>abstract="Plaats DMARC verslag om leveringskwesties met ISPs te vermijden"

>[!CAUTION]
>
>Na de recente Gmail en Yahoo aankondigingen voor bulkafzenders, steunt Journey Optimizer nu de DMARC authentificatietechnologie. //U moet alle subdomeinen die u al voor uw instantie hebt gemaakt bijwerken om DMARC-ondersteuning op te nemen.//

Het is belangrijk om het tegen 1 februari te doen Doc zal spoedig komen

Starten bij

U hebt twee opties:

* Doe het nu op uw eigen manier: stel het in met uw IT-afdeling - wanneer u wilt

* Doe het in AJO - maar in dat geval moet je wachten tot 30 jan.

   * Volledige delegatie: u kunt dit doen op 30 januari (AJO-release)

   * CNAME plant het met uw afdeling van IT zodat is het niet tijdrovend maar u moet het plannen

Google en Yahoo hebben als onderdeel van hun best practices in de branche hun best practices afgedwongen dat u een DMARC-record hebt voor elk domein dat u gebruikt om e-mail naar hen te verzenden. Deze nieuwe eis begint op **1 februari 2024**.

Meer informatie over Google en Yahoo&#39;s vereisten voor DMARC-record vindt u in [deze sectie](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Meer informatie over de aangekondigde wijzigingen vindt u op Google en Yahoo [deze pagina](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

DMARC, die staat voor **Op domein-gebaseerde Authentificatie van het Bericht, Rapportering, en Conformiteit**, is een e-mailverificatieprotocol dat bescherming biedt tegen spoofing, phishing en andere frauduleuze activiteiten.

* E-mailverificatie:

   * SPF (het Kader van het Beleid van de Afzender): DMARC baseert zich op SPF om de identiteit van de verzendende postserver voor authentiek te verklaren. SPF helpt verifiëren dat het e-mailbericht uit een erkende bron door het IP van de verzendende server adres tegen een lijst van erkende IP adressen voor het domein te controleren komt.
   * DKIM (DomainKeys Identified Mail): DMARC gebruikt DKIM ook om een digitale handtekening toe te voegen aan e-mailberichten, zodat de ontvanger de integriteit en authenticiteit van het bericht kan verifiëren.

* DMARC helpt te voorkomen dat kwaadaardige acteurs e-mails verzenden die van uw domein lijken te komen. Door DMARC in te stellen, kunt u opgeven hoe e-mailproviders berichten moeten afhandelen die verificatiecontroles niet doorstaan, waardoor de kans kleiner is dat phishinge-mails ontvangers bereiken.

* DMARC helpt de e-mailleverbaarheid te verbeteren door een duidelijk beleid te bieden dat e-mailproviders kunnen volgen bij het ontvangen van berichten die beweren dat ze afkomstig zijn van uw domein. Dit kan de kans verkleinen dat legitieme e-mailberichten als spam worden gemarkeerd of worden afgewezen.

* Door DMARC te implementeren, kunt u uw merkreputatie beschermen door ervoor te zorgen dat onbevoegde partijen uw domein niet kunnen misbruiken voor phishing of andere schadelijke activiteiten. Dit is met name belangrijk voor bedrijven en organisaties die vertrouwen op e-mailcommunicatie met klanten en partners.

Het vestigen van een DMARC- verslag impliceert het toevoegen van een DNS TXT- verslag aan DNS van uw domein montages. Dit verslag specificeert uw beleid DMARC, zoals of aan quarantaine of verwerpt berichten die authentificatie ontbreken. Het uitvoeren van DMARC is een pro-actieve stap om e-mailveiligheid te verbeteren en zowel uw organisatie als uw ontvangers tegen e-mailgebaseerde bedreigingen te beschermen.

[Meer informatie over DMARC vindt u in de gids over best practices voor levering](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} om beter inzicht te krijgen in de impact van DMARC op e-mailleverbaarheid.

Als u geen DMARC toevoegt, zult u (minstens) in quarantaine worden geplaatst.

zorg ervoor dat u een echte postvak hebt waarin u de gegevens kunt ontvangen - u beheert deze postvak (mag geen Adobe-inbox zijn)

De aanbeveling is 24 omdat, als minder, uw capaciteit over het algemeen evalueert/uw > praatje GPT controleert

Google en Yahoo, en waarschijnlijk alle andere belangrijkste ISP&#39;s

voor CNAME in de editie moet u het CSV-bestand opnieuw downloaden (niet voor volledig gedelegeerde versie)

nieuwe DMARC-record

In RN > put it first Alle subdomeinen moeten worden bijgewerkt met DMARC-ondersteuning



