---
solution: Journey Optimizer
product: journey optimizer
title: Automatisch genereren van inhoudsvarianten (Beta)
description: Leer hoe u inhoudsvarianten automatisch kunt genereren met behulp van op AI gebaseerde simulatie.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="Private bèta" type="Informative"
hidefromtoc: true
hide: true
source-git-commit: 53d8fbb28e8516e4ee79f556a335b2d084af42e7
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---


# Automatisch genereren van inhoudsvarianten (Beta){#auto-generate-variants}

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in **privé bèta** en kan niet in uw milieu beschikbaar zijn. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

[!DNL Journey Optimizer] introduceert op AI gebaseerde simulatie die automatisch meerdere varianten kan genereren om uw inhoud te testen. Met deze functie vermindert u de noodzaak om handmatig varianten te maken, waardoor het gemakkelijker wordt om aanpassingslogica in complexe sjablonen te valideren.

Wanneer het teruggeven van inhoud voor simulatie of het proef, analyseert het systeem uw inhoud en identificeert alle verpersoonlijkingstokens en vertakkende regels. Deze vervangt personalisatietokens door betekenisvolle waarden die een vrijwel realistische voorvertoning van de uiteindelijke inhoud bieden.

Overweeg een e-mailmalplaatje van de financiële diensten met vertakkende logica die op **wordt gebaseerd investeringstype**, **leeftijdsgroep**, **burgerlijke status**, **controle van fiscale identiteitskaart**, en **plaats**. Zonder het genereren van varianten moet u handmatig tientallen varianten maken om alle paden te valideren. Met automatisch gegenereerde varianten produceert het systeem representatieve varianten die deze voorwaarden automatisch dekken.  Elke gegenereerde variant wordt weergegeven in het voorvertoningsvenster en geeft precies aan welke blokken en voorwaarden zijn toegepast.

## Inhoudsvarianten genereren

Ga als volgt te werk om variaties voor uw inhoud te genereren en deze voor te vertonen:

1. Open de inhoud en selecteer **[!UICONTROL Simulate content]** / **[!UICONTROL Simulate content variations]** .

   ![](assets/simulate-sample.png)

2. Klik op de knop **[!UICONTROL Generate]**.

   ![](assets/simulate-generate-variant.png)

3. [!DNL Journey Optimizer] genereert automatisch varianten op basis van gedetecteerde kenmerken.

4. Controleer de lijst met gegenereerde varianten in het linkerdeelvenster en selecteer een variant om de gepersonaliseerde rendering weer te geven in het voorvertoningsvenster.

>[!NOTE]
>
>Deze functie werkt op dezelfde manier als de standaardfunctie voor het simuleren van inhoudsvariaties. Voor meer informatie over de simulaties van inhoudsvariaties en de bijbehorende guardrails en beperkingen, verwijs naar deze sectie: [&#x200B; simuleer inhoudsvariaties &#x200B;](../test-approve/simulate-sample-input.md)
