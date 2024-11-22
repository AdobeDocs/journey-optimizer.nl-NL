---
title: Op code gebaseerde implementatiemonsters
description: Op deze pagina staan voorbeelden van de implementatiemethode voor de op code gebaseerde Journey Optimizer-functie
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: bf0a6fa496a08348be16896a7f2313882eb97c06
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 1%

---

# Voorbeelden van op code gebaseerde implementatiemethoden {#implementation-samples}

De op code-gebaseerde ervaring steunt om het even welk type van klantenimplementatie. Op deze pagina kunt u steekproeven voor elke implementatiemethode vinden:

* [Client-kant](#client-side-implementation)
* [Server-kant](#server-side-implementation)
* [Hybride](#hybrid-implementation)

>[!IMPORTANT]
>
>Volg [ deze verbinding ](https://github.com/adobe/alloy-samples/tree/main/ajo) {target="_blank"} om steekproefimplementaties voor verschillende verpersoonlijking en het experimenteren gebruiksgevallen te vinden. Controleer hen uit en stel hen in werking om beter te begrijpen wat de implementatiestappen nodig zijn en hoe de verpersoonlijkingsstroom van begin tot eind werkt.

## Implementatie op de client {#client-side-implementation}

Als u een client-side implementatie hebt, kunt u een van de AEP client-SDK&#39;s gebruiken: AEP Web SDK of AEP Mobile SDK.

* De stappen [ beschrijven hieronder ](#client-side-how) het proces om de inhoud te halen die op de rand door de op code-gebaseerde ervaringstransporten en campagnes in een 3} implementatie wordt gepubliceerd van het steekproef **Web SDK {en het tonen van de gepersonaliseerde inhoud.**

* De stappen om code-gebaseerd kanaal uit te voeren gebruikend **Mobiele SDK** worden beschreven in [ dit leerprogramma ](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/) {target="_blank"}.

  >[!NOTE]
  >
  >De implementaties van de steekproef voor mobiele gebruiksgevallen zijn beschikbaar voor [ app van iOS ](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI) {target="_blank"} en [ app van Android ](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp) {target="_blank"}.

### Hoe het werkt - Web SDK {#client-side-how}

1. [ SDK van het Web ](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) {target="_blank"} is inbegrepen op de pagina.

1. U moet het `sendEvent` bevel gebruiken en de [ oppervlakte URI ](code-based-surface.md)<!--( or location/path)--> specificeren om verpersoonlijkingsinhoud te halen.

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. Op code-gebaseerde ervaringspunten zouden manueel door de implementatiecode (gebruikend de [`applyPersonalization` ](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js) {target="_blank"} methode) moeten worden toegepast om DOM bij te werken die op het besluit wordt gebaseerd.

1. Voor op code-gebaseerde ervaringsreizen en campagnes, moeten de vertoningsgebeurtenissen manueel worden verzonden om erop te wijzen wanneer de inhoud is getoond. Dit gebeurt via de opdracht `sendEvent` .

   ```javascript
   function sendDisplayEvent(decision) {
     const { id, scope, scopeDetails = {} } = decision;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionDisplay",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
           },
         },
       },
     });
   }
   ```

1. Voor op code-gebaseerde ervaringsreizen en campagnes, moeten de interactiegebeurtenissen manueel worden verzonden om erop te wijzen wanneer een gebruiker met de inhoud heeft gecommuniceerd. Dit gebeurt via de opdracht `sendEvent` .

   ```javascript
   function sendInteractEvent(label, proposition) {
     const { id, scope, scopeDetails = {} } = proposition;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionInteract",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
             propositionEventType: {
               interact: 1
             },
             propositionAction: {
               label: label
             },
           },
         },
       },
     });
   }
   ```

### Belangrijke opmerkingen

**Cookies**

Cookies worden gebruikt om de gebruikersidentiteit en clusterinformatie voort te zetten. Wanneer het gebruiken van een cliënt-zijimplementatie, behandelt het Web SDK het opslaan en het verzenden van deze koekjes automatisch tijdens de verzoeklevenscyclus.

| Cookie | Doel | Opgeslagen door | Verzonden door |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kCtr_AdobeOrg_identity | Bevat identiteitsgegevens van gebruiker | Web SDK | Web SDK |
| kndctr_AdobeOrg_cluster | Geeft aan met welke Edge-cluster aanvragen kunnen worden afgehandeld | Web SDK | Web SDK |

**plaatsing van het Verzoek**

Aanvragen aan de Adobe Experience Platform API zijn vereist om voorstellen te ontvangen en een weergavemelding te verzenden. Wanneer het gebruiken van een cliënt-zijimplementatie, doet het Web SDK deze verzoeken wanneer het `sendEvent` bevel wordt gebruikt.

| Verzoek | Door |
| ---------------------------------------------- | ----------------------------------- |
| interactief verzoek om voorstellen te krijgen | Web SDK met de opdracht sendEvent |
| interactief verzoek om weergavemeldingen te verzenden | Web SDK met de opdracht sendEvent |

**Diagram van de Stroom**

![](assets/code-based-client-side-implementation.png)

## Implementatie op de server {#server-side-implementation}

Als u een server-zijimplementatie hebt, kunt u één AEP Edge Network API gebruiken.

In de onderstaande stappen wordt beschreven hoe u de inhoud die op de rand van de code is gepubliceerd, ophaalt via een op code gebaseerde ervaringsreis en -campagne in een voorbeeldimplementatie van de Edge Network-API voor een webpagina en hoe u de gepersonaliseerde inhoud weergeeft.

### Werking

1. De webpagina wordt opgevraagd en cookies die eerder zijn opgeslagen door de browser die vooraf is ingesteld op `kndctr_` , worden opgenomen.
1. Wanneer de pagina van de toepassingsserver wordt gevraagd, wordt een gebeurtenis verzonden naar het [ interactieve eindpunt van de gegevensinzameling ](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html) om verpersoonlijkingsinhoud te halen. Deze steekproef app maakt gebruik van sommige helpermethodes om het bouwen en het verzenden van verzoeken naar API (zie [ aepEdgeClient.js ](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js) te vereenvoudigen {target="_blank"}). Maar de aanvraag is gewoon een `POST` met een payload die een gebeurtenis en query bevat. De cookies (indien beschikbaar) uit de voorgaande stap worden opgenomen in de aanvraag in de array `meta>state>entries` .

   ```javascript
   fetch(
     "https://edge.adobedc.net/ee/v2/interact?dataStreamId=abc&requestId=123",
     {
       headers: {
         accept: "*/*",
         "accept-language": "en-US,en;q=0.9",
         "cache-control": "no-cache",
         "content-type": "text/plain; charset=UTF-8",
         pragma: "no-cache",
         "sec-fetch-dest": "empty",
         "sec-fetch-mode": "cors",
         "sec-fetch-site": "cross-site",
         "sec-gpc": "1",
         "Referrer-Policy": "strict-origin-when-cross-origin",
         Referer: "https://localhost/",
       },
       body: JSON.stringify({
         event: {
           xdm: {
             eventType: "decisioning.propositionFetch",
             web: {
               webPageDetails: {
                 URL: "https://localhost/",
               },
               webReferrer: {
                 URL: "",
               },
             },
             identityMap: {
               FPID: [
                 {
                   id: "xyz",
                   authenticatedState: "ambiguous",
                   primary: true,
                 },
               ],
             },
             timestamp: "2022-06-23T22:21:00.878Z",
           },
           data: {},
         },
         query: {
           identity: {
             fetch: ["ECID"],
           },
           personalization: {
             schemas: [
               "https://ns.adobe.com/personalization/default-content-item",
               "https://ns.adobe.com/personalization/html-content-item",
               "https://ns.adobe.com/personalization/json-content-item",
               "https://ns.adobe.com/personalization/redirect-item",
               "https://ns.adobe.com/personalization/dom-action",
             ],
             surfaces: ["web://localhost/","web://localhost/#sample-json-content"],
           },
         },
         meta: {
           state: {
             domain: "localhost",
             cookiesEnabled: true,
             entries: [
               {
                 key: "kndctr_XXX_AdobeOrg_identity",
                 value: "abc123",
               },
               {
                 key: "kndctr_XXX_AdobeOrg_cluster",
                 value: "or2",
               },
             ],
           },
         },
       }),
       method: "POST",
     }
   ).then((res) => res.json());
   ```

1. De JSON-ervaring van de op code gebaseerde ervaringstransporten en -campagne wordt gelezen uit de reactie en gebruikt bij het produceren van de HTML-respons.

1. Voor op code-gebaseerde ervaringsreizen en campagnes, moeten de vertoningsgebeurtenissen in de implementatie manueel worden verzonden om erop te wijzen wanneer de reis of campagneinhoud is getoond. In dit voorbeeld wordt het bericht tijdens de levenscyclus van de aanvraag naar de server verzonden.

   ```javascript
   function sendDisplayEvent(aepEdgeClient, req, propositions, cookieEntries) {
     const address = getAddress(req);
   
     aepEdgeClient.interact(
       {
         event: {
           xdm: {
             web: {
               webPageDetails: { URL: address },
               webReferrer: { URL: "" },
             },
             timestamp: new Date().toISOString(),
             eventType: "decisioning.propositionDisplay",
             _experience: {
               decisioning: {
                 propositions: propositions.map((proposition) => {
                   const { id, scope, scopeDetails } = proposition;
   
                   return {
                     id,
                     scope,
                     scopeDetails,
                   };
                 }),
               },
             },
           },
         },
         query: { identity: { fetch: ["ECID"] } },
         meta: {
           state: {
             domain: "",
             cookiesEnabled: true,
             entries: [...cookieEntries],
           },
         },
       },
       {
         Referer: address,
       }
     );
   }
   ```

1. Wanneer de HTML-reactie wordt geretourneerd, worden de identiteits- en clustercookies ingesteld op de reactie van de toepassingsserver.

### Belangrijke opmerkingen

**Cookies**

Cookies worden gebruikt om de gebruikersidentiteit en clusterinformatie voort te zetten. Wanneer u een serverimplementatie gebruikt, moet de toepassingsserver de opslag en verzending van deze cookies tijdens de levenscyclus van de aanvraag afhandelen.

| Cookie | Doel | Opgeslagen door | Verzonden door |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kCtr_AdobeOrg_identity | Bevat identiteitsgegevens van gebruiker | toepassingsserver | toepassingsserver |
| kndctr_AdobeOrg_cluster | Geeft aan met welke Edge-cluster aanvragen kunnen worden afgehandeld | toepassingsserver | toepassingsserver |

**plaatsing van het Verzoek**

Aanvragen aan de Adobe Experience Platform API zijn vereist om voorstellen te ontvangen en een weergavemelding te verzenden. Wanneer het gebruiken van een cliënt-zijimplementatie, doet het Web SDK deze verzoeken wanneer het `sendEvent` bevel wordt gebruikt.

| Verzoek | Door |
| ---------------------------------------------- | ------------------------------------------------------------ |
| interactief verzoek om voorstellen te krijgen | toepassingsserver die de Adobe Experience Platform API aanroept |
| interactief verzoek om weergavemeldingen te verzenden | toepassingsserver die de Adobe Experience Platform API aanroept |

**Diagram van de Stroom**

![](assets/code-based-server-side-implementation.png)

## Hybride implementatie {#hybrid-implementation}

Als u een hybride implementatie hebt, checkt u de onderstaande koppelingen uit.

* Tech Blog van de Adobe: [ Hybride Personalization in het Web SDK van Adobe Experience Platform ](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41) {target="_blank"}
* De Documentatie van SDK: [ Hybride verpersoonlijking die Web SDK en de Server API van de Edge Network gebruiken ](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html) {target="_blank"}
