---
solution: Journey Optimizer
product: journey optimizer
title: Push generation met AI Assistant in Journey Optimizer
description: Push-inhoud genereren met AI Assistant in Journey Optimizer
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: a9f9d8af-c762-4038-8bbc-bbd519e0ef3a
source-git-commit: 50933d991c6a337e6d1739652d680778759ef0d5
workflow-type: tm+mt
source-wordcount: '1548'
ht-degree: 1%

---

# Push generation met AI Assistant {#generative-push}

>[!IMPORTANT]
>
>Alvorens te beginnen gebruikend dit vermogen, lees uit verwante [&#x200B; Grafieken en Beperkingen &#x200B;](gs-generative.md#generative-guardrails).
></br>
>
>U moet met a [&#x200B; gebruikersovereenkomst &#x200B;](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) akkoord gaan alvorens u AI Medewerker in Journey Optimizer kunt gebruiken. Neem voor meer informatie contact op met uw Adobe-vertegenwoordiger.

Als je berichten hebt gemaakt en gepersonaliseerd, ga je pushberichten naar het volgende niveau met AI Assistant in Journey Optimizer.

Bekijk de onderstaande tabbladen voor meer informatie over het gebruik van AI Assistant in Journey Optimizer.

>[!BEGINTABS]

>[!TAB  Volledige duw generatie ]

In dit voorbeeld leert u hoe u een aansprekende pushmelding verzendt met gebruik van AI Assistant in Journey Optimizer.

Voer de volgende stappen uit:

1. Klik op **[!UICONTROL Edit content]** nadat u de pushmeldingscampagne hebt gemaakt en geconfigureerd.

   Voor meer informatie over hoe te om uw campagne van het pushbericht te vormen, verwijs naar [&#x200B; deze pagina &#x200B;](../push/create-push.md).

1. Vul **[!UICONTROL Basic details]** in voor uw campagne. Klik op **[!UICONTROL Edit content]** als u klaar bent.

1. Pas uw pushmelding naar wens aan. [Meer informatie](../push/design-push.md)

1. Open het menu **[!UICONTROL Show AI Assistant]** .

   ![](assets/push-genai-full-1.png){zoomable="yes"}

1. Schakel de optie **[!UICONTROL Use original content]** voor AI Assistant in om de nieuwe inhoudsoptie aan te passen op basis van de geselecteerde inhoud.

1. Selecteer **[!UICONTROL Brand]** om te zorgen dat door AI gegenereerde inhoud wordt uitgelijnd op de specificaties van uw merk. [&#x200B; leer meer &#x200B;](brands.md) op Banden.

   Merk op dat de eigenschap van Merken als privé bèta wordt vrijgegeven en aan alle klanten in toekomstige versies geleidelijk beschikbaar zal zijn.

1. Verfijn de inhoud door te beschrijven wat u wilt genereren in het veld **[!UICONTROL Prompt]** .

   Als u hulp bij het ontwerpen van uw herinnering zoekt, toegang **[!UICONTROL Prompt Library]** die een diverse waaier van snelle ideeën verstrekt om uw campagnes te verbeteren.

   ![](assets/push-genai-full-2.png){zoomable="yes"}

1. Kies welk veld u wilt genereren: **[!UICONTROL Title]** , **[!UICONTROL Message]** en/of **[!UICONTROL Image]** .

1. Volg uw vraag met de optie **[!UICONTROL Text settings]** :

   * **[!UICONTROL Communication strategy]**: Kies de meest geschikte communicatiestijl voor de gegenereerde tekst.
   * **[!UICONTROL Languages]**: kies de taal van de gegenereerde inhoud.
   * **[!UICONTROL Tone]**: De toon van uw pushberichten zou met uw publiek moeten resoneren. Of u informatief wilt klinken, playful, of overtuigend, AI Medewerker kan het bericht dienovereenkomstig aanpassen.

   ![](assets/push-genai-full-3.png){zoomable="yes"}

1. Kies uw **[!UICONTROL Image settings]** :

   * **[!UICONTROL Content type]**: hiermee wordt de aard van het visuele element gecategoriseerd, waarbij onderscheid wordt gemaakt tussen verschillende vormen van visuele representatie, zoals foto&#39;s, afbeeldingen of illustraties.
   * **[!UICONTROL Visual intensity]**: U kunt de invloed van de afbeelding bepalen door de intensiteit ervan aan te passen. Bij een lagere instelling (2) wordt het uiterlijk zachter en minder sterk, terwijl bij een hogere instelling (10) de afbeelding levendiger en visueel krachtiger wordt.
   * **[!UICONTROL Color & tone]**: De algemene weergave van de kleuren in een afbeelding en de sfeer die of de sfeer die door de afbeelding wordt overgebracht.
   * **[!UICONTROL Lighting]**: hiermee wordt de bliksemschicht in een afbeelding bedoeld, die de atmosfeer van de afbeelding bepaalt en specifieke elementen markeert.
   * **[!UICONTROL Composition]**: dit heeft betrekking op de rangschikking van elementen binnen het kader van een afbeelding

   ![](assets/push-genai-full-5.png){zoomable="yes"}

1. Klik in het menu **[!UICONTROL Brand assets]** op **[!UICONTROL Upload brand asset]** om een merkelement toe te voegen dat inhoud bevat die extra context-AI-assistent kan bieden of selecteer een eerder geüpload element.

   Eerder geüploade bestanden zijn beschikbaar in de vervolgkeuzelijst **[!UICONTROL Uploaded brand assets]** . Schakel eenvoudig de elementen in die u wilt opnemen in uw generatie.

1. Klik op **[!UICONTROL Generate]** als de vraag gereed is.

1. Blader door het gegenereerde bestand **[!UICONTROL Variations]** .

   Klik op **[!UICONTROL Preview]** om een schermvullende versie van de geselecteerde variant weer te geven of klik op **[!UICONTROL Apply]** om de huidige inhoud te vervangen.

1. Klik op het percentagepictogram om uw **[!UICONTROL Brand Alignment Score]** weer te geven en eventuele onjuiste uitlijningen met uw merk te identificeren.

   Leer meer op [&#x200B; de groeperingsscore van het Merk &#x200B;](brands-score.md).

   ![](assets/push-genai-full-4.png){zoomable="yes"}

1. Navigeer naar de optie **[!UICONTROL Refine]** in het **[!UICONTROL Preview]** -venster voor toegang tot extra aanpassingsfuncties:

   * **[!UICONTROL Use as reference content]**: De gekozen variant zal als verwijzingsinhoud voor het produceren van andere resultaten dienen.

   * **[!UICONTROL Rephrase]**: De AI-assistent kan uw bericht op verschillende manieren herformuleren, zodat u steeds fris schrijft en aantrekkelijk wordt voor verschillende soorten publiek.

   * **[!UICONTROL Use simpler language]**: Gebruik AI Assistant om uw taal te vereenvoudigen, zodat een groter publiek helderheid en toegankelijkheid krijgt.

   U kunt ook de **[!UICONTROL Tone]** en **[!UICONTROL Communication strategy]** van de tekst wijzigen.

   ![](assets/push-genai-full-6.png){zoomable="yes"}

1. Open het **[!UICONTROL Brand Alignment]** lusje om te zien hoe uw inhoud zich op uw [&#x200B; merkrichtlijnen &#x200B;](brands.md) richt.

1. Klik op **[!UICONTROL Select]** zodra u de juiste inhoud hebt gevonden.

   U kunt ook experimenteren met uw inhoud inschakelen. [Meer informatie](generative-experimentation.md)

1. Voeg verpersoonlijkingsgebieden in om uw inhoud van het pushbericht aan te passen die op profielgegevens wordt gebaseerd. Klik vervolgens op de knop **[!UICONTROL Simulate content]** om de rendering te beheren en controleer de instellingen voor aanpassing met testprofielen. [Meer informatie](../personalization/personalize.md)

Wanneer u de inhoud, het publiek en het programma hebt gedefinieerd, kunt u uw pushcampagne voorbereiden. [Meer informatie](../campaigns/review-activate-campaign.md)

>[!TAB  Tekst slechts generatie ]

In dit voorbeeld leert u hoe u AI Assistant in Journey Optimizer kunt gebruiken voor specifieke inhoud. Voer de volgende stappen uit:

1. Klik op **[!UICONTROL Edit content]** nadat u de pushmeldingscampagne hebt gemaakt en geconfigureerd.

   Voor meer informatie over hoe te om uw pushcampagne te vormen, verwijs naar [&#x200B; deze pagina &#x200B;](../push/create-push.md).

1. Vul **[!UICONTROL Basic details]** in voor uw campagne. Klik op **[!UICONTROL Edit content]** als u klaar bent.

1. Pas uw pushmelding naar wens aan. [Meer informatie](../push/design-push.md)

1. Open het menu **[!UICONTROL Edit text with AI Assistant]** naast de velden **[!UICONTROL Title]** of **[!UICONTROL Message]** .

   ![](assets/push-genai-1.png){zoomable="yes"}

1. Schakel de optie **[!UICONTROL Use reference content]** voor AI Assistant in om nieuwe inhoud aan te passen op basis van de geselecteerde inhoud.

1. Selecteer **[!UICONTROL Brand]** om te zorgen dat door AI gegenereerde inhoud wordt uitgelijnd op de specificaties van uw merk. [&#x200B; leer meer &#x200B;](brands.md) op Banden.

   Merk op dat de eigenschap van Merken als privé bèta wordt vrijgegeven en aan alle klanten in toekomstige versies geleidelijk beschikbaar zal zijn.

1. Verfijn de inhoud door te beschrijven wat u wilt genereren in het veld **[!UICONTROL Prompt]** .

   Als u hulp bij het ontwerpen van uw herinnering zoekt, toegang **[!UICONTROL Prompt Library]** die een diverse waaier van snelle ideeën verstrekt om uw campagnes te verbeteren.

   ![](assets/push-genai-2.png){zoomable="yes"}

1. Volg uw vraag met de optie **[!UICONTROL Text settings]** :

   * **[!UICONTROL Communication strategy]**: Kies de meest geschikte communicatiestijl voor de gegenereerde tekst.
   * **[!UICONTROL Languages]**: kies de taal van de gegenereerde inhoud.
   * **[!UICONTROL Tone]**: De toon van uw pushmelding zou op uw publiek moeten passen. Of u informatief wilt klinken, playful, of overtuigend, AI Medewerker kan het bericht dienovereenkomstig aanpassen.
   * **[!UICONTROL Length]**: selecteer de lengte van de inhoud met de schuifregelaar voor het bereik.

   ![](assets/push-genai-4.png){zoomable="yes"}

1. Klik in het menu **[!UICONTROL Brand assets]** op **[!UICONTROL Upload brand asset]** om een merkelement toe te voegen dat inhoud bevat die extra context-AI-assistent kan bieden of selecteer een eerder geüpload element.

   Eerder geüploade bestanden zijn beschikbaar in de vervolgkeuzelijst **[!UICONTROL Uploaded brand assets]** . Schakel eenvoudig de elementen in die u wilt opnemen in uw generatie.

1. Klik op **[!UICONTROL Generate]** als de vraag gereed is.

1. Blader door het gegenereerde bestand **[!UICONTROL Variations]** .

1. Klik op het percentagepictogram om uw **[!UICONTROL Brand Alignment Score]** weer te geven en eventuele onjuiste uitlijningen met uw merk te identificeren.

   Leer meer op [&#x200B; de groeperingsscore van het Merk &#x200B;](brands-score.md).

   ![](assets/push-genai-5.png){zoomable="yes"}

1. Navigeer naar de optie **[!UICONTROL Refine]** in het **[!UICONTROL Preview]** -venster voor toegang tot extra aanpassingsfuncties:

   * **[!UICONTROL Use as reference content]**: De gekozen variant zal als verwijzingsinhoud voor het produceren van andere resultaten dienen.

   * **[!UICONTROL Elaborate]**: De AI-assistent kan u helpen bij het uitvouwen van specifieke onderwerpen en biedt extra informatie voor een beter begrip en betrokkenheid.

   * **[!UICONTROL Summarize]**: langdurige informatie kan ontvangers overladen. Met AI Assistant kunt u belangrijke punten samenvoegen tot heldere, beknopte samenvattingen die aandacht trekken en hen aanmoedigen om verder te lezen.

   * **[!UICONTROL Rephrase]**:TheAI Assistant kan uw bericht op verschillende manieren herformuleren, zodat u steeds fris schrijft en aantrekkelijk wordt voor verschillende soorten publiek.

   * **[!UICONTROL Use simpler language]**: Gebruik AI Assistant om uw taal te vereenvoudigen, zodat een groter publiek helderheid en toegankelijkheid krijgt.

   U kunt ook de **[!UICONTROL Tone]** en **[!UICONTROL Communication strategy]** van de tekst wijzigen.

   ![](assets/push-genai-6.png){zoomable="yes"}

1. Open het **[!UICONTROL Brand Alignment]** lusje om te zien hoe uw inhoud zich op uw [&#x200B; merkrichtlijnen &#x200B;](brands.md) richt.

1. Klik op **[!UICONTROL Select]** zodra u de juiste inhoud hebt gevonden.

   U kunt ook experimenteren met uw inhoud inschakelen. [Meer informatie](generative-experimentation.md)

1. Voeg verpersoonlijkingsgebieden in om uw inhoud van het pushbericht aan te passen die op profielgegevens wordt gebaseerd. Klik vervolgens op de knop **[!UICONTROL Simulate content]** om de rendering te beheren en controleer de instellingen voor aanpassing met testprofielen. [Meer informatie](../personalization/personalize.md)

Wanneer u de inhoud, het publiek en het programma hebt gedefinieerd, kunt u uw pushcampagne voorbereiden. [Meer informatie](../campaigns/review-activate-campaign.md)

>[!TAB  slechts generatie van het Beeld ]

1. Klik op **[!UICONTROL Edit content]** nadat u de pushmeldingscampagne hebt gemaakt en geconfigureerd.

   Voor meer informatie over hoe te om uw campagne van het pushbericht te vormen, verwijs naar [&#x200B; deze pagina &#x200B;](../push/create-push.md).

1. Vul **[!UICONTROL Basic details]** in voor uw campagne. Klik op **[!UICONTROL Edit content]** als u klaar bent.

1. Pas uw pushmelding naar wens aan. [Meer informatie](../push/design-push.md)

1. Open het menu **[!UICONTROL Add media]** .

   ![](assets/push-gen-img-1.png){zoomable="yes"}

1. Schakel de optie **[!UICONTROL Reference style]** voor AI Assistant in om nieuwe inhoud aan te passen op basis van de referentie-inhoud. U kunt ook een afbeelding uploaden om context aan uw variatie toe te voegen.

1. Selecteer **[!UICONTROL Brand]** om te zorgen dat door AI gegenereerde inhoud wordt uitgelijnd op de specificaties van uw merk. [&#x200B; leer meer &#x200B;](brands.md) op Banden.

   Merk op dat de eigenschap van Merken als privé bèta wordt vrijgegeven en aan alle klanten in toekomstige versies geleidelijk beschikbaar zal zijn.

1. Verfijn de inhoud door te beschrijven wat u wilt genereren in het veld **[!UICONTROL Prompt]** .

   Als u hulp bij het ontwerpen van uw herinnering zoekt, toegang **[!UICONTROL Prompt Library]** die een diverse waaier van snelle ideeën verstrekt om uw campagnes te verbeteren.

   ![](assets/push-gen-img.png){zoomable="yes"}

1. Kies uw **[!UICONTROL Image settings]** :

   * **[!UICONTROL Content type]**: hiermee wordt de aard van het visuele element gecategoriseerd, waarbij onderscheid wordt gemaakt tussen verschillende vormen van visuele representatie, zoals foto&#39;s, afbeeldingen of illustraties.
   * **[!UICONTROL Visual intensity]**: U kunt de invloed van de afbeelding bepalen door de intensiteit ervan aan te passen. Bij een lagere instelling (2) wordt het uiterlijk zachter en minder sterk, terwijl bij een hogere instelling (10) de afbeelding levendiger en visueel krachtiger wordt.
   * **[!UICONTROL Color & tone]**: De algemene weergave van de kleuren in een afbeelding en de sfeer die of de sfeer die door de afbeelding wordt overgebracht.
   * **[!UICONTROL Lighting]**: hiermee wordt de bliksemschicht in een afbeelding bedoeld, die de atmosfeer van de afbeelding bepaalt en specifieke elementen markeert.
   * **[!UICONTROL Composition]**: dit heeft betrekking op de rangschikking van elementen binnen het kader van een afbeelding

1. Klik in het menu **[!UICONTROL Brand assets]** op **[!UICONTROL Upload brand asset]** om een merkelement toe te voegen dat inhoud bevat die extra context-AI-assistent kan bieden of selecteer een eerder geüpload element.

   Eerder geüploade bestanden zijn beschikbaar in de vervolgkeuzelijst **[!UICONTROL Uploaded brand assets]** . Schakel eenvoudig de elementen in die u wilt opnemen in uw generatie.

1. Klik op **[!UICONTROL Generate]** als de vraag gereed is.

1. Blader door het gegenereerde bestand **[!UICONTROL Variations]** .

1. Klik op het percentagepictogram om uw **[!UICONTROL Brand Alignment Score]** weer te geven en eventuele onjuiste uitlijningen met uw merk te identificeren.

   Leer meer op [&#x200B; de groeperingsscore van het Merk &#x200B;](brands-score.md).

1. Navigeer naar de optie **[!UICONTROL Refine]** in het **[!UICONTROL Preview]** -venster voor toegang tot extra aanpassingsfuncties:

   * **[!UICONTROL Generate Similar]** om verwante afbeeldingen met deze variant weer te geven.
   * **[!UICONTROL Edit in Adobe Express]** om uw element verder aan te passen.

[Meer informatie over Adobe Express-integratie](../integrations/express.md)

   * **[!UICONTROL Save]** gebruiken om de elementen op te slaan, zodat u ze later kunt gebruiken.

   ![](assets/push-gen-img-2.png){zoomable="yes"}

1. Open het **[!UICONTROL Brand Alignment]** lusje om te zien hoe uw inhoud zich op uw [&#x200B; merkrichtlijnen &#x200B;](brands.md) richt.

1. Klik op **[!UICONTROL Select]** zodra u de juiste inhoud hebt gevonden.

   U kunt ook experimenteren met uw inhoud inschakelen. [Meer informatie](generative-experimentation.md)

Wanneer u de inhoud, het publiek en het programma hebt gedefinieerd, kunt u uw pushcampagne voorbereiden. [Meer informatie](../campaigns/review-activate-campaign.md)

>[!ENDTABS]
