---
solution: Journey Optimizer
product: journey optimizer
title: Dynamische inhoud maken
description: Leer hoe u dynamisch berichten kunt toevoegen.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, editor, dynamic, content
exl-id: 639ad7df-0d0f-4c9b-95d1-f3101267aae2
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# Dynamische inhoud maken {#dynamic-content}

Met Adobe Journey Optimizer kunt u voorwaardelijke regels die in de bibliotheek zijn gemaakt, gebruiken om dynamische inhoud aan uw berichten toe te voegen.

Dynamische inhoud kan in elk veld worden gemaakt waarin u personalisatie kunt toevoegen met de verpersoonlijkingseditor. Dit zijn onder andere onderwerpregel, koppelingen, inhoud van pushberichten of representaties van teksttypeaanbiedingen. [Meer informatie over verpersoonlijkingscontexten](personalization-contexts.md)

Bovendien kunt u voorwaardelijke regels gebruiken in de e-mailontwerper om meerdere varianten van een inhoudscomponent te maken.

## Dynamische inhoud toevoegen aan expressies {#perso-expressions}

U kunt als volgt dynamische inhoud in expressies toevoegen:

1. Navigeer naar het veld waaraan u dynamische inhoud wilt toevoegen en open vervolgens de verpersoonlijkingseditor.

1. Selecteer de **[!UICONTROL Conditions]** om de lijst met beschikbare voorwaardelijke regels weer te geven. Klik op + naast een regel om deze toe te voegen aan de huidige expressie.

   U kunt ook een nieuwe regel maken door **[!UICONTROL Create new]**. [Leer hoe u voorwaarden kunt maken](create-conditions.md)

   ![](assets/conditions-expression.png)

1. Toevoegen tussen de `{%if}` en `{%/if}` plaatst codes voor de inhoud die u wilt weergeven als aan de voorwaardelijke regel is voldaan. U kunt zoveel regels toevoegen als nodig zijn om verschillende varianten van een expressie te maken.

   In het onderstaande voorbeeld zijn twee varianten gemaakt voor een SMS-inhoud, afhankelijk van de voorkeurstaal van de ontvanger.

   ![](assets/conditions-language-sample.png)

1. Als de inhoud gereed is, kunt u een voorvertoning van de verschillende varianten weergeven met de opdracht **[!UICONTROL Simulate content]** knop. [Leer hoe u berichten kunt testen en bekijken](../content-management/preview-test.md)

   ![](assets/conditions-preview.png)

## Dynamische inhoud toevoegen aan e-mails {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="Voorwaardelijke inhoud"
>abstract="Gebruik voorwaardelijke regels om meerdere varianten van een inhoudscomponent te maken. Als aan geen van de voorwaarden wanneer het verzenden van het bericht wordt voldaan, zal de inhoud van de Standaardvariant tonen."

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="Voorwaardelijke inhoud"
>abstract="Gebruik een voorwaardelijke regel die u in de bibliotheek hebt opgeslagen of maak een nieuwe regel."

U kunt als volgt varianten van een inhoudscomponent maken in E-mailontwerper:

1. In de [E-mailDesigner](../email/content-from-scratch.md)selecteert u een inhoudscomponent en klikt u vervolgens op **[!UICONTROL Enable conditional content]**.

   ![](assets/conditions-enable-conditional.png)

1. De **[!UICONTROL Conditional Content]** wordt aan de linkerkant weergegeven. In dit deelvenster kunt u meerdere varianten van de geselecteerde inhoudscomponent maken aan de hand van voorwaarden.

   Vorm uw eerste variant door te selecteren **[!UICONTROL Select condition]** knop.

   ![](assets/conditions-apply.png)

1. De weergave van de voorwaardenbibliotheek. Selecteer de voorwaardelijke regel die u aan de variant wilt koppelen en klik vervolgens op **[!UICONTROL Select]**. In dit voorbeeld willen we de componenttekst aanpassen, afhankelijk van de voorkeurstaal van de ontvanger.

   ![](assets/conditions-select.png)

   U kunt ook een nieuwe regel maken door op **[!UICONTROL Create new]**. [Leer hoe u voorwaarden kunt maken](create-conditions.md)

1. De voorwaardelijke regel is gekoppeld aan de variant. Voor een betere leesbaarheid kunt u de naam van de variant wijzigen door de optie **[!UICONTROL Rename]** uit het pictogram Meer handelingen.

   ![](assets/conditions-rename.png)

1. Vorm hoe de component zou moeten tonen als de regel wordt ontmoet wanneer het verzenden van het bericht. In dit voorbeeld willen we de tekst in het Frans weergeven als dit de voorkeurstaal van de ontvanger is.

   ![](assets/conditions-design.png)

1. Voeg zoveel varianten toe als nodig zijn voor de inhoudscomponent. U kunt op elk gewenst moment schakelen tussen de verschillende varianten om te controleren hoe de inhoudcomponent afhankelijk van de voorwaardelijke regels wordt weergegeven.

   >[!NOTE]
   >Als aan geen van de regels in de varianten wordt bepaald wanneer het verzenden van het bericht wordt voldaan, zal de inhoudscomponent de inhoud tonen die in wordt bepaald **[!UICONTROL Default variant]**.
   >
   >Voorwaardelijke inhoud wordt geëvalueerd op basis van de bijbehorende regels in de volgorde waarin de varianten worden weergegeven. De standaardvariant wordt altijd weergegeven als aan geen andere voorwaarden wordt voldaan.

1. Als u een variant wilt verwijderen, klikt u op het pictogram Meer handelingen naast de gewenste variant en selecteert u **[!UICONTROL Delete]**.

   ![](assets/conditions-delete.png)
