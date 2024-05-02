---
solution: Journey Optimizer
product: journey optimizer
title: Algemene gebeurtenissen
description: Leer hoe u algemene gebeurtenissen kunt gebruiken
feature: Journeys, Events
topic: Content Management
role: User
level: Intermediate
keywords: aangepast, algemeen, evenementen, reizen
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '537'
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

De reis zal dan aan de gebeurtenis tijdens de tijd luisteren die in de timeout wordt gespecificeerd. Als een gebeurtenis tijdens die periode wordt ontvangen, zal de persoon in de gebeurtenisweg stromen. Als niet, zal de klant of in de onderbrekingspad stromen als het wordt bepaald, of zal die reis voortzetten.

Als er geen time-outpad is gedefinieerd, fungeert de time-outinstelling als een wachtbewerking. Het profiel wordt dan gedurende een bepaalde periode gewacht. Dit kan worden gestopt als een gebeurtenis plaatsvindt vóór het einde van die wachttijd. Als u profielen van die reis na onderbreking wilt worden uitgesloten, zult u een onderbrekingspad moeten plaatsen.

Voer de volgende stappen uit om een time-out voor een gebeurtenis te configureren:

1. Activeer **[!UICONTROL Define the event timeout]** van de eigenschappen van de gebeurtenis.

1. Geef op hoeveel tijd de reis moet wachten op de gebeurtenis. De maximale duur is 29 dagen.

1. Als u de personen naar een time-outpad wilt sturen wanneer er geen gebeurtenis is ontvangen binnen de opgegeven time-out, schakelt u de optie **[!UICONTROL Set a timeout path]** -optie. Als deze optie niet wordt ingeschakeld, wordt de reis voor de persoon voortgezet zodra de time-out is bereikt. We raden u aan om de **Een time-outpad instellen** -optie.

   ![](assets/event-timeout.png)

In dit voorbeeld stuurt de reis een eerste welkomstmail naar een klant nadat hij/zij de lobby is binnengekomen. Het verzendt dan een e-mail van de maaltijdkorting slechts als de klant het restaurant binnen de volgende dag ingaat. Daarom hebben we de restaurant-gebeurtenis geconfigureerd met een time-out van 1 dag:

* Als de restaurantgebeurtenis minder dan 1 dag na de welkomstmail wordt ontvangen, wordt de e-mail met maaltijdkorting verzonden.
* Als er de volgende dag geen restaurantgebeurtenis wordt ontvangen, loopt de persoon door het time-outpad.

Merk op dat als u een onderbreking op veelvoudige gebeurtenissen wilt vormen die na een **[!UICONTROL Wait]** activiteit, moet u de onderbreking op één van deze gebeurtenissen slechts vormen.

De gedefinieerde time-out is van toepassing op alle gebeurtenissen na de **[!UICONTROL Wait]** activiteit:

* Als één gebeurtenis binnen de time-outduur wordt weergegeven, loopt de afzonderlijke gebeurtenis door naar het pad van de ontvangen gebeurtenis.
* Als er geen gebeurtenis wordt ontvangen binnen de tijdsduur van de time-out, loopt de afzonderlijke gebeurtenis door naar de time-outvertakking van de gebeurtenis waar de time-out is gedefinieerd.

![](assets/event-timeout-group.png)
