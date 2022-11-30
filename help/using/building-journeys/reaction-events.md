---
solution: Journey Optimizer
product: journey optimizer
title: Gebeurtenissen van Reacties
description: Meer informatie over reacties
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 9b7898d0fe008a0e7ef711b1303230c6f901b712
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 3%

---

# Reactiegebeurtenissen {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Reactiegebeurtenissen"
>abstract="Met deze activiteit kunt u reageren op volggegevens die betrekking hebben op een bericht dat binnen dezelfde reis wordt verzonden. We leggen deze informatie in real time vast op het moment dat ze met Adobe Experience Platform wordt gedeeld."

De ingebouwde **[!UICONTROL Reactions]** gebeurtenis. Met deze activiteit kunt u reageren op volggegevens die betrekking hebben op een bericht dat binnen dezelfde reis wordt verzonden. We leggen deze informatie in real time vast op het moment dat ze met Adobe Experience Platform wordt gedeeld.

U kunt reageren op geklikte of geopende berichten.

U kunt dit mechanisme ook gebruiken om een actie uit te voeren wanneer er geen reactie op uw berichten is. Hiertoe maakt u een tweede pad parallel aan de reactieactiviteit en voegt u een wachtactiviteit toe. Als er geen reactie optreedt tijdens de periode die is gedefinieerd in de wachtdienst, wordt het tweede pad gekozen. U kunt bijvoorbeeld een vervolgbericht verzenden.

Let op: u kunt een reactieactiviteit alleen gebruiken op het canvas als er al eerder een kanaalactieactiviteit is (E-mail en push).

Zie [Informatie over actieactiviteiten](../building-journeys/about-journey-activities.md#action-activities).

![](assets/journey45.png)

Hier volgen de verschillende stappen voor het configureren van reactiegebeurtenissen:

1. Voeg een **[!UICONTROL Label]** op de reactie. Deze stap is optioneel.
1. Selecteer in de vervolgkeuzelijst de activiteit waarop u wilt reageren. U kunt alle handelingen selecteren die zich in de vorige stappen van het pad bevinden.
1. Afhankelijk van de actie die u hebt geselecteerd, kiest u waarop u wilt reageren.
1. U kunt een time-out voor de gebeurtenis (tussen 40 seconden en 30 dagen) en een time-outpad definiëren. Hierdoor wordt een tweede pad gemaakt voor personen die niet binnen de gedefinieerde tijdsduur hebben gereageerd. Bij het testen van een traject waarbij een reactiegebeurtenis wordt gebruikt, de testmodus **[!UICONTROL Wait time]** standaard en minimumwaarde is 40 seconden. Zie [deze sectie](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>
>Reactiegebeurtenissen kunnen geen berichten bijhouden die op een andere reis plaatsvinden.
>
>In de gebeurtenissentrack van Reaction wordt geklikt op koppelingen van het type &quot;bijgehouden&quot;. Er wordt geen rekening gehouden met abonnements- en spiegelpaginakoppelingen.

>[!IMPORTANT]
>
>E-mailclients zoals Gmail staan het blokkeren van afbeeldingen toe. E-mails die worden geopend, worden bijgehouden met een afbeelding van 0 pixels die in de e-mail is opgenomen. Als afbeeldingen worden geblokkeerd, wordt er geen rekening gehouden met het openen van e-mail.
