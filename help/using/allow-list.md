---
title: Lijst van gewenste personen
description: Leer hoe u de lijst van gewenste personen gebruikt.
feature: Leverbaarheid
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: 288c27d4fc64a6d0a6f07b634ed044a6e858d0c1
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 1%

---

# Lijst van gewenste personen {#allow-list}

Het is nu mogelijk om een specifieke het verzenden-veilige lijst op het [zandbak](administration/sandboxes.md) niveau te bepalen, om een veilige milieu voor testend doel te hebben. Op een niet-productiegeval, waar de fouten kunnen voorkomen, verzekert de lijst van gewenste personen u geen risico om ongewenste berichten naar uw klanten te verzenden.

>[!CAUTION]
>
>Deze functie is niet beschikbaar voor productiesandboxen.

Met de lijst van gewenste personen kunt u afzonderlijke e-mailadressen of domeinen opgeven die de enige ontvangers of domeinen zijn die geautoriseerd zijn om de e-mails te ontvangen die u vanuit een specifieke sandbox verzendt. Dit kan voorkomen dat u per ongeluk e-mailberichten naar de adressen van de echte klant stuurt wanneer u zich in een testomgeving bevindt.

>[!NOTE]
>
>Deze functie is alleen van toepassing op het e-mailkanaal.

## De lijst van gewenste personen inschakelen {#enable-allow-list}

Om de lijst van gewenste personen op een niet productiesandbox toe te laten, moet u een Adobe API vraag maken.

* Met deze API kunt u de functie ook op elk gewenst moment uitschakelen.

* U kunt de lijst van gewenste personen bijwerken voor of na het inschakelen van de functie.

* De logica van de lijst van gewenste personen is van toepassing wanneer de functie is ingeschakeld en als de lijst van gewenste personen niet leeg is. Meer informatie vindt u in [deze sectie](#logic).

>[!NOTE]
>
>Als deze optie is ingeschakeld, wordt de functie lijst van gewenste personen gerespecteerd bij het uitvoeren van reizen, maar ook bij het testen van berichten met [proefdrukken](preview.md#send-proofs) en het testen van reizen met de [testmodus](building-journeys/testing-the-journey.md).

## Entiteiten toevoegen aan de lijst van gewenste personen {#add-entities}

>[!CAUTION]
>
>Deze functie is **niet** beschikbaar op productiestanddozen. Dit is alleen van toepassing op e-mailkanalen.

Als u nieuwe e-mailadressen of domeinen wilt toevoegen aan de lijst van gewenste personen voor een specifieke sandbox, moet u de API voor onderdrukking aanroepen met de waarde `ALLOWED` voor het kenmerk `listType`. Bijvoorbeeld:

![](assets/allow-list-api.png)

U kunt de bewerkingen **Add**, **Delete** en **Get** uitvoeren.

>[!NOTE]
>
>De lijst van gewenste personen kan maximaal 1.000 items bevatten.

Leer meer bij het maken van Adobe API vraag in [Experience Platform documentatie](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).

## Lijst van gewenste personen-logica {#logic}

<!-- When the allowed list is \[enabled\]\(\add link here\) at the sandbox level using the API call above, the following applies.-->

1. Wanneer de lijst van gewenste personen **empty** is, wordt de logica van de lijst van gewenste personen niet toegepast. Dit betekent dat u e-mailberichten naar profielen kunt verzenden, op voorwaarde dat deze niet voorkomen in de [suppressielijst](suppression-list.md).

1. Wanneer de lijst van gewenste personen **niet leeg** is, wordt de logica van de lijst van gewenste personen toegepast:

   * Als een entiteit **niet op de lijst van gewenste personen**, en niet op de onderdrukkingslijst is, zal de overeenkomstige ontvanger niet de e-mail ontvangen, de reden is **[!UICONTROL Not allowed]**.

   * Als een entiteit **op de lijst van gewenste personen**, en niet op de onderdrukkingslijst is, kan e-mail naar de overeenkomstige ontvanger worden verzonden. Als de entiteit zich echter ook op de [suppressielijst](suppression-list.md) bevindt, zal de overeenkomstige ontvanger de e-mail niet ontvangen, omdat **[!UICONTROL Suppressed]**.




