---
solution: Journey Optimizer
product: journey optimizer
title: Uitsluitingslijst
description: Meer informatie over uitsluitingen tijdens verzenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a34ba1a8-87d5-4f9c-a181-2f49e74e8f09
source-git-commit: 8ced9477edf8a7129e974d007755e132f3079943
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 7%

---

# Uitsluitingsredenen {#exclusion-list}

## Hoe uitsluitingen in campagnerapporten worden geteld

Wanneer het bekijken van campagnerapporten, merk op dat *metrisch van Uitsluiting* als volgt wordt berekend:

**Uitsluitingen = Unieke Uitsluitingen + Dubbele Gebeurtenissen van de Uitsluiting**

Dit betekent dat als een profiel meerdere keren wordt uitgesloten (bijvoorbeeld als gevolg van meerdere uitsluitingsgebeurtenissen voor hetzelfde profiel), elke gebeurtenis wordt meegeteld in het totaal van uitsluitingen. Dientengevolge, kan de som van *Geleverde* en *Uitsluitingen* de originele gerichte publieksgrootte overschrijden. Dit gedrag wordt verwacht en weerspiegelt de manier waarop uitsluitingsgebeurtenissen in het systeem worden bijgehouden.

**Voorbeeld:**

- Doelgroep: 94.000 profielen
- Geleverd: 69.000
- Uitsluitingen: 37.000 (inclusief dubbele gebeurtenissen voor uitsluiten)
- Totaal (geleverd + uitsluitingen): 106.000

Het totaal overschrijdt het doelpubliek omdat dubbele uitsluitingsgebeurtenissen zijn opgenomen in het aantal uitsluitingen.

Zie de tabel hieronder voor meer informatie over de specifieke redenen voor uitsluiting.

## Lijst met redenen voor uitsluiting

| Uitsluitingsreden | Foutcode | Kanaal | Toelichting |
|-|-|-|-|
| RuntimeDispatchError | 050301 | Alle kanalen | Algemene uitsluitingsgebeurtenis voor een verzendfout bij uitvoering. |
| RuntimeRenderingError | 050302 | Alle kanalen | Algemene uitsluitingsgebeurtenis voor elke renderfout bij uitvoering. |
| NamespaceErrorForExperimentation | 050017 | Alle kanalen | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer Namespace in Experiment afwijkt van de naamruimte van het profiel. |
| ExperimentationHoldoutExclusion | 050018 | Alle kanalen | Deze uitsluitingsgebeurtenis wordt gegenereerd wanneer de gekwalificeerde behandeling voor een experiment &quot;Holdout&quot; is. |
| ExcludedForControlRules | 050002 | Alle kanalen | Deze uitsluitingsgebeurtenis wordt gegenereerd wanneer de levering van het huidige bericht leidt tot een schending van de controleregels, bijvoorbeeld het aantal e-mails dat in een maand is toegestaan. |
| DirectMailNoVariantDefined | 050062 | DirectMail | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer de variant Direct mail niet is gedefinieerd. |
| DirectMailNoMessageFoundForTreatment | 050061 | DirectMail | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het experiment is ingeschakeld voor het bericht en er geen bericht wordt gevonden voor de gekwalificeerde behandeling. |
| EmailNoConsent | 050101 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer de gebruiker geen marketinge-mails meer ontvangt. |
| Onderdrukt | 050107 | Email | Uitsluiting vanwege een van de onderdrukkingsredenen. |
| EmailSuppressed | 050102 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het doel-e-mailadres wordt onderdrukt. |
| DomainSuppressed | 050105 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het domein van de beoogde e-mail wordt onderdrukt. |
| NotAllowed | 050108 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer de lijst van gewenste personen is ingeschakeld en het e-mailbericht dat als doel is geselecteerd, niet in de lijst van gewenste personen wordt opgenomen. |
| EmailNotAllowed | 050103 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer de lijst van gewenste personen is ingeschakeld en het e-mailbericht dat als doel is geselecteerd, niet in de lijst van gewenste personen wordt opgenomen. |
| DomainNotAllowed | 050106 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer de lijst van gewenste personen is ingeschakeld en het domein van de beoogde e-mail is uitgesloten van de lijst van gewenste personen. |
| EmailNoSubscriberIdFoundInProfile | 050025 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer subscriberId niet wordt gevonden in het profiel voor een e-mailabonnement. |
| EmailNoAddressFoundInProfile | 050020 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het e-mailadres niet wordt gevonden in het uitvoeringsadres. |
| EmailNoAddressDefinedInPreset | 050021 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het uitvoeringsadres niet in de configuratie is gedefinieerd. |
| EmailNoVariantDefined | 050026 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer er geen variant in het e-mailbericht is gedefinieerd. |
| EmailNoMessageFoundForTreatment | 050027 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het experiment is ingeschakeld voor het bericht en er geen bericht wordt gevonden voor de gekwalificeerde behandeling. |
| EmailMalformedAddress | 050024 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer de e-mail een onjuist adres bevat. |
| UnsubscribeLinkNotValid | 050081 | Email | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer de lengte van het onderwerp List-Unsubscribe mailTo groter is dan de RFC-limiet van 998 tekens. |
| InAppNoVariantDefined | 050041 | InApp | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer geen variant wordt gedefinieerd voor InApp-bericht. |
| InAppNoMessageFoundForTreatment | 050042 | InApp | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het experiment is ingeschakeld voor het bericht en er geen bericht wordt gevonden voor de gekwalificeerde behandeling. |
| PushNoTokenFoundInProfile | 050030 | Push | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het profiel geen pushtokens heeft. |
| PushNoValidTokenFoundForApps | 050031 | Push | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer er geen geldig token wordt gevonden voor de beoogde apps in de configuratie. **Belangrijk:** wanneer het gebruiken van een productiecertificaat, moet het `pushNotificationDetails.platform` attribuut in het gebruikersprofiel aan `apns` worden geplaatst. Als u een sandboxcertificaat gebruikt, stelt u dit in op `apnsSandbox` . Deze uitsluiting wordt geactiveerd als het platformkenmerk niet overeenkomt met het certificaattype. |
| PushMalformedProfile | 050034 | Push | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer pushNotificationDetails in het profiel onjuist is geformuleerd. |
| PushNoConsent | 050111 | Push | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer de gebruiker geen pushberichten meer op de markt heeft gebracht. |
| PushNoApplicationDefinedInPreset | 050033 | Push | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer de configuratie geen toepassing bevat die als doel moet worden ingesteld. |
| PushNoVariantDefined | 050035 | Push | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer geen variant wordt gedefinieerd. |
| PushNoMessageFoundForTreatment | 050036 | Push | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het experiment is ingeschakeld voor het bericht en er geen bericht wordt gevonden voor de gekwalificeerde behandeling. |
| SMSNoConsent | 050104 | Sms | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer de gebruiker ervoor heeft gekozen geen SMS meer op de markt te brengen. |
| SMSFromNumberNotDefinedInPreset | 050152 | Sms | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer &quot;FromNumber&quot; niet in de configuratie is gedefinieerd. |
| SMSNoToNumberDefinedInProfile | 050153 | Sms | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer &quot;ToNumber&quot; niet is gedefinieerd in de configuratie. |
| SMSNoVariantDefined | 050154 | Sms | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer geen variant wordt gedefinieerd. |
| SMSNoMessageFoundForTreatment | 050155 | Sms | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het experiment is ingeschakeld voor het bericht en er geen bericht wordt gevonden voor de gekwalificeerde behandeling. |
| WebNoVariantDefined | 050041 | Web | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer geen variant voor een webbericht wordt gedefinieerd. |
| WebNoMessageFoundForTreatment | 050042 | Web | Er wordt een uitsluitingsgebeurtenis gegenereerd wanneer het experiment is ingeschakeld voor het bericht en er geen bericht wordt gevonden voor de gekwalificeerde behandeling. |
