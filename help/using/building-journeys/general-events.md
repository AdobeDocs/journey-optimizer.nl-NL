---
solution: Journey Orchestration
title: Algemene gebeurtenissen
description: Leer hoe u algemene gebeurtenissen kunt gebruiken
feature: Journeys
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: 285942ec51859a4cea888d9974f79f52acf3aabf
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 2%

---

# Algemene gebeurtenissen {#section_ofg_jss_dgb}

Voor dit type gebeurtenis kunt u alleen een label en een beschrijving toevoegen. De rest van de configuratie kan niet worden bewerkt. Het werd uitgevoerd door de technische gebruiker. Zie [deze pagina](../event/about-events.md).

![](../assets/general-events.png)

Wanneer u een bedrijfsgebeurtenis laat vallen, voegt het automatisch een **Leessegment** activiteit toe. Raadpleeg [deze sectie](../event/about-events.md) voor meer informatie over bedrijfsgebeurtenissen

## Luisteren naar gebeurtenissen tijdens een bepaald tijdstip {#events-specific-time}

Een gebeurtenisactiviteit die in de reis wordt geplaatst luistert voor onbepaalde tijd naar gebeurtenissen. Als u alleen tijdens een bepaalde tijd naar een gebeurtenis wilt luisteren, moet u een time-out voor de gebeurtenis configureren.

De reis zal dan aan de gebeurtenis tijdens de tijd luisteren die in de timeout wordt gespecificeerd. Als een gebeurtenis tijdens die periode wordt ontvangen, zal de persoon in de gebeurtenisweg stromen. Als niet, zal de klant of in een onderbrekingspad stromen, of zijn reis beëindigen.

Voer de volgende stappen uit om een time-out voor een gebeurtenis te configureren:

1. Activeer de optie **[!UICONTROL Define the event timeout]** uit de eigenschappen van de gebeurtenis.

1. Geef op hoeveel tijd de reis moet wachten op de gebeurtenis.

1. Schakel de optie **[!UICONTROL Set a timeout path]** in als u de personen naar een time-outpad wilt sturen wanneer er geen gebeurtenis binnen de opgegeven time-out is ontvangen. Als deze optie niet wordt ingeschakeld, eindigt de reis voor het individu zodra de time-out is bereikt.

   ![](../assets/event-timeout.png)

In dit voorbeeld, verzendt de reis een eerste welkome duw naar een klant. Het verzendt dan een duw van de maaltijdkorting slechts als de klant het restaurant binnen de volgende dag ingaat. Daarom hebben we de restaurant-gebeurtenis geconfigureerd met een time-out van 1 dag:

* Als de restaurantgebeurtenis minder dan 1 dag na de welkomstpush wordt ontvangen, wordt de pushactiviteit voor de maaltijdkorting verzonden.
* Als er de volgende dag geen restaurantgebeurtenis wordt ontvangen, loopt de persoon door het time-outpad.

Merk op dat als u een onderbreking op veelvoudige gebeurtenissen wilt vormen die na een **[!UICONTROL Wait]** activiteit worden geplaatst, u de onderbreking op één van deze gebeurtenissen slechts moet vormen.

De time-out wordt toegepast op alle gebeurtenissen die na de activiteit **[!UICONTROL Wait]** worden geplaatst. Als er geen gebeurtenis is ontvangen vóór de opgegeven time-out, gaan de personen naar één enkel time-outpad of beëindigen ze hun reis.

![](../assets/event-timeout-group.png)
