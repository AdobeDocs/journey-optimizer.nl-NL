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
source-git-commit: 18296fe54dcef6620d4f74374848199368f01475
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 1%

---

# Een reis beëindigen{#journey-ending}

Een reis kan voor een individu in twee specifieke contexten eindigen:

* De persoon komt bij de laatste activiteit van een weg aan.
* De persoon komt bij a **Voorwaarde** activiteit (of a **wacht** activiteit met een voorwaarde) aan en past geen van de voorwaarden aan.

De persoon kan dan de reis opnieuw betreden als zijn binnenkomst is toegestaan. Zie [ deze pagina ](../building-journeys/journey-properties.md#entrance)

Om een live reis te beëindigen, adviseren wij dat u het sluit. De komst van nieuwe klanten op de reis zal dan worden geblokkeerd. Klanten die al op reis zijn gegaan, kunnen het tot het einde ervaren. Zie [ deze sectie ](../building-journeys/journey.md#close-journey)

U kunt een reis alleen stoppen als zich een noodsituatie voordoet en alle verwerking onmiddellijk op een reis moet worden beëindigd. Personen die al een reis zijn binnengekomen, worden in de loop der tijd gestopt. Zie [ deze sectie ](../building-journeys/journey.md#stop-journey)

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

* De reis wordt manueel gesloten via de **[!UICONTROL Close to new entrances]** knoop.
* Een reis op basis van een segment met één opname die klaar is met de uitvoering.
* Na het laatste optreden van een terugkerende, op het publiek gebaseerde reis.

Als u een reis handmatig sluit, weet u zeker dat klanten die de reis al hebben betreden, hun pad kunnen voltooien, maar dat nieuwe gebruikers de reis niet kunnen betreden. Wanneer een reis wordt gesloten (om een van de bovenstaande redenen), heeft deze de status **[!UICONTROL Closed]** . De reis houdt in dat nieuwe individuen de reis kunnen betreden. Personen die al onderweg zijn, kunnen de reis normaal afmaken.

Na de globale onderbreking van 91 dagen [ ](journey-properties.md#timeout), leest de schakelaars van de publiekstraject aan de **voltooide** status. Dit gedrag wordt geplaatst voor 91 dagen slechts (d.w.z. [ reis globale onderbrekingswaarde ](journey-properties.md#global_timeout)) aangezien al informatie over profielen die de reis inging 91 dagen wordt verwijderd nadat zij ingegaan. Personen die nog onderweg zijn, worden automatisch getroffen. Ze verlaten de reis na de 91-dagen onderbreking.

Zie deze [ sectie ](../building-journeys/journey-properties.md#global_timeout).

Een gesloten reisversie kan niet opnieuw worden gestart of verwijderd. U kunt er een nieuwe versie van maken of deze dupliceren. Alleen voltooide reizen kunnen worden verwijderd.

Als u een rit wilt sluiten in de lijst met ritten, klikt u op de knop **[!UICONTROL Ellipsis]** rechts van de naam van de rit en selecteert u **[!UICONTROL Close to new entrances]** .

![](assets/journey-finish-quick-action.png)

U kunt ook het volgende doen:

1. Klik in de lijst **[!UICONTROL Journeys]** op de rit die u wilt sluiten.
1. Klik rechtsboven op de pijl omlaag.

   ![](assets/finish_drop_down_list.png)

1. Klik op **[!UICONTROL Close to new entrances]** en bevestig dit in het dialoogvenster.

## Een reis stoppen{#stop-journey}

Als u de voortgang van alle mensen op de reis moet stoppen, kunt u deze stoppen. Als de reis wordt stopgezet, wordt een time-out voor alle personen op de reis vastgesteld. Als we echter een reis stoppen, moeten mensen die al een reis hebben afgelegd, in de loop van hun reis worden gestopt. De reis is in feite uitgeschakeld. Als u een reis wilt beëindigen, raden wij u aan deze te sluiten.

Een voltooide reisversie kan niet opnieuw worden gestart.

Wanneer deze wordt gestopt, wordt de reisstatus ingesteld op **[!UICONTROL Stopped]** .

U kunt bijvoorbeeld een reis stoppen als een markeerder beseft dat de reis het verkeerde publiek aanvalt of dat een aangepaste actie die berichten moet leveren, niet correct werkt. Als u een reis wilt stoppen in de lijst met reizen, klikt u op de knop **[!UICONTROL Ellipsis]** rechts van de naam van de reis en selecteert u **[!UICONTROL Stop]** .

![](assets/journey-finish-quick-action.png)

U kunt ook het volgende doen:

1. Klik in de lijst **[!UICONTROL Journeys]** op de rit die u wilt stoppen.
1. Klik rechtsboven op de pijl omlaag.

   ![](assets/finish_drop_down_list2.png)

1. Klik op **[!UICONTROL Stop]** en bevestig dit in het dialoogvenster.
