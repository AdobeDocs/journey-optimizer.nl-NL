---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met gegevens in [!DNL Journey Optimizer]
description: Leer hoe u met gegevens werkt in [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 34f6f25560cbe7873f8aea9edda3d63dab63935a
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Aan de slag met gegevensbeheer in [!DNL Journey Optimizer] {#about-data}

De rijkheid en de dekking van eindklantengegevens is wat de sterkte en het succes van om het even welke oplossing van de klantenervaring bepaalt; en deze gegevens zijn voor elke klant van de hoogste waarde. De selectie van de technologie is nu inherent ingebouwd met strenge evaluatie van de mogelijkheden van het gegevensbeheer.

Met Adobe Journey Optimizer kunt u deze gegevens eenvoudig beheren, behouden en exporteren naar platforms of systemen die deel uitmaken van uw technologiestapel.

**Mijn gegevens, Mijn regels** - Journey Optimizer creëert voortdurend (en in real-time) een uitgebreide reeks klantprofielgegevens, naast alle reisgegevens en biedt gegevens aan die inherent zijn aan zijn activiteiten. Strawman-versies van gebruikersgegevens die van uw gegevensbestanden worden opgenomen worden verrijkt en omgezet in high-value gegevens met dekking evenals diepte. U wilt deze gegevens veilig, en tegelijkertijd alomtegenwoordig, zodat u de waarde ervan in uw totale IT-ecosysteem kunt benutten.

In grote lijnen is de flexibiliteit die u van uw gegevens wilt gebruiken driemaal zo groot:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <img alt="bestemmingen" src="assets/do-not-localize/dest.png" />
    <br>
  </td>
  <td>
    <div>Beschikbaar in andere bestemmingen - terwijl Journey Optimizer gegevens voor een hyper-gepersonaliseerde klantenervaring synergieert en integreert, wilt u deze gegevens in andere systemen in uw algemeen technologielandschap, terwijl u voor andere manieren kijkt om deze gegevens te gebruiken.
    <div>
     <a href="../start/ajo-integrations.md">Meer informatie</a></div>
    </div>
    <br>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <img alt="retentie" src="assets/do-not-localize/retention.png" />
  </td>
  <td>
    <div>Behouden voor een bepaalde duur - Industriële of regionale regelgeving (zoals de GDPR of de CCPA) of intern beleid inzake gegevensbeheer bepalen hoe lang of hoe kort gegevens in het Data Lake van Adobe Experience Platform moeten worden bewaard of gearchiveerd. <a href="../privacy/get-started-privacy.md">Meer informatie</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <img alt="beleid" src="assets/do-not-localize/policy.png" />
    <br>
  </td>
  <td>
    <div>Verwijderde basis een overeengekomen tijdlijn of uw beleid - Gegevensverwijdering is een cruciaal aspect van gegevensbescherming en is een belangrijke stap in alle processen voor gegevensbeheer. Journey Optimizer kan meer gegevens produceren dan vereist. Ook, wilt u uiterst zorgvuldig wat gebeurt na de vereiste duur voor een dataset - of het wegens nut of regelgeving gebeurt. Het besturingselement dat u nodig hebt, moet gegevens op elk gewenst moment verwijderen.</div>
  </td>
</tr>
</table>

Adobe Experience Platform, waarop Journey Optimizer is gebouwd, biedt u de hoogste niveaus van controle over gegevens - tijdens de service en aan het einde van de service. Binnen Journey Optimizer hebt u volledige controle over de gegevens (die worden ingevoerd in of gegenereerd door Journey Optimizer), het beheer dat op die gegevens van toepassing is en de bestemmingen waarnaar die gegevens worden verzonden.

Alle gegevens worden beschouwd als het bezit van Klanten en kunnen slechts op uw verzoek worden gehandhaafd, worden gecodeerd, worden verspreid of worden vernietigd. Adobe fungeert als uw fiduciair, zonder dat u rechten heeft op uw gegevens.

U kunt de gegevensflexibiliteit van Journey Optimizer gebruiken om te voldoen aan uw specifieke vereisten met betrekking tot het bewaren, archiveren of verwijderen van gegevens:

* **Gegevens extraheren/exporteren**: U kunt de extractie van brongegevens op elk moment starten via de API voor gegevenstoegang zonder boetes of vertragingen. De [API voor gegevenstoegang](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html) voorziet gebruikers van een interface RESTful die op de ontdekkingsbaarheid en de toegankelijkheid van ingebedde datasets binnen het Experience Platform wordt geconcentreerd. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Merk op dat de inhoud die in reizen of campagnes wordt gebruikt niet via hierboven vermelde API- of doelmethoden kan worden geëxtraheerd.

* **Bewaren van profielservicegegevens**: Voor gedragsgegevens en tijdreeksgegevens die aan een profiel worden toegevoegd, kunt u ervoor kiezen om de standaardinstelling van Journey Optimizer te gebruiken om deze gegevens te behouden gedurende maximaal 30 dagen vanaf de datum van toevoeging aan een profiel, of tot een andere door u geselecteerde tijdsperiode. De tijd die Adobe deze gegevens bewaart varieert van contract tot contract, en in het beleid van het de gegevensbehoud van een organisatie geschetst.

* **Opschoonings- en archiveringsmechanismen**: Het wissen van gegevens en archivering kan in Journey Optimizer vrij worden gedefinieerd en geautomatiseerd om het beleid voor gegevensbewaring te automatiseren. Het is mogelijk verschillende verouderingsstrategieën voor de verschillende gegevensentiteiten te definiëren. Exportmechanismen kunnen ook worden gedefinieerd om verouderde gegevens automatisch te exporteren voordat deze worden gewist of gearchiveerd.

* **Data Lake and Deletions**: De gegevens van de klant die in het Datameer worden opgeslagen kunnen door Journey Optimizer worden bewaard:

   * gedurende 7 dagen om het aan boord nemen van klantgegevens in de profielservices te vergemakkelijken, waarna deze gegevens definitief kunnen worden verwijderd, of
   * totdat u ervoor kiest om door u te worden verwijderd

* **Gegevens Extraheren bij beëindiging service/afsluiten**: Wanneer het contract volledig wordt geëindigd, worden de gegevens volledig verwijderd uit de opslagruimte van de Adobe. U kunt ook volledige profielextracten ophalen voordat u een overeenkomst beëindigt. Er zijn geen extra kosten voor deze functie. Dit kan op elk ogenblik en niet alleen bij beëindiging worden gedaan.

De bovenstaande methoden zijn contractueel gedefinieerd en gedetailleerd uiteengezet in de gegevensverwerkingsovereenkomst (DPA) die Adobe met u deelt aan het begin van een overeenkomst. Adobe-toepassingen, met inbegrip van Journey Optimizer, worden ontwikkeld op basis van het beginsel dat de gegevens van elke client worden behandeld als het eigen gegevensactief van die client.
