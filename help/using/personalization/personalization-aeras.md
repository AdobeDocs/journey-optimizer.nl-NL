---
title: Personalisatiecontexten in Journey Optimizer
description: Leer in welke contexten u verpersoonlijking kunt toevoegen
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 3%

---

# De context en het hulpmiddel van de aanpassing {#personalization-areas}

![](../assets/do-not-localize/badge.png)

De inhoud en weergave van berichten die door Journey Optimizer worden geleverd, kunnen op verschillende manieren worden gepersonaliseerd.

Alle gebieden verbonden aan het redacteurspictogram kunnen de verpersoonlijkingsredacteur openen en verpersoonlijkingsinhoud ontvangen.

![](assets/perso_icon.png)

## Je e-mails aanpassen

Wanneer u een e-mail maakt, kunt u personalisatie toevoegen in het veld **E-mailonderwerp** van het bericht.

![](assets/perso_subject.png)

In de e-mailontwerper kunt u de inhoud personaliseren:

* In **message**: Klik in een tekstblok, klik **Persoonlijk** pictogram van de contextafhankelijke toolbar en selecteer **Personalisatie invoegen** gebied. Zie deze [sectie](../design-emails.md) voor meer informatie over de interface E-mailontwerper.

   ![](assets/perso_insert.png)

* Voor een **link**: Selecteer tekst of afbeelding in een tekstblok en klik op het pictogram **Koppeling invoegen** op de contextafhankelijke werkbalk. In het venster, kunt u een verpersoonlijkingsblok toevoegen door op **Add verpersoonlijking** pictogram te klikken.

   ![](assets/perso_link.png)

## Pushmeldingen aanpassen

U kunt uw **Pushmeldingen** op de volgende gebieden ook personaliseren:

* **Titel**
* **Lichaam**
* **Aangepast geluid**
* **Badges**
* **Aangepaste gegevens**

![](assets/perso_push.png)

Leer meer over de configuratie van de pushmelding in [deze sectie](../create-push.md).

## Expressieeditor gebruiken

De expression editor is het middelpunt van de personalisatie in Journey Optimizer.

Het is beschikbaar in elke context waarin u personalisatie als e-mail, push en aanbiedingen moet definiëren.

In de interface van de uitdrukkingsredacteur, zult u, alle gegevens selecteren schikken aanpassen en bevestigen om een aangepaste verpersoonlijking voor uw inhoud tot stand te brengen.

![](assets/perso_ee1.png)

In het linkergedeelte van het scherm wordt een domeinkiezer weergegeven waarmee u de bron voor personalisatie kunt selecteren.

* **Profiel** : Hiermee worden alle referenties weergegeven die zijn gekoppeld aan het profielschema dat wordt beschreven in de documentatie [ van het ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl)Adobe Experience Platform-gegevensmodel (XDM).
* **Segmentlidmaatschap** : maakt een lijst van alle segmenten die in de dienst van de Segmentatie van Adobe Experience Platform worden gecreeerd. Meer informatie over segmentatie is [hier](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en) beschikbaar
* **Voorstellen** : geeft een overzicht van alle aanbiedingen verbonden aan een specifieke plaatsing. Selecteer de plaatsing en voeg de aanbiedingen in uw inhoud in. Raadpleeg [deze sectie](../deliver-personalized-offers.md) voor een volledige documentatie over het beheren van aanbiedingen
* **Context** : wanneer de activiteit van het  **** Overseinen in een reis wordt gebruikt, zijn de contextuele reisgebieden beschikbaar in dit menu. Zie [deze sectie](personalization-use-case.md)
* **Helperfuncties** : Hiermee worden alle hulpfuncties weergegeven die beschikbaar zijn om bewerkingen uit te voeren op gegevens, zoals berekeningen, gegevensopmaak of conversies, voorwaarden en deze te manipuleren in de context van personalisatie. [Meer informatie](functions/functions.md)



Bij selectie wordt de verwijzing toegevoegd in de editor.

>[!NOTE]
>
>Het infopictogram naast &quot;+&quot;pictogram opent omhoog tooltip die meer details voor elke variabele verstrekt.

In het volgende voorbeeld, laat de uitdrukkingsredacteur u de profielen selecteren die hun verjaardag vandaag hebben dan de aanpassing voltooien door een specifieke aanbieding op te nemen die aan deze dag beantwoordt.

![](assets/perso_ee2.png)




