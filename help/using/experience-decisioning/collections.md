---
title: Verzamelingen
description: Leer hoe u met verzamelingen werkt
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 1%

---

# Verzamelingen {#collections}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collections"
>title="Verzamelingen maken"
>abstract="Met verzamelingen kunt u uw beslissingsitems categoriseren en groeperen op basis van uw voorkeuren. Deze categorieën worden gecreeerd door het ontwerpen van regels die hefboomwerking de attributen van besluitvormingspunten."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collection_rules"
>title="Bepaal regels voor uw inzameling"
>abstract="Voeg één of veelvoudige regels toe om de punten te bepalen die in de inzameling moeten worden omvat. Kies een itemkenmerk dat u als criterium wilt gebruiken. Selecteer de gewenste operator en voer de waarde in waarop u wilt filteren. Voeg zoveel regels toe als nodig is."

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_collection"
>title="Een verzameling kiezen"
>abstract="Selecteer de verzameling die de aanbiedingen bevat die u wilt overwegen. Deze stap is verplicht bij het maken van een selectiestrategie. Met verzamelingen kunt u uw beslissingsitems categoriseren en groeperen op basis van uw voorkeuren. U kunt bijvoorbeeld een verzameling maken die alle beslissingsitems met de waarde &quot;Yoga&quot; bevat in het aangepaste kenmerk &quot;Categorie&quot;."

Met verzamelingen kunt u uw beslissingsitems categoriseren en groeperen op basis van uw voorkeuren. Deze categorieën worden gecreeerd door het ontwerpen van regels die hefboomwerking de attributen van besluitvormingspunten.

Bijvoorbeeld, laten wij zeggen u een &quot;Categorie&quot;douanekenmerk aan het catalogusschema van uw besluitvormingspunten hebt toegevoegd. Dit staat u toe om een inzameling tot stand te brengen die alle besluitpunten met de waarde &quot;Yoga&quot;in het &quot;attribuut van de Categorie&quot;omvat.

De lijst met verzamelingen is toegankelijk via het menu **[!UICONTROL Catalogs]** .

Ga als volgt te werk om een verzameling te maken:

1. Navigeer naar **[!UICONTROL Catalogs]** > **[!UICONTROL Collections]** en klik op **[!UICONTROL Create collection]** .
1. Geef een naam en een beschrijving voor de verzameling op.
1. Voeg één of veelvoudige regels toe om de punten te bepalen die in de inzameling moeten worden omvat. Dit doet u als volgt:

   1. Kies een itemkenmerk dat u als criterium wilt gebruiken. De lijst met kenmerken bevat alle standaard- en aangepaste kenmerken die zijn gedefinieerd in het catalogusschema. [ Leer meer over de catalogus van punten ](catalogs.md)
   1. Selecteer de gewenste operator en voer de waarde in waarop u wilt filteren.Geef elke aanbiedingsnaam expliciet op of maak een &quot;luma-zomer&quot;-tag aan elke aanbieding en wijs deze toe.

      >[!NOTE]
      >
      >**BEVAT** exploitant geen gedeeltelijke of vervangingsgelijken. Het werkt als een **IN** exploitant, betekenend moet u een serie van nauwkeurige waarden voor de attributen verstrekken.
      >
      >Bijvoorbeeld, zeggen u veelvoudige zomeraanbiedingen hebt u in een inzameling wilt omvatten: *&quot;luma-zomer-yoga&quot;*, *&quot;luma-zomer-fitness&quot;*, en *&quot;luma-zomer-lopend&quot;*. Als u deze items wilt opnemen, moet u een regel definiëren, zoals &quot;Naam van aanbieding&quot; BEVAT &quot;luma-zomer-yoga&quot;, &quot;luma-zomer-fitness&quot;, &quot;luma-zomer-running&quot;. Deze regel retourneert alleen die aanbiedingen die exact overeenkomen met een van de namen in de lijst.
      >
      >Als u gedeeltelijke aanpassing (b.v., alle aanbiedingen die *&quot;luma-zomer&quot;* bevatten) nodig hebt, wordt dit momenteel niet gesteund. U moet elke aanbiedingsnaam uitdrukkelijk specificeren, of a *&quot;luma-zomer&quot;* markering toewijzen aan elke aanbieding en die markering in uw regel gebruiken.

   1. Herhaal deze stappen om zoveel regels toe te voegen als nodig is. Wanneer de veelvoudige regels worden toegevoegd, kunt u tussen **kiezen en** en **of** exploitanten om hen te combineren. Klik hiertoe op het bedieningspaneel om te schakelen tussen de twee keuzen.
   1. Klik op de knop **[!UICONTROL Preview collection]** om de items weer te geven die voldoen aan de regels die u hebt gedefinieerd.

   ![](assets/collection-create.png)

1. Klik op **[!UICONTROL Create]** als de verzamelingsregels zijn gedefinieerd. De verzameling wordt nu in de lijst weergegeven.

>[!NOTE]
>
>Elke objectverzameling kan maximaal 500 aangeboden objecten bevatten. [ leer meer over het Beslissen van gidsen &amp; beperkingen ](gs-experience-decisioning.md#guardrails)
