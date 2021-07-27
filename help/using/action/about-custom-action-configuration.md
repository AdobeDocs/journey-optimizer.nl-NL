---
solution: Journey Orchestration
title: Aangepaste acties configureren
description: Leer hoe u een aangepaste handeling configureert
feature: Acties
topic: Beheer
role: Admin
level: Intermediate
source-git-commit: e6d8d8ee637008a886ca308b5b0d9d53d90b11ce
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 9%

---

# Een actie configureren {#configure-an-action}

Als u een derdesysteem gebruikt om berichten te verzenden of als u reizen API vraag naar een derdesysteem wilt verzenden, is dit waar u zijn verbinding aan reizen vormt. De aangepaste actie die door technische gebruikers is gedefinieerd, is dan beschikbaar in het linkerpalet van uw reis, in de categorie **[!UICONTROL Action]** (zie [deze pagina](../building-journeys/about-journey-activities.md#action-activities). Hier volgen enkele voorbeelden van systemen waarmee u verbinding kunt maken met aangepaste handelingen: Epsilon, Facebook, Adobe.io, Firebase, enz.
Beperkingen worden vermeld in [deze pagina](../building-journeys/limitations.md).

Hier zijn de belangrijkste stappen die worden vereist om een douaneactie te vormen:

1. Selecteer **[!UICONTROL Configurations]** in de sectie van het menu BEHEER. Klik in de sectie **[!UICONTROL Actions]** op **[!UICONTROL Manage]**. Klik **[!UICONTROL Create Action]** om een nieuwe actie tot stand te brengen. Het deelvenster Handelingsconfiguratie wordt aan de rechterkant van het scherm geopend.

   ![](../assets/custom2.png)

1. Voer een naam in voor de handeling.

   >[!NOTE]
   >
   >Gebruik geen spaties of speciale tekens. Gebruik niet meer dan 30 tekens.

1. Voeg een beschrijving aan uw actie toe. Deze stap is optioneel.
1. Het aantal ritten dat deze handeling gebruikt, wordt weergegeven in het veld **[!UICONTROL Used in]**. U kunt op de knop **[!UICONTROL View journeys]** klikken om de lijst met ritten weer te geven die deze handeling gebruiken.
1. Definieer de verschillende **[!UICONTROL URL Configuration]** parameters. Zie [deze pagina](../action/about-custom-action-configuration.md#url-configuration).
1. Configureer de sectie **[!UICONTROL Authentication]**. Deze configuratie is het zelfde als voor gegevensbronnen.  Zie [deze sectie](../datasource/external-data-sources.md#section_wjp_nl5_nhb).
1. Definieer de **[!UICONTROL Action parameters]**. Zie [deze pagina](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Klik op **[!UICONTROL Save]**.

   De aangepaste handeling is nu geconfigureerd en klaar om te worden gebruikt tijdens uw reizen. Zie [deze pagina](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Wanneer een douaneactie in een reis wordt gebruikt, zijn de meeste parameters read-only. U kunt alleen de velden **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** en **[!UICONTROL Authentication]** wijzigen.

## URL-configuratie {#url-configuration}

Wanneer het vormen van een douaneactie, moet u de volgende **[!UICONTROL URL Configuration]** parameters bepalen:

![](../assets/journeyurlconfiguration.png)

1. Voeg de **[!UICONTROL URL]** van de externe service toe.

   >[!NOTE]
   >
   >We raden u uit beveiligingsoverwegingen sterk aan om HTTPS te gebruiken. Wij staan niet het gebruik van Adobe adressen toe die niet openbaar en het gebruik van IP adressen zijn.

1. Selecteer de vraag **[!UICONTROL Method]**: kan **[!UICONTROL POST]** of **[!UICONTROL PUT]** zijn.
1. Klik in de sectie **[!UICONTROL Headers]** op **[!UICONTROL Add a header field]** om een nieuw sleutel-/waardepaar te definiëren. Ze komen overeen met de HTTP-headers van de aanvraag die aan de externe service is gedaan. Als u sleutel-/waardeparen wilt verwijderen, plaatst u de cursor in het koptekstveld en klikt u op het pictogram **[!UICONTROL Delete]**.

   **[!UICONTROL Content-Type]** en  **[!UICONTROL Charset]** worden standaard ingesteld en kunnen niet worden verwijderd of overschreven.

   >[!NOTE]
   >
   >Kopteksten worden gevalideerd volgens de volgende [parseringsregels](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## De actieparameters definiëren {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

Plak in de sectie **[!UICONTROL Action parameters]** een voorbeeld van de JSON-payload die u naar de externe service wilt verzenden.

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>Veldnamen in de payload mogen geen &quot;.&quot; bevatten teken. Ze kunnen niet beginnen met het teken ‘$’.

U kunt het parametertype definiëren (bijvoorbeeld: tekenreeks, geheel getal, enz.).

U kunt ook opgeven of een parameter een constante of een variabele is.

* Constante betekent dat de waarde van de parameter in de ruit van de actieconfiguratie door een technische persoon wordt bepaald. De waarde zal altijd het zelfde over reizen zijn. De kleur verandert niet en de markeerstift ziet deze niet wanneer u de aangepaste handeling voor de reis gebruikt. Het kan bijvoorbeeld een id zijn die het externe systeem verwacht. In dat geval is het veld rechts van de schakelconstante/variabele de doorgegeven waarde.
* Variabele betekent dat de waarde van de parameter varieert. De markering die deze aangepaste actie gebruikt, kan de gewenste waarde doorgeven of opgeven waar de waarde voor deze parameter moet worden opgehaald (bijvoorbeeld van het evenement, van de Adobe Experience Platform, enz.). In dat geval is het veld aan de rechterkant van de schakelconstante/variabele het label dat de markator in de reis ziet om deze parameter een naam te geven.

![](../assets/customactionpayloadmessage2.png)
