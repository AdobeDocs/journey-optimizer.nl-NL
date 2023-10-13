---
solution: Journey Optimizer
product: journey optimizer
title: Algemene gebeurtenissen
description: Leer hoe u algemene gebeurtenissen kunt gebruiken
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: aangepast, algemeen, evenementen, reizen
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 055b735308cc6f0f942c165541d87dfdb74f557c
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 1%

---

# Algemene gebeurtenissen {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Unitaire gebeurtenissen"
>abstract="Gebeurtenissen stellen u in staat om uw reizen tijdelijk te activeren en berichten in real-time te verzenden aan de persoon die de reis maakt. Voor dit type gebeurtenis kunt u alleen een label en een beschrijving toevoegen. De gebeurtenisconfiguratie wordt uitgevoerd door een gegevensingenieur en kan niet worden uitgegeven."

Gebeurtenissen stellen u in staat om uw reizen tijdelijk te activeren en berichten in real-time te verzenden aan de persoon die de reis maakt.

Voor dit type gebeurtenis kunt u alleen een label en een beschrijving toevoegen. De rest van de configuratie kan niet worden bewerkt. Het werd uitgevoerd door de technische gebruiker. Zie [deze pagina](../event/about-events.md).

![](assets/general-events.png)

Wanneer u een bedrijfsgebeurtenis neerzet, wordt automatisch een **Publiek lezen** activiteit. Raadpleeg voor meer informatie over bedrijfsgebeurtenissen [deze sectie](../event/about-events.md)

## Luisteren naar gebeurtenissen tijdens een bepaald tijdstip {#events-specific-time}

Een gebeurtenisactiviteit die in de reis wordt geplaatst luistert voor onbepaalde tijd naar gebeurtenissen. Als u alleen tijdens een bepaalde tijd naar een gebeurtenis wilt luisteren, moet u een time-out voor de gebeurtenis configureren.

De reis zal dan aan de gebeurtenis tijdens de tijd luisteren die in de timeout wordt gespecificeerd. Als een gebeurtenis tijdens die periode wordt ontvangen, zal de persoon in de gebeurtenisweg stromen. Als niet, zal de klant of in een onderbrekingspad stromen, of hun reis beëindigen.

Voer de volgende stappen uit om een time-out voor een gebeurtenis te configureren:

1. Activeer **[!UICONTROL Define the event timeout]** van de eigenschappen van de gebeurtenis.

1. Geef op hoeveel tijd de reis moet wachten op de gebeurtenis.

1. Als u de personen naar een time-outpad wilt sturen wanneer er geen gebeurtenis is ontvangen binnen de opgegeven time-out, schakelt u de optie **[!UICONTROL Set a timeout path]** -optie. Als deze optie niet wordt ingeschakeld, eindigt de reis voor het individu zodra de time-out is bereikt.

   ![](assets/event-timeout.png)

In dit voorbeeld, verzendt de reis een eerste welkome duw naar een klant. Het verzendt dan een duw van de maaltijdkorting slechts als de klant het restaurant binnen de volgende dag ingaat. Daarom hebben we de restaurant-gebeurtenis geconfigureerd met een time-out van 1 dag:

* Als de restaurantgebeurtenis minder dan 1 dag na de welkomstpush wordt ontvangen, wordt de pushactiviteit voor de maaltijdkorting verzonden.
* Als er de volgende dag geen restaurantgebeurtenis wordt ontvangen, loopt de persoon door het time-outpad.

Merk op dat als u een onderbreking op veelvoudige gebeurtenissen wilt vormen die na een **[!UICONTROL Wait]** activiteit, moet u de onderbreking op één van deze gebeurtenissen slechts vormen.

De time-out wordt toegepast op alle gebeurtenissen na de gebeurtenis **[!UICONTROL Wait]** activiteit. Als er geen gebeurtenis is ontvangen vóór de opgegeven time-out, gaan de personen naar één enkel time-outpad of beëindigen ze hun reis.

![](assets/event-timeout-group.png)
