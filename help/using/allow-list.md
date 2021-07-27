---
title: Lijst van gewenste personen
description: Leer hoe u de lijst van gewenste personen gebruikt.
feature: Leverbaarheid
topic: Contentmanagement
role: User
level: Intermediate
source-git-commit: 2d03285400b86b2c296997537852bb89ae0f6d0a
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---

# Lijst van gewenste personen {#allow-list}

Het is nu mogelijk om een specifieke het verzenden-veilige lijst op het [zandbak](administration/sandboxes.md) niveau te bepalen, om een veilige milieu voor testend doel te hebben. Op een niet-productiegeval, waar de fouten kunnen voorkomen, verzekert de lijst van gewenste personen u geen risico om ongewenste berichten naar uw klanten te verzenden.

Met de lijst van gewenste personen kunt u afzonderlijke e-mailadressen of domeinen opgeven die de enige ontvangers of domeinen zijn die geautoriseerd zijn om de e-mails te ontvangen die u vanuit een specifieke sandbox verzendt. Dit kan voorkomen dat u per ongeluk e-mailberichten naar de adressen van de echte klant stuurt wanneer u zich in een testomgeving bevindt.


>[!CAUTION]
>
>Deze functie is **niet** beschikbaar op productiestanddozen. Dit is alleen van toepassing op e-mailkanalen.


## De lijst van gewenste personen inschakelen {#enable-allow-list}

Als u de lijst van gewenste personen wilt inschakelen in een niet-productiesandbox, werkt u de lijst van gewenste personen bij zodat deze niet langer leeg is. Als u de functie wilt uitschakelen, maakt u de lijst leeg.

<!--
you need to make an Adobe API call.

* Using this API, you can also disable the feature at any time.

* You can update the allowed list before or after enabling the feature.

* The allowed list logic applies when the feature is enabled and if the allowed list is not empty. Learn more in [this section](#logic).

-->
>[!NOTE]
>
>Als deze optie is ingeschakeld, wordt de functie lijst van gewenste personen gerespecteerd bij het uitvoeren van reizen, maar ook bij het testen van berichten met [proefdrukken](preview.md#send-proofs) en het testen van reizen met de [testmodus](building-journeys/testing-the-journey.md).

## Entiteiten toevoegen aan de lijst van gewenste personen {#add-entities}

Als u nieuwe e-mailadressen of domeinen wilt toevoegen aan de lijst van gewenste personen voor een specifieke sandbox, moet u de API voor onderdrukking aanroepen met de waarde `ALLOWED` voor het kenmerk `listType`. Bijvoorbeeld:

![](assets/allow-list-api.png)

U kunt de bewerkingen **Add**, **Delete** en **Get** uitvoeren.

>[!NOTE]
>
>De lijst van gewenste personen kan maximaal 1.000 items bevatten.

<!--
Learn more on making Adobe API calls in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).
-->


## Lijst van gewenste personen-logica {#logic}

<!-- When the allowed list is [enabled](#enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Wanneer de lijst van gewenste personen **empty** is, wordt de logica van de lijst van gewenste personen niet toegepast. Dit betekent dat u e-mailberichten naar profielen kunt verzenden, op voorwaarde dat deze niet voorkomen in de [suppressielijst](suppression-list.md).

Wanneer de lijst van gewenste personen **niet leeg** is, wordt de logica van de lijst van gewenste personen toegepast:

* Als een entiteit **niet op de lijst van gewenste personen**, en niet op de onderdrukkingslijst is, zal de overeenkomstige ontvanger niet de e-mail ontvangen, de reden is **[!UICONTROL Not allowed]**.

* Als een entiteit **op de lijst van gewenste personen**, en niet op de onderdrukkingslijst is, kan e-mail naar de overeenkomstige ontvanger worden verzonden. Als de entiteit zich echter ook op de [suppressielijst](suppression-list.md) bevindt, zal de overeenkomstige ontvanger de e-mail niet ontvangen, omdat **[!UICONTROL Suppressed]**.




