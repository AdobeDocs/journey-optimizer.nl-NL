---
solution: Journey Optimizer
product: journey optimizer
title: Inhoud testen met behulp van voorbeeldinvoergegevens (Beta)
description: Leer hoe u een voorbeeld van inhoud bekijkt en een e-mailproefdruk verzendt met voorbeeldinvoergegevens uit een CSV- of JSON-bestand of die u handmatig toevoegt.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
exl-id: 8462c75e-4f4b-4c4f-8734-19efbbc70c7a
source-git-commit: e6e7890d2ff1fc91155da14e1e6c1cde01f25447
workflow-type: tm+mt
source-wordcount: '902'
ht-degree: 0%

---

# Inhoud testen met behulp van voorbeeldinvoergegevens (Beta) {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simuleren met behulp van voorbeeldinvoer"
>abstract="In dit scherm kunt u verschillende varianten van uw inhoud testen door waarden voor verpersoonlijkingsgebieden door een malplaatje CSV of JSON te verstrekken, of door de waarden manueel in te gaan."

>[!AVAILABILITY]
>
>Deze functies zijn momenteel beschikbaar voor alle klanten als een openbare bètaversie.

Met Reis optimizer kunt u verschillende varianten van uw inhoud testen door deze voor te vertonen en proefdrukken te verzenden met behulp van voorbeeldinvoergegevens die vanuit een CSV- of JSON-bestand zijn geüpload of handmatig zijn toegevoegd. Alle profielkenmerken die in de inhoud worden gebruikt voor personalisatie worden automatisch gedetecteerd door het systeem en kunnen worden gebruikt voor uw tests om meerdere varianten te maken. Een variant verwijst naar een versie van de inhoud met verschillende waarden voor de kenmerken ervan.

>[!NOTE]
>
>Vooralsnog zijn wijzigingen in de inhoud alleen beschikbaar voor de kanalen voor e-mail-, sms- en pushmeldingen.

Klik op de knop **[!UICONTROL Simulate content]** en kies **[!UICONTROL Simulate content variations (Beta)]** voor toegang tot deze ervaring.

![](assets/simulate-sample.png)

De belangrijkste stappen om uw inhoud te testen zijn als volgt:

1. Voeg maximaal 30 varianten toe met voorbeeldinvoergegevens door een bestand te uploaden of door handmatig gegevens toe te voegen. [ Leer hoe te om variabelen toe te voegen ](#profiles)
1. Controleer de voorvertoning van de inhoud met de verschillende varianten. [ Leer hoe te om uw inhoud ](#preview) voor te vertonen
1. Voor e-mailinhoud verzendt u maximaal 10 proefdrukken naar e-mailadressen met de verschillende varianten. [ Leer hoe te om proefdrukken ](#proofs) te verzenden


## Afbeeldingen en beperkingen {#limitations}

Overweeg de volgende instructies en voorwaarden voordat u begint met het testen van de inhoud met behulp van voorbeeldinvoergegevens.

* Vanaf nu is het testen met behulp van voorbeeldinvoergegevens alleen beschikbaar voor de communicatiekanalen E-mail, SMS en Push. U hebt geen toegang tot deze ervaring via de knop Inhoud simuleren in de Designer-e-mail.
* De volgende functies zijn niet beschikbaar in de huidige ervaring: Inbox rendering, spamrapporten, meertalige content en content experiment. Als u deze functies wilt gebruiken, selecteert u de knop **[!UICONTROL Simulate content]** in de inhoud om toegang te krijgen tot de vorige gebruikersinterface.
* Momenteel worden alleen profielkenmerken ondersteund. Als contextafhankelijke kenmerken in uw inhoud worden gebruikt voor personalisatie, kunt u de inhoud niet testen met deze kenmerken.
* Alleen de volgende gegevenstypen worden ondersteund bij het invoeren van gegevens voor de varianten: getal (geheel getal en decimaal), tekenreeks, boolean en datumtype. Voor elk ander gegevenstype wordt een fout weergegeven.

## Varianten toevoegen {#profiles}

U kunt maximaal 30 varianten toevoegen om de inhoud te testen met behulp van een bestand of handmatig.

>[!NOTE]
>
>De toegevoegde varianten dienen alleen als testdoeleinden voor de huidige inhoud. De tags worden niet opgeslagen in Adobe Experience Platform, maar in uw gebruikersbrowsersessie. Dit houdt in dat ze niet worden weergegeven wanneer ze worden afgemeld of wanneer er vanaf een ander apparaat wordt gewerkt.

### Variant toevoegen met een bestand {#file}

Ga als volgt te werk als u een variant uit een bestand wilt toevoegen:

1. Klik op de koppeling **[!UICONTROL download sample]** om een bestandssjabloon op te halen en kies vervolgens de bestandsindeling die u wilt gebruiken (CSV, JSON of JSONLINES).
1. Klik op **[!UICONTROL Download]** en sla de sjabloon op de gewenste locatie op.
1. Open het bestand en vul de sjabloon naar wens in. De sjabloon bevat een kolom voor elk profielkenmerk dat in uw inhoud wordt gebruikt voor personalisatie.

   +++Bestandsmonster

   ```
   {
   "profile": {
       "attributes": {
       "person": {
           "name": {
               "lastName": "Doe",
               "firstName": "John"
               }
           }
       }
   }
   }
   ```

+++

1. Wanneer het bestand gereed is, klikt u op **[!UICONTROL Upload Input data]** om het te laden en de inhoud te testen.
1. Nadat het bestand is geüpload, wordt in het linkerdeelvenster voor elke regel van het bestand een vak toegevoegd. Elk vak bevat alle profielkenmerken die in de inhoud worden gebruikt voor personalisatie. U kunt de varianten nu gebruiken om een voorvertoning van de inhoud weer te geven in het rechterdeelvenster en proefdrukken te verzenden.

   ![](assets/simulate-custom-variants.png)

### Varianten handmatig toevoegen {#manual}

Voer de volgende stappen uit om een variant handmatig toe te voegen:

1. Klik op de knop **[!UICONTROL Create sample input]**.

   In het linkerdeelvenster wordt een vak toegevoegd met alle profielkenmerken die in de inhoud worden gebruikt voor personalisatie.

1. Vul de gegevens van de voorbeeldinvoer voor de variant in en klik op **[!UICONTROL Save]** .

   ![](assets/simulate-custom-add.png)

1. Nadat u varianten hebt toegevoegd, kunt u deze gebruiken om een voorvertoning van de inhoud weer te geven in het rechterdeelvenster en om proefdrukken te verzenden.

## Een voorvertoning van de inhoudvarianten weergeven {#preview}

Als u een voorvertoning van de inhoud wilt weergeven met een van de varianten, selecteert u het desbetreffende vak om de voorvertoning van de inhoud in de rechtersectie bij te werken met de informatie die u voor deze variant hebt ingevoerd.

In het onderstaande voorbeeld hebben we twee varianten toegevoegd voor de onderwerpregel van de e-mail:

| Selectie van variant 1 | Selectie van variant 2 |
|----------|-------------|
| ![](assets/simulate-custom-boxes.png) | ![](assets/simulate-custom-boxes2.png) |

U kunt een variant op elk gewenst moment verwijderen met de ellipknop in de rechterbovenhoek en door **[!UICONTROL Remove]** te selecteren. Als u informatie voor een variant wilt bewerken, klikt u op de knop voor weglatingsteken en selecteert u **[!UICONTROL Edit]** .

## Proefdrukken verzenden {#proofs}

Met Journey Optimizer kunt u proefdrukken naar e-mailadressen verzenden en tegelijkertijd een of meerdere varianten nabootsen die u in het simulatiescherm hebt toegevoegd. De stappen zijn als volgt:

1. Controleer of er varianten zijn toegevoegd om de inhoud te testen en klik op de knop **[!UICONTROL Send Proof]** .

1. Voer in het veld **[!UICONTROL Recipients]** het e-mailadres in waarnaar u de proefdruk wilt verzenden en klik vervolgens op **[!UICONTROL Add]** . Herhaal de bewerking om de proefdruk naar extra e-mailadressen te verzenden. U kunt maximaal tien proefontvangers toevoegen.

1. Selecteer in het onderste gedeelte van het scherm de variant die u wilt gebruiken in de proefdruk. U kunt meerdere varianten selecteren. In dat geval bevat het e-mailbericht evenveel proefdrukken als geselecteerde varianten.

   Selecteer de koppeling **[!UICONTROL View profile details]** voor meer informatie over een variant. Op deze manier kunt u de informatie die u in het vorige scherm hebt ingevoerd, weergeven voor de verschillende varianten.

   ![](assets/simulate-custom-proofs.png)

1. Klik op de knop **[!UICONTROL Send Proof]** om de proefdruk te verzenden.

1. Klik op de knop **[!UICONTROL View proofs]** in het scherm Inhoud simuleren om het verzenden van de proefdrukken bij te houden.

![](assets/simulate-custom-sent-proofs.png)
