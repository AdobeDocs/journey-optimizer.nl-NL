---
solution: Journey Optimizer
product: journey optimizer
title: Expressiefragmenten gebruiken
description: Leer hoe u expressiefragmenten kunt gebruiken in het dialoogvenster [!DNL Journey Optimizer] personalisatie-editor.
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressie, editor, bibliotheek, personalisatie
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: e6924928e03d494817a2368b33997029ca2eca1c
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Expressiefragmenten benutten {#use-expression-fragments}

Wanneer u de opdracht **personalisatie-editor**, kunt u alle expressiefragmenten benutten die zijn gemaakt of opgeslagen in de huidige sandbox.

Een fragment is een herbruikbare component waarnaar kan worden verwezen [!DNL Journey Optimizer] campagnes en reizen. Met deze functionaliteit kunt u meerdere blokken met aangepaste inhoud vooraf samenstellen. Deze blokken kunnen door marketinggebruikers worden gebruikt om inhoud snel samen te stellen in een verbeterd ontwerpproces. [Leer hoe u fragmenten maakt en beheert](../content-management/fragments.md).

➡️ [Leer hoe u fragmenten beheert, ontwerpt en gebruikt in deze video](../content-management/fragments.md#video-fragments)

## Expressiefragment gebruiken {#use-expression-fragment}

Volg onderstaande stappen om expressiefragmenten aan uw inhoud toe te voegen.

>[!NOTE]
>
>U kunt maximaal 30 fragmenten in een bepaalde levering toevoegen. Fragmenten kunnen maximaal 1 niveau worden genest.

1. Open de [personalisatie-editor](personalization-build-expressions.md) en selecteert u de **[!UICONTROL Fragments]** in het linkerdeelvenster.

   In de lijst worden alle uitdrukkingsfragmenten weergegeven die als fragmenten in de huidige sandbox zijn gemaakt of opgeslagen. Ze worden gesorteerd op aanmaakdatum: recent toegevoegde expressiefragmenten worden als eerste weergegeven in de lijst. [Meer informatie](../content-management/fragments.md#create-expression-fragment)

   ![](assets/expression-fragments-pane.png)

   U kunt deze lijst ook vernieuwen.

   >[!NOTE]
   >
   >Als sommige fragmenten zijn gewijzigd of toegevoegd terwijl u de inhoud bewerkt, wordt de lijst bijgewerkt met de meest recente wijzigingen.

1. Klik op het pictogram + naast een expressiefragment om de bijbehorende fragment-id in te voegen in de editor.

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >U kunt elke **Concept** of **Live** fragment naar uw inhoud. U kunt uw reis of campagne echter niet activeren als er een fragment met de status Concept in wordt gebruikt. Tijdens de reis- of campagnepublicatie wordt een fout weergegeven in ontwerpfragmenten die u moet goedkeuren om te kunnen publiceren.

1. Nadat de fragment-id is toegevoegd, opent u het bijbehorende expressiefragment en [bewerken](../content-management/fragments.md#edit-fragments) vanuit de interface worden de wijzigingen gesynchroniseerd. Ze worden automatisch doorgegeven aan alle concepten of live reizen/campagnes die die fragment-id bevatten.

1. Klik op de knop **[!UICONTROL More actions]** naast een fragment. Selecteer in het contextmenu dat wordt geopend de optie **[!UICONTROL View fragment]** voor meer informatie over dat fragment. De **[!UICONTROL Fragment ID]** wordt ook weergegeven en kan hier worden gekopieerd.

   ![](assets/expression-fragment-view.png)

1. U kunt het uitdrukkingsfragment in een ander venster openen om zijn inhoud en eigenschappen uit te geven - of gebruikend **[!UICONTROL Open fragment]** in het contextmenu of vanuit het **[!UICONTROL Fragment info]** venster. [Leer hoe u een fragment bewerkt](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Vervolgens kunt u de inhoud op de gebruikelijke manier aanpassen en valideren met alle personalisatie- en ontwerpmogelijkheden van de [personalisatie-editor](personalization-build-expressions.md).

>[!NOTE]
>
>Als u een expressiefragment maakt dat meerdere regeleinden bevat en het gebruikt in [SMS](../sms/create-sms.md#sms-content) of [duwen](../push/design-push.md) inhoud, blijven de regeleinden behouden. Zorg er dus voor dat u uw [SMS](../sms/send-sms.md) of [duwen](../push/send-push.md) bericht voordat het wordt verzonden.

## Bewerkbare velden aanpassen {#customize-fields}

Als bepaalde delen van een expressiefragment bewerkbaar zijn gemaakt met variabelen, kunt u de standaardwaarden ervan overschrijven met een specifieke syntaxis. [Leer hoe u uw fragmenten aanpasbaar kunt maken](../content-management/customizable-fragments.md)

Voer de volgende stappen uit om de velden aan te passen:

1. Het fragment invoegen in uw code vanuit het dialoogvenster **Fragmenten** -menu.

1. Gebruik de `<fieldId>="<value>"` code aan het einde van de syntaxis om de standaardwaarde van de variabele te overschrijven.

   In het onderstaande voorbeeld overschrijven we de waarde van een variabele waarvan de id &#39;sport&#39; is met de waarde &#39;yoga&#39;. Hiermee wordt &quot;yoga&quot; in uw fragmentinhoud weergegeven, overal waar naar de variabele &quot;sport&quot; wordt verwezen.

   ![](../content-management/assets/fragment-expression-use.png)

Een voorbeeld waarin wordt getoond hoe u bewerkbare velden kunt toevoegen aan een expressiefragmenten en de waarden ervan kunt overschrijven wanneer u een e-mailbericht maakt, is beschikbaar in [deze sectie](../content-management/customizable-fragments.md#example).

## Overerving onderbreken {#break-inheritance}

Wanneer u een fragment-id toevoegt aan de personalisatie-editor, worden de wijzigingen in het oorspronkelijke expressiefragment gesynchroniseerd.

U kunt echter ook de inhoud van een expressiefragment in de editor plakken. Selecteer in het contextmenu de optie **[!UICONTROL Paste fragment]** om die inhoud in te voegen.

![](assets/expression-fragment-paste.png)

In dat geval wordt de overerving van het oorspronkelijke fragment verbroken. De inhoud van het fragment wordt naar de editor gekopieerd en de wijzigingen worden niet meer gesynchroniseerd.

Het wordt een zelfstandig element dat niet meer aan het oorspronkelijke fragment is gekoppeld. U kunt het net als elk ander element in de code bewerken.

