---
solution: Journey Optimizer
product: journey optimizer
title: De beste praktijken van SMS voor kostenoptimalisering
description: Leer hoe u de kosten van SMS-berichten kunt optimaliseren door tekenlimieten, codering en personalisatie te beheren in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Intermediate
source-git-commit: 13b3c8aa7fce85029167ef31feb7272e4877b7b0
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Aanbevolen procedures voor optimalisatie van de SMS-kosten {#sms-cost-optimization}

SMS-berichten worden meestal in rekening gebracht door providers op basis van een limiet van 160 tekens per bericht. Het verzenden van SMS-berichten kan extra kosten met zich meebrengen als berichten in meerdere delen worden gesplitst.

Volg deze richtlijnen om uw overseinenstrategie te optimaliseren en uitgaven te verminderen.

## Berichten kort houden {#keep-messages-short}

Journey Optimizer staat maximaal 1.500 tekens toe in een SMS-berichttekst. Er wordt een waarschuwing weergegeven wanneer u deze limiet overschrijdt. Bij berichten boven deze drempel treedt een fout op.

De meeste SMS-providers ondersteunen 7-bits GSM-codering, waarbij één SMS maximaal 160 tekens kan bevatten. Berichten die deze lengte overschrijden, worden automatisch gesplitst in meerdere SMS-onderdelen (samenvoegen):

* **minder dan 160 karakters**: 1 het deel van SMS
* **161-306 karakters**: 2 de delen van SMS
* **307-459 karakters**: 3 de delen van SMS

**om kosten** te minimaliseren, doel om berichten onder 160 karakters te houden zodat worden zij in rekening gebracht als één enkel deel van SMS.

Een bericht van 1.600 tekens kan bijvoorbeeld 10 SMS-credits verbruiken, ook al wordt het als één bericht weergegeven in Journey Optimizer.

## Gebruik geen speciale tekens die de lengte vergroten {#avoid-special-characters}

Bepaalde tekens, zoals `| ^ € { } [ ] ~ \` , worden geteld als twee tekens in GSM-codering. Het omvatten van deze karakters kan uw bericht veroorzaken om de **160 karaktergrens** sneller te overschrijden.

## UCS-2-codering voorkomen {#prevent-ucs2-encoding}

Als het bericht niet-GSM karakters, zoals Chinese of Arabische tekst, handelsmerksymbolen, of harde terugkeer van rijk-formatterende hulpmiddelen omvat, zal het bericht door de leverancier worden gecodeerd gebruikend UCS-2, die slechts 70 karakters per SMS steunt.

Het gebruik van UCS-2-codering kan het aantal tekens doen toenemen en kan daarom invloed hebben op het factureren van berichten bij uw serviceprovider.

Bijvoorbeeld, zal een 200 karakterUnicode bericht in 3 delen van SMS worden geleverd.

## Aanbevolen werkwijzen ontwerpen {#authoring-best-practices}

Stel het laatste SMS-bericht rechtstreeks samen in Journey Optimizer of plak het vanuit platte toepassingen.

Vermijd het gebruik van RTF-toepassingen, aangezien deze verborgen tekens of regeleinden kunnen introduceren die UCS-2-codering activeren, waardoor zowel het aantal SMS-onderdelen als de bijbehorende kosten kunnen toenemen.

## Tekenaantal controleren vóór verzending {#check-character-count}

Gebruik normale tekst of Journey Optimizer **[!UICONTROL Simulate content]** om het aantal tekens te controleren.

Terwijl Journey Optimizer een aantal tekens weergeeft, inclusief spaties, tijdens het simuleren van inhoud, moet u het volgende opmerken:

* Het **&#x200B;**&#x200B;omvat geen karakters die door dynamische verpersoonlijking of bepaalde speciale karakters worden geproduceerd.

* De **x/1500 telling** dient als visuele indicator van de technische ladingsgrens, niet de per-berichtgrens, bijvoorbeeld, de 160 karakterGSM 7 beetjegrens.

* Adobe ondersteunt UTF-8-codering in de editor, die verschilt van GSM-7-bits codering.

## Werken met rapportage {#understanding-reporting}

**Journey Optimizer die** meldt telt het volledige bericht als één verzendt, ongeacht de delen van SMS.

**Leverancier die** meldt wijst op het daadwerkelijke aantal SMS berichtdelen die voor levering worden gebruikt en zou moeten worden bedoeld om het factureren en om het even welke potentiële overages te bevestigen. Als Adobe je SMS-provider via Sinch is, ontvang je dit factureringsrapport maandelijks apart.

## Personalization-overwegingen {#personalization-considerations}

De dynamische verpersoonlijking kan de lengte van een bericht verhogen. Als u bijvoorbeeld een variabele vervangt door een lange voornaam, kunt u extra tekens toevoegen.

## Aanvullende bronnen {#additional-resources}

Herzie gesteunde karakters en het coderen regels in {de Gids van de Steun van het Teken van 0} Sinch [&#128279;](https://developers.sinch.com/docs/sms/resources/message-info/character-support/)

