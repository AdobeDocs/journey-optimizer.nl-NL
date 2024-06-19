---
solution: Journey Optimizer
product: journey optimizer
title: Reiseinde
description: Leer hoe een reis eindigt in Journey Optimizer
feature: Journeys
role: User
level: Intermediate
keywords: reenter, transport, end, live, stop
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 6ff54583c729175c74b3a7ea4ab9188505fde897
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 1%

---

# Een reis beëindigen{#journey-ending}

Een reis kan voor een individu in twee specifieke contexten eindigen:

* De persoon komt bij de laatste activiteit van een weg aan.
* De persoon komt aan bij een **Voorwaarde** activiteit (of **Wachten** activiteit met een voorwaarde) en voldoet aan geen van de voorwaarden.

De persoon kan dan opnieuw de reis betreden als herbinnenkomst is toegestaan. Zie [deze pagina](../building-journeys/journey-gs.md#change-properties)

Om een live reis te beëindigen, adviseren wij dat u het sluit. De komst van nieuwe klanten op de reis zal dan worden geblokkeerd. Klanten die al op reis zijn gegaan, kunnen het tot het einde ervaren. Zie [deze sectie](../building-journeys/journey.md#close-journey)

U kunt een reis alleen stoppen als zich een noodsituatie voordoet en alle verwerking onmiddellijk op een reis moet worden beëindigd. Personen die al een reis zijn binnengekomen, worden in de loop der tijd gestopt. Zie [deze sectie](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>U kunt een gesloten of gestopt reis niet hervatten.

## Tag voor einde van reis{#end-tag}

Tijdens het ontwerpen van een rit wordt aan het einde van elk pad een &quot;eindtag&quot; weergegeven. Dit knooppunt kan niet door een gebruiker worden toegevoegd, kan niet worden verwijderd en alleen het label ervan kan worden gewijzigd. Het markeert het einde van elk pad van de reis. Als de reis verscheidene wegen heeft, adviseren wij dat u een etiket aan elk eind toevoegt om rapporten gemakkelijker te maken te lezen. Zie [deze pagina](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## Een reis sluiten{#close-journey}

Een reis kan om de volgende redenen worden gesloten:

* De reis wordt handmatig gesloten via de **[!UICONTROL Close to new entrances]** knop.
* Een reis op basis van een segment met één opname die klaar is met de uitvoering.
* Na het laatste optreden van een terugkerende, op het publiek gebaseerde reis.

Als u een reis handmatig sluit, weet u zeker dat klanten die de reis al hebben betreden, hun pad kunnen voltooien, maar dat nieuwe gebruikers de reis niet kunnen betreden. Wanneer een reis wordt gesloten (om een van de bovenstaande redenen), heeft deze de status **[!UICONTROL Closed]**. De reis houdt in dat nieuwe individuen de reis kunnen betreden. Personen die al onderweg zijn, kunnen de reis normaal afmaken.

Na 91 dagen [standaardtime](journey-gs.md#global_timeout), een leest publiek schakelt over naar de **Voltooid** status. Dit gedrag is alleen voor 91 dagen ingesteld (d.w.z. [time-outstandaardwaarde voor transport](journey-gs.md#global_timeout)), aangezien alle informatie over profielen die de reis hebben betreden, 91 dagen na het binnenkomen wordt verwijderd. Personen die nog onderweg zijn, worden automatisch getroffen. Ze verlaten de reis na de 91-dagen onderbreking.

Zie dit [sectie](../building-journeys/journey-gs.md#global_timeout).

Een gesloten reisversie kan niet opnieuw worden gestart of verwijderd. U kunt er een nieuwe versie van maken of deze dupliceren. Alleen voltooide reizen kunnen worden verwijderd.

Als u een reis wilt sluiten in de lijst met ritten, klikt u op de knop **[!UICONTROL Ellipsis]** knop rechts van de naam van de reis en selecteer **[!UICONTROL Close to new entrances]**.

![](assets/journey-finish-quick-action.png)

U kunt ook het volgende doen:

1. In de **[!UICONTROL Journeys]** klikt u op de rit die u wilt sluiten.
1. Klik rechtsboven op de pijl omlaag.

   ![](assets/finish_drop_down_list.png)

1. Klikken **[!UICONTROL Close to new entrances]** en bevestigen in het dialoogvenster.

## Een reis stoppen{#stop-journey}

Als u de voortgang van alle mensen op de reis moet stoppen, kunt u deze stoppen. Als de reis wordt stopgezet, wordt een time-out voor alle personen op de reis vastgesteld. Als we echter een reis stoppen, moeten mensen die al een reis hebben afgelegd, in de loop van hun reis worden gestopt. De reis is in feite uitgeschakeld. Als u een reis wilt beëindigen, raden wij u aan deze te sluiten.

Een voltooide reisversie kan niet opnieuw worden gestart.

Wanneer deze wordt gestopt, wordt de reisstatus ingesteld op **[!UICONTROL Stopped]**.

U kunt bijvoorbeeld een reis stoppen als een markeerder beseft dat de reis het verkeerde publiek aanvalt of dat een aangepaste actie die berichten moet leveren, niet correct werkt. Om een reis van de lijst van reizen tegen te houden, klik **[!UICONTROL Ellipsis]** knop rechts van de naam van de reis en selecteer **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

U kunt ook het volgende doen:

1. In de **[!UICONTROL Journeys]** klikt u op de reis die u wilt stoppen.
1. Klik rechtsboven op de pijl omlaag.

   ![](assets/finish_drop_down_list2.png)

1. Klikken **[!UICONTROL Stop]** en bevestigen in het dialoogvenster.
