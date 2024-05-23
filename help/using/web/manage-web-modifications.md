---
title: Webwijzigingen beheren
description: Leer hoe u wijzigingen in Journey Optimizer-webpagina-inhoud kunt beheren
feature: Web Channel
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 213511b4-7556-4a25-aa23-b50acd11cd34
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 0%

---

# Webwijzigingen beheren {#manage-web-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Eenvoudig al uw wijzigingen beheren"
>abstract="Met dit deelvenster kunt u door alle aanpassingen en stijlen navigeren die u aan uw webpagina hebt toegevoegd en deze beheren."

U kunt eenvoudig alle componenten, aanpassingen en stijlen beheren die u aan uw webpagina hebt toegevoegd. U kunt wijzigingen ook rechtstreeks vanuit het desbetreffende deelvenster toevoegen.

## Werken met het venster Wijzigingen {#use-modifications-pane}

1. Selecteer de **[!UICONTROL Modifications]** pictogram om het corresponderende venster links weer te geven.

   ![](assets/web-designer-modifications-pane.png)

1. U kunt alle wijzigingen bekijken die u op de pagina hebt aangebracht.

1. Selecteer een ongewenste wijziging en klik op de knop **[!UICONTROL Delete modification]** van de **[!UICONTROL More actions]** om deze te verwijderen.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Ga voorzichtig te werk wanneer u een actie verwijdert, aangezien dit van invloed kan zijn op volgende acties.

1. Als u meerdere wijzigingen tegelijk wilt verwijderen, klikt u op de knop **[!UICONTROL Select]** boven op de knop **[!UICONTROL Modifications]** , controleert u de gewenste wijzigingen en klikt u op de knop **[!UICONTROL Delete]** pictogram.

   ![](assets/web-designer-modifications-select-delete.png)

1. Gebruik de **[!UICONTROL More actions]** boven op de knop **[!UICONTROL Modifications]** om alle wijzigingen tegelijk te verwijderen.

   ![](assets/web-designer-delete-modifications.png)

1. U kunt ook alleen de ongeldige wijzigingen verwijderen. Dit houdt in dat de wijzigingen worden overschreven door andere wijzigingen. Als u bijvoorbeeld de kleur van een tekst wijzigt en die tekst verwijdert, wordt de kleurwijziging ongeldig omdat de tekst niet meer bestaat.

1. U kunt handelingen annuleren en opnieuw uitvoeren met de opdracht **[!UICONTROL Undo/Redo]** op de rechterbovenhoek van het scherm.

   ![](assets/web-designer-undo-redo.png)

   Klik en houd de knoop om tussen te schakelen **[!UICONTROL Undo]** en **[!UICONTROL Redo]** opties. Klik vervolgens op de knop zelf om de gewenste actie toe te passen.

## Wijzigingen toevoegen vanuit het toegewezen venster {#add-modifications}

Wanneer u een pagina bewerkt met de webontwerper, kunt u nieuwe wijzigingen rechtstreeks vanuit de **[!UICONTROL Modifications]** deelvenster - zonder dat u een component hoeft te selecteren en te bewerken in de interface van de webontwerper. Voer de onderstaande stappen uit.

1. Van de **[!UICONTROL Modifications]** klikt u op het deelvenster **[!UICONTROL More actions]** knop.

1. Selecteren **[!UICONTROL Add a modification]**.

   ![](assets/web-designer-add-modification.png)

1. Selecteer het wijzigingstype:

   * **[!UICONTROL CSS Selector]** - [Meer informatie](#css-selector)
   * **[!UICONTROL Page `<Head>`]** - [Meer informatie](#page-head)

1. Voer uw inhoud in en **[!UICONTROL Save]** uw wijzigingen.

1. Klik op de knop **[!UICONTROL More actions]** naast uw wijziging en selecteer **[!UICONTROL Info]** om de details weer te geven.

   ![](assets/web-designer-add-modification-info.png)

### CSS-kiezer {#css-selector}

Als u een **CSS-kiezer** als u tekst wilt wijzigen, volgt u de onderstaande stappen.

1. Selecteren **[!UICONTROL CSS Selector]** als het wijzigingstype.

1. De **[!UICONTROL CSS Element Selector]** kunt u in dit veld gemakkelijker de HTML-elementen (of knooppunten in de DOM-structuur) vinden en selecteren waarop u wijzigingen wilt toepassen. <!--specify the desired CSS element that you want to modify.-->

   ![](assets/web-designer-add-modification-css.png)

1. Selecteer een handelingstype (**[!UICONTROL Set Content]** of **[!UICONTROL Set Attribute]**) en vult de vereiste informatie/inhoud in.

   * **[!UICONTROL Set Content]**: specificeer de inhoud die in het element gaat dat door wordt geïdentificeerd **[!UICONTROL CSS Element Selector]** veld.

   * **[!UICONTROL Set Attribute]**: geef een kenmerk op dat aan de huidige CSS-kiezer moet worden gekoppeld, zodat deze kiezer vervolgens ook door dit kenmerk kan worden geïdentificeerd. Voer hiertoe een naam in het dialoogvenster **[!UICONTROL Attribute name]** en een waarde in het veld **[!UICONTROL Content]** veld. Als het kenmerk al bestaat, wordt de waarde bijgewerkt; anders wordt een nieuw kenmerk toegevoegd met de opgegeven naam en waarde.

     ![](assets/web-designer-add-modification-css-attribute.png)

### Pagina `<head>` {#page-head}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_head"
>title="Aangepaste code toevoegen"
>abstract="Het HEAD-element is een container voor metagegevens en wordt tussen de tag HTML en de tag BODY geplaatst. Voeg alleen SCRIPT- en STIJLelementen toe. Als u DIV-tags en andere elementen toevoegt, komen de resterende HEAD-elementen mogelijk in de BODY terecht."

U kunt aangepaste code toevoegen met de **[!UICONTROL Page `<head>`]** wijzigingstype.

De `<head>` element is een container voor metagegevens (gegevens over gegevens) en wordt tussen de `<html>` en de `<body>` -tag. In dit geval wacht de code niet op gebeurtenissen voor het laden van de hoofdtekst of de pagina. Deze wordt uitgevoerd aan het begin van het laden van de pagina.

De `<head>` -element wordt doorgaans gebruikt om JavaScript- of CSS-code boven aan de pagina toe te voegen. Kiezers voor volgende visuele handelingen zijn afhankelijk van de HTML-elementen die op dit tabblad worden toegevoegd.

Als u een **Pagina`<head>`** als u tekst wilt wijzigen, volgt u de onderstaande stappen.

1. Selecteren **[!UICONTROL Page `<head>`]** als het wijzigingstype.

   ![](assets/web-designer-add-modification-head-type.png)

1. Voeg uw aangepaste code toe in het dialoogvenster **[!UICONTROL Content]** doos.

   >[!CAUTION]
   >
   >U kunt alleen toevoegen `<script>` en `<style>` aan de `<head>` sectie. Toevoegen `<div>` tags en andere elementen kunnen de resterende `<head>` elementen die in de `<body>`.

1. Klik op de knop **[!UICONTROL Advanced editing options]** knop. De verpersoonlijkingsredacteur opent.

   ![](assets/web-designer-add-modification-head-advanced.png)

   U kunt de [!DNL Journey Optimizer] verpersoonlijkingsredacteur met al zijn verpersoonlijking en auteursmogelijkheden. [Meer informatie](../personalization/personalization-build-expressions.md)

#### Aangepaste codevoorbeelden {#custom-code-examples}

U kunt de **[!UICONTROL Page `<head>`]** wijzigingstype:

* JavaScript inline gebruiken of koppelen naar een extern JavaScript-bestand.

  Bijvoorbeeld om de kleur van een element te wijzigen:

  ```
  <script type="text/javascript">
  document.getElementById("element_id").style.color = "blue";
  </script>
  ```

* Configureer een stijl inline of koppel deze aan een externe stijlpagina.

  U kunt bijvoorbeeld een klasse definiëren voor een overlay-element:

  ```
  <style>
  .overlay
  { position: absolute; top:0; left: 0; right: 0; bottom: 0; background: red; }
  </style>
  ```

#### Aangepaste tips voor code {#custom-code-best-practices}

+++ **Plaats de aangepaste code altijd in één element.**

Bijvoorbeeld:

```
<script>
// Code goes here
</script>
```

Als er wijzigingen nodig zijn, brengt u wijzigingen aan in deze container.

Als u de aangepaste code niet meer nodig hebt, laat u deze container leeg, maar verwijdert u deze niet. Dit zorgt ervoor dat andere ervaringswijzigingen niet worden beïnvloed.

+++

+++ **Voer geen document.write acties in de manuscripten van de douanecode uit.**

Scripts worden asynchroon uitgevoerd. Hierdoor worden documenten.write-handelingen vaak op de verkeerde plaats op de pagina weergegeven. Het gebruik van document.write in scripts die in aangepaste code zijn gemaakt, wordt afgeraden.

+++

+++ **Als u een element maakt en het vervolgens wijzigt, verwijdert u het oorspronkelijke element niet.**

Bij elke wijziging wordt een nieuw element gemaakt in het dialoogvenster **[!UICONTROL Modifications]** deelvenster. Omdat de tweede actie Element 1 wijzigt, als u Element 1 schrapt, heeft die actie niet meer om het even wat te wijzigen, zodat werkt de verandering niet meer.

+++

+++ **Wees voorzichtig met het gebruik van de **[!UICONTROL Page `<head>`]**wijzigingstype voor twee campagnes die invloed hebben op dezelfde URL.**

Als u het **[!UICONTROL Page `<head>`]** Als u het type wilt wijzigen voor twee campagnes die van invloed zijn op dezelfde URL, wordt het JavaScript vanuit beide campagnes in de pagina geïnjecteerd. [!DNL Journey Optimizer] bepaalt automatisch de orde van de geleverde inhoud. Zorg ervoor dat de code niet afhankelijk is van plaatsing. Het is aan u om ervoor te zorgen dat er geen conflicten in de code zijn.

+++
