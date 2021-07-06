---
title: Inhoud personaliseren in Journey Optimizer
description: Aan de slag met personalisatie
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Beginner
source-git-commit: adb915a2013d1d1bf17ed5efb7ac4eb9c655c501
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 2%

---

# Aan de slag met personalisatie{#add-personalization}

Ontdek [!DNL Adobe Journey Optimizer] verpersoonlijkingsmogelijkheden om uw berichten aan elke specifieke ontvanger aan te passen door de gegevens en de informatie te gebruiken u over hem/haar hebt. Het kan zijn voornaam zijn, zijn belangen, waar hij woont, wat hij gekocht heeft, en meer.

[!DNL :arrow_forward:] [Leer hoe u een bericht in deze video&#39;s kunt aanpassen](#video-perso)

[!DNL Journey Optimizer] gebruikt een  **** inlinesimple verpersoonlijkingssyntaxis die op Handlebars wordt gebaseerd die u toestaat om uitdrukkingen met inhoud tot stand te brengen die door dubbele krullende steunen **{} wordt ingesloten}**. U kunt meerdere expressies zonder beperkingen toevoegen in dezelfde inhoud of hetzelfde veld. Meer informatie vindt u in [Persoonlijkheidssyntaxis](personalization-syntax.md).

De verpersoonlijking is gebaseerd op de profielgegevens die door **XDM Individual Profile** schema in Adobe Experience Platform wordt bepaald. Raadpleeg [Adobe Experience Platform Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) voor meer informatie.

>[!CAUTION]
>Het **XDM Individual Profile** schema is het enige schema u kunt gebruiken om inhoud in [!DNL Journey Optimizer] te personaliseren.

**Voorbeelden:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Bij het verwerken van het bericht (e-mail en push) vervangt Journey Optimizer de expressie door de gegevens in de database van het Experience Cloud Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` wordt &quot;Hello John Doe&quot;.


## Persoonlijke context{#personalization-areas}

De inhoud en weergave van berichten die door [!DNL Journey Optimizer] worden geleverd, kunnen op verschillende manieren worden gepersonaliseerd.

In elke gebieden met het redacteurspictogram, kunt u de verpersoonlijkingsredacteur (ook die als Redacteur van de Uitdrukking wordt bekend) openen en verpersoonlijking bepalen.

![](assets/perso_icon.png)

### Je e-mails aanpassen

Wanneer u een e-mail maakt, kunt u personalisatie toevoegen in het veld **E-mailonderwerp** van het bericht.

![](assets/perso_subject.png)

In de e-mailontwerper kunt u de inhoud personaliseren:

* In **message**: Klik in een tekstblok, klik **Persoonlijk** pictogram van de contextafhankelijke toolbar en selecteer **Personalisatie invoegen** gebied. Zie deze [sectie](../design-emails.md) voor meer informatie over de interface E-mailontwerper.

   ![](assets/perso_insert.png)

* Voor een **link**: Selecteer tekst of afbeelding in een tekstblok en klik op het pictogram **Koppeling invoegen** op de contextafhankelijke werkbalk. In het venster, kunt u een verpersoonlijkingsblok toevoegen door op **Add verpersoonlijking** pictogram te klikken.

   ![](assets/perso_link.png)

In beide gevallen, hebt u toegang tot de verpersoonlijkingsredacteur.

![](assets/perso_ee.png)


### Pushmeldingen aanpassen

U kunt uw **Pushmeldingen** op de volgende gebieden ook personaliseren:

* **Titel**
* **Lichaam**
* **Aangepast geluid**
* **Badges**
* **Aangepaste gegevens**

![](assets/perso_push.png)

Leer meer over de configuratie van de pushmelding in [deze sectie](../push-gs.md).

## De Expressieeditor gebruiken

De uitdrukkingsredacteur is het belangrijkste stuk van de verpersoonlijking in [!DNL Journey Optimizer].

Het is beschikbaar in elke context waarin u personalisatie als e-mail, push en aanbiedingen moet definiëren.

In de interface van de uitdrukkingsredacteur, zult u, alle gegevens selecteren schikken aanpassen en bevestigen om een aangepaste verpersoonlijking voor uw inhoud tot stand te brengen.

![](assets/perso_ee1.png)

In het linkergedeelte van het scherm wordt een domeinkiezer weergegeven waarmee u de bron voor personalisatie kunt selecteren. Beschikbare bronnen zijn:

* **Profiel** : Hiermee worden alle referenties weergegeven die zijn gekoppeld aan het profielschema dat wordt beschreven in de documentatie [ van het ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html)Adobe Experience Platform-gegevensmodel (XDM).
* **Segmentlidmaatschap** : maakt een lijst van alle segmenten die in de dienst van de Segmentatie van Adobe Experience Platform worden gecreeerd. Meer informatie over segmentatie is [hier](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en) beschikbaar.
* **Voorstellen** : geeft een overzicht van alle aanbiedingen verbonden aan een specifieke plaatsing. Selecteer de plaatsing en voeg de aanbiedingen in uw inhoud in. Raadpleeg [deze sectie](../deliver-personalized-offers.md) voor een volledige documentatie over het beheren van aanbiedingen.
* **Context** : wanneer de activiteit van het  **** Overseinen in een reis wordt gebruikt, zijn de contextuele reisgebieden beschikbaar in dit menu. Meer informatie vindt u in [deze sectie](personalization-use-case.md).
* **Helperfuncties** : Hiermee worden alle hulpfuncties weergegeven die beschikbaar zijn om bewerkingen uit te voeren op gegevens, zoals berekeningen, gegevensopmaak of conversies, voorwaarden en deze te manipuleren in de context van personalisatie. Meer informatie vindt u in [deze sectie](functions/functions.md).

Bij selectie wordt de verwijzing toegevoegd in de editor.

>[!NOTE]
>
>Het infopictogram naast &quot;+&quot;pictogram opent omhoog tooltip die meer details voor elke variabele verstrekt.

In het volgende voorbeeld, laat de uitdrukkingsredacteur u de profielen selecteren die hun verjaardag vandaag hebben dan de aanpassing voltooien door een specifieke aanbieding op te nemen die aan deze dag beantwoordt.

![](assets/perso_ee2.png)

## Instructievideo&#39;s{#video-perso}

Leer hoe u contextuele gebeurtenisinformatie van een reis kunt gebruiken om een bericht aan te passen.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Leer hoe u contextuele gebeurtenisinformatie van een reis kunt gebruiken om een bericht aan te passen.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
