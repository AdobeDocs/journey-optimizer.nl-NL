---
title: Profiel bijwerken
description: Leer hoe u de activiteit van het Profiel van de Update tijdens een reis gebruikt
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 80e0fea3be11dcd594b1de04a0a903b87b9c7b68
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Profiel bijwerken {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Profielactiviteit bijwerken"
>abstract="Met de actie Profiel bijwerken kunt u een bestaand Adobe Experience Platform-profiel bijwerken met informatie die afkomstig is van de gebeurtenis, een gegevensbron of een specifieke waarde gebruiken."

Gebruik de **[!UICONTROL Update Profile]** activiteit om een bestaand profiel van Adobe Experience Platform met informatie bij te werken die uit een gebeurtenis, een gegevensbron of met een specifieke waarde komt.

## Aanbevelingen

* De **Profiel bijwerken** Actie kan alleen worden gebruikt tijdens reizen die beginnen met een gebeurtenis met een naamruimte.
* Met de handeling worden alleen bestaande velden bijgewerkt. Er worden geen nieuwe profielvelden gemaakt.
* U kunt de **Profiel bijwerken** actie om ervaringsgebeurtenissen te genereren, bijvoorbeeld een aankoop.
* Net als bij andere acties kunt u een alternatief pad definiëren in het geval van een fout of time-out. U kunt geen twee acties parallel plaatsen.
* Het updateverzoek dat naar Adobe Experience Platform wordt verzonden, is onmiddellijk of binnen een seconde. Het duurt normaal een paar seconden, maar soms nog meer zonder garantie. Als een handeling bijvoorbeeld &#39;field 1&#39; gebruikt, bijgewerkt door een **Profiel bijwerken** Actie die eerder is geplaatst, mag u niet verwachten dat &quot;veld 1&quot; wordt bijgewerkt in de handeling.
* De **Profiel bijwerken** activiteit steunt geen gebieden XDM die als opsomming worden bepaald.

## De profielupdate gebruiken

1. Ontwerp uw reis door met een gebeurtenis te beginnen. Zie dit [sectie](../building-journeys/journey.md).

1. In de **Handeling** van het palet, zet de **Profiel bijwerken** op het canvas.

   ![](assets/profileupdate0.png)

1. Selecteer een schema in de lijst.

1. Klikken op **Veld** om het veld te selecteren dat u wilt bijwerken. Er kan slechts één veld worden geselecteerd.

   ![](assets/profileupdate2.png)

1. Selecteer een gegevensset in de lijst.

   >[!NOTE]
   >
   >De **Profiel bijwerken** De actie werkt de profielgegevens in realtime bij, maar werkt datasets niet bij. De datasetselectie is nodig aangezien het profiel een verslag met betrekking tot een dataset is.

1. Klik op de knop **Waarde** veld voor het definiëren van de waarde die u wilt gebruiken:

   * Met de eenvoudige expressieeditor kunt u een veld uit een gegevensbron of uit de binnenkomende gebeurtenis selecteren.

      ![](assets/profileupdate4.png)

   * Als u een specifieke waarde wilt definiëren of geavanceerde functies wilt gebruiken, klikt u op **Geavanceerde modus**.

      ![](assets/profileupdate3.png)

De **Profiel bijwerken** is nu geconfigureerd.

![](assets/profileupdate1.png)


## De testmodus gebruiken {#using-the-test-mode}

In de testmodus wordt de profielupdate niet gesimuleerd. De update wordt uitgevoerd op het testprofiel.

Alleen testprofielen kunnen een reis maken in de testmodus. U kunt een nieuw testprofiel maken of een bestaand profiel omzetten in een testprofiel. In Adobe Experience Platform kunt u profielkenmerken bijwerken via een CSV-bestand importeren of API-aanroepen. Een eenvoudigere methode is om een **Profiel bijwerken** en wijzig het Booleaanse veld voor het testprofiel van false in true.

Raadpleeg voor meer informatie over de manier waarop u een bestaand profiel in een testprofiel kunt omzetten [sectie](../segment/creating-test-profiles.md#create-test-profiles-csv).
