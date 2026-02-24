---
solution: Journey Optimizer
product: journey optimizer
title: Mobiel en web instellen
description: Leer hoe u mobiele en webkanalen kunt configureren en controleren
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: kanaal, oppervlak, technisch, parameters, optimalisator
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: 7cca968a161a26d0af385a028c4404261088f033
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 3%

---

# Aan de slag met de instelling van het kanaal met instructies {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Naam van mobiele en webconfiguratie"
>abstract="Voer de naam in van uw mobiele of webconfiguratie. Deze naam zal voor elk middel automatisch worden gebruikt die met de Geleide Opstelling van het Kanaal wordt gecreeerd."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Valideren met Assurance"
>abstract="Adobe Experience Platform Assurance is ingesloten in deze workflow om u te helpen uw SDK-implementatie te controleren en toepassingsgebeurtenissen te simuleren en te valideren."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home" text="Adobe Experience Platform Assurance - Overzicht"

**Geleide Opstelling van het Kanaal** is een gestroomlijnde werkschema in Adobe Journey Optimizer die u snel mobiele en Web marketing kanalen helpt vormen. Het leeft onder **Beleid** > **Kanalen** > **configuratie van het Kanaal** en automatiseert de verwezenlijking van essentiële middelen-zulke zoals markeringseigenschappen, gegevensstromen, en kanaal configuratie-over Adobe Experience Platform, Journey Optimizer, en de Inzameling van Gegevens. In plaats van elke component handmatig te configureren, volgt u een geleide workflow die alles voor u instelt, zodat uw marketingteam zonder vertraging In-app-berichten, pushmeldingen en webervaringen kan gaan maken.

De instelling van het kanaal met instructies ondersteunt de volgende platforms en kanalen.

* Platforms en SDK&#39;s:

   * Swift door Apple, iOS

   * Kotlin, Android

   * JavaScript, web

* Kanalen:

   * Mobiele in-app

   * Mobiel pushbericht

   * Web Basic


Merk op dat voor elk platform dat u zou willen opstelling, het wordt vereist om een afzonderlijke configuratie tot stand te brengen. Dit komt omdat elke toepassing een unieke kanaalconfiguratie vereist, en dit verstrekt de flexibiliteit om te bepalen welke kanalen u voor elk platform zou willen.

## Vereisten {#prereq}

* Om dit effectief te kunnen uitvoeren, is het van essentieel belang dat een lid van de organisatie met de bevoegdheid en technische capaciteit om website of mobiele code te wijzigen toezicht houdt op de installatie.

  Hieronder vindt u de machtigingen die vereist zijn om de instelling van het kanaal met instructies uit te voeren.

  +++ Vereiste machtigingen

  <table>
    <thead>
      <tr>
        <th><strong>Oplossing</strong></th>
        <th><strong>Machtigingen</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          <p>Dataverzameling</p>
        </td>
        <td>
          <ul>
            <li>Bedrijfsrechten &gt; Eigenschappen</li>
            <li>Eigenschappenrechten: extensies en omgevingen ontwikkelen, publiceren, beheren</li>
            <li>Toepassingsoppervlakken: toepassingsconfiguratie beheren</li>
         </ul>
        </td>
      </tr>
      <tr>
        <td>
          <p>Adobe Experience Platform</p>
        </td>
        <td>
        <ul>
            <li>Gegevensverzameling: gegevensstromen beheren</li>
           <li>Sandbox: toegang verlenen tot sandboxen</li>
            <li>Segmenten beheren: segmentdefinities lezen, maken, bewerken en verwijderen</li>
            <li>Profielen beheren: profielen lezen, maken, bewerken en verwijderen</li>
            <li>Gelezen datasets: read-only toegang tot datasets</li>
            <li>Leesschema's: alleen-lezen toegang tot schema's</li>
            <li>Naamruimte voor identiteit lezen: alleen-lezen toegang tot naamruimte voor identiteit</li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>
         <p>Adobe Journey Optimizer</p>
        </td>
        <td>
          <p>Campagnes: campagnes beheren en publiceren</p>
        </td>
      </tr>
    </tbody>
  </table>

  +++

* Als u de bestaande configuratieoptie gebruikt, moet u ervoor zorgen dat u de volgende Adobe Experience Platform Mobile SDK extensieversies gebruikt. Voor meer details op de opstelling van SDK met inbegrip van de vereiste gebiedsdelen en initialisatiecode, gelieve te verwijzen naar [ volgende documentatie ](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks).

  Voor Android

   * Mobile Core v3.1.0 of hoger
   * Adobe Journey Optimizer v3.1.0 of hoger

  Voor iOS

   * Mobile Core v5.2.0 of hoger
   * Adobe Journey Optimizer v5.1.1 of hoger

## Automatisch gemaakte bronnen {#auto-create-resources}

De instelling van het kanaal met instructies vereenvoudigt de snelle configuratie van marketingkanalen, zodat alle essentiële bronnen gemakkelijk beschikbaar zijn in de Experience Platform-, Journey Optimizer- en Data Collection-apps. Hierdoor kan uw marketingteam snel beginnen met het maken van campagnes en reizen. Hieronder ziet u een lijst met de bronnen die automatisch worden gegenereerd en geconfigureerd als onderdeel van de instelling Kanaal met instructies.

Blader door de onderstaande tabbladen voor toegang tot de uitgebreide lijsten met alle bronnen die automatisch worden gegenereerd:

>[!BEGINTABS]

>[!TAB  iOS ]

Voor de **Aanvankelijke configuratie**, hieronder is een uitvoerige lijst van alle middelen die op het **scherm van de Details van de Configuratie** worden gecreeerd wanneer u **Auto-creeer Middelen** klikt.

<table>
  <thead>
  <tr>
  <th><strong>Oplossing</strong></th>
  <th><strong>Automatisch gemaakte bronnen</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tags</p>
  </td>
  <td>
  <ul>
  <li>Eigenschap van mobiele tag</li>
  <li>Regels</li>
  <li>Gegevenselementen</li>
  <li>Bibliotheek</li>
  <li>Milieu (staging, productie, ontwikkeling)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Labelextensies</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Toestemming (met standaard ingeschakeld toestemmingsbeleid)</li>
  <li>Identiteit (met standaard ECID, met standaard stitching-regels)</li>
  <li>Mobiele kern</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Assurance-sessie</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Gegevensstromen</p>
  </td>
  <td>
  <p>DataStream met services</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Gegevensset</li>
  <li>Schema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Voor de **opstelling van het Kanaal**, hieronder is een uitvoerige lijst van alle middelen die op **worden gecreeerd voeg Kanalen** scherm toe.

<table>
  <thead>
  <tr>
  <th><strong>Oplossing</strong></th>
  <th><strong>Automatisch gemaakte bronnen</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Kanaalconfiguratie</li>
  <li>Push Credential uploaden (alleen mobiel pushbericht)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB  Android ]

Voor de **Aanvankelijke configuratie**, hieronder is een uitvoerige lijst van alle middelen die op het **scherm van de Details van de Configuratie** worden gecreeerd wanneer u **Auto-creeer Middelen** klikt.

<table>
  <thead>
  <tr>
  <th><strong>Oplossing</strong></th>
  <th><strong>Automatisch gemaakte bronnen</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tags</p>
  </td>
  <td>
  <ul>
  <li>Eigenschap van mobiele tag</li>
  <li>Regels</li>
  <li>Gegevenselementen</li>
  <li>Bibliotheek</li>
  <li>Milieu (staging, productie, ontwikkeling)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Labelextensies</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Toestemming (met standaard ingeschakeld toestemmingsbeleid)</li>
  <li>Identiteit (met standaard ECID, met standaard stitching-regels)</li>
  <li>Mobiele kern</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Assurance-sessie</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Gegevensstromen</p>
  </td>
  <td>
  <p>DataStream met services</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Gegevensset</li>
  <li>Schema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Voor de **opstelling van het Kanaal**, hieronder is een uitvoerige lijst van alle middelen die op **worden gecreeerd voeg Kanalen** scherm toe.

<table>
  <thead>
  <tr>
  <th><strong>Oplossing</strong></th>
  <th><strong>Automatisch gemaakte bronnen</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Kanaalconfiguratie</li>
  <li>Push Credential uploaden (alleen mobiel pushbericht)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB  Web ]

Voor de **Aanvankelijke configuratie**, hieronder is een uitvoerige lijst van alle middelen die op het **scherm van de Details van de Configuratie** worden gecreeerd wanneer u **Auto-creeer Middelen** klikt.

<table>
  <thead>
  <tr>
  <th><strong>Oplossing</strong></th>
  <th><strong>Automatisch gemaakte bronnen</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tags</p>
  </td>
  <td>
  <ul>
  <li>Eigenschap van mobiele tag</li>
  <li>Regels</li>
  <li>Gegevenselementen</li>
  <li>Bibliotheek</li>
  <li>Milieu (staging, productie, ontwikkeling)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Labelextensies</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Toestemming (met standaard ingeschakeld toestemmingsbeleid)</li>
  <li>Identiteit (met standaard ECID, met standaard stitching-regels)</li>
  <li>Mobiele kern</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Assurance-sessie</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Gegevensstromen</p>
  </td>
  <td>
  <p>DataStream met services</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Gegevensset</li>
  <li>Schema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!ENDTABS]

