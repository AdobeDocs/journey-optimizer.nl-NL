---
solution: Journey Optimizer
product: journey optimizer
title: Een pushmelding configureren
description: Meer informatie over het maken van een pushmelding in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 5e5b078fa61e2c615a2242f50439c2f20ea5216a
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 1%

---

# Een pushmelding maken {#create-push-notification-bis}

## Maak de pushmelding tijdens een reis of campagne

Voer de onderstaande stappen uit om een pushmelding te maken:

>[!BEGINTABS]

>[!TAB Een duwtje toevoegen aan een reis]

1. Open de reis en sleep een duwactiviteit van de sectie van Acties van het palet.

1. Verstrek basisinformatie over uw bericht (etiket, beschrijving, categorie), dan kies de berichtoppervlakte aan gebruik.

   Voor meer informatie over hoe te om een reis te vormen, verwijs naar

1. Van het scherm van de reisconfiguratie, klik **[!UICONTROL Edit content]** om de pushinhoud te configureren.

1. Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen.

1. Wanneer uw duw klaar is, voltooi de configuratie van uw om het te verzenden.

   Om het gedrag van uw ontvangers door drukknooppen en/of interactie te volgen, zorg ervoor dat de specifieke opties in de volgende sectie worden toegelaten in.

>[!TAB Een duwtje toevoegen aan een campagne]

1. Maak een nieuwe geplande of door API geactiveerde campagne, selecteer **[!UICONTROL Push notification]** als uw actie en kies **[!UICONTROL App surface]** te gebruiken.

1. Klik op **[!UICONTROL Create]**.

1. Van de **[!UICONTROL Properties]** sectie, uw campagne bewerken **[!UICONTROL Title]** en **[!UICONTROL Description]**.

1. Klik op de knop **[!UICONTROL Select audience]** om het publiek te bepalen om van de lijst van beschikbare segmenten van Adobe Experience Platform te richten.

1. In de **[!UICONTROL Identity namespace]** , kiest u de naamruimte die u wilt gebruiken om de personen van het geselecteerde segment te identificeren.

1. Campagnes worden ontworpen om op een specifieke datum of op een terugkomende frequentie worden uitgevoerd. Leer hoe u de **[!UICONTROL Schedule]** van uw campagne in.

1. Van de **[!UICONTROL Action triggers]** kiest u de **[!UICONTROL Frequency]** van uw pushmelding:

   * Eenmaal
   * Dagelijks
   * Wekelijks
   * Maandelijks

1. Van het scherm van de campagneconfiguratie, klik **[!UICONTROL Edit content]** om de pushinhoud te configureren.

1. Nadat de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om een voorbeeld van de inhoud weer te geven en deze te testen.

1. Wanneer uw duw klaar is, voltooi de configuratie van uw om het te verzenden.

   Als u het gedrag van de ontvangers wilt bijhouden via pushopeningen en/of interacties, moet u ervoor zorgen dat de toegewezen opties in de sectie Tekstspatiëring zijn ingeschakeld in de sectie.)

>[!ENDTABS]

## Snelle leveringsmodus

De snelle leveringswijze, die vroeger als wijze van de Borst bij reizen wordt bekend, is een [!DNL Journey Optimizer] een invoegtoepassing waarmee via campagnes zeer snel pushberichten op grote volumes kunnen worden verzonden.

Snelle levering wordt gebruikt wanneer de vertraging in berichtlevering zaken-kritiek is, wanneer u een dringende duwalarm op mobiele telefoons wilt verzenden, bijvoorbeeld een breekbericht aan gebruikers die uw nieuwskanaal app hebben geïnstalleerd.

Raadpleeg voor meer informatie over prestaties bij gebruik van de modus Snelle levering.

### Vereisten

Snelle levering overseinen komt met de volgende vereisten:

* Snelle levering is beschikbaar voor **[!UICONTROL Scheduled]** alleen campagnes, en niet beschikbaar voor API-gestuurde campagnes;
* In het pushbericht is geen personalisatie toegestaan.
* Het doelpubliek moet minder dan 30M profielen bevatten,
* U kunt tot 5 campagnes gelijktijdig uitvoeren gebruikend de Snelle leveringswijze.

### Modus Snelle levering activeren

1. Maak een pushmeldingscampagne en schakel de optie **[!UICONTROL Rapid delivery]** optie.

1. Vorm de berichtinhoud en selecteer het publiek om te richten.

   >[!IMPORTANT]
   >
   >Zorg ervoor dat de inhoud van het bericht geen personalisatie omvat, en dat het publiek minder dan 30M profielen bevat.

1. Controleer en activeer uw campagne op de gebruikelijke manier. In de testmodus worden berichten niet verzonden via de snelle leveringsmodus.