---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met gegevensbeheer in Journey Optimizer
description: Leer hoe u met gegevens werkt in Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: gegevens, beheer, platform
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Aan de slag met gegevensbeheer {#about-data}

De rijkheid en de dekking van eindklantengegevens is wat de sterkte en het succes van om het even welke oplossing van de klantenervaring bepaalt; en deze gegevens zijn heilig en van de hoogste waarde aan om het even welke bepaalde klant. De selectie van de technologie is nu inherent ingebouwd met strenge evaluatie van de mogelijkheden van het gegevensbeheer.

Met [!DNL Adobe Journey Optimizer] kunt u deze gegevens eenvoudig beheren, behouden en exporteren naar platforms of systemen die deel uitmaken van uw technologiestapel.

**Mijn Gegevens, Mijn Regels** - [!DNL Adobe Journey Optimizer] leidt voortdurend (en in real time) tot een rijke reeks gegevens van het klantenprofiel, naast alle reisgegevens en aanbiedergegevens die aan zijn verrichtingen inherent zijn. Strawman-versies van gebruikersgegevens die van uw gegevensbestanden worden opgenomen worden verrijkt en omgezet in high-value gegevens met dekking evenals diepte. U wilt deze gegevens veilig, en tegelijkertijd alomtegenwoordig, zodat u de waarde ervan in uw totale IT-ecosysteem kunt benutten.

In grote lijnen is de flexibiliteit die u van uw gegevens wilt gebruiken:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="bestemmingen" src="assets/do-not-localize/dest.png" /> 
    <br> Beschikbaar in andere bestemmingen - terwijl [!DNL Adobe Journey Optimizer] gegevens voor een hyper-gepersonaliseerde klantenervaring synergieert en integreert, wilt u deze gegevens in andere systemen in uw algemeen technologielandschap, terwijl u voor andere manieren kijkt om deze gegevens te gebruiken.
    <div>
     <a href="../integrations/ajo-integrations.md">Meer informatie</a></div>
    </div>
    <br>
  </td>
</tr>
</table>

<!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td>
</tr>
<tr style="border: 0;"-->
<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="beleid" src="assets/do-not-localize/policy.png" /> 
    <br> Geschrapte basis een overeengekomen chronologie of uw beleid - de schrapping van Gegevens is een kritiek aspect van gegevensbescherming en is een zeer belangrijke stap in alle processen van het gegevensbeheer. [!DNL Adobe Journey Optimizer] levert mogelijk meer gegevens op dan vereist. Ook, wilt u uiterst zorgvuldig wat gebeurt na de vereiste duur voor een dataset - of het wegens nut of regelgeving gebeurt. Het besturingselement dat u nodig hebt, moet gegevens op elk gewenst moment verwijderen. 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">Meer informatie</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform] , waarop [!DNL Adobe Journey Optimizer] is gebouwd, biedt u de hoogste niveaus van controle over gegevens tijdens de service en aan het einde van de service. Binnen [!DNL Journey Optimizer] hebt u volledige controle over de gegevens (die worden overgebracht naar of gegenereerd door [!DNL Journey Optimizer] ), het beheer dat op die gegevens van toepassing is en de bestemmingen waarnaar die gegevens worden verzonden.

Alle gegevens worden beschouwd als het bezit van Klanten en kunnen slechts op uw verzoek worden gehandhaafd, worden gecodeerd, worden verspreid of worden vernietigd. Adobe treedt op als uw fiduciair, zonder dat er rechten op uw gegevens zijn.

U kunt de gegevensflexibiliteit van [!DNL Journey Optimizer] gebruiken om te voldoen aan uw specifieke vereisten met betrekking tot het bewaren, archiveren of verwijderen van gegevens:

* **Extractie van Gegevens/de Uitvoer van Gegevens**: U kunt de extractie van brongegevens op elk ogenblik in werking stellen via de API van de gegevenstoegang zonder boetes of tijdvertragingen. De [ Toegang API van Gegevens ](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target="_blank"} voorziet gebruikers van een interface RESTful die op de ontdekkingsbaarheid en de toegankelijkheid van ingebedde datasets binnen [!DNL Adobe Experience Platform] wordt geconcentreerd. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

  Merk op dat de inhoud die in reizen of campagnes wordt gebruikt niet via hierboven vermelde API- of doelmethoden kan worden geëxtraheerd.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer's default setting of retaining this data for up to 91 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization's data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Aankopen en archiveringsmechanismen**: Het zuiveren van gegevens en archivering kan vrij worden bepaald en in [!DNL Adobe Journey Optimizer] worden geautomatiseerd om beleid van het gegevensbehoud te automatiseren. Het is mogelijk verschillende verouderingsstrategieën voor de verschillende gegevensentiteiten te definiëren. Exportmechanismen kunnen ook worden gedefinieerd om verouderde gegevens automatisch te exporteren voordat deze worden gewist of gearchiveerd.

  De werkruimte van de Levenscyclus van Gegevens staat u toe om diverse taken van de gegevenslevenscyclus tot stand te brengen en te controleren, met inbegrip van het schrappen van consumentenidentiteiten en het plannen van datasettermijnen. Deze werkruimte is beschikbaar met het beveiligings- en privacyschild en het gezondheidsschild. Leer meer op [ deze pagina ](../privacy/data-hygiene.md).

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Extraheren van Gegevens bij de Beëindiging/van de Beëindiging van de Overeenkomst**: Wanneer het contract wordt geëindigd, worden uw gegevens volledig verwijderd uit de opslagruimte van Adobe. U kunt ook volledige profielextracten ophalen voordat u een overeenkomst beëindigt. Er zijn geen extra kosten voor deze functie. Dit kan op elk ogenblik en niet alleen bij beëindiging worden gedaan.

De bovenstaande methoden zijn contractueel gedefinieerd en gedetailleerd uiteengezet in de gegevensverwerkingsovereenkomst (DPA) die Adobe met u deelt aan het begin van een overeenkomst. Adobe-toepassingen, waaronder [!DNL Journey Optimizer] , zijn ontwikkeld op basis van het principe dat de gegevens van elke client worden behandeld als het gegevenselement dat eigendom is van de client.
