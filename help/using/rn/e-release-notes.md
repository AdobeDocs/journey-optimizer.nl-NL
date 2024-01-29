---
solution: Journey Optimizer
product: journey optimizer
title: Aanvullende informatie
description: Opmerkingen bij de vervroegde release van Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: fd6f83019aa9cd5b4d6561007f5e0068256bb211
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 3%

---

# Vroege aanvullende informatie {#e-release-notes}

[!DNL Adobe Journey Optimizer] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen. Alle wijzigingen worden geconsolideerd op de laatste week van elke maand in de [releaseopmerkingen](release-notes.md).

Opmerkingen bij de eerste release hieronder kunnen zonder voorafgaande kennisgeving worden gewijzigd tot de beschikbaarheidsdatum van de release. De verbindingen, de schermen en de bijgewerkte documentatie worden gepubliceerd in [releaseopmerkingen](release-notes.md), op de datum van vrijgave.

## Opmerkingen bij de vervroegde release januari 2024 {#oct-jan-2024}

**Releasedatum**: 30-31 januari 2024

### Nieuwe functies{#jan-2024-features}

Deze release biedt de nieuwe mogelijkheden die hieronder worden vermeld.


<table>
<thead>
<tr>
<th><strong>Updates van de leverbaarheid</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ondersteunt nu de DMARC-verificatietechnologie.</p>
<p>Vanaf 1 februari 2024, Google en Yahoo! u hebt een DMARC-record nodig voor elk domein dat u gebruikt om e-mail naar hen te verzenden. Zorg ervoor dat u DMARC- verslag opstelling voor alle subdomeinen hebt hebt die u of aan Adobe in Journey Optimizer hebt gedelegeerd.</p>
<!--img src="assets/channel-reports.png"/-->
<p>Raadpleeg de <a href="../configuration/dmarc-record-update.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</tr>
</tbody>
</table>



### Verbeteringen {#jan-2024-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

**Rapportage**

* **Nieuwe op domein gebaseerde widgets voor indeling** - Er zijn nieuwe widgets toegevoegd om uw campagne- en journalistieke rapporten te verbeteren. De **Bounce Reden per domein**, **Verzonden en geleverd op domeinen**, **Opent en klikt op domein** en **Stuiteren en fouten per domein** widgets bieden een gedetailleerde uitsplitsing op domeinniveau voor belangrijke gegevens voor het verzenden van e-mail en het bijhouden van gegevens.

**SMS-kanaal**

* **Dubbele plug-in** - De dubbele Opt-In workflow voor SMS garandeert dat gebruikers zich expliciet aanmelden om berichten te ontvangen wanneer het verzoek van hun apparaat wordt geïnitieerd. Gebruikers starten het goedkeuringsproces door een binnenkomend SMS-bericht te verzenden. Na bevestiging van hun toestemming wordt een vervolgbericht verzonden waarin om een definitieve verificatie wordt verzocht. Als een gebruikersprofiel niet bestaat, wordt het gecreeerd na succesvolle bevestiging.

  Merk op dat dit slechts op de leveranciers van SMS van Sinch en Infobip van toepassing is.

**Reizen**

* **Duur van reactiegebeurtenissen** - De maximale duur die u kunt definiëren in het dialoogvenster **Gebeurtenissen van Reaction** is nu 29 dagen in plaats van 30.

* **Datumfilters** - U kunt nu aangepaste datums gebruiken om naast de bestaande vooraf gedefinieerde datumfilters de reisinventaris te filteren. Op deze manier kunt u de lijst verfijnen door ritten weer te geven die op een bepaalde datum zijn gepubliceerd, binnen een bepaalde maand, gedurende een heel jaar, of binnen een bepaald tijdsbereik.

* **Lees publiek**  - De activiteit van het Leespubliek baseert zich nu op de dataset van de profielmomentopname voor partijsegmenten, die slechts eenmaal per dag wordt geproduceerd nadat de geplande dagelijkse partijbaan in werking wordt gesteld.

**Frequentieregels**

* **Wekelijks en dagelijks frequentiegrens** - U kunt nu het maximum aantal berichten opgeven dat naar een klantprofiel wordt verzonden in een week of een dag, in aanvulling op de maand. De maximale frequentie is gebaseerd op de geselecteerde kalenderperiode en wordt opnieuw ingesteld aan het begin van het corresponderende tijdkader.


**Beslissingsbeheer**

* **Frequentiecorrectie op rand** - De teller van de frequentiecappend wordt nu bijgewerkt en beschikbaar in een besluit van de Beslissing API van de Rand in minder dan 3 seconden.