---
solution: Journey Optimizer
product: journey optimizer
title: Een aangepaste handeling configureren
description: Leer hoe u een aangepaste handeling configureert
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: handeling, extern, aangepast, reizen, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 12423d9fe07e5c757154ae4f732ff20ec6dc2427
workflow-type: tm+mt
source-wordcount: '1750'
ht-degree: 1%

---

# Een aangepaste handeling configureren {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Aangepaste acties"
>abstract="Als u een derdesysteem gebruikt om berichten te verzenden of als u reizen API vraag naar een derdesysteem wilt verzenden, gebruik douaneacties om zijn verbinding aan uw reis te vormen. U kunt bijvoorbeeld met aangepaste handelingen verbinding maken met de volgende systemen: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase, enz."

Als u een derdesysteem gebruikt om berichten te verzenden of als u reizen API vraag naar een derdesysteem wilt verzenden, gebruik douaneacties om zijn verbinding aan uw reis te vormen. U kunt bijvoorbeeld met aangepaste handelingen verbinding maken met de volgende systemen: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, enz.

Aangepaste acties zijn aanvullende acties die door technische gebruikers worden gedefinieerd en beschikbaar worden gesteld aan verkopers. Zodra gevormd, verschijnen zij in het linkerpalet van uw reis, in **[!UICONTROL Action]** categorie. Meer informatie vindt u [op deze pagina](../building-journeys/about-journey-activities.md#action-activities).

## Beperkingen{#custom-actions-limitations}

Aangepaste acties worden geleverd met enkele beperkingen die worden vermeld in [deze pagina](../start/guardrails.md).

In parameters voor aangepaste handelingen kunt u een eenvoudige verzameling en een verzameling objecten doorgeven. Meer informatie over verzamelingsbeperkingen vindt u in [deze pagina](../building-journeys/collections.md#limitations).

De parameters voor aangepaste handelingen hebben een verwachte indeling (bijvoorbeeld tekenreeks, decimaal, enz.). U moet deze verwachte formaten zorgvuldig respecteren. Meer informatie in deze [use case](../building-journeys/collections.md).

Aangepaste acties ondersteunen alleen de JSON-indeling bij gebruik van [verzoek](../action/about-custom-action-configuration.md#define-the-message-parameters) of [antwoordlading](../action/action-response.md).

## Best practices{#custom-action-enhancements-best-practices}

Wanneer het kiezen van een eindpunt om het gebruiken van een douaneactie te richten, ben zeker dat:

* Dit eindpunt kan de productie van de reis, gebruikend configuraties van steunen [Throttling API](../configuration/throttling.md) of [API voor uitlijnen](../configuration/capping.md) om het te beperken. Wees voorzichtig dat een snelheidsbegrenzingsconfiguratie niet lager kan zijn dan 200 TPS. Om het even welk gericht eindpunt zal minstens 200 TPS moeten steunen.
* Dit eindpunt moet een reactietijd hebben zo laag mogelijk. Afhankelijk van uw verwachte productie, zou het hebben van een hoge reactietijd de daadwerkelijke productie kunnen beïnvloeden.

Een maximum van 300.000 vraag over één minuut wordt bepaald voor alle douaneacties. Daarnaast wordt de standaarduitlijning uitgevoerd per host en per sandbox. Op een sandbox bijvoorbeeld als u twee eindpunten met dezelfde host hebt (bijvoorbeeld: `https://www.adobe.com/endpoint1` en `https://www.adobe.com/endpoint2`), wordt de aftopping toegepast op alle eindpunten onder de host adobe.com. De &quot;eindpunt1&quot;en &quot;eindpunt2&quot;zullen de zelfde het begrenzen configuratie delen en het hebben van één eindpunt bereikt de grens zal een effect op het andere eindpunt hebben.

Deze grens is geplaatst gebaseerd op klantengebruik, om externe eindpunten te beschermen die door douaneacties worden gericht. U moet hiermee rekening houden bij reizen voor uw publiek door een juiste leessnelheid te definiëren (5000 profielen/s wanneer aangepaste handelingen worden gebruikt). Indien nodig, kunt u deze het plaatsen met voeten treden door een grotere het maximum van het maximum of het vertragen grens door onze Capping/het Draaien APIs te bepalen. Zie [deze pagina](../configuration/external-systems.md).

U zou openbare eindpunten met douaneacties niet om verschillende redenen moeten richten:

* Zonder behoorlijk het in kaart brengen of het vertragen, is er een risico om teveel vraag naar een openbaar eindpunt te verzenden dat zulk volume niet kan steunen.
* De gegevens van het profiel kunnen door douaneacties worden verzonden, zodat het richten van een openbaar eindpunt tot onbedoeld het delen van persoonlijke informatie buiten zou kunnen leiden.
* U hebt geen controle over de gegevens die door openbare eindpunten worden teruggekeerd. Als een eindpunt zijn API verandert of onjuiste informatie begint te verzenden, zullen die in verzonden mededelingen, met potentiële negatieve gevolgen ter beschikking worden gesteld.

## Toestemming en gegevensbeheer {#privacy}

In Journey Optimizer kunt u beleid voor gegevensbeheer en toestemming toepassen op uw aangepaste acties om te voorkomen dat bepaalde velden worden geëxporteerd naar systemen van derden of om klanten uit te sluiten die niet hebben ingestemd met het ontvangen van e-mail, push- of SMS-berichten. Raadpleeg de volgende pagina&#39;s voor meer informatie:

* [Gegevensbeheer](../action/action-privacy.md).
* [Toestemming](../action/action-privacy.md).


## Configuratiestappen {#configuration-steps}

Hier zijn de belangrijkste stappen die worden vereist om een douaneactie te vormen:

1. Selecteer in de sectie van het menu ADMINISTRATIE de optie **[!UICONTROL Configurations]**. In de  **[!UICONTROL Actions]** sectie, klikken **[!UICONTROL Manage]**. Klikken **[!UICONTROL Create Action]** om een nieuwe handeling te maken. Het deelvenster Handelingsconfiguratie wordt aan de rechterkant van het scherm geopend.

   ![](assets/custom2.png)

1. Voer een naam in voor de handeling.

   >[!NOTE]
   >
   >Alleen alfanumerieke tekens en onderstrepingstekens zijn toegestaan. De maximumlengte is 30 tekens.

1. Voeg een beschrijving aan uw actie toe. Deze stap is optioneel.
1. Het aantal ritten dat deze handeling gebruikt, wordt weergegeven in het dialoogvenster **[!UICONTROL Used in]** veld. U kunt op de knop **[!UICONTROL View journeys]** om de lijst met reizen weer te geven die deze handeling gebruiken.
1. Verschillende definiëren **[!UICONTROL URL Configuration]** parameters. Zie [deze pagina](../action/about-custom-action-configuration.md#url-configuration).
1. Vorm **[!UICONTROL Authentication]** sectie. Deze configuratie is het zelfde als voor gegevensbronnen.  Zie [deze sectie](../datasource/external-data-sources.md#custom-authentication-mode).
1. Definieer de **[!UICONTROL Action parameters]**. Zie [deze pagina](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Klik op **[!UICONTROL Save]**.

   De aangepaste handeling is nu geconfigureerd en klaar om te worden gebruikt tijdens uw reizen. Zie [deze pagina](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Wanneer een douaneactie in een reis wordt gebruikt, zijn de meeste parameters read-only. U kunt alleen de **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** en de **[!UICONTROL Authentication]** sectie.

## Eindpuntconfiguratie {#url-configuration}

Wanneer het vormen van een douaneactie, moet u het volgende bepalen **[!UICONTROL Endpoint Configuration]** parameters:

![](assets/action-response1bis.png){width="70%" align="left"}

1. In de **[!UICONTROL URL]** -veld, geeft u de URL van de externe service op:

   * Als de URL statisch is, voert u de URL in dit veld in.

   * Als de URL een dynamisch pad bevat, voert u alleen het statische gedeelte van de URL in, dat wil zeggen het schema, de host, de poort en eventueel een statisch gedeelte van het pad.

     Voorbeeld: `https://xxx.yyy.com/somethingstatic/`

     U geeft het dynamische pad van de URL op wanneer u de aangepaste handeling aan een rit toevoegt. [Meer informatie](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >Om veiligheidsredenen raden we u ten zeerste aan het HTTPS-schema te gebruiken voor de URL. Wij staan niet het gebruik van Adobe adressen toe die niet openbaar en het gebruik van IP adressen zijn.
   >
   >Alleen de standaardpoorten zijn toegestaan bij het definiëren van een aangepaste handeling: 80 voor http en 443 voor https.

1. Selecteer de vraag **[!UICONTROL Method]**: het kan **[!UICONTROL POST]**, **[!UICONTROL GET]** of **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > De **DELETE** methode wordt niet ondersteund. Als u een bestaande bron moet bijwerken, selecteert u de optie **PUT** methode.

1. Definieer de headers en queryparameters:

   * In de **[!UICONTROL Headers]** sectie, klikken **[!UICONTROL Add a header field]** om de kopballen van HTTP van het verzoekbericht te bepalen dat naar de externe dienst moet worden verzonden. De **[!UICONTROL Content-Type]** en **[!UICONTROL Charset]** koptekstvelden worden standaard ingesteld. U kunt deze velden niet verwijderen. Alleen de **[!UICONTROL Content-Type]** header kan worden gewijzigd. De waarde ervan moet de JSON-indeling respecteren. Hier is de standaardwaarde:

   ![](assets/content-type-header.png)

   * In de **[!UICONTROL Query parameters]** sectie, klikken **[!UICONTROL Add a Query parameter field]** om de parameters te bepalen u in URL wilt toevoegen.

   ![](assets/journeyurlconfiguration2bis.png)

1. Voer het label of de naam van het veld in.

1. Selecteer het type: **[!UICONTROL Constant]** of **[!UICONTROL Variable]**. Als u **[!UICONTROL Constant]** Voer vervolgens de constante waarde in het dialoogvenster **[!UICONTROL Value]** veld. Als u **[!UICONTROL Variable]**, dan zult u deze variabele specificeren wanneer het toevoegen van de douaneactie aan een reis. [Meer informatie](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Nadat u de douaneactie aan een reis hebt toegevoegd, kunt u kopbal of vraagparametergebieden aan het nog toevoegen als de reis in ontwerpstatus is. Als u niet wilt dat de reis door configuratieveranderingen wordt beïnvloed, dupliceer de douaneactie en voeg de gebieden aan de nieuwe douaneactie toe.
   >
   >Kopteksten worden gevalideerd volgens veldparseringsregels. Meer informatie in [deze documentatie](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## De parameters voor de nuttige lading definiëren {#define-the-message-parameters}

1. In de **[!UICONTROL Request]** plakken, plakt u een voorbeeld van de JSON-payload die u naar de externe service wilt verzenden. Dit gebied is facultatief en slechts beschikbaar voor POST en PUT die methodes roepen.

1. In de **[!UICONTROL Response]** plakken, een voorbeeld van de lading die door de vraag is teruggekeerd. Dit veld is optioneel en beschikbaar voor alle aanroepmethoden. Voor gedetailleerde informatie over het gebruik van API-aanroepreacties in aangepaste handelingen raadpleegt u [deze pagina](../action/action-response.md).

>[!NOTE]
>
>De responscapaciteit is momenteel beschikbaar in bèta.

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>Het voorbeeld voor de laadbewerking mag geen null-waarden bevatten. Veldnamen in de payload mogen geen &quot;.&quot; bevatten teken. Ze kunnen niet beginnen met het teken ‘$’.

U kunt het parametertype definiëren (bijvoorbeeld: tekenreeks, geheel getal, enz.).

U kunt ook opgeven of een parameter een constante of een variabele is.

* **Constante** betekent dat de waarde van de parameter in de ruit van de actieconfiguratie door een technische persoon wordt bepaald. De waarde zal altijd het zelfde over reizen zijn. Het zal niet variëren en de marktleider zal het niet zien wanneer het gebruiken van de douaneactie in de reis. Het kan bijvoorbeeld een id zijn die het externe systeem verwacht. In dat geval is het veld rechts van de schakelconstante/variabele de doorgegeven waarde.
* **Variabele** betekent dat de waarde van de parameter zal variëren. Marktdeelnemers die deze aangepaste handeling tijdens een reis gebruiken, kunnen de gewenste waarde doorgeven of opgeven waar de waarde voor deze parameter moet worden opgehaald (bijvoorbeeld vanaf het evenement, vanuit Adobe Experience Platform, enz.). In dat geval, is het gebied op het recht van de knevelconstante/variabele de etiketmarketers in de reis zullen zien om deze parameter te noemen.

![](assets/customactionpayloadmessage2.png)

## mTLS-protocolondersteuning {#mtls-protocol-support}

U kunt de Wederzijdse Veiligheid van de Laag van het Vervoer (mTLS) nu gebruiken om verbeterde veiligheid in uitgaande verbindingen aan de bestemmingen van HTTP API en de douaneacties van Adobe Journey Optimizer te verzekeren. mTLS is een end-to-end veiligheidsmethode voor wederzijdse authentificatie die ervoor zorgt dat beide partijen die informatie delen wie zij beweren te zijn alvorens de gegevens worden gedeeld. mTLS bevat een extra stap in vergelijking met TLS, waarin de server ook om het certificaat van de client vraagt en dit aan het einde verifieert.

In Adobe Journey Optimizer wordt mTLS gebruikt in combinatie met aangepaste handelingen. U hebt geen aanvullende configuratie voor aangepaste Adobe Journey Optimizer-acties nodig om mTLS in te schakelen. Wanneer het eindpunt voor een douaneactie mTLS-Toegelaten is, haalt het systeem het certificaat van keystore van Adobe Experience Platform en verstrekt het automatisch aan het eindpunt (zoals wordt vereist voor mTLS verbindingen).

Als u mTLS met deze de bestemmingswerkschema&#39;s van Adobe Journey Optimizer en van HTTP van het Experience Platform wilt gebruiken API, moet het serveradres u in de UI van de de klantenactie van Adobe Journey Optimizer of UI van Doelen plaatsen protocollen van TLS hebben onbruikbaar gemaakt en slechts mTLS toegelaten. Als het TLS 1.2 protocol nog op dat eindpunt wordt toegelaten, wordt geen certificaat verzonden voor de cliëntauthentificatie. Dit betekent dat om mTLS met deze werkschema&#39;s te gebruiken, uw &quot;ontvangende&quot;servereindpunt mTLS moet zijn **alleen** Toegelaten verbindingspunt.

>[!IMPORTANT]
>
>Er is geen aanvullende configuratie vereist in uw aangepaste Adobe Journey Optimizer-actie of -reis om mTLS te activeren. Dit proces wordt automatisch uitgevoerd wanneer een met mTLS geschikt eindpunt wordt gedetecteerd. De Common Name (CN) en de Alternative Names van het Onderwerp (San) voor elk certificaat zijn beschikbaar in de documentatie als deel van het certificaat en kunnen als extra laag van bezitsbevestiging worden gebruikt als u dit wenst.
>
>RFC 2818, gepubliceerd in mei 2000, vervangt het gebruik van het gebied van de Gemeenschappelijke Naam (CN) in HTTPS certificaten voor onderwerpnaamcontrole. In plaats daarvan wordt aangeraden de extensie &quot;Alternatieve naam onderwerp&quot; (SAN) van het type &quot;naam dns&quot; te gebruiken.

Als u de CN of SAN wilt controleren voor aanvullende validatie door derden, kunt u de relevante certificaten hier downloaden:

```
Prod:
{
    "serviceName": "AJO Journeys",
    "publicCertificate": "-----BEGIN CERTIFICATE-----
MIIG9TCCBd2gAwIBAgIQBX+pDP5hB0gqDzFKyq5wLjANBgkqhkiG9w0BAQsFADBZ
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMTMwMQYDVQQDEypE
aWdpQ2VydCBHbG9iYWwgRzIgVExTIFJTQSBTSEEyNTYgMjAyMCBDQTEwHhcNMjQw
NTA5MDAwMDAwWhcNMjUwNjA5MjM1OTU5WjB0MQswCQYDVQQGEwJVUzETMBEGA1UE
CBMKQ2FsaWZvcm5pYTERMA8GA1UEBxMIU2FuIEpvc2UxEzARBgNVBAoTCkFkb2Jl
IEluYy4xKDAmBgNVBAMTH2Fqby1qb3VybmV5cy5hZXAtbXRscy5hZG9iZS5jb20w
ggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDaI8HZHzbmPEgTy9O7cYmq
ZVX5283Gw7j7v4/O810jZXItBDmsSiWotvTgAT0s2oZMZZ6tGPbQB7hL+xJJ+yu2
HxFl1WzB4UGHJ+UbrL94hI930xQs0FVgSOGgIarj5HucF2ZxwHIkVHY5whrOq9t4
UxFBG0siUPQrTzV9GfA0wREElugpTbwaM8CTWwOQ9ekroOD2C5zAcLTycXFtSMiU
B4L4u38S9hGoBByzzKv9GnUMQudvt/s5zsGykZgEEYeN6IitfVO6BOD9jT94Aytx
/O3XH5w8v4KNTn+An99bXFmyg3JRUFSYZFxha8s1f6uu0XbdToQ+ao0WkE06nMmV
AgMBAAGjggOcMIIDmDAfBgNVHSMEGDAWgBR0hYDAZsffN97PvSk3qgMdvu3NFzAd
BgNVHQ4EFgQUn8OqtzccNdrsb+fbRnTHmtTZxLMwKgYDVR0RBCMwIYIfYWpvLWpv
dXJuZXlzLmFlcC1tdGxzLmFkb2JlLmNvbTA+BgNVHSAENzA1MDMGBmeBDAECAjAp
MCcGCCsGAQUFBwIBFhtodHRwOi8vd3d3LmRpZ2ljZXJ0LmNvbS9DUFMwDgYDVR0P
AQH/BAQDAgWgMB0GA1UdJQQWMBQGCCsGAQUFBwMBBggrBgEFBQcDAjCBnwYDVR0f
BIGXMIGUMEigRqBEhkJodHRwOi8vY3JsMy5kaWdpY2VydC5jb20vRGlnaUNlcnRH
bG9iYWxHMlRMU1JTQVNIQTI1NjIwMjBDQTEtMS5jcmwwSKBGoESGQmh0dHA6Ly9j
cmw0LmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAy
MENBMS0xLmNybDCBhwYIKwYBBQUHAQEEezB5MCQGCCsGAQUFBzABhhhodHRwOi8v
b2NzcC5kaWdpY2VydC5jb20wUQYIKwYBBQUHMAKGRWh0dHA6Ly9jYWNlcnRzLmRp
Z2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAyMENBMS0x
LmNydDAMBgNVHRMBAf8EAjAAMIIBfwYKKwYBBAHWeQIEAgSCAW8EggFrAWkAdwBO
daMnXJoQwzhbbNTfP1LrHfDgjhuNacCx+mSxYpo53wAAAY9ecsWsAAAEAwBIMEYC
IQDQclgq89ZVlwdYBJFEIs8q4WIcZ9Siw+jb9OgCrz+wjwIhALQLnC1WyT+dHjvY
FvZjc99WkjnEwhIevj/Rz7r0EzhmAHUAfVkeEuF4KnscYWd8Xv340IdcFKBOlZ65
Ay/ZDowuebgAAAGPXnLF5AAABAMARjBEAiBy9cNT3CnmSMOdJe+JbG8f7ha1UGgN
TdDlaR9x9fKmKQIgNmGjz5AzP1evB2G1TTvVLkHfWQw0864c4F23WSV+6TsAdwDP
EVbu1S58r/OHW9lpLpvpGnFnSrAX7KwB0lt3zsw7CAAAAY9ecsYnAAAEAwBIMEYC
IQCTcB7s1xDP8Olif3jj4X8jHgVxv5C3bTvG6wDYBByfcQIhAOt8PhR6tWSLtF1V
HB8r7dns7Oth1+QT7WMonQZsP/3WMA0GCSqGSIb3DQEBCwUAA4IBAQAjTy45fbQV
aVTZ71wcIyHnkJfq/8SSc/UNT5//6AMiV6kb3YsFW1+EaQ1wPHZS0Qfjs7aIsXi5
f2TCGps8onELNpOfFfptrOCMfcYGMvV1wPCBy+kuoGY/YRZlsdNUTTzQAGztfRev
79w+XIDzioCrY+sfyUkkw+N/F7/RIjzMKjP6onSfuD+5WjqVKq9kFE0fCyJixedV
BPoPM4Cktgvc9SsK17JmLWkg+V2yH1eDzmjF3sR0/dcmoAM0qgV/CDuhIIqX2o7m
3/aQSNsPUpgBVbkz+SjEtchmw8DXW/Kro8QVulsXdbkiLTOj4JopxdOzrbKgWMwr
pIw7KKJoktDk
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIEyDCCA7CgAwIBAgIQDPW9BitWAvR6uFAsI8zwZjANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0yMTAzMzAwMDAwMDBaFw0zMTAzMjkyMzU5NTlaMFkxCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxMzAxBgNVBAMTKkRpZ2lDZXJ0IEdsb2Jh
bCBHMiBUTFMgUlNBIFNIQTI1NiAyMDIwIENBMTCCASIwDQYJKoZIhvcNAQEBBQAD
ggEPADCCAQoCggEBAMz3EGJPprtjb+2QUlbFbSd7ehJWivH0+dbn4Y+9lavyYEEV
cNsSAPonCrVXOFt9slGTcZUOakGUWzUb+nv6u8W+JDD+Vu/E832X4xT1FE3LpxDy
FuqrIvAxIhFhaZAmunjZlx/jfWardUSVc8is/+9dCopZQ+GssjoP80j812s3wWPc
3kbW20X+fSP9kOhRBx5Ro1/tSUZUfyyIxfQTnJcVPAPooTncaQwywa8WV0yUR0J8
osicfebUTVSvQpmowQTCd5zWSOTOEeAqgJnwQ3DPP3Zr0UxJqyRewg2C/Uaoq2yT
zGJSQnWS+Jr6Xl6ysGHlHx+5fwmY6D36g39HaaECAwEAAaOCAYIwggF+MBIGA1Ud
EwEB/wQIMAYBAf8CAQAwHQYDVR0OBBYEFHSFgMBmx9833s+9KTeqAx2+7c0XMB8G
A1UdIwQYMBaAFE4iVCAYlebjbuYP+vq5Eu0GF485MA4GA1UdDwEB/wQEAwIBhjAd
BgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwdgYIKwYBBQUHAQEEajBoMCQG
CCsGAQUFBzABhhhodHRwOi8vb2NzcC5kaWdpY2VydC5jb20wQAYIKwYBBQUHMAKG
NGh0dHA6Ly9jYWNlcnRzLmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbFJvb3RH
Mi5jcnQwQgYDVR0fBDswOTA3oDWgM4YxaHR0cDovL2NybDMuZGlnaWNlcnQuY29t
L0RpZ2lDZXJ0R2xvYmFsUm9vdEcyLmNybDA9BgNVHSAENjA0MAsGCWCGSAGG/WwC
ATAHBgVngQwBATAIBgZngQwBAgEwCAYGZ4EMAQICMAgGBmeBDAECAzANBgkqhkiG
9w0BAQsFAAOCAQEAkPFwyyiXaZd8dP3A+iZ7U6utzWX9upwGnIrXWkOH7U1MVl+t
wcW1BSAuWdH/SvWgKtiwla3JLko716f2b4gp/DA/JIS7w7d7kwcsr4drdjPtAFVS
slme5LnQ89/nD/7d+MS5EHKBCQRfz5eeLjJ1js+aWNJXMX43AYGyZm0pGrFmCW3R
bpD0ufovARTFXFZkAdl9h6g4U5+LXUZtXMYnhIHUfoyMo5tS58aI7Dd8KvvwVVo4
chDYABPPTHPbqjc1qCmBaZx2vN4Ye5DUys/vZwP9BFohFrH/6j/f3IL16/RZkiMN
JCqVJUzKoZHm1Lesh3Sz8W2jmdv51b2EQJ8HmA==
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65TANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0xMzA4MDExMjAwMDBaFw0zODAxMTUxMjAwMDBaMGExCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxGTAXBgNVBAsTEHd3dy5kaWdpY2VydC5j
b20xIDAeBgNVBAMTF0RpZ2lDZXJ0IEdsb2JhbCBSb290IEcyMIIBIjANBgkqhkiG
9w0BAQEFAAOCAQ8AMIIBCgKCAQEAuzfNNNx7a8myaJCtSnX/RrohCgiN9RlUyfuI
2/Ou8jqJkTx65qsGGmvPrC3oXgkkRLpimn7Wo6h+4FR1IAWsULecYxpsMNzaHxmx
1x7e/dfgy5SDN67sH0NO3Xss0r0upS/kqbitOtSZpLYl6ZtrAGCSYP9PIUkY92eQ
q2EGnI/yuum06ZIya7XzV+hdG82MHauVBJVJ8zUtluNJbd134/tJS7SsVQepj5Wz
tCO7TG1F8PapspUwtP1MVYwnSlcUfIKdzXOS0xZKBgyMUNGPHgm+F6HmIcr9g+UQ
vIOlCsRnKPZzFBQ9RnbDhxSJITRNrw9FDKZJobq7nMWxM4MphQIDAQABo0IwQDAP
BgNVHRMBAf8EBTADAQH/MA4GA1UdDwEB/wQEAwIBhjAdBgNVHQ4EFgQUTiJUIBiV
5uNu5g/6+rkS7QYXjzkwDQYJKoZIhvcNAQELBQADggEBAGBnKJRvDkhj6zHd6mcY
1Yl9PMWLSn/pvtsrF9+wX3N3KjITOYFnQoQj8kVnNeyIv/iPsGEMNKSuIEyExtv4
NeF22d+mQrvHRAiGfzZ0JFrabA0UWTW98kndth/Jsw1HKj2ZL7tcu7XUIOGZX1NG
Fdtom/DzMNU+MeKNhJ7jitralj41E6Vf8PlwUHBHQRFXGU7Aj64GxJUTFy8bJZ91
8rGOmaFvE7FBcf6IKshPECBV1/MUReXgRPTqh5Uykw7+U0b6LJ3/iyK5S9kJRaTe
pLiaWN0bfVKfjllDiIGknibVb63dDcY3fe0Dkhvld1927jyNxF1WW6LZZm6zNTfl
MrY=
-----END CERTIFICATE-----",
    "expiryDate": "2025-06-09T23:59:59Z"
}
```

