---
title: '&Hoofdlettergebruik voor persoonlijke voorkeur; kennisgeving orderstatus'
description: Leer hoe u een bericht kunt personaliseren met profiel, beschikking en contextinformatie.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: c058c4835c560f12e3d53bfb766324405b12968f
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Gebruiksscenario voor personalisatie: kennisgeving orderstatus {#personalization-use-case}

In dit gebruiksgeval, zult u zien hoe te om veelvoudige types van verpersoonlijking in één enkel duw bericht te gebruiken. Er worden drie typen personalisatie gebruikt:

* **Profiel**: berichten personaliseren op basis van een profielveld
* **Offertebeslissing**: personalisatie op basis van offer decisioning variabelen
* **Context**: personalisatie op basis van contextuele gegevens van de reis

Het doel van dit voorbeeld is om een gebeurtenis naar [!DNL Journey Optimizer] elke keer dat een order van een klant wordt bijgewerkt. Vervolgens wordt een pushmelding naar de klant gestuurd met informatie over de bestelling en een persoonlijke aanbieding.

Voor dit gebruik zijn de volgende voorwaarden nodig:

* Maak en ontwerp een pushmelding zonder deze te publiceren. Zie dit [sectie](../messages/get-started-content.md).
* een bestelgebeurtenis configureren, waaronder het ordernummer, de status en de naam van het item. Zie dit [sectie](../event/about-events.md).
* een besluit nemen (voorheen &quot;aanbiedingsactiviteit&quot; genoemd), naar deze [sectie](../offers/offer-activities/create-offer-activities.md).

## Stap 1 - personalisatie toevoegen aan profiel {#add-perso}

1. Klik op de knop **[!UICONTROL Message]** en selecteert u uw bericht.

   ![](assets/perso-uc.png)

1. Klik op de knop **Titel** veld.

   ![](assets/perso-uc2.png)

1. Typ het onderwerp en voeg profielpersonalisatie toe. Gebruik de zoekbalk om het voornaamveld van het profiel te zoeken. Plaats de cursor in de onderwerptekst op de plaats waar u het aanpassingsveld wilt invoegen en klik op de knop **+** pictogram. Klikken **Opslaan**.

   ![](assets/perso-uc3.png)

   >[!NOTE]
   >
   >Laat het bericht in concept staan. Publiceer het bestand nog niet.

## Stap 2 - Maak de reis {#create-journey}

1. Klik op de knop **[!UICONTROL Journeys]** en maak een nieuwe reis.

   ![](assets/perso-uc4.png)

1. Voeg uw ingangsgebeurtenis toe, a **Bericht** en **Einde** activiteit.

   ![](assets/perso-uc5.png)

1. In de **Bericht** activiteit, selecteer het eerder gecreeerd bericht. Klikken **OK**.

   ![](assets/perso-uc6.png)

   Er wordt een bericht weergegeven om u te laten weten dat de gegevens van de entry-gebeurtenis en de reiseigenschappen zijn doorgegeven aan het bericht.

   ![](assets/perso-uc7.png)

   >[!NOTE]
   >
   >Het bericht wordt weergegeven met een waarschuwingspictogram. Dit komt omdat het bericht nog niet is gepubliceerd.

## Stap 3 - Verpersoonlijking toevoegen aan contextuele gegevens {#add-perso-contextual-data}

1. Van de **Bericht** activiteit, klik **Het bericht openen** pictogram. Het bericht wordt geopend op een nieuw tabblad.

   ![](assets/perso-uc8.png)

1. Klik op de knop **Titel** veld.

   ![](assets/perso-uc9.png)

1. Selecteer **Contextafhankelijke kenmerken** -menu. Contextuele kenmerken zijn alleen beschikbaar als een reis contextuele gegevens heeft doorgegeven aan het bericht. Klikken **Journey Orchestration**. De volgende contextafhankelijke informatie wordt weergegeven:

   * **Gebeurtenissen**: deze categorie groepeert alle velden van de gebeurtenis(sen) die voor de **Bericht** tijdens de reis.
   * **Reiseigenschappen**: de technische gebieden die verband houden met de reis voor een bepaald profiel, bijvoorbeeld de reis-id of de specifieke fouten die zijn geconstateerd. Meer informatie in [Journey Orchestration-documentatie](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. Breid uit **Gebeurtenissen** en zoek het veld ordernummer voor uw gebeurtenis. U kunt ook het zoekvak gebruiken. Klik op de knop **+** pictogram om het verpersoonlijkingsgebied in de onderwerptekst op te nemen. Klikken **Opslaan**.

   ![](assets/perso-uc11.png)

1. Klik nu op de knop **Lichaam** veld.

   ![](assets/perso-uc12.png)

1. Typ het bericht en voeg het toe, van **[!UICONTROL Contextual attributes]** , de naam van het orderitem en de voortgang van de volgorde.

   ![](assets/perso-uc13.png)

1. Selecteer in het linkermenu de optie **Besluiten voorstellen** om een variabele van de offer decisioning op te nemen. Selecteer de plaatsing en klik op **+** pictogram naast de beslissing (voorheen bekend als &#39;aanbiedingsactiviteit&#39;) om deze aan het lichaam toe te voegen.

   ![](assets/perso-uc14.png)

1. Klik op Valideren om te controleren of er geen fouten zijn en klik op **Opslaan**.

   ![](assets/perso-uc15.png)

1. Publiceer nu het bericht.

   ![](assets/perso-uc16.png)

## Stap 4 - De reis testen en publiceren {#test-publish}

1. Open de reis opnieuw. Als de reis reeds open is, zorg ervoor u de pagina verfrist. Nu het bericht wordt gepubliceerd, kunt u zien dat er geen fout in de reis is. Klik op de knop **Testen** klikt u vervolgens op **Een gebeurtenis activeren**.

   ![](assets/perso-uc17.png)

1. Voer de verschillende waarden in die tijdens de test moeten worden doorstaan. De testmodus werkt alleen met testprofielen. De profiel-id moet overeenkomen met een testprofiel. Klikken **Verzenden**.

   ![](assets/perso-uc18.png)

   Het pushbericht wordt verzonden en weergegeven op de mobiele telefoon van het testprofiel.

   ![](assets/perso-uc19.png)

1. Controleer of er geen fout is en publiceer de reis.
