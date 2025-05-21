---
title: Afbakening van reizen en arbitrage
description: Leer hoe u regels voor aftopping kunt maken voor uw reizen en hoe u een arbitrage kunt instellen bij het betreden van een reis
role: User
level: Beginner
badge: label="Beperkte beschikbaarheid"
exl-id: 4c0ee178-81fb-41ae-b7f5-22da995e6fc6
source-git-commit: b2446c6a243d6d95b6f695b9c7007e62c51d8fa3
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%

---

# Afbakening van reizen en arbitrage {#journey-capping}

>[!AVAILABILITY]
>
>Conflict- en prioriteitsmogelijkheden zijn momenteel beschikbaar in Beperkte beschikbaarheid voor een geselecteerde groep klanten. Houd er rekening mee dat deze functies in de toekomst geleidelijk aan voor meer gebruikers beschikbaar zullen zijn. Neem contact op met uw accountteam als u interesse hebt in het toevoegen van deze functies aan de wachtlijst.

Met de functie voor aftopping kunt u het aantal ritten beperken waarin een profiel kan worden ingeschreven, zodat overbelasting van communicatie wordt voorkomen. In Journey Optimizer kunt u twee typen uitlijningsregels instellen:

* **toegang begrensd** beperkt het aantal reisingangen over een bepaalde periode voor een profiel.
* **In samenloop het maximum** beperkt hoeveel reizen een profiel in gelijktijdig kan worden ingeschreven.

Beide typen aftopping maken gebruik van prioriteitsscores om items te scheiden.

>[!AVAILABILITY]
>
>**de reeksen van de de domeinregel van 0&rbrace; Reis &lbrace;zijn beschikbaar slechts aan een beperkte reeks gebruikers (Beperkte Beschikbaarheid).** Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

➡️ [Ontdek deze functie in video](#video)

## Een regel voor het afdekken van reizen maken {#create-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_set_concurrency_prioritization"
>title="Prioritaire toekomst"
>abstract=" Als een reis met een hogere prioriteit binnen de hier gespecificeerde periode wordt gepland, dan zal de klant van het ingaan van deze reis worden onderdrukt. Voor situaties waarin u op de eerste dag reizen wilt maken, stellen wij voor om eerst de Daily-periode te kiezen en ervoor te zorgen dat de prioriteitsscore van andere reizen op die dag lager is dan de prioriteitsscore voor de reis. Een prioriteitsscore van 100 voor een reis zou er ook voor zorgen dat het wordt ingevoerd."

>[!CONTEXTUALHELP]
>id="ajo_rule_set_rule_type"
>title="Type regel"
>abstract="Geef het type uitlijnen voor de regel op. **[!UICONTROL Journey Entry Cap]** beperkt het aantal items in de reis over een bepaalde periode voor een profiel, terwijl **[!UICONTROL Journey Concurrency Cap]** beperkt hoeveel reizen een profiel tegelijkertijd kan inschrijven."

Voer de volgende stappen uit om een regel voor het afdekken van reizen te maken:

1. Navigeer naar het menu **[!UICONTROL Business rules]** voor toegang tot het overzicht van regelsets.

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

     >[!AVAILABILITY]
     >
     >De &quot;Daily&quot;duur is slechts beschikbaar voor een reeks organisaties (Beperkte Beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

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

>[!CONTEXTUALHELP]
>id="ajo_journey_capping_rule"
>title="Regel toepassen op reizen"
>abstract="Pas een Regelreeks toe om deze reis aan een deel van uw publiek uit te sluiten die op frequentie het begrenzen regels wordt gebaseerd."

Om een afluisterregel op een reis toe te passen, toegang tot de reis en open zijn eigenschappen. Selecteer in de vervolgkeuzelijst **[!UICONTROL Capping rules]** de desbetreffende regelset. Zodra de reis in werking wordt gesteld, zullen de plafondregels die in de vastgestelde regel worden bepaald van kracht worden.

![](assets/journey-capping-apply.png)

>[!IMPORTANT]
>
>Als een reis onmiddellijk wordt geactiveerd, kan het tot 20 minuten duren voordat het systeem begint met het onderdrukken van klanten. U kunt uw reis plannen om minstens 20 minuten in de toekomst te beginnen om deze mogelijkheid te verhinderen.

Zodra de reis levend is, kunt u het reisrapport controleren als de vastgestelde regel tot om het even welke uitsluiting van de reis, in de **[!UICONTROL Journey Exclusions]** lijst heeft geleid. [ Leer hoe te met reisrapporten ](../reports/journey-global-report-cja.md) te werken

![](assets/journey-report.png)

## Hoe kan ik-video {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3447621?quality=12&captions=dut)
