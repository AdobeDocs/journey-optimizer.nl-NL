---
title: Configuratie webSDK voor inhoudskaarten
description: Ondersteuning voor inhoudskaarten configureren in Web SDK
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: bb67b55f-2eac-4775-a9f5-78288009477e
source-git-commit: 37862682a25843ce138c076e443f6d9b6229ece3
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Ondersteuning voor inhoudskaarten configureren in Web SDK {#content-card-configuration-sdk}

In dit voorbeeld ziet u hoe u inhoudskaarten kunt ophalen van Adobe Journey Optimizer (AJO) met Adobe Experience Platform. Door [&#x200B; SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/home) leveraging, wordt de verpersoonlijkingsinhoud opgehaald en volledig op de cliëntkant teruggegeven.

Als de pagina voor het eerst wordt geladen, wordt de standaardstatus van de pagina weergegeven. Nochtans, als u met de **Fondsen van de Aanhouding** of **Aandeel op sociale media** knopen in wisselwerking staat, zullen de extra inhoudskaarten verschijnen. Deze kaarten worden geactiveerd door omstandigheden aan de clientzijde, zodat ze alleen worden weergegeven wanneer specifieke handelingen worden uitgevoerd.

![](assets/content-card-web-1.png)

## Het voorbeeld uitvoeren {#run-sample}

>[!PREREQUISITES]
>
>U moet knooppunt en npm installeren. [&#x200B; verwijs naar deze documentatie &#x200B;](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)


1. Stel lokale SSL-certificaten in voor HTTPS. Voor deze voorbeelden zijn lokaal ondertekende SSL-certificaten vereist om inhoud via HTTPS te kunnen leveren:

   1. Installeer `mkcert` op de computer.

   1. Voer na de installatie `mkcert -install` uit om het `mkcert root` -certificaat te installeren.

1. Kloont de opslagplaats naar uw lokale computer.

1. Open een terminal en navigeer naar de map van het voorbeeld.

1. Installeer de vereiste afhankelijkheden door `npm install` uit te voeren.

1. Start de toepassing door `npm start` uit te voeren.

1. Open uw webbrowser en ga naar `https://localhost` .

## Werking {#setup}

1. Omvat en vorm [&#x200B; SDK van het Web &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/home) op de pagina gebruikend montages van het `.env` dossier in de steekproefomslag.

   ```
   <script src="https://cdn1.adoberesources.net/alloy/2.18.0/alloy.min.js" async></script>
   alloy("configure", {
       defaultConsent: "in",
       edgeDomain: "{{edgeDomain}}",
       edgeConfigId: "{{edgeConfigId}}",
       orgId:"{{orgId}}",
       debugEnabled: false,
       personalizationStorageEnabled: true,
       thirdPartyCookiesEnabled: false
   });
   ```

1. Gebruik de opdracht `sendEvent` om persoonlijke inhoud op te halen.

   ```
   alloy("sendEvent", {
       renderDecisions: true,
       personalization: {
           surfaces: ["web://alloy-samples.adobe.com/#content-cards-sample"],
       },
   });
   ```

1. Abonneren op inhoudskaarten voor een specifiek oppervlak met de opdracht `subscribeRulesetItems` . Telkens wanneer linialen worden geëvalueerd, handelt u het resultaatobject in de callback af. Deze bevat `propositions` met inhoudskaartgegevens.

   ```
   const contentCardManager = createContentCardManager("content-cards");
   
   alloy("subscribeRulesetItems", {
       surfaces: ["web://alloy-samples.adobe.com/#content-cards-sample"],
       schemas: ["https://ns.adobe.com/personalization/message/content-card"],
       callback: (result, collectEvent) => {
           const { propositions = [] } = result;
           contentCardManager.refresh(propositions, collectEvent);
       },
   });
   ```

1. Het renderen van inhoudskaarten beheren en `interact` - en `display` -gebeurtenissen verzenden met behulp van het `contentCardsManager` -object in `script.js` . Extraheer, sorteer en verwerkt inhoudskaarten van de ontvangen voorstellen.

   ```
   const createContentCard = (proposition, item) => {
       const { data = {}, id } = item;
       const {
           content = {},
           meta = {},
           publishedDate,
           qualifiedDate,
           displayedDate,
       } = data;
   
       return {
           id,
           ...content,
           meta,
           qualifiedDate,
           displayedDate,
           publishedDate,
           getProposition: () => proposition,
       };
   };
   
   const extractContentCards = (propositions) =>
       propositions
           .reduce((allItems, proposition) => {
           const { items = [] } = proposition;
   
           return [
               ...allItems,
               ...items.map((item) => createContentCard(proposition, item)),
           ];
       }, [])
       .sort(
           (a, b) =>
               b.qualifiedDate - a.qualifiedDate || b.publishedDate - a.publishedDate
       );
   
   const contentCards = extractContentCards(propositions);
   ```

1. Render de inhoudskaarten op de details worden gebaseerd die voor elke campagne worden bepaald. Elke kaart bevat een `title` , `body` , `imageUrl` en andere aangepaste gegevenswaarden.

   ```
   const renderContentCards = () => {
       const contentCardsContainer = document.getElementById(containerElementId);
       contentCardsContainer.addEventListener("click", handleContentCardClick);
   
       let contents = "";
   
       contentCards.forEach((card) => {
           const { id, title, body, imageUrl, meta = {} } = card;
           const { buttonLabel = "" } = meta;
   
           contents += `
               <div class="col">
                   <div data-id="${id}" class="card h-100">
                       <img src="${imageUrl}" class="card-img-top" alt="...">
                       <div class="card-body d-flex flex-column">
                           <h5 class="card-title">${title}</h5>
                           <p class="card-text">${body}</p>
                           <a href="#" class="mt-auto btn btn-primary">${buttonLabel}</a>
                       </div>
                   </div>
                </div>
            `;
       });
   
       contentCardsContainer.innerHTML = contents;
       collectEvent(
           "display",
           contentCards.map((card) => card.getProposition())
        );
   };
   ```

1. Wanneer de callback van `subscribeRulesetItems` wordt aangeroepen, wordt ook een gebruiksfunctie met de naam `collectEvent` opgegeven. Deze functie wordt gebruikt om Experience Edge-gebeurtenissen te verzenden om interacties, weergaven en andere gebruikersacties bij te houden. In dit voorbeeld volgt collectEvent wanneer op een inhoudskaart wordt geklikt. Als u bovendien op de knop op de inhoudskaart klikt, wordt de browser omgeleid naar de `actionUrl` die door de campagne is opgegeven.

   ```
   const handleContentCardClick = (evt) => {
       const cardEl = evt.target.closest(".card");
   
       if (!cardEl) {
           return;
       }
   
       const isAnchor = evt.target.nodeName === "A";
       const card = contentCards.find((card) => card.id === cardEl.dataset.id);
   
       if (!card) {
           return;
       }
   
       collectEvent("interact", [card.getProposition()]);
   
       if (isAnchor) {
           evt.preventDefault();
           evt.stopImmediatePropagation();
           const { actionUrl } = card;
           if (actionUrl && actionUrl.length > 0) {
               window.location.href = actionUrl;
           }
       }
   };
   ```

## Belangrijke opmerkingen {#key-observations}

### personalizationStorageEnabled

De optie `personalizationStorageEnabled` wordt ingesteld op `true` in de opdracht `configure` . Dit zorgt ervoor dat eerder gekwalificeerde inhoudskaarten worden opgeslagen en over gebruikerszittingen blijven worden getoond.

### Triggers

Inhoudskaarten ondersteunen aangepaste triggers die aan de clientzijde worden geëvalueerd. Wanneer aan een triggerregel wordt voldaan, worden extra inhoudskaarten weergegeven. In dit voorbeeld worden vier verschillende campagnes gebruikt, één voor elke inhoudskaart, die allemaal hetzelfde oppervlak delen: `web://alloy-samples.adobe.com/#content-cards-sample` . In de onderstaande tabel staan de triggerregels voor elke campagne en de manier waarop u hieraan kunt voldoen.

<table>
    <tr>
        <th>Triggerregel</th>
        <th>Kaart</th>
        <th>De triggerregel naleven</th>
    </tr>
    <tr>
        <td>Geen</td>
        <td><img src="assets/content-card-web-2.png"></td>
        <td>sendEvent, opdracht. Geen clientregel om tevreden te zijn.</td>
    </tr>
    <tr>
        <td>Geen</td>
        <td><img src="assets/content-card-web-3.png"></td>
        <td>sendEvent, opdracht. Geen clientregel om tevreden te zijn.</td>
    </tr>
    <tr>
        <td><img src="assets/content-card-web-4.png"></td>
        <td><img src="assets/content-card-web-5.png"></td>
        <td><img src="assets/content-card-web-6.png"></td>
    </tr>
    <tr>
        <td><img src="assets/content-card-web-7.png"></td>
        <td><img src="assets/content-card-web-8.png"></td>
        <td><img src="assets/content-card-web-9.png"></td>
    </tr>
</table>

De opdracht `evaluateRulesets` wordt geactiveerd wanneer u op de knoppen &quot;Stortingsfondsen&quot; en &quot;Delen op sociale media&quot; klikt. Elke knop geeft de relevante `decisionContext` aan om te voldoen aan de regels die voor de respectievelijke campagnes zijn gedefinieerd.

```
document.getElementById("action-button-1").addEventListener("click", () => {
    alloy("evaluateRulesets", {
        renderDecisions: true,
        personalization: {
            decisionContext: {
                action: "deposit-funds",
            },
        },
    });
});

document.getElementById("action-button-2").addEventListener("click", () => {
    alloy("evaluateRulesets", {
        renderDecisions: true,
        personalization: {
            decisionContext: {
                action: "social-media",
            },
        },
    });
});
```
