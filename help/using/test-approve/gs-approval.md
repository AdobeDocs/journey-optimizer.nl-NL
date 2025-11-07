---
title: Aan de slag met reizen en campagnes goedkeuren
description: Leer hoe u een goedkeuringsproces instelt voor uw reizen en campagnes.
role: User
level: Beginner
feature: Approval
exl-id: 92d1439e-5cac-4e7d-85f8-ebf432e9ef7c
source-git-commit: efb943e5a6f27becc6e8b6128b776e46d6141823
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Aan de slag met reizen en campagnes goedkeuren {#send-proofs}

## Aan de slag met goedkeuringsbeleid {#gs}

Met Journey Optimizer kunt u een goedkeuringsproces instellen waarmee marketingteams kunnen garanderen dat campagnes en reizen worden gecontroleerd en afgemeld door de relevante belanghebbenden voordat ze live gaan.

Het goedkeuringsbeleid introduceert een gestructureerde werkstroom direct binnen het gebruikersinterface, die de behoefte aan externe media zoals e-mail of taakbeheersinstrumenten elimineert, en ervoor zorgt dat alle goedkeuringen centraal worden beheerd en worden gevolgd.

Bovendien biedt deze functie een betere controle op de publicatie van uw reizen en campagnes: met het goedkeuringsproces dat in Journey Optimizer is ingebed, blijven campagnes en reizen tijdens de herziening vergrendeld, zodat er geen wijzigingen of onbedoelde activeringen plaatsvinden voordat alle noodzakelijke goedkeuringen zijn ingesteld.

## Vereisten {#prerequisites}

Voordat u begint, moet u controleren of de onderstaande machtigingen zijn geconfigureerd.

Om toegang te hebben keur en publiceer reizen en campagnes goed, moeten de gebruikers **worden verleend goedkeuren en publiceer Campagnes** en **goedkeuren en publiceren de toestemmingen van de Reizen**. [Meer informatie](../administration/permissions.md)

+++  Leer hoe u machtigingen voor goedkeuring toewijst

1. In het **product van Toestemmingen**, ga naar het **lusje van Rollen** en selecteer de gewenste **Rol**.

1. Klik **uitgeven** om de toestemmingen te wijzigen.

1. Voeg het **middel van Campagnes** toe, dan uitgezocht **goedkeuren en publiceer Campagnes** van het drop-down menu.

   ![](assets/permissions_approval.png){zoomable="yes"}

1. Voeg het **1} middel van de Reizen {toe, dan uitgezocht** goedkeuren en publiceer Reizen **van het drop-down menu.**

   ![](assets/permissions_approval_2.png){zoomable="yes"}

1. Klik **sparen** om veranderingen toe te passen.

Voor alle gebruikers die al zijn toegewezen aan deze rol, worden hun machtigingen automatisch bijgewerkt.

1. Om deze rol aan nieuwe gebruikers toe te wijzen, navigeer aan het **lusje van Gebruikers** binnen het **dashboard van Rollen** en klik **toevoegen Gebruiker**.

1. Ga de naam van de gebruiker, e-mailadres in, of kies van de lijst, dan klik **sparen**.

1. Als de gebruiker niet eerder werd gecreeerd, verwijs naar [ deze documentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users).

De gebruiker ontvangt een e-mail met instructies om toegang te krijgen tot uw exemplaar.

+++

## Overzicht van goedkeuringsproces {#process}

Het algemene goedkeuringsproces is als volgt:

![](assets/approval-process.png){zoomable="yes"}

1. **opstelling van het beleid van de Goedkeuring**

   Beheerders voeren een goedkeuringsbeleid waarin de voorwaarden worden gedefinieerd waaronder het beleid op reizen of campagnes van toepassing is. U kunt bijvoorbeeld een goedkeuringsbeleid maken dat vereist dat alle geplande campagnes die door een bepaalde gebruiker zijn gemaakt, worden goedgekeurd voordat ze worden geactiveerd. [ leer hoe te om goedkeuringsbeleid ](approval-policies.md) tot stand te brengen

1. **Campagne/reis voorlegging voor goedkeuring**

   De makers van de campagne/reis bouwen een reis of campagne en leggen deze ter goedkeuring voor. De campagne/reis gaat een &quot;in Herziening&quot;staat in, waarin geen veranderingen kunnen worden aangebracht tenzij het verzoek wordt geannuleerd. [ Leer hoe te om goedkeuring ](request-approval.md) te verzoeken

   >[!NOTE]
   >
   >Campagnes en reizen hoeven alleen ter goedkeuring te worden voorgelegd als er een goedkeuringsbeleid bestaat. Als een dergelijk beleid niet van toepassing is, kan de maker de campagne of de reis rechtstreeks publiceren zonder dat daarvoor goedkeuring nodig is.

1. **Overzicht en goedkeuring**

   De fiatteur(s) die is (zijn) gedefinieerd in het goedkeuringsbeleid dat van toepassing is op de reis of campagne, ontvangt (ontvangen) een kennisgeving. Ze kunnen de inhoud, het publiek en de instellingen van de reis of campagne bekijken. Als er wijzigingen nodig zijn, vraagt de fiatteur om deze en retourneert hij de campagne naar &quot;Concept&quot; voor revisies. Als ze klaar zijn, kunnen ze de reis of campagne activeren en starten. [ leer hoe te om een verzoek ](review-approve-request.md) te herzien en goed te keuren

## Goedkeuringsaanvragen controleren {#monitor}

U kunt alle goedkeurings- en wijzigingsverzoeken controleren die voor een bepaalde reis of campagne zijn ingediend. Klik hiertoe op het pictogram **[!UICONTROL Show Audit Trail]** in de rechterbovensectie van het canvas of het scherm voor het reviseren van de campagne.

![](assets/monitor-requests.png)

## Aanvullende bronnen

* **[creeer goedkeuringsbeleid](approval-policies.md)** - leer hoe te opstelling goedkeuringsbeleid om overzichtswerkschema&#39;s voor campagnes en reizen af te dwingen.
* **[Goedkeuring van het Verzoek](request-approval.md)** - begrijp hoe te om inhoud voor goedkeuring en de status van de spoorgoedkeuring voor te leggen.
* **[Overzicht en keurt verzoeken](review-approve-request.md)** goed - ontdek hoe te, goedkeurt of goedkeurt goedkeuringsverzoeken als fiatteur.
* **[Simuleer met steekproefinput](simulate-sample-input.md)** - leer hoe te om inhoud te testen en te bevestigen gebruikend de gegevens van het steekproefprofiel.
