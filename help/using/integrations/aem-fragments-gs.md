---
solution: Journey Optimizer
product: journey optimizer
title: AEM-inhoudsfragmenten
description: Leer hoe u AEM Content Fragments kunt openen en beheren
topic: Content Management
role: User
level: Beginner
source-git-commit: b06229e7a2fc64fbe28154c798b152cca8203a86
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 0%

---

# Aan de slag met Adobe Experience Manager-inhoudsfragmenten {#aem-fragments}

Door Adobe Experience Manager as a Cloud Service te integreren met Adobe Journey Optimizer, kunt u nu uw AEM-inhoudsfragmenten naadloos opnemen in uw Journey Optimizer-inhoud. Deze gestroomlijnde verbinding vereenvoudigt het proces van toegang tot en gebruik van AEM-inhoud, waardoor persoonlijke en dynamische campagnes en reizen kunnen worden gemaakt.

Meer over de Fragmenten van de Inhoud van AEM leren, verwijs naar [&#x200B; Werkend met de Fragmenten van de Inhoud &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} in de documentatie van Experience Manager.

## Voordat u begint {#start}

>[!AVAILABILITY]
>
>Voor klanten in de gezondheidszorg is de integratie alleen mogelijk na het in licentie geven van het Journey Optimizer Healthcare Shield- en Adobe Experience Manager Enhanced Security-add-on-aanbod.

### Beperkingen {#limitations}

Houd rekening met de volgende beperkingen wanneer u werkt met Adobe Experience Manager Content Fragments in Journey Optimizer:

* **de Types van Fragmenttypes van Inhoud**: De eenvoudige Fragmenten van de Inhoud en de genestelde Fragmenten van de Inhoud worden gesteund. Variaties in inhoudsfragmenten worden momenteel niet ondersteund.

* **Meertalige inhoud**: Slechts wordt de handstroom gesteund. Elke taalvariant moet onafhankelijk van elkaar zijn ontworpen in Adobe Experience Manager, gecodeerd, gepubliceerd en handmatig zijn geselecteerd in Journey Optimizer. Er is geen automatische taalresolutie of fallback-mechanisme.

* **Toegang van de Bewaarplaats**: Journey Optimizer integreert exclusief met Adobe Experience Manager publiceer rij, waar de Fragmenten van de Inhoud door een openbaar, niet voor authentiek verklaard eindpunt beschikbaar zijn. Hoewel Author repositories kunnen verschijnen in de repository kiezer, kunnen alleen Content Fragments die gepubliceerd worden naar de Publish tier gebruikt worden in Journey Optimizer.

* **status van het Fragment van de Inhoud**: De vertoningen van Journey Optimizer de Fragmenten van de Inhoud met **Gepubliceerde** en **Gewijzigde** status. In alle gevallen wordt alleen de meest recente gepubliceerde versie gebruikt. Als een fragment na publicatie wordt gewijzigd, worden deze wijzigingen pas in Journey Optimizer doorgevoerd als het inhoudsfragment opnieuw wordt gepubliceerd in Adobe Experience Manager. Er is geen automatische afstemming van versies tussen Adobe Experience Manager en Journey Optimizer.

* **Personalization**: Slechts profielattributen, contextuele attributen, statische koorden, en pre-gedeclareerde variabelen worden gesteund. Afgeleide of berekende kenmerken worden niet ondersteund.

* **Updates en versioning**: De updates van het Fragment van de inhoud vereisen handherpublicatie van Adobe Experience Manager. Er is geen automatische afstemming van versies tussen Adobe Experience Manager en Journey Optimizer. Wanneer een inhoudsfragment in Adobe Experience Manager wordt gepubliceerd, ontvangt Journey Optimizer een gebeurtenis en updates aan de Journey Optimizer-zijde. Als de update succesvol is, is deze na 5 minuten beschikbaar voor Eenheidstijden en in de volgende batch voor Gebruiksgevallen Batch.

* **Caching en het proef**: De Fragmenten van de inhoud worden teruggewonnen in echt - tijd van Adobe Experience Manager publiceren rij. Er is geen pre-render of momentopname caching. Proefdrukken voor campagnes en reizen weerspiegelen altijd de meest recente gepubliceerde versie van het inhoudsfragment en historische versies kunnen niet worden vergrendeld voor proefdrukken.

* **toegang van de Gebruiker**: Het wordt geadviseerd om het aantal gebruikers met toegang te beperken om de Fragmenten van de Inhoud te publiceren om het risico van toevallige fouten te verminderen.


### Levenscyclus van inhoudsfragment

![](assets/do-not-localize/AEM_CF.png)

Inhoudsfragmenten volgen verschillende fasen in de levenscyclus, afhankelijk van de Adobe Experience Manager-laag waarin ze voorkomen. [&#x200B; leer meer in de documentatie van Adobe Experience Manager &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

De inhoud wordt gecreeerd en op de **rij van de Auteur** geleid, waar de fragmenten statussen zoals Nieuw, Ontwerp, Gepubliceerd, Gewijzigd, of Unpublished kunnen hebben. Deze statussen zijn slechts op de **rij van de Auteur** van toepassing en steunen inhoudsverwezenlijking en overzicht.

Wanneer een tevreden Fragment wordt gepubliceerd, wordt een exemplaar gecreeerd op **publiceer rij** en blootgesteld door een openbaar, niet voor authentiek verklaard eindpunt. Journey Optimizer integreert exclusief met dit **publiceer rij**.

Als gevolg hiervan heeft Journey Optimizer alleen oppervlakken van Gepubliceerde of Gewijzigde inhoudsfragmenten en wordt altijd de meest recente gepubliceerde versie gebruikt. Wijzigingen die na publicatie worden aangebracht, worden pas in Journey Optimizer doorgevoerd als het inhoudsfragment opnieuw wordt gepubliceerd.


## Problemen oplossen {#troubleshooting}

Als u problemen tegenkomt bij het werken met Adobe Experience Manager Content Fragments in Journey Optimizer, raadpleegt u de volgende algemene problemen en resoluties:

| Probleem | Oorzaak | Resolutie |
|-|-|-|
| **Markering niet gevonden** of **het Fragment van de Inhoud niet zichtbaar in selecteur** | De syntaxis van de Adobe Experience Manager-tag komt niet overeen met de vereiste indeling `ajo-enabled:{OrgId}/{SandboxName}` | Valideer dat identiteitskaart van de markering correcte **identiteitskaart van de Organisatie** en **Naam Sandbox** gebruikt. Zorg ervoor dat er geen spaties of onjuiste scheidingstekens zijn. Publiceer het inhoudsfragment opnieuw nadat u de tag hebt gecorrigeerd. |
| **het Fragment van de Inhoud verschijnt niet in lijst** | Inhoudsfragment bevindt zich in concept of is niet goedgekeurd | Alleen goedgekeurde en gepubliceerde inhoudsfragmenten worden weergegeven in de Journey Optimizer-kiezer. Publiceer het inhoudsfragment in Adobe Experience Manager en controleer of het de goedgekeurde status heeft. |
| **Veranderlijke niet gedefiniëerde fout** | Tijdelijke aanduiding voor Personalization is niet gedeclareerd in fragment helper-tag | Voeg alle vereiste parameters toe aan de fragmenthulplijntag. Elke tijdelijke aanduiding die in het inhoudsfragment wordt gebruikt, moet expliciet worden gedeclareerd met de toewijzing ervan. |
| **de vertoningen van de proef onverwachte inhoud** | Proef gebruikt de meest recente gepubliceerde versie van Adobe Experience Manager | Proefversies weerspiegelen altijd de meest recente publicatie van het inhoudsfragment in Adobe Experience Manager. Als u recente wijzigingen hebt aangebracht in Adobe Experience Manager, publiceert u het fragment opnieuw en vernieuwt u de proefdruk. |
| **Ontkende Toegang (CPES) fout** | Gebruikersrol is niet geautoriseerd voor toegang tot bepaalde kenmerken | Neem contact op met de systeembeheerder om te controleren of uw rol de juiste machtigingen heeft voor het profiel of de contextafhankelijke kenmerken die worden gebruikt in personalisatie. |
| **de vertoningen van het fragment leeg of ontbrekende inhoud** | Ontbrekende vereiste verpersoonlijkingsparameters of terugvalwaarden | Zorg ervoor dat alle vereiste parameters zijn opgegeven en denk na of u terugvalwaarden voor optionele kenmerken wilt toevoegen. |

Als het probleem zich blijft voordoen, neemt u contact op met uw Adobe-vertegenwoordiger voor meer informatie over uw Content Fragment ID, campagne- of reis-id en eventuele weergegeven foutberichten.
