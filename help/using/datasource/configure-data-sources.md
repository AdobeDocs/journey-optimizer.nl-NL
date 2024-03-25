---
solution: Journey Optimizer
product: journey optimizer
title: Een gegevensbron configureren
description: Een databron configureren
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: gegevens, bron, configuratie, veld
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: e45ec5f0e1bbcc73892f9cde5923627886f44ef6
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 7%

---

# Een gegevensbron configureren {#configure-data-source}

>[!NOTE]
>
>De databronconfiguratie wordt altijd uitgevoerd door een **technische gebruiker**.

Volg onderstaande stappen om een gegevensbron te configureren:

1. Selecteer in de sectie van het menu ADMINISTRATIE de optie **[!UICONTROL Configurations]**. In de  **[!UICONTROL Data Sources]** sectie, klikken **[!UICONTROL Manage]**. De lijst met databronnen wordt weergegeven. Zie [deze pagina](../start/user-interface.md) voor meer informatie over de interface.

   ![](assets/journey18.png)

1. Vervolgens kunt u veldgroepen toevoegen aan de ingebouwde gegevensbron (zie [deze pagina](../datasource/adobe-experience-platform-data-source.md)) of een nieuwe externe gegevensbron maken (zie [deze pagina](../datasource/external-data-sources.md)) en bijbehorende veldgroepen (zie [deze pagina](../datasource/configure-data-sources.md#define-field-groups)).

   ![](assets/journey23.png)

1. Klik op **[!UICONTROL Save]**.

   De databron is nu geconfigureerd en klaar om te worden gebruikt in uw journey’s.

## Veldgroepen definiëren {#define-field-groups}

Veldgroepen zijn sets velden die u kunt ophalen van een gegevensbron en gebruiken tijdens een reis.

Voor elke gegevensbron kunt u verschillende veldgroepen definiëren.

U kunt bijvoorbeeld een veldgroep maken met het telefoonnummer, de e-mail, de voornaam en het adres van het profiel. Dan kunt u deze gegevens gebruiken om voorwaarden te creëren. U kunt bijvoorbeeld alleen een pushmelding verzenden als de klant de mobiele toepassing heeft geïnstalleerd. Als het leeg is, kunt u een e-mail verzenden.

Hoewel automatisch een standaardnaam wordt toegevoegd, raden wij u aan een naam aan uw veldgroep toe te voegen. De naam van de veldgroep is namelijk zichtbaar voor andere gebruikers in [!DNL Journey Optimizer]. U kunt het beste veldgroepen een relevante naam geven.

Wanneer een gegevensbrongebied in een reis wordt gebruikt, zal het systeem alle gebieden terugwinnen die voor die gebiedsgroep worden bepaald. Daarom is het verstandig alleen de velden te selecteren die u nodig hebt voor uw reizen. Hierdoor wordt de wachttijd bij het aanvragen van uw reizen verminderd, waardoor de prestaties toenemen. U kunt later gemakkelijk meer velden in veldgroepen toevoegen.

Het aantal ritten dat een veldgroep gebruikt, wordt weergegeven in het dialoogvenster **[!UICONTROL Used in]** veld. U kunt op de knop **[!UICONTROL View journeys]** om de lijst met reizen weer te geven met deze veldgroep.

>[!NOTE]
>
>Als een veldgroep geen veld heeft, wordt dit niet weergegeven in de expressieeditor.

![](assets/journey3bis.png)

## Levenscyclus veldgroep {#field-group-lifecycle}

U kunt velden toevoegen aan of verwijderen uit een veldgroep die niet wordt gebruikt in concepten of live reizen.

U kunt een veld toevoegen, maar u kunt dit niet verwijderen uit een veldgroep die wordt gebruikt in een of meer concepten of livedagen. Zo voorkomt u dat de reis wordt afgebroken.

Voer de volgende stappen uit om een veld te verwijderen uit een veldgroep die wordt gebruikt voor een of meer reizen. Laten we een voorbeeld gebruiken van een veldgroep met de naam &quot;Veldgroep A&quot;.

1. Plaats de cursor in de lijst met veldgroepen op Veldgroep A en klik op de knop **[!UICONTROL Duplicate]** rechts op het scherm. Geef de gedupliceerde veldgroep bijvoorbeeld de naam &quot;Veldgroep B&quot;.
1. Verwijder in &quot;Veldgroep B&quot; de velden die u niet meer wilt gebruiken.
1. Controleer in &quot;Veldgroep A&quot; waar deze veldgroep wordt gebruikt. Deze informatie wordt weergegeven in het dialoogvenster **[!UICONTROL Used in]** veld.
1. Open alle reizen die gebruikmaken van &quot;Veldgroep A&quot;.
1. Maak nieuwe versies van elk van deze reizen. Bewerk alle activiteiten met &quot;Veldgroep A&quot; en selecteer &quot;Veldgroep B&quot;.
1. Oude versies van ritten die &quot;Groep A van het Gebied&quot;gebruiken stoppen. U zou dan geen reis moeten hebben gebruikend &quot;Groep A van het Gebied&quot;.
1. Verwijder &quot;Veldgroep A&quot; zoals deze niet meer wordt gebruikt.
