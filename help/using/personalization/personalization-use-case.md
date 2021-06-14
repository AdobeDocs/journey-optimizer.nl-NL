---
title: Gebruiksscenario voor persoonlijke voorkeur
description: Gebruiksscenario voor persoonlijke voorkeur
feature: Personalisatie
topic: Personalisatie
role: Data Engineer
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---


# Hoofdlettergebruik {#personalization-use-case}

![](../assets/do-not-localize/badge.png)

In dit gebruiksgeval, zult u zien hoe te om veelvoudige types van verpersoonlijking in één enkel duw bericht te gebruiken. Er worden drie typen personalisatie gebruikt:

* **Profiel**: berichten personaliseren op basis van een profielveld
* **Beslissing** voorstel: personalisatie op basis van de variabelen van het aanbiedingsbesluit
* **Context**: personalisatie op basis van contextuele gegevens van de reis

Het doel van dit voorbeeld is om een gebeurtenis naar Journey Optimizer te duwen telkens wanneer een klantenbestelling wordt bijgewerkt. Vervolgens wordt een pushmelding naar de klant gestuurd met informatie over de bestelling en een persoonlijke aanbieding.

Voor dit gebruik zijn de volgende voorwaarden nodig:

* Maak en ontwerp een pushmelding zonder deze te publiceren. Zie deze [sectie](../create-message.md).
* een bestelgebeurtenis configureren, waaronder het ordernummer, de status en de naam van het item. Zie deze [sectie](../event/about-events.md).
* een beslissing maken (voorheen bekend als &quot;aanbiedingsactiviteit&quot;), naar deze [sectie](../offers/offer-activities/create-offer-activities.md) verwijzen.

## Stap 1 - personalisatie toevoegen aan profiel

1. Klik op het menu **[!UICONTROL Message]** en selecteer uw bericht.

   ![](assets/perso-uc.png)

1. Klik op het veld **Titel**.

   ![](assets/perso-uc2.png)

1. Typ het onderwerp en voeg profielpersonalisatie toe. Gebruik de zoekbalk om het voornaamveld van het profiel te zoeken. Plaats de cursor in de onderwerptekst op de plaats waar u het aanpassingsveld wilt invoegen en klik op het pictogram **+**. Klik **Opslaan**.

   ![](assets/perso-uc3.png)

   >[!NOTE]
   >
   >Laat het bericht in concept staan. Publiceer het bestand nog niet.

## Stap 2 - Maak de reis

1. Klik op het menu **[!UICONTROL Journeys]** en maak een nieuwe reis.

   ![](assets/perso-uc4.png)

1. Voeg uw ingangsgebeurtenis, een **Bericht** en een **Eind** activiteit toe.

   ![](assets/perso-uc5.png)

1. Selecteer in de activiteit **Bericht** het eerder gemaakte bericht. Klik **Ok**.

   ![](assets/perso-uc6.png)

   Er wordt een bericht weergegeven om u te laten weten dat de gegevens van de entry-gebeurtenis en de reiseigenschappen zijn doorgegeven aan het bericht.

   ![](assets/perso-uc7.png)

   >[!NOTE]
   >
   >Het bericht wordt weergegeven met een waarschuwingspictogram. Dit komt omdat het bericht nog niet is gepubliceerd.

## Stap 3 - Verpersoonlijking toevoegen aan contextuele gegevens

1. Van **Bericht** activiteit, klik **Open het bericht** pictogram. Het bericht wordt geopend op een nieuw tabblad.

   ![](assets/perso-uc8.png)

1. Klik op het veld **Titel**.

   ![](assets/perso-uc9.png)

1. Selecteer de categorie **Context**. Dit item is alleen beschikbaar als een reis contextuele gegevens heeft doorgegeven aan het bericht. Klik **Journey Orchestration**. De volgende contextafhankelijke informatie wordt weergegeven:

   * **Gebeurtenissen**: deze categorie groepeert alle velden van de gebeurtenis(sen) die vóór de  **** berichtenactiviteit in de reis zijn geplaatst.
   * **Reiseigenschappen**: de technische gebieden die verband houden met de reis voor een bepaald profiel, bijvoorbeeld de reis-id of de specifieke fouten die zijn geconstateerd. Raadpleeg de [Journey Orchestration-documentatie](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/syntax/journey-properties.html#building-advanced-conditions-journeys).

   ![](assets/perso-uc10.png)

1. Vouw het item **Gebeurtenissen** uit en zoek het veld ordernummer dat betrekking heeft op uw gebeurtenis. U kunt ook het zoekvak gebruiken. Klik op het pictogram **+** om het aanpassingsveld in te voegen in de onderwerptekst. Klik **Opslaan**.

   ![](assets/perso-uc11.png)

1. Klik nu op het veld **Body**.

   ![](assets/perso-uc12.png)

1. Typ het bericht en voeg, vanuit de categorie **Context**, de naam van het orderitem en de voortgang van de order in.

   ![](assets/perso-uc13.png)

1. Van drop-down, uitgezochte **Beslissing van de aanbieding** om een variabele van de offer decisioning op te nemen. Selecteer de plaatsing en klik **+** pictogram naast het besluit (eerder genoemd als &quot;aanbiedingsactiviteit&quot;) om het aan het lichaam toe te voegen.

   ![](assets/perso-uc14.png)

1. Klik bevestigen om ervoor te zorgen dat er geen fouten zijn, en klik **sparen**.

   ![](assets/perso-uc15.png)

1. Publiceer nu het bericht.

   ![](assets/perso-uc16.png)

## Stap 4 - De reis testen en publiceren

1. Open de reis opnieuw. Als de reis reeds open is, zorg ervoor u de pagina verfrist. Nu het bericht wordt gepubliceerd, kunt u zien dat er geen fout in de reis is. Klik op de knop **Testen** en klik vervolgens op **Een gebeurtenis activeren**.

   ![](assets/perso-uc17.png)

1. Voer de verschillende waarden in die tijdens de test moeten worden doorstaan. De testmodus werkt alleen met testprofielen. De profiel-id moet overeenkomen met een testprofiel. Klik **Send**.

   ![](assets/perso-uc18.png)

   Het pushbericht wordt verzonden en weergegeven op de mobiele telefoon van het testprofiel.

   ![](assets/perso-uc19.png)

1. Controleer of er geen fout is en publiceer de reis.

