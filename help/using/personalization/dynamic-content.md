---
solution: Journey Optimizer
product: journey optimizer
title: Dynamische inhoud maken
description: Leer hoe u dynamisch berichten kunt toevoegen.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---


# Dynamische inhoud maken {#dynamic-content}

Met Adobe Journey Optimizer kunt u voorwaardelijke regels die in de bibliotheek zijn gemaakt, gebruiken om dynamische inhoud aan uw berichten toe te voegen.

Dynamische inhoud kan worden gemaakt in elk veld waarin u personalisatie kunt toevoegen met de Expressieeditor. Dit zijn onder andere onderwerpregel, koppelingen, inhoud van pushberichten of representaties van teksttypeaanbiedingen. [Meer informatie over verpersoonlijkingscontexten](personalization-contexts.md)

Bovendien kunt u voorwaardelijke regels gebruiken in de e-mailontwerper om meerdere varianten van een inhoudscomponent te maken.

## Dynamische inhoud toevoegen aan expressies {#perso-expressions}

U kunt als volgt dynamische inhoud in expressies toevoegen:

1. Navigeer naar het veld waaraan u dynamische inhoud wilt toevoegen en open vervolgens de Expressieeditor.

1. Selecteer **[!UICONTROL Conditions]** om de lijst met beschikbare voorwaardelijke regels weer te geven. Klik op + naast een regel om deze toe te voegen aan de huidige expressie.

   U kunt ook een nieuwe regel maken door **[!UICONTROL Create new]**. [Leer hoe u voorwaarden kunt maken](create-conditions.md)

   ![](assets/conditions-expression.png)

1. Toevoegen tussen de `{%if}` en `{%/if}` plaatst codes voor de inhoud die u wilt weergeven als aan de voorwaardelijke regel is voldaan. U kunt zoveel regels toevoegen als nodig zijn om verschillende varianten van een expressie te maken.

   In het onderstaande voorbeeld zijn twee varianten gemaakt voor een SMS-inhoud, afhankelijk van de voorkeurstaal van de ontvanger.

   ![](assets/conditions-language-sample.png)

1. Als de inhoud gereed is, kunt u een voorvertoning van de verschillende varianten weergeven met de opdracht **[!UICONTROL Simulate content]** knop. [Leer hoe u berichten kunt testen en bekijken](../design/preview.md)

   ![](assets/conditions-preview.png)

## Dynamische inhoud toevoegen aan e-mails {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="Voorwaardelijke content"
>abstract="Gebruik voorwaardelijke regels om meerdere varianten van een inhoudscomponent te maken. Als aan geen van de voorwaarden wanneer het verzenden van het bericht wordt voldaan, zal de inhoud van de Standaardvariant tonen."

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="Voorwaardelijke content"
>abstract="Gebruik een voorwaardelijke regel die u in de bibliotheek hebt opgeslagen of maak een nieuwe regel."

U kunt als volgt varianten van een inhoudscomponent maken in E-mailontwerper:

1. Selecteer in de e-mailontwerper een inhoudscomponent en klik vervolgens op **[!UICONTROL Enable conditional content]**.

   ![](assets/conditions-enable-conditional.png)

1. De **[!UICONTROL Conditional Content]** wordt aan de linkerkant weergegeven. In dit deelvenster kunt u meerdere varianten van de geselecteerde inhoudscomponent maken aan de hand van voorwaarden.

   Vorm uw eerste variant door te selecteren **[!UICONTROL Apply condition]** knop.

   ![](assets/conditions-apply.png)

1. De weergave van de voorwaardenbibliotheek. Selecteer de voorwaardelijke regel die u aan de variant wilt koppelen en klik op **[!UICONTROL Select]**. In dit voorbeeld willen we de componenttekst aanpassen, afhankelijk van de voorkeurstaal van de ontvanger.

   ![](assets/conditions-select.png)

   U kunt ook een nieuwe regel maken door op **[!UICONTROL Create new]**. [Leer hoe u voorwaarden kunt maken](create-conditions.md)

1. De voorwaardelijke regel is gekoppeld aan de variant. Voor betere leesbaarheid raden we u aan de naam van de variant te wijzigen door op het ovaalmenu te klikken.

   Vorm nu hoe de component zou moeten tonen als de regel wordt voldaan aan wanneer het verzenden van het bericht. In dit voorbeeld willen we de tekst in het Frans weergeven als dit de voorkeurstaal van de ontvanger is.

   ![](assets/conditions-design.png)

1. Voeg zoveel varianten toe als nodig zijn voor de inhoudscomponent. U kunt op elk gewenst moment schakelen tussen de verschillende varianten om te controleren hoe de inhoudcomponent afhankelijk van de voorwaardelijke regels wordt weergegeven.

   >[!NOTE]
   >Als aan geen van de regels in de varianten wordt bepaald wanneer het verzenden van het bericht wordt voldaan, zal de inhoudscomponent de inhoud tonen die in wordt bepaald **[!UICONTROL Default variant]**.
   >
   >Voorwaardelijke inhoud wordt geëvalueerd op basis van de bijbehorende regels in de volgorde waarin de varianten worden weergegeven. De standaardvariant wordt altijd weergegeven als aan geen andere voorwaarden wordt voldaan.
