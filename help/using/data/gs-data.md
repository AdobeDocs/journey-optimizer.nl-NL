---
solution: Journey Optimizer
product: journey optimizer
title: Aan de slag met gegevens in [!DNL Journey Optimizer]
description: Leer hoe u met gegevens werkt in [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: df1b520f693d33d7080b203df0d3808144feb6e3
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Aan de slag met gegevensbeheer in [!DNL Journey Optimizer] {#about-data}

De rijkheid en de dekking van eindklantengegevens is wat de sterkte en het succes van om het even welke oplossing van de klantenervaring bepaalt; en deze gegevens zijn heilig en van de hoogste waarde voor elke klant. De selectie van de technologie is nu inherent ingebouwd met strenge evaluatie van de mogelijkheden van het gegevensbeheer.

Met [!DNL Adobe Journey Optimizer]kunt u deze gegevens eenvoudig beheren, behouden en exporteren naar platforms of systemen die deel uitmaken van uw technologiestapel.

**Mijn gegevens, Mijn regels** - [!DNL Adobe Journey Optimizer] voortdurend (en in real time) leidt tot een rijke reeks gegevens van het klantenprofiel, naast alle reisgegevens en aanbiedt gegevens die aan zijn verrichtingen inherent zijn. Strawman-versies van gebruikersgegevens die van uw gegevensbestanden worden opgenomen worden verrijkt en omgezet in high-value gegevens met dekking evenals diepte. U wilt deze gegevens veilig, en tegelijkertijd alomtegenwoordig, zodat u de waarde ervan in uw totale IT-ecosysteem kunt benutten.

In grote lijnen is de flexibiliteit die u van uw gegevens wilt gebruiken:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="bestemmingen" src="assets/do-not-localize/dest.png" /> 
    <br>Beschikbaar op andere bestemmingen - terwijl [!DNL Adobe Journey Optimizer] synergieert en integreert gegevens voor een hyper-gepersonaliseerde klantenervaring, wilt u deze gegevens in andere systemen in uw algemeen technologielandschap, terwijl u voor andere manieren kijkt om deze gegevens te gebruiken.
    <div>
     <a href="../start/ajo-integrations.md">Meer informatie</a></div>
    </div>
    <br>
  </td>
</tr>
  <!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td-->
</tr>
<tr style="border: 0;">
  <td>
    <div><img alt="beleid" src="assets/do-not-localize/policy.png" /> 
    <br>Verwijderde basis een overeengekomen tijdlijn of uw beleid - Gegevensverwijdering is een cruciaal aspect van gegevensbescherming en is een belangrijke stap in alle processen voor gegevensbeheer. [!DNL Adobe Journey Optimizer] kan meer gegevens produceren dan vereist. Ook, wilt u uiterst zorgvuldig wat gebeurt na de vereiste duur voor een dataset - of het wegens nut of regelgeving gebeurt. Het besturingselement dat u nodig hebt, moet gegevens op elk gewenst moment verwijderen. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">Meer informatie over gegevenshygiëne vindt u in de documentatie van Adobe Experience Platform</a></div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], waarover [!DNL Adobe Journey Optimizer] is samengesteld, biedt u de hoogste niveaus van controle over gegevens - tijdens de service en aan het einde van de service. Within [!DNL Journey Optimizer], hebt u volledige controle over de gegevens (die worden overgebracht naar of gegenereerd door, [!DNL Journey Optimizer]), het beheer dat op die gegevens betrekking heeft en de bestemmingen waar die gegevens worden verzonden.

Alle gegevens worden beschouwd als het bezit van Klanten en kunnen slechts op uw verzoek worden gehandhaafd, worden gecodeerd, worden verspreid of worden vernietigd. Adobe fungeert als uw fiduciair, zonder dat u rechten heeft op uw gegevens.

U kunt de [!DNL Journey Optimizer]De flexibiliteit van gegevens om te voldoen aan uw specifieke vereisten met betrekking tot het bewaren, archiveren of verwijderen van gegevens:

* **Gegevens extraheren/exporteren**: U kunt de extractie van brongegevens op elk moment starten via de API voor gegevenstoegang zonder boetes of vertragingen. De [API voor gegevenstoegang](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target=&quot;_blank&quot;} biedt gebruikers een RESTful-interface die gericht is op de detecteerbaarheid en toegankelijkheid van opgenomen datasets binnen [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Merk op dat de inhoud die in reizen of campagnes wordt gebruikt niet via hierboven vermelde API- of doelmethoden kan worden geëxtraheerd.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Opschoonings- en archiveringsmechanismen**: Het wissen van gegevens en archivering kan vrij worden gedefinieerd en geautomatiseerd in [!DNL Adobe Journey Optimizer] om het beleid voor gegevensbewaring te automatiseren. Het is mogelijk verschillende verouderingsstrategieën voor de verschillende gegevensentiteiten te definiëren. Exportmechanismen kunnen ook worden gedefinieerd om verouderde gegevens automatisch te exporteren voordat deze worden gewist of gearchiveerd.

   De werkruimte van de Hygiëne van Gegevens in Adobe Experience Platform UI staat u toe om diverse taken van de gegevenshygiëne tot stand te brengen en te controleren, met inbegrip van het schrappen van consumentenidentiteiten en het plannen van datasetvervalsing. Deze werkruimte is beschikbaar met het beveiligings- en privacyschild en het gezondheidsschild. Meer informatie in [Adobe Experience Platform-documentatie](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html){target=&quot;_blank&quot;}.

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Gegevens Extraheren bij beëindiging service/afsluiten**: Wanneer het contract volledig wordt geëindigd, worden de gegevens volledig verwijderd uit de opslagruimte van de Adobe. U kunt ook volledige profielextracten ophalen voordat u een overeenkomst beëindigt. Er zijn geen extra kosten voor deze functie. Dit kan op elk ogenblik en niet alleen bij beëindiging worden gedaan.

De bovenstaande methoden zijn contractueel gedefinieerd en gedetailleerd uiteengezet in de gegevensverwerkingsovereenkomst (DPA) die Adobe met u deelt aan het begin van een overeenkomst. Adobe-toepassingen, inclusief [!DNL Journey Optimizer], zijn gebaseerd op het beginsel dat de gegevens van elke cliënt worden behandeld als het eigen gegevensactief van die cliënt.
