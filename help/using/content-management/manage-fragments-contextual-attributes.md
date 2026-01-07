---
solution: Journey Optimizer
product: journey optimizer
title: Contextafhankelijke kenmerken toevoegen aan gepubliceerde fragmenten
description: Leer hoe u contextafhankelijke kenmerken aan gepubliceerde fragmenten kunt toevoegen (beperkte beschikbaarheid)
feature: Fragments
topic: Content Management
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
source-git-commit: 4162403bedc1632ed28db122e2ec16e3c00a2630
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---

# Contextafhankelijke kenmerken toevoegen aan gepubliceerde fragmenten {#adding-contextual-attributes}

>[!AVAILABILITY]
>
>Deze mogelijkheid is alleen beschikbaar voor bepaalde klanten en houdt aanzienlijke risico&#39;s in. Bevestig met uw Adobe-vertegenwoordiger dat deze functie is ingeschakeld voor uw organisatie.

Door gebrek, wordt het toevoegen van nieuwe [&#x200B; verpersoonlijkingsattributen &#x200B;](../personalization/personalization-build-expressions.md) aan een gepubliceerd fragment niet gesteund. Nadat een fragment is gepubliceerd, is de set met profiel of contextafhankelijke kenmerken vergrendeld voor alle campagnes en reizen.

Nochtans, voor uitgezochte klanten, is het mogelijk om **contextafhankelijke attributen** slechts aan gepubliceerde fragmenten toe te voegen.

>[!WARNING]
>
>Wanneer u aanpassingskenmerken toevoegt aan een gepubliceerd fragment, is het validatieproces minder streng en kunnen fouten niet worden gedetecteerd. Dit kan leiden tot ongewenste breuken over reizen en campagnes waarbij dat fragment op schaal wordt gebruikt.

## Afvoerkanalen en beperkingen {#limitations}

* Zorg ervoor dat alle reizen en campagnes die momenteel het fragment gebruiken, de nieuwe contextafhankelijke kenmerken kunnen verwerken.
* Profielkenmerken kunnen niet worden toegevoegd aan gepubliceerde fragmenten. Alleen contextuele kenmerken worden ondersteund.
* Contextafhankelijke kenmerken moeten handmatig worden ingevoerd in de code-editor. Ze kunnen niet worden geselecteerd in de gebruikersinterface van de verpersoonlijkingseditor.
* Wanneer u gepersonaliseerde kenmerken toevoegt aan live fragmenten, worden validaties versoepeld. Dit betekent dat fouten mogelijk niet worden gedetecteerd en dat er onbedoelde schaling kan optreden.
* Na publicatie zullen eventuele fouten direct invloed hebben op alle communicatie met dat fragment.

## Contextafhankelijke kenmerken toevoegen {#add-contextual-attributes}

Voer de onderstaande stappen uit om contextafhankelijke kenmerken aan een gepubliceerd fragment toe te voegen.

>[!IMPORTANT]
>
>Ga alleen verder als u de effecten op reizen en campagnes die verwijzen naar het fragment volledig begrijpt. [Meer informatie](#limitations)

1. Ga naar **[!UICONTROL Content Management]** > **[!UICONTROL Fragments]**.

1. Selecteer het gepubliceerde fragment en klik op **[!UICONTROL Modify]** om een conceptversie te maken.

   ![](assets/fragment-live-modify.png){width="70%" align="left"}

1. Klik op **[!UICONTROL Edit]** om de fragmentinhoudeditor te openen.

1. Ga naar **[!UICONTROL Code editor]** of **[!UICONTROL Advanced mode]** in de verpersoonlijkingseditor.

1. Typ of kopieer het contextafhankelijke kenmerk handmatig met de syntaxis:

   ```
   {{context.attribute_name}}
   ```

   Voorbeeld voor een kenmerk `promotionCode` :

   ```
   {{context.promotionCode}}
   ```

   >[!CAUTION]
   >
   >Controleer het kenmerkpad op nauwkeurigheid. Fouten kunnen niet worden ontdekt en kunnen reis- of campagnecommunicatie op schaal verstoren.

1. Sla uw wijzigingen op.

1. Klik op **[!UICONTROL Publish]** om de wijzigingen live te zetten.

>[!NOTE]
>Om ongewenste breuken over reizen en campagnes te vermijden, kunt u de contextafhankelijke kenmerkwegen in een niet-productiemilieu testen.

## Verwante onderwerpen {#related-topics}

* [Fragmenten beheren](manage-fragments.md)
* [Visuele fragmenten in e-mails gebruiken](../email/use-visual-fragments.md)
* [Expressiefragmenten gebruiken](../personalization/use-expression-fragments.md)
* [API-gestuurde campagnes](../campaigns/api-triggered-campaigns.md)
* [Personalization-syntaxis](../personalization/personalization-syntax.md)

