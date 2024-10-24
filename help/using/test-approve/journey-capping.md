---
title: Afbakening van reizen en arbitrage
description: Leer hoe u regels voor aftopping kunt maken voor uw reizen en hoe u een arbitrage kunt instellen bij het betreden van een reis
role: User
level: Beginner
badge: label="Beperkte beschikbaarheid"
hide: true
hidefromtoc: true
source-git-commit: 0eedadee1e8c1d4642d8602d48bcc9a49a0a2e53
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---


# Afbakening van reizen en arbitrage {#journey-capping}

>[!BEGINSHADEBOX]

Wat u in deze documentatiehandleiding zult vinden:

* [Aan de slag met conflictbeheer en -prioriteiten](gs-conflict-prioritization.md)
* [Mogelijke conflicten tijdens reizen en campagnes detecteren](conflicts.md)
* [Prioritaire scores toewijzen aan reizen en campagnes](priority-scores.md)
* **[Reis het in kaart brengen &amp; arbitrage](journey-capping.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>De hulpmiddelen voor Conflictbeheer en prioritering zijn momenteel alleen beschikbaar als Beperkte beschikbaarheid voor geselecteerde gebruikers.

Met de functie voor aftopping kunt u het aantal ritten beperken waarin een profiel kan worden ingeschreven, zodat overbelasting van communicatie wordt voorkomen. In Journey Optimizer kunt u twee typen uitlijningsregels instellen:

* **toegang begrensd** beperkt het aantal reisingangen over een bepaalde periode voor een profiel.
* **In samenloop het maximum** beperkt hoeveel reizen een profiel in gelijktijdig kan worden ingeschreven.

Beide typen aftopping maken gebruik van prioriteitsscores om items te scheiden.

➡️ [ ontdekt deze eigenschap in video ](#video)

## Een regel voor het afdekken van reizen maken {#create-rule}

Voer de volgende stappen uit om een regel voor het afdekken van reizen te maken:

1. Navigeer naar het menu **[!UICONTROL Business rules (Beta)]** voor toegang tot het overzicht van regelsets.

1. Selecteer de regelset waaraan u de afkapregel wilt toevoegen of maak een nieuwe regelset:

   * Om een bestaande regelreeks te gebruiken, selecteer het van de lijst. Regels voor het afdekken van reizen kunnen alleen worden toegevoegd aan regelsets met het domein &#39;reis&#39;. U kunt deze informatie controleren in de lijsten met regelsets in de kolom **[!UICONTROL Domain]** .

     ![](assets/journey-capping-list.png)

   * Klik op **[!UICONTROL Create rule set]** om de afkapregel binnen een nieuwe regelset te maken, geef een unieke naam voor de regelset op en selecteer &#39;Reis&#39; in de vervolgkeuzelijst **[!UICONTROL Rule Set Domain]** en klik vervolgens op **[!UICONTROL Save]** .

     ![](assets/journey-capping-rule-set.png)

1. In het scherm van de regelreeks, klik de **[!UICONTROL Add Rule]** knoop dan vormt de regel om uw behoeften aan te passen:

   ![](assets/journey-capping-concurrency.png)

   * Geef de regel een unieke naam.

   * Geef in de vervolgkeuzelijst **[!UICONTROL Rule Type]** het type uitlijning voor de regel op.

      * **[!UICONTROL Journey Entry Cap]**: beperkt het aantal items dat gedurende een bepaalde periode voor een profiel wordt ingevoerd in de reis.
      * **[!UICONTROL Journey Concurrency Cap]**: hiermee wordt beperkt hoeveel ritten een profiel gelijktijdig kan worden ingeschreven.

   * Vouw de onderstaande secties uit om te leren hoe u elk type uitvulling kunt configureren:

     +++Configureer een regel voor het afdekken van verplaatsingen

      1. Stel in het veld **[!UICONTROL Capping]** het maximum aantal ritten in dat een profiel kan invoeren.
      1. Definieer in het veld **[!UICONTROL Duration]** de tijdsperiode die u wilt overwegen. De duur is gebaseerd op de UTC-tijdzone. Zo wordt de Daily cap ingesteld op middernacht UTC.

     In dit voorbeeld willen we de profielen beperken om meer dan &quot;5&quot; reizen per maand in te voeren.

     ![](assets/journey-capping-entry-example.png)

     >[!NOTE]
     >
     >In het systeem zal rekening worden gehouden met de prioriteit van komende geplande reizen waarop dezelfde regel van toepassing is.
     >
     >In dit voorbeeld, als de markteur reeds vier reizen heeft betreden en er een volgende geplande reis is deze maand met een hogere prioriteit, dan zullen de klanten van het ingaan van de lagere prioritaire reis worden onderdrukt.

+++

     +++Configureer een regel voor het aftoppen van de route

      1. Stel in het veld **[!UICONTROL Capping]** het maximumaantal ritten in waarin een profiel gelijktijdig kan worden ingeschreven.

      1. Gebruik het veld **[!UICONTROL Prioritization look ahead]** om te scheiden hoe items in de reis worden geplaatst op basis van prioriteitsscores over een bepaalde periode (bijvoorbeeld 1 dag, 7 dagen, 30 dagen). Dit helpt om voorrang te geven aan het binnenkomen van duurdere reizen als een profiel in aanmerking komt voor meerdere reizen.

     In dit voorbeeld willen we profielen beperken van het betreden van de reis als ze al zijn ingeschreven voor een andere reis die dezelfde regel bevat. Als een andere reis binnen de volgende 7 dagen een hogere prioritaire score heeft, zal het profiel deze reis niet ingaan.

     ![](assets/journey-capping-concurrency-example.png){width="50%" zommable="yes"}

+++

1. Wanneer de afschilderregel klaar is om te worden toegepast op reizen, activeert u deze door op de knop Ovaal naast de naam te klikken.

   ![](assets/journey-capping-activate-rule.png)

1. Activeer de volledige die regel door de elliptische knoop naast de Add knoop van de Regel in de hoger-juiste hoek van het scherm wordt geplaatst te klikken.

   ![](assets/journey-capping-activate-rule-set.png)

## Afdekkingsregels toepassen op reizen {#apply-capping}

Om een afluisterregel op een reis toe te passen, toegang tot de reis en open zijn eigenschappen. Selecteer in de vervolgkeuzelijst **[!UICONTROL Capping rules]** de desbetreffende regelset.

Zodra de reis in werking wordt gesteld, zullen de plafondregels die in de vastgestelde regel worden bepaald van kracht worden.

![](../test-approve/assets/journey-capping-apply.png)

>[!IMPORTANT]
>
>Als een reis onmiddellijk wordt geactiveerd, kan het tot 15 minuten duren voordat het systeem begint met het onderdrukken van klanten. U kunt uw reis plannen om minstens 15 minuten in de toekomst te beginnen om deze mogelijkheid te verhinderen.

## Hoe kan ik-video {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435530?quality=12)
