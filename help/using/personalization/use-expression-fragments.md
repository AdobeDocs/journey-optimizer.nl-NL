---
solution: Journey Optimizer
product: journey optimizer
title: Expressiefragmenten gebruiken
description: Leer hoe u expressiefragmenten kunt gebruiken in het dialoogvenster [!DNL Journey Optimizer] Expressieeditor.
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressie, editor, bibliotheek, personalisatie
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Expressiefragmenten benutten {#use-expression-fragments}

Wanneer u de expressie-editor gebruikt, kunt u alle uitdrukkingsfragmenten benutten die zijn gemaakt of opgeslagen in de huidige sandbox.

Leer hoe u fragmenten maakt en beheert in [deze sectie](../content-management/fragments.md).

➡️ [Leer hoe u fragmenten beheert, ontwerpt en gebruikt in deze video](../content-management/fragments.md#video-fragments)

## Expressiefragment gebruiken {#use-expression-fragment}

Volg onderstaande stappen om expressiefragmenten aan uw inhoud toe te voegen.

1. Open de [Expression-editor](personalization-build-expressions.md) en selecteert u de **[!UICONTROL Fragments]** in het linkerdeelvenster.

   ![](assets/expression-fragments-pane.png)

   In de lijst worden alle uitdrukkingsfragmenten weergegeven die als fragmenten in de huidige sandbox zijn gemaakt of opgeslagen. [Meer informatie](../content-management/fragments.md#create-expression-fragment)

   >[!NOTE]
   >
   >Fragmenten worden gesorteerd op aanmaakdatum: recent toegevoegde uitdrukkingsfragmenten worden eerst weergegeven in de lijst.

1. U kunt de lijst ook vernieuwen.

   >[!NOTE]
   >
   >Als sommige fragmenten zijn gewijzigd of toegevoegd terwijl u de inhoud bewerkt, wordt de lijst bijgewerkt met de meest recente wijzigingen.

1. Klik op het pictogram + naast een expressiefragment om de bijbehorende fragment-id in te voegen in de editor.

   ![](assets/expression-fragment-add.png)

   Nadat de fragment-id is toegevoegd, opent u het bijbehorende expressiefragment en [bewerken](../content-management/fragments.md#edit-fragments) vanuit de interface worden de wijzigingen gesynchroniseerd. Ze worden automatisch doorgegeven aan iedereen **[!UICONTROL Draft]** ritten/campagnes met die fragment-id.

   >[!NOTE]
   >
   >De wijzigingen worden niet doorgegeven aan inhoud die wordt gebruikt in **[!UICONTROL Live]** reizen of campagnes.

1. Klik op de knop **[!UICONTROL More actions]** naast een fragment.

1. Selecteer in het contextmenu dat wordt geopend de optie **[!UICONTROL View fragment]** voor meer informatie over dat fragment. De **[!UICONTROL Fragment ID]** wordt ook weergegeven en kan hier worden gekopieerd.

   ![](assets/expression-fragment-view.png)

1. U kunt het uitdrukkingsfragment in een ander venster openen om zijn inhoud en eigenschappen uit te geven - of gebruikend **[!UICONTROL Open fragment]** in het contextmenu of vanuit het **[!UICONTROL Fragment info]** venster. [Leer hoe u een fragment bewerkt](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Vervolgens kunt u de inhoud op de gebruikelijke manier aanpassen en valideren met alle personalisatie- en ontwerpmogelijkheden van de [Expression-editor](personalization-build-expressions.md).

>[!NOTE]
>
>Als u een expressiefragment maakt dat meerdere regeleinden bevat en het gebruikt in [SMS](../sms/create-sms.md#sms-content) of [duwen](../push/design-push.md) inhoud, blijven de regeleinden behouden. Zorg er dus voor dat u uw [SMS](../sms/send-sms.md) of [duwen](../push/send-push.md) bericht voordat het wordt verzonden.

## Overerving onderbreken {#break-inheritance}

Wanneer u een fragment-id toevoegt aan de expressie-editor, worden de wijzigingen die in het oorspronkelijke expressiefragment zijn aangebracht, gesynchroniseerd.

U kunt echter ook de inhoud van een expressiefragment in de editor plakken. Selecteer in het contextmenu de optie **[!UICONTROL Paste fragment]** om die inhoud in te voegen.

![](assets/expression-fragment-paste.png)

In dat geval wordt de overerving van het oorspronkelijke fragment verbroken. De inhoud van het fragment wordt naar de editor gekopieerd en de wijzigingen worden niet meer gesynchroniseerd.

Het wordt een zelfstandig element dat niet meer aan het oorspronkelijke fragment is gekoppeld. U kunt het net als elk ander element in de code bewerken.

