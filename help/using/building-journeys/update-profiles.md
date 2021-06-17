---
title: Profiel bijwerken
description: Leer hoe u de activiteit van het Profiel van de Update tijdens een reis gebruikt
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: d76eee0efa6735d6d81d7d7c752ed253b4cbebb5
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---

# Profiel {#update-profile} bijwerken

Met de actieactiviteit **[!UICONTROL Update Profile]** kunt u een bestaand Adobe Experience Platform-profiel bijwerken met informatie die afkomstig is van de gebeurtenis, een gegevensbron of het gebruik van een specifieke waarde.

## Belangrijke opmerkingen

* De handeling **Profiel bijwerken** kan alleen worden gebruikt tijdens reizen die beginnen met een gebeurtenis met een naamruimte.
* Met de handeling worden alleen bestaande velden bijgewerkt. Er worden geen nieuwe profielvelden gemaakt.
* U kunt de handeling **Profiel bijwerken** niet gebruiken om ervaringsgebeurtenissen te genereren, bijvoorbeeld een aankoop.
* Net als bij andere acties kunt u een alternatief pad definiëren in het geval van een fout of time-out. U kunt geen twee acties parallel plaatsen.
* Het updateverzoek dat naar het Platform wordt verzonden, wordt snel verzonden, maar niet onmiddellijk/binnen een seconde. Het duurt normaal een paar seconden, maar soms nog meer zonder garantie. Als een handeling bijvoorbeeld &#39;field 1&#39; gebruikt die is bijgewerkt met een handeling Profiel bijwerken die eerder is geplaatst, mag u niet verwachten dat &#39;field 1&#39; wordt bijgewerkt in de handeling.
* Gegevensbronnen hebben een begrip van cacheduur, op het niveau van de gebiedsgroep. Als u tijdens een rit een profielveld wilt gebruiken dat onlangs is bijgewerkt, moet u zorgvuldig een zeer korte cache-duur definiëren.

## De testmodus {#using-the-test-mode} gebruiken

In de testmodus wordt de profielupdate niet gesimuleerd. De update wordt uitgevoerd op het testprofiel.

Alleen testprofielen kunnen een reis maken in de testmodus. U kunt een nieuw testprofiel maken of een bestaand profiel omzetten in een testprofiel. In het Platform van de Ervaring van Adobe, kunt u profielattributen via csv- dossierinvoer of API vraag bijwerken. Een eenvoudigere methode is om een **Actieactiviteit van het Profiel van de Update** te gebruiken en het van het testprofiel booleaanse gebied van vals in waar te veranderen.

Raadpleeg deze [sectie](../building-journeys/creating-test-profiles.md#create-test-profiles-csv) voor meer informatie over de manier waarop u een bestaand profiel in een testprofiel kunt omzetten.

## De profielupdate gebruiken

1. Ontwerp uw reis door met een gebeurtenis te beginnen. Zie deze [sectie](../building-journeys/journey.md).

1. In **Actie** sectie van het palet, laat vallen **Update Profiel** activiteit in het canvas.

   ![](../assets/profileupdate0.png)

1. Selecteer een schema in de lijst.

1. Klik op **Veld** om het veld te selecteren dat u wilt bijwerken. Er kan slechts één veld worden geselecteerd.

   ![](../assets/profileupdate2.png)

1. Selecteer een gegevensset in de lijst.

   >[!NOTE]
   >
   >De actie **Profiel bijwerken** werkt de profielgegevens in realtime bij, maar werkt datasets niet bij. De datasetselectie is nodig aangezien het profiel een verslag met betrekking tot een dataset is.

1. Klik op het veld **Waarde** om de waarde te definiëren die u wilt gebruiken:

   * Met de eenvoudige expressieeditor kunt u een veld uit een gegevensbron of uit de binnenkomende gebeurtenis selecteren.

      ![](../assets/profileupdate4.png)

   * Als u een specifieke waarde wilt definiëren of geavanceerde functies wilt gebruiken, klikt u op **Geavanceerde modus**.

      ![](../assets/profileupdate3.png)

**Het Profiel van de Update** wordt nu gevormd.

![](../assets/profileupdate1.png)
