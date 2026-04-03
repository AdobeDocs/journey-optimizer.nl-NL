---
solution: Journey Optimizer
product: journey optimizer
title: Overwegingen en problemen met Adobe Experience Manager-inhoudsfragmenten
description: Overwegingen en algemene problemen met AEM Content Fragments in Journey Optimizer.
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 0%

---

# Overwegingen en problemen oplossen {#aem-fragments-limitations}

## Belangrijkste overwegingen {#considerations}

Houd rekening met het volgende wanneer u Content Fragments van [!DNL Adobe Experience Manager] in [!DNL Journey Optimizer] gebruikt:

* **de fragmenttypes van inhoud**
   * De eenvoudige Fragmenten van de Inhoud, de genestelde Fragmenten van de Inhoud, en **variaties van het Fragment van de Inhoud** worden gesteund. Kies de variatie wanneer u het fragment invoegt in [!DNL Journey Optimizer] . Als u geen variatie selecteert, wordt de **Hoofd** variatie (de primaire inhoud van het fragment in [!DNL Adobe Experience Manager]) gebruikt.

* **Meertalige inhoud**
   * Elke variatie moet worden geschreven, gecodeerd en gepubliceerd in [!DNL Adobe Experience Manager] . Selecteer in [!DNL Journey Optimizer] de fragmentvariatie die overeenkomt met elke berichttaal of landinstelling.
   * Er is geen automatische taalresolutie of fallback tussen variaties.

* **Toegang van de Bewaarplaats**
   * [!DNL Journey Optimizer] integreert met [!DNL Adobe Experience Manager] **** publiceer slechts rij (Plaatsen, de Fragmenten van de Inhoud). Inhoudsfragmenten zijn beschikbaar via een openbaar, niet-geverifieerd eindpunt.
   * De bewaarplaatsen van de auteur kunnen in de bewaarplaatskiezer verschijnen, maar slechts fragmenten die aan **worden gepubliceerd publiceren** kunnen in [!DNL Journey Optimizer] worden gebruikt.

* **status van het Fragment van de Inhoud**
   * De fragmenten kunnen **[!UICONTROL Published]** of **[!UICONTROL Modified]** status tonen; [!DNL Journey Optimizer] gebruikt altijd de **recentste gepubliceerde versie**.
   * Wijzigingen die u na publicatie aanbrengt, worden pas doorgevoerd in [!DNL Journey Optimizer] als het fragment opnieuw wordt gepubliceerd in [!DNL Adobe Experience Manager] . Er is geen automatische afstemming van de versie tussen de twee producten.

* **Personalization**
   * Ondersteund: profielkenmerken, contextuele kenmerken, statische tekenreeksen en vooraf gedeclareerde variabelen.
   * Niet ondersteund: afgeleide of berekende kenmerken.

* **Updates en versioning**
   * Updates moeten handmatig opnieuw worden gepubliceerd vanuit [!DNL Adobe Experience Manager] . Er is geen automatische versiecomitatie.
   * Wanneer een Fragment van de Inhoud in [!DNL Adobe Experience Manager] wordt gepubliceerd of opnieuw gepubliceerd, [!DNL Journey Optimizer] werkt dat fragment bij en verfrist **alle variaties van dat fragment dat** in actieve campagnes of reizen van verwijzingen wordt voorzien.
   * [!DNL Adobe Experience Manager] [ publiceer actie ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-publication) kan worden vertraagd. Wanneer deze is voltooid, ontvangt [!DNL Journey Optimizer] een gebeurtenis en wordt de inhoud vernieuwd.
   * Na een succesvolle update, zijn de veranderingen typisch beschikbaar binnen ongeveer **5 minuten** voor unitaire reizen en in de **volgende partij** voor partijgebruiksgevallen.

* **Caching en het proef**
   * Wanneer een fragment voor het eerst aan een campagne of reis wordt toegevoegd, plaatst [!DNL Journey Optimizer] het in cache. Als u een fragment selecteert dat al ergens anders door **[!UICONTROL Open AEM CF selector]** werd gebruikt, wordt het vanuit de cache van [!DNL Journey Optimizer] geladen.
   * Nadat u een gewijzigd fragment opnieuw hebt gepubliceerd in [!DNL Adobe Experience Manager] , luistert [!DNL Journey Optimizer] naar de gebeurtenis en wordt de cache bijgewerkt.
   * De proeven wijzen altijd op **onlangs gepubliceerde** versie; u kunt geen historische versie voor het proef sluiten.

## Problemen oplossen {#troubleshooting}

Als u problemen tegenkomt bij het werken met Adobe Experience Manager Content Fragments in Journey Optimizer, raadpleegt u de volgende algemene problemen en resoluties:

| Probleem | Oorzaak | Resolutie |
|-|-|-|
| **Markering niet gevonden** of **het Fragment van de Inhoud niet zichtbaar in selecteur** | De syntaxis van de Adobe Experience Manager-tag komt niet overeen met de vereiste indeling `ajo-enabled:{OrgId}/{SandboxName}` | Valideer dat identiteitskaart van de markering correcte **identiteitskaart van de Organisatie** en **Naam Sandbox** gebruikt. Zorg ervoor dat er geen spaties of onjuiste scheidingstekens zijn. Publiceer het inhoudsfragment opnieuw nadat u de tag hebt gecorrigeerd. |
| **het Fragment van de Inhoud verschijnt niet in lijst** | Inhoudsfragment bevindt zich in concept of is niet gepubliceerd | Alleen goedgekeurde en gepubliceerde inhoudsfragmenten worden weergegeven in de Journey Optimizer-kiezer. Publiceer het inhoudsfragment in Adobe Experience Manager en controleer of dit de publicatiestatus heeft. |
| **Veranderlijke niet gedefiniëerde fout** | Tijdelijke aanduiding voor Personalization is niet gedeclareerd in fragment helper-tag | Voeg alle vereiste parameters toe aan de fragmenthulplijntag. Elke tijdelijke aanduiding die in het inhoudsfragment wordt gebruikt, moet expliciet worden gedeclareerd met de toewijzing ervan. |
| **de vertoningen van de proef onverwachte inhoud** | Proef gebruikt de meest recente gepubliceerde versie van Adobe Experience Manager | Proefversies weerspiegelen altijd de meest recente publicatie van het inhoudsfragment in Adobe Experience Manager. Als u recente wijzigingen hebt aangebracht in Adobe Experience Manager, publiceert u het fragment opnieuw en vernieuwt u de proefdruk. |
| **Ontkende Toegang (CPES) fout** | Gebruikersrol is niet geautoriseerd voor toegang tot bepaalde kenmerken | Neem contact op met de systeembeheerder om te controleren of uw rol de juiste machtigingen heeft voor het profiel of de contextafhankelijke kenmerken die worden gebruikt in personalisatie. |
| **de vertoningen van het fragment leeg of ontbrekende inhoud** | Ontbrekende vereiste verpersoonlijkingsparameters of terugvalwaarden | Zorg ervoor dat alle vereiste parameters zijn opgegeven en denk na of u terugvalwaarden voor optionele kenmerken wilt toevoegen. |
| **het Beeld geeft niet terug of lijkt gebroken** | De afbeeldings-URL in het inhoudsfragment is een relatief pad of kan niet vanaf het kanaal worden bereikt | Gebruik **absolute** URLs (`https://...`) voor beeldgebieden. Relatieve paden uit Adobe Experience Manager worden niet ondersteund. Bevestig de URL in een browser of berichtvoorbeeld. |
| **de verbindingswinst van AEM van Experience League 404** | Lege bladwijzer, voorvertoning van build of niet-gepubliceerde AEM Help-pagina | Open de [ Fragmenten van de Inhoud met Adobe Journey Optimizer ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} onderwerp van de levende documentatie van Experience Manager en navigeer van de op-pagina inhoudstafel, of onderzoek naar de sectienaam (bijvoorbeeld **de Configuratie van Dispatcher**). |

Als het probleem zich blijft voordoen, neemt u contact op met uw Adobe-vertegenwoordiger voor meer informatie over uw Content Fragment ID, campagne- of reis-id en eventuele weergegeven foutberichten.
