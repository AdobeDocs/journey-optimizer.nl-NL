---
title: Inhoud personaliseren in Journey Optimizer
description: Aan de slag met personalisatie
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 244f05998098bf1770d5f33c955f09688f58ffe7
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 5%

---

# Aan de slag met personalisatie{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] personaliseringsmogelijkheden om uw berichten aan elke specifieke ontvanger aan te passen door de gegevens en de informatie te gebruiken u over hen hebt. Het kan hun voornaam zijn, belangen, waar ze wonen, wat ze hebben gekocht, en meer.

➡️ [Leer hoe u een bericht in deze video&#39;s kunt aanpassen](#video-perso)

[!DNL Journey Optimizer] gebruikt een **inline** eenvoudige verpersoonlijkingssyntaxis die op Handlebars wordt gebaseerd die u toestaat om uitdrukkingen tot stand te brengen met inhoud die door dubbele krullende steunen wordt ingesloten **{{}**. U kunt meerdere expressies zonder beperkingen toevoegen in dezelfde inhoud of hetzelfde veld. Meer informatie in [Personalisatiesyntaxis](personalization-syntax.md).

De verpersoonlijking is gebaseerd op de profielgegevens die door **Afzonderlijk XDM-profiel** schema gedefinieerd in Adobe Experience Platform. Meer informatie in [Adobe Experience Platform Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl){target=&quot;_blank&quot;}.

>[!CAUTION]
>De **Afzonderlijk XDM-profiel** schema is het enige schema dat u kunt gebruiken om inhoud in te personaliseren [!DNL Journey Optimizer].

**Voorbeelden:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Bij het verwerken van het bericht (e-mail en push) vervangt Journey Optimizer de expressie door de gegevens in de database van het Experience Cloud Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` wordt &quot;Hello John Doe&quot;.


## Persoonlijke context{#personalization-areas}

De inhoud en weergave van door [!DNL Journey Optimizer] U kunt op verschillende manieren een persoonlijk tintje geven.

In elke gebieden met het redacteurspictogram, kunt u de verpersoonlijkingsredacteur (ook die als Redacteur van de Uitdrukking wordt bekend) openen en verpersoonlijking bepalen.

![](assets/perso_icon.png)

### Je e-mails aanpassen

Wanneer u een e-mailbericht maakt, kunt u personalisatie toevoegen aan de **[!UICONTROL Subject line]** veld van het bericht.

![](assets/perso_subject.png)

In de e-mailontwerper kunt u de inhoud personaliseren:

* In de **message**: Klik in een tekstblok en klik op de knop **Persoonlijk maken** pictogram in de contextafhankelijke werkbalk en selecteer **Verpersoonlijking invoegen** veld. Zie deze voor meer informatie over de interface E-mailontwerper [sectie](../design-emails.md).

   ![](assets/perso_insert.png)

* Voor een **link**: Selecteer tekst of een afbeelding in een tekstblok. Klik op de knop **Koppeling invoegen** van de contextafhankelijke werkbalk. In het venster kunt u een verpersoonlijkingsblok toevoegen door op het **Aanpassing toevoegen** pictogram.

   ![](assets/perso_link.png)

In beide gevallen, hebt u toegang tot de verpersoonlijkingsredacteur.

![](assets/perso_ee.png)

### Pushmeldingen aanpassen

U kunt uw **Pushmeldingen** in de volgende velden:

* **Titel**
* **Lichaam**
* **Aangepast geluid**
* **Badges**
* **Aangepaste gegevens**

![](assets/perso_push.png)

Meer informatie over de configuratie voor pushmeldingen in [deze sectie](../push-gs.md).

### Je aanbiedingen aanpassen {#personalize-offers}

U kunt tot de verpersoonlijkingsredacteur ook toegang hebben wanneer het toevoegen van tekst-type inhoud aan uw aanbiedingen&#39; vertegenwoordiging.

Meer informatie over het beheren van inhoud met Beslissingsbeheer in [deze sectie](../offers/offer-library/creating-personalized-offers.md#custom-text).

## De Expressieeditor gebruiken {#use-expression-editor}

De uitdrukkingsredacteur is het middelstuk van de verpersoonlijking in [!DNL Journey Optimizer].

Het is beschikbaar in elke context waarin u personalisatie als e-mail, push en aanbiedingen moet definiëren.

In de interface van de uitdrukkingsredacteur, zult u, alle gegevens selecteren schikken aanpassen en bevestigen om een aangepaste verpersoonlijking voor uw inhoud tot stand te brengen.

![](assets/perso_ee1.png)

In het linkergedeelte van het scherm wordt een domeinkiezer weergegeven waarmee u de bron voor personalisatie kunt selecteren.

![](assets/perso_ee3.png)

Beschikbare bronnen zijn:

* **[!UICONTROL Profile attributes]** : Hiermee worden alle verwijzingen weergegeven die zijn gekoppeld aan het profielschema dat wordt beschreven in [Adobe Experience Platform Data Model (XDM)-documentatie](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : maakt een lijst van alle segmenten die in de dienst van de Segmentatie van Adobe Experience Platform worden gecreeerd. Meer informatie over segmentatie is beschikbaar [hier](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : geeft een overzicht van alle aanbiedingen verbonden aan een specifieke plaatsing. Selecteer de plaatsing en voeg de aanbiedingen in uw inhoud in. Voor volledige documentatie over het beheren van aanbiedingen raadpleegt u [deze sectie](../deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** : wanneer de **Bericht** wordt gebruikt in een reis, zijn de contextuele reisgebieden beschikbaar door dit menu. Meer informatie in [deze sectie](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : Hiermee worden alle hulpfuncties weergegeven die beschikbaar zijn om bewerkingen uit te voeren op gegevens, zoals berekeningen, gegevensopmaak of conversies, voorwaarden en deze te manipuleren in de context van personalisatie. Meer informatie in [deze sectie](functions/functions.md).

Bij selectie wordt de verwijzing toegevoegd in de editor.

>[!NOTE]
>
>Het infopictogram naast &quot;+&quot;pictogram opent omhoog tooltip die meer details voor elke variabele verstrekt.

In het volgende voorbeeld, laat de uitdrukkingsredacteur u de profielen selecteren die hun verjaardag vandaag hebben dan de aanpassing voltooien door een specifieke aanbieding op te nemen die aan deze dag beantwoordt.

![](assets/perso_ee2.png)

### Toevoegen aan Favorieten{#fav}

Door verschillende kenmerken toe te voegen aan het menu Favorieten hebt u snel toegang tot de meest gebruikte items. Als u een kenmerk aan uw favorieten wilt toevoegen, klikt u op het ovaalmenu en kiest u **[!UICONTROL Add to favorites]**.

![](assets/favorite-option.png)

Als u toegang wilt tot favoriete objecten, gebruikt u de opdracht **[!UICONTROL Favorites]** in het keuzemenu.

![](assets/favorite-menu.png)

Vanuit deze lijst kunt u het aanpassingsobject snel toevoegen aan uw huidige expressie.

![](assets/favorite-list.png)

Als je een object niet meer wilt zien in je lijst met favorieten, kun je het uit de favorieten verwijderen.

![](assets/favorite-remove.png)

## Instructievideo&#39;s{#video-perso}

Leer hoe u contextuele gebeurtenisinformatie van een journey kunt gebruiken om een bericht te personaliseren.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Leer hoe u contextuele gebeurtenisinformatie van een journey kunt gebruiken om een bericht te personaliseren.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
