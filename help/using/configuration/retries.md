---
title: Hernieuwde pogingen
description: Leer hoe opnieuw proberen alvorens een adres naar de onderdrukkingslijst te verzenden
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: 80c307a349a8ca7449639e7819683bf1f3ec3d13
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Hernieuwde pogingen {#retries}

Wanneer een bericht wegens een tijdelijke **Zachte bounce** of **Genegeerde** fout ontbreekt, worden verscheidene pogingen uitgevoerd. Elke fout verhoogt een foutenteller. Wanneer deze teller de grensdrempel bereikt, wordt het adres toegevoegd aan de onderdrukkingslijst.

In de standaardconfiguratie<!--so can you edit this setting or not?? contradictory information was given-->, wordt de drempel geplaatst bij drie fouten:

* Voor dezelfde levering, bij de derde aangetroffen fout, wordt het adres onderdrukt.

* Als er verschillende leveringen zijn en twee fouten minstens 24 uur uit elkaar voorkomen, wordt de foutenteller verhoogd op elke fout en het adres wordt ook onderdrukt bij de derde poging.

Als de levering succesvol is nadat opnieuw is geprobeerd, wordt de foutenteller van het adres opnieuw geïnitialiseerd.

U kunt de limietdrempel wijzigen met de knop **[!UICONTROL Edit]** in het menu **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**.<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4-->

![](../assets/retries-edition.png)

## Duur voor opnieuw proberen van bericht {#retry-duration}

Opnieuw proberen wordt uitgevoerd gedurende **3,5 dagen** vanaf het moment dat het bericht aan de e-mailwachtrij is toegevoegd.

De minimale vertraging tussen pogingen en het maximumaantal uit te voeren pogingen zijn <!--managed by the Enhanced MTA,--> gebaseerd op hoe goed IP presteert, zowel historisch als momenteel bij een bepaald domein.

Na 3.5 dagen, zal om het even welk bericht in de hertry rij worden verwijderd uit de rij en terug als stuit worden verzonden.<!--???-->