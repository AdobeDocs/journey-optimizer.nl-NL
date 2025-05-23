---
solution: Journey Optimizer
product: journey optimizer
title: Hoofdlettergebruik&dubbele punt; statusmelding bestellen
description: Leer hoe u een bericht kunt personaliseren met profiel, beschikking en contextinformatie.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: uitdrukking, redacteur, gebruiksgeval, verpersoonlijking
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: 1deb04490e53cbd5d67abda229bb4f850055510f
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Hoofdlettergebruik voor persoonlijk gebruik: kennisgeving van status van bestelling {#personalization-use-case}

In dit gebruiksgeval, zult u zien hoe te om veelvoudige types van verpersoonlijking in één enkel duw bericht te gebruiken. Er worden drie typen personalisatie gebruikt:

* **Profiel**: berichtpersonalisatie op basis van een profielveld
* **Offertebeslissing**: personalisatie op basis van variabelen voor besluitvormingsbeheer
* **Context**: personalisatie op basis van contextuele gegevens van de reis

Het doel van dit voorbeeld is om een gebeurtenis naar [!DNL Journey Optimizer] telkens wanneer een klantenorder wordt bijgewerkt. Vervolgens wordt een pushmelding naar de klant gestuurd met informatie over de bestelling en een persoonlijke aanbieding.

Voor dit gebruik zijn de volgende voorwaarden nodig:

* een bestelgebeurtenis configureren, waaronder het ordernummer, de status en de naam van het item. Zie dit [sectie](../event/about-events.md).
* een besluit te nemen, verwijs naar [sectie](../offers/offer-activities/create-offer-activities.md).

➡️ [Ontdek een vergelijkbaar gebruiksgeval in video](#video)

## Stap 1 - Maak de reis {#create-journey}

1. Klik op de knop **[!UICONTROL Journeys]** en maak een nieuwe reis.

   ![](assets/perso-uc4.png)

1. Voeg uw ingangsgebeurtenis toe, en a **Push** actieactiviteit.

   ![](assets/perso-uc5.png)

1. Configureer en ontwerp uw pushmelding. Zie dit [sectie](../push/create-push.md).

## Stap 2 - personalisatie toevoegen aan profiel {#add-perso}

1. In de **Push** activiteit, klik **Inhoud bewerken**.

1. Klik op de knop **Titel** veld.

   ![](assets/perso-uc2.png)

1. Voer het onderwerp in en voeg profielpersonalisatie toe. Gebruik de zoekbalk om het voornaamveld van het profiel te zoeken. Plaats de cursor in de onderwerptekst op de plaats waar u het aanpassingsveld wilt invoegen en klik op de knop **+** pictogram. Klikken **Opslaan**.

   ![](assets/perso-uc3.png)

## Stap 3 - Verpersoonlijking toevoegen aan contextuele gegevens {#add-perso-contextual-data}

1. In de **Push** activiteit, klik **Inhoud bewerken** en klik op de knop **Titel** veld.

   ![](assets/perso-uc9.png)

1. Selecteer de **Contextafhankelijke kenmerken** -menu. Contextafhankelijke kenmerken zijn alleen beschikbaar als een reis contextuele gegevens heeft doorgegeven aan het bericht. Klikken **Journey Orchestration**. De volgende contextafhankelijke informatie wordt weergegeven:

   * **Gebeurtenissen**: deze categorie hergroepeert alle velden van de gebeurtenis(sen) die vóór de kanaalactieactiviteit in de reis zijn geplaatst.
   * **Reiseigenschappen**: de technische gebieden die verband houden met de reis voor een bepaald profiel, bijvoorbeeld de reis-id of de specifieke fouten die zijn geconstateerd. Meer informatie in [Documentatie Journey Orchestration](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. Breid uit **Gebeurtenissen** en zoek het veld ordernummer voor uw gebeurtenis. U kunt ook het zoekvak gebruiken. Klik op de knop **+** pictogram om het verpersoonlijkingsgebied in de onderwerptekst op te nemen. Klikken **Opslaan**.

   ![](assets/perso-uc11.png)

1. Klik nu op de knop **Lichaam** veld.

   ![](assets/perso-uc12.png)

1. Typ het bericht en voeg het toe, van **[!UICONTROL Contextual attributes]** , de naam van het orderitem en de voortgang van de volgorde.

   ![](assets/perso-uc13.png)

1. Selecteer in het linkermenu de optie **Beslissingen voorstellen** om een beslissingsvariabele in te voegen. Selecteer de plaatsing en klik op **+** pictogram naast de beslissing om het aan het lichaam toe te voegen.

   ![](assets/perso-uc14.png)

1. Klik op Valideren om te controleren of er geen fouten zijn en klik op **Opslaan**.

   ![](assets/perso-uc15.png)

## Stap 4 - De reis testen en publiceren {#test-publish}

1. Klik op de knop **Testen** klikt u vervolgens op **Een gebeurtenis activeren**.

   ![](assets/perso-uc17.png)

1. Voer de verschillende waarden in die tijdens de test moeten worden doorstaan. De testmodus werkt alleen met testprofielen. De profiel-id moet overeenkomen met een testprofiel. Klikken **Verzenden**.

   ![](assets/perso-uc18.png)

   Het pushbericht wordt verzonden en weergegeven op de mobiele telefoon van het testprofiel.

   ![](assets/perso-uc19.png)

1. Controleer of er geen fout is en publiceer de reis.

## Hoe kan ik-video {#video}

In de onderstaande video ziet u een vergelijkbaar gebruiksscenario waarin gebruik wordt gemaakt van contextafhankelijke gegevens van een reis om een e-mail aan te passen.

>[!VIDEO](https://video.tv.adobe.com/v/3428532?quality=12&captions=dut)
