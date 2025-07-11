---
solution: Journey Optimizer
product: journey optimizer
title: Uw eerste regel samenstellen
description: Leer hoe u regels maakt voor uw georkestreerde campagnes
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 5e956a6a-0b89-4d78-8f16-fe9fceb25674
source-git-commit: 779c90f0be57749a63da103d18cc642106c5f837
workflow-type: tm+mt
source-wordcount: '1783'
ht-degree: 0%

---

# Uw eerste regel samenstellen {#build-query}

+++ Inhoudsopgave

| Welkom bij georkestreerde campagnes | Start uw eerste georkestreerde campagne | De database opvragen | Gecontroleerde campagnes |
|---|---|---|---|
| [ wordt begonnen met georkestreerde campagnes ](gs-orchestrated-campaigns.md)<br/><br/>[ stappen van de Configuratie ](configuration-steps.md)<br/><br/>[ Toegang en beheer georkestreerde campagnes ](access-manage-orchestrated-campaigns.md)<br/><br/>[ Belangrijke stappen om een georkestreerde campagne ](gs-campaign-creation.md) tot stand te brengen | [ creeer en programma de campagne ](create-orchestrated-campaign.md)<br/><br/>[ Orchestrate activiteiten ](orchestrate-activities.md)<br/><br/>[ Begin en controleer de campagne ](start-monitor-campaigns.md)<br/><br/>[ Meldend ](reporting-campaigns.md) | [ Werk met de regelbouwer ](orchestrated-rule-builder.md)<br/><br/><b>[ bouwt uw eerste vraag ](build-query.md)</b><br/><br/>[ uit geeft uitdrukkingen ](edit-expressions.md)<br/><br/>[ opnieuw op ](retarget.md) | [ wordt begonnen met activiteiten ](activities/about-activities.md)<br/><br/> Activiteiten:<br/>[ en-sluit zich aan ](activities/and-join.md) - [ bouwt publiek ](activities/build-audience.md) - [ dimensie van de Verandering ](activities/change-dimension.md) - [ de activiteiten van het Kanaal ](activities/channels.md) - [ combineren ](activities/combine.md) - [ Deduplicatie ](activities/deduplication.md) - [ Verrijking ](activities/enrichment.md) Formeel k [ - ](activities/fork.md) Verzoening [ - ](activities/reconciliation.md) sparen publiek [ - ](activities/save-audience.md) Gesplitst [ - ](activities/split.md) wacht [](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

Documentatie in uitvoering

>[!ENDSHADEBOX]

De belangrijkste stappen om regels voor uw georkestreerde campagnes te bouwen zijn als volgt:

1. **voegt voorwaarden** toe - creeer douanevoorwaarden om uw vraag te filtreren door uw eigen voorwaarde met attributen van het gegevensbestand en geavanceerde uitdrukkingen te bouwen.
1. **combineer voorwaarden** - plaats de voorwaarden in het canvas gebruikend groepen en logische exploitanten.
1. **Controle en bevestig de regel** - controleer de resulterende gegevens van uw regel alvorens het op te slaan.

## Een voorwaarde toevoegen {#conditions}

Ga als volgt te werk om voorwaarden aan uw query toe te voegen:

1. Heb toegang tot de regelbouwer van een **[!UICONTROL Build audience]** activiteit.

1. Klik **toevoegen voorwaarde** knoop om een eerste voorwaarde voor uw vraag tot stand te brengen.

   U kunt de query ook starten met een vooraf gedefinieerd filter. Klik hiertoe op de knop **[!UICONTROL Select or save filter]** en kies **[!UICONTROL Select predefined filter]** .

   ![ beeld dat de regelbouwer ](assets/rule-builder-add.png) toont

1. Identificeer het attribuut van de dabatase als criteria voor uw voorwaarde te gebruiken. Het pictogram &quot;i&quot; naast een kenmerk bevat informatie over de tabel waarin het wordt opgeslagen en het gegevenstype van het kenmerk.

   ![ beeld dat de selectie van een attribuut ](assets/rule-builder-select-attribute.png) toont

   >[!NOTE]
   >
   >De **geeft uitdrukking** knoop uit staat u toe om de uitdrukkingsredacteur te gebruiken om een uitdrukking manueel te bepalen gebruikend gebieden van het gegevensbestand en hulpfuncties. [ Leer hoe te om uitdrukkingen uit te geven ](../orchestrated/edit-expressions.md)

1. Klik het ![ beeld dat de Meer actieknoop ](assets/do-not-localize/rule-builder-icon-more.svg) naast een attribuut toont om tot deze extra opties toegang te hebben:

+++ Verdeling van waarden

   Analyseer de verdeling van waarden voor een bepaald kenmerk binnen de tabel. Deze functie is handig voor het begrijpen van de beschikbare waarden, hun aantallen en percentages. Het helpt ook problemen zoals inconsistente hoofdlettergebruik of spelling te voorkomen bij het maken van query&#39;s of het maken van expressies.

   Voor kenmerken met een groot aantal waarden wordt alleen de eerste twintig weergegeven. In dergelijke gevallen lijkt een **[!UICONTROL Partial load]** -melding deze beperking aan te geven. U kunt geavanceerde filters toepassen om de weergegeven resultaten te verfijnen en de focus op specifieke waarden of subsets van gegevens te richten.

   ![ beeld dat de Distributie van waardeinterface toont ](assets/rule-builder-distribution-values.png)

+++

+++ Toevoegen aan Favorieten

   Door kenmerken toe te voegen aan het menu Favorieten hebt u snel toegang tot de meest gebruikte kenmerken. U kunt maximaal 20 kenmerken toevoegen aan favorieten. Favoriete en recente kenmerken zijn gekoppeld aan elke gebruiker binnen een organisatie, zodat de toegankelijkheid op verschillende computers gegarandeerd is en een naadloze ervaring op alle apparaten mogelijk is.

   Gebruik het menu **[!UICONTROL Favorites and recents]** voor toegang tot de gewenste kenmerken. Favoriete kenmerken worden als eerste weergegeven, gevolgd door recent gebruikte kenmerken, zodat u gemakkelijk de vereiste kenmerken kunt vinden. Als u een kenmerk uit de favorieten wilt verwijderen, selecteert u het sterpictogram opnieuw.

   ![ beeld dat de favoriete interface ](assets/rule-builder-favorites.png) toont

+++

1. Klik op **[!UICONTROL Confirm]** om het geselecteerde kenmerk aan uw voorwaarde toe te voegen.

1. Er wordt een deelvenster met eigenschappen weergegeven waarin u de gewenste waarde voor het kenmerk kunt configureren.

   ![ beeld dat de regelbouwer met een toegevoegde voorwaarde toont ](assets/rule-builder-condition.png)

1. Selecteer de **[!UICONTROL Operator]** die u wilt toepassen in de vervolgkeuzelijst. Er zijn verschillende operatoren beschikbaar voor gebruik. Operatoren die beschikbaar zijn in de vervolgkeuzelijst, zijn afhankelijk van het gegevenstype van het kenmerk.

   +++Lijst met beschikbare operatoren

   | Operator | Doel | Voorbeeld |
   |---|---|---|
   | Gelijk aan | Retourneert een resultaat dat identiek is aan de gegevens die zijn ingevoerd in de tweede kolom Waarde. | Achternaam (@lastName) gelijk aan &#39;Jones&#39; retourneert alleen ontvangers met als achternaam Jones. |
   | Niet gelijk aan | Retourneert alle waarden die niet identiek zijn aan de ingevoerde waarde. | Taal (@taal) is niet gelijk aan &#39;Engels&#39;. |
   | Groter dan | Retourneert een waarde die groter is dan de ingevoerde waarde. | Leeftijd (@age) groter dan 50 zal alle waarden groter dan &quot;50&quot;terugkeren, zoals &quot;51&quot;, &quot;52&quot;. |
   | Minder dan | Retourneert een waarde die kleiner is dan de ingevoerde waarde. | Aanmaakdatum (@created) voordat &#39;DaysAgo(100)&#39; alle ontvangers retourneert die minder dan 100 dagen geleden zijn gemaakt. |
   | Groter dan of gelijk aan | Retourneert alle waarden die gelijk zijn aan of groter zijn dan de ingevoerde waarde. | Leeftijd (@age) groter dan of gelijk aan &#39;30&#39; retourneert alle ontvangers van 30 jaar of ouder. |
   | Kleiner dan of gelijk aan | Retourneert alle waarden die gelijk zijn aan of lager zijn dan de ingevoerde waarde. | Leeftijd (@age) kleiner dan of gelijk aan &#39;60&#39; retourneert alle ontvangers van 60 jaar of ouder. |
   | Opgenomen in | Retourneert resultaten die zijn opgenomen in de aangegeven waarden. Deze waarden moeten door een komma worden gescheiden. | De geboortedatum (@geboortedatum) is opgenomen in &#39;12-10-1979.12-10-1984&#39; en retourneert de tussen deze data geboren ontvangers. |
   | Niet in | Werkt zoals is opgenomen in operator. Hier worden ontvangers uitgesloten op basis van de ingevoerde waarden. | Geboortedatum (@geboortedatum) is niet opgenomen in &quot;10-12-1979,12-10-1984&quot;. Ontvangers die binnen deze datums zijn geboren, worden niet geretourneerd. |
   | Is leeg | Retourneert resultaten die overeenkomen met een lege waarde in de tweede kolom Waarde. | Mobiele (@mobilePhone) is leeg en retourneert alle ontvangers die geen mobiel nummer hebben. |
   | Is niet leeg | Werkt in omgekeerde volgorde naar de operator Is leeg. Het is niet nodig gegevens in te voeren in de tweede kolom Waarde. | E-mail (@email) is niet leeg. |
   | Begint met | Retourneert resultaten die beginnen met de ingevoerde waarde. | Account # (@account) begint met &#39;32010&#39;. |
   | Begint niet met | Retourneert resultaten die niet beginnen met de ingevoerde waarde. | Account # (@account) begint niet met &#39;20&#39;. |
   | Bevat | Retourneert resultaten die ten minste de ingevoerde waarde bevatten. | Het e-maildomein (@domain) bevat &#39;mail&#39; en retourneert alle domeinnamen die &#39;mail&#39; bevatten, zoals &#39;gmail.com&#39;. |
   | Bevat niet | Retourneert resultaten die niet de ingevoerde waarde bevatten. | E-maildomein (@domein) bevat geen &#39;vo&#39;. Domeinnamen die &#39;vo&#39; bevatten, zoals &#39;voila.fr&#39;, worden niet weergegeven in de resultaten. |
   | leuk | Net als bij de operator Bevat kunt u een jokerteken % in de waarde invoegen. | Achternaam (@lastName) zoals &#39;Jon%s&#39;. Het jokerteken fungeert als een &#39;joker&#39; om namen als &#39;Jones&#39; te zoeken. |
   | Niet leuk | Net als bij de operator Bevat kunt u een jokerteken % in de waarde invoegen. | Achternaam (@lastName) houdt niet van &#39;Smi%h&#39;. Ontvangers met de achternaam Smith worden niet geretourneerd. |

+++

1. Op het **gebied van de Waarde**, bepaal de verwachte waarde. U kunt de uitdrukkingsredacteur ook gebruiken om een uitdrukking manueel te bepalen gebruikend gebieden van het gegevensbestand en hulpfuncties. Om dit te doen, klik het ![ beeld dat het pictogram van de uitdrukkingsredacteur ](assets/do-not-localize/rule-builder-icon-editor.svg) toont. [ Leer hoe te om uitdrukkingen uit te geven ](../orchestrated/edit-expressions.md)

   Voor datumtekstkenmerken zijn vooraf gedefinieerde waarden beschikbaar met de optie **[!UICONTROL Presets]** .

   +++Zie voorbeeld

   ![ beeld dat de vooraf ingestelde optie ](assets/rule-builder-attribute-preset.png) toont

+++

### Aangepaste voorwaarden voor gekoppelde tabellen (1-1 en 1-N koppelingen){#links}

De voorwaarden van de douane staan u toe om lijsten te vragen verbonden aan de lijst die momenteel door uw regel wordt gebruikt. Dit omvat lijsten met een 1-1 kardinaliteitsverbinding, of inzamelingstabellen (verbinding 1-N).

Voor a **1-1 verbinding**, navigeer aan de verbonden lijst, selecteer de gewenste attributen en bepaal de verwachte waarde.

U kunt een lijstverbinding in de **plukker van de Waarde** ook direct selecteren en bevestigen. In dat geval moeten de waarden die beschikbaar zijn voor de geselecteerde tabel, worden geselecteerd met een speciale kiezer, zoals in het onderstaande voorbeeld wordt getoond.

+++voorbeeld van Query

Hier, richt de vraag zich merken het waarvan etiket &quot;loopt&quot;.

1. Navigeer binnen de **Merk** lijst en selecteer het **3} attribuut van het Etiket {.**

   ![ Schermafbeelding van de lijst van het Merk ](assets/rule-builder-1-1-attribute.png)

1. Definieer de verwachte waarde voor het kenmerk.

   ![ Schermafbeelding van de lijst van het Merk ](assets/rule-builder-1-1-attribute-value.png)

Hier volgt een queryvoorbeeld waarin een tabelkoppeling rechtstreeks is geselecteerd. Beschikbare waarden voor deze tabel moeten worden geselecteerd in een speciale kiezer.

![ Schermafbeelding van de lijst van het Merk ](assets/rule-builder-1-1-attribute-table.png)

+++

Voor a **1-N verbinding**, kunt u sub-voorwaarden bepalen om uw vraag te verfijnen, zoals aangetoond in het hieronder voorbeeld.

+++voorbeeld van Query

Hier richt de vraag zich op ontvangers die aankopen hebben gedaan met betrekking tot het Brewmsaster-product, voor meer dan 100$.

1. Selecteer **Aankopen** lijst en bevestig.

1. Klik op **[!UICONTROL Add condition]** om de subvoorwaarden te definiëren die op de geselecteerde tabel moeten worden toegepast.

   ![ Schermafbeelding van de lijst van de Aankoop ](assets/rule-builder-1-n-purchase.png)

1. Voeg subvoorwaarden toe die aan uw behoeften voldoen.

   ![ Schermafbeelding van de lijst van de Aankoop ](assets/rule-builder-1-n-collection.png)

+++

### Aangepaste omstandigheden met geaggregeerde gegevens {#aggregate}

Met aangepaste omstandigheden kunt u gezamenlijke bewerkingen uitvoeren. Hiervoor moet u rechtstreeks een kenmerk in een verzamelingstabel selecteren:

1. Navigeer binnen de gewenste inzamelingstabel en selecteer de attributen waarop u een gezamenlijke verrichting wilt uitvoeren.

1. In de eigenschappen ruit, knevel op de **Samengevoegde gegevens** optie en selecteer de gewenste gezamenlijke functie.

   ![ Schermafbeelding van de Samengevoegde gegevensoptie ](assets/rule-builder-aggregate.png)

## Voorwaarden combineren met operatoren {#operators}

Telkens als u een nieuwe voorwaarde in uw regel toevoegt, wordt het automatisch verbonden met de bestaande voorwaarde door een **EN** exploitant. Dit betekent dat de resultaten van de twee voorwaarden worden gecombineerd.

Als u de operator tussen voorwaarden wilt wijzigen, klikt u erop en selecteert u de gewenste operator.

![ Voorbeeld van een vraag ](assets/rule-builder-change-operator.png)

Beschikbare operatoren zijn:

* **EN (Doorsnede)**: Combineert resultaten die alle het filtreren componenten in de uitgaande overgangen aanpassen.
* **OF (Unie)**: Omvat resultaten die minstens één van de het filtreren componenten in de uitgaande overgangen aanpassen.
* **BEHALVE (Uitsluiting)**: Sluit resultaten uit die alle het filtreren componenten in de uitgaande overgang aanpassen.

## Manipulatieomstandigheden {#manipulate}

De werkbalk van het canvas van de regelbouwer biedt opties voor het eenvoudig manipuleren van de voorwaarden binnen uw regel:

| Werkbalkpictogram | Beschrijving |
|--- |--- |
| ![ Beweging omhoog selectiepictogram ](assets/do-not-localize/rule-builder-icon-up.svg) | Verplaats de component omhoog een rij. |
| ![ Beweging onderaan selectiepictogram ](assets/do-not-localize/rule-builder-icon-down.svg) | Verplaats de component een rij omlaag. |
| ![ het selectiepictogram van de Groep ](assets/do-not-localize/rule-builder-icon-group.svg) | Plaats twee componenten in een groep. |
| ![ Ungroup selectiepictogram ](assets/do-not-localize/rule-builder-icon-ungroup.svg) | Scheid de componenten van één groep. |
| ![ breid al pictogram ](assets/do-not-localize/rule-builder-icon-expand.svg) uit | Vouw alle groepen uit. |
| ![ Vouw al pictogram ](assets/do-not-localize/rule-builder-icon-collapse.svg) samen | Vouw alle groepen samen. |
| ![ verwijder al pictogram ](assets/do-not-localize/rule-builder-icon-delete.svg) | Alle groepen en componenten verwijderen. |

Afhankelijk van uw behoeften, kunt u tussenliggende groepen componenten moeten tot stand brengen door componenten in een zelfde groep te groeperen en hen te verbinden samen.

* Om twee bestaande voorwaarden te groeperen, selecteer één van de twee voorwaarden en klik de ![ Beweging omhoog selectiepictogram ](assets/do-not-localize/rule-builder-icon-up.svg) of ![ Beweging onderaan selectiepictogram ](assets/do-not-localize/rule-builder-icon-down.svg) knoop om het met de voorwaarde hierboven of onder te groeperen.

* Om een bestaande voorwaarde met nieuwe te groeperen, selecteer de voorwaarde, klik het ![ beeld dat de Meer actieknoop ](assets/do-not-localize/rule-builder-icon-more.svg) toont en **[!UICONTROL Add group]** selecteert. Selecteer het nieuwe kenmerk dat u aan de groep wilt toevoegen en bevestig het vervolgens.

  ![](assets/rule-builder-edit-groups.png)

In het onderstaande voorbeeld hebben we een tussengroep opgericht voor klanten die het BrewMaster- of VanillaVelvet-product hebben aangeschaft.

![](assets/rule-builder-groups.png)

## Uw query controleren en valideren

Zodra u uw vraag in het canvas hebt gebouwd, kunt u het controleren gebruikend de **eigenschappen van de Regel** ruit. Beschikbare bewerkingen zijn:

* **resultaten van de Mening:** toont de gegevens die uit uw vraag voortvloeien.
* **mening van de Code**: Toont een op code-gebaseerde versie van de vraag in SQL.
* **berekent**: Updates en toont het aantal verslagen die door uw regel worden gericht.
* **Uitgezocht of sparen filter**: Kies een bestaand vooraf bepaald filter om in het canvas te gebruiken, of sparen uw vraag als vooraf bepaald filter voor toekomstig hergebruik.

<br/>

    >[!BELANGRIJK] 
    > 
    >Selecteer een vooraf bepaald filter van de de eigenschappen van de Regel ruit vervangt de regel die in het canvas met de geselecteerde filter is gebouwd.

Wanneer uw regel gereed is, klikt u op de knop **[!UICONTROL Confirm]** in de map om deze op te slaan.
