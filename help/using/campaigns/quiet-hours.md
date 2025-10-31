---
solution: Journey Optimizer
product: journey optimizer
title: Quiet Hours
description: Leer hoe te verhinderen dat communicatie tijdens specifieke periodes wordt verzonden gebruikend rustige urenregels
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: stille uren, tijduitsluitingen, bedrijfsregels, regelsets, planning, campagnes
hide: true
hidefromtoc: true
source-git-commit: e5243565241551fab98a79fa118618535ce58de8
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 0%

---

# Quiet Hours {#quiet-hours}

>[!AVAILABILITY]
>
>De regels voor de korte uren zijn momenteel alleen beschikbaar voor een aantal organisaties (Beperkte Beschikbaarheid). Neem contact op met uw Adobe-vertegenwoordiger om aan de wachtlijst toe te voegen.

Met stille uren kunt u op tijd gebaseerde uitsluitingen definiëren voor e-mail-, SMS-, push- en WhatsApp-kanalen. Zij zorgen ervoor dat geen berichten tijdens specifieke periodes worden verzonden, die u helpen klantenvoorkeur en nalevingsvereisten respecteren.

U kunt stille uren toepassen via regelsets, die u kunt toewijzen aan afzonderlijke acties in campagnes of reizen voor een nauwkeurige controle.

## Waarom Quiet Hours gebruiken {#why-quiet-hours}

De stille uren helpen u klantenervaring verbeteren en naleving op verscheidene manieren handhaven:

* **respecteer klantenvoorkeur**: Vermijd verzendend berichten tijdens ongeschikte tijden (b.v., laat bij nacht of vroege ochtend), die merkreputatie en klantenloyaliteit negatief kunnen beïnvloeden.

* **verbeter overeenkomst**: Door berichten te verzenden wanneer de klanten waarschijnlijker zijn om op hen te zien en te handelen, verhoogt u de doeltreffendheid van uw mededelingen.

* **wettelijke naleving**: Bepaalde staten en gebieden verbieden SMS marketing berichten tijdens specifieke uren. De stille uren helpen u volgzaam met verordeningen zoals TCPA en staat-specifieke wetten van SMS blijven.

* **optimaliseer timing**: Als teveel tijd is overgegaan aangezien een bericht werd gepland, kan het niet meer relevant zijn. De stille uren staan u toe of verouderde berichten verwerpen of hen tot een aangewezen tijd houden.

## Hoe Quiet Uren werken {#how-quiet-hours-work}

De stille uren worden uitgevoerd door bedrijfsregels die u creeert en op uw campagnes en reizen toepast gebruikend regelreeksen.

Wanneer een bericht gepland is om tijdens een rustige uren periode te worden verzonden, [!DNL Adobe Journey Optimizer] neemt één van twee acties die op uw configuratie worden gebaseerd:

* **Weigeren**: Het bericht wordt permanent onderdrukt en verzendt nooit.
* **Rij**: Het bericht wordt gehouden en automatisch verzonden zodra de stille uren periode beëindigt.

Het systeem evalueert stille uren die op timezone van de ontvanger worden gebaseerd, die kan zijn:

* De tijdzone die is opgegeven in het profiel van de klant
* Een afgeleide tijdzone op basis van andere profiel- en gebeurtenisgegevens
* Een vaste tijdzone die u opgeeft in de regel

>[!NOTE]
>
>Het venster van de presuppressie: Het systeem begint mededelingen 30 minuten vóór stille urenbegin te onderdrukken, die ervoor zorgen dat geen berichten worden geleverd zodra de stille periode begint.

## Een regel voor stille uren maken {#create-quiet-hours-rule}

Een regel voor stille uren maken:

1. Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Business Rules]**.

1. Maak in de sectie **[!UICONTROL Rule sets]** een nieuwe regelset of selecteer een bestaande regel waaraan u de regel voor de stille uren wilt toevoegen.

1. Klik op **[!UICONTROL Create rule]** en selecteer **[!UICONTROL Quiet Hours]** als regeltype.

1. Configureer de instellingen voor stille uren:

   * **naam van de Regel**: Geef uw regel een beschrijvende naam.

   * **periode van de Tijd**: Bepaal wanneer de stille uren zouden moeten van toepassing zijn:
      * **Uren van de dag**: Plaats specifieke uren (b.v., 8 :00 PM aan 8 :00 AM)
      * **Dagen van de week**: Selecteer specifieke dagen (b.v., weekends)
      * **de data van de Douane**: Kies specifieke kalenderdata (b.v., vakanties)

   * **Tijdzone**: Selecteer hoe te om timezone te bepalen:
      * **lokale timezone van de Gebruiker**: Gebruik timezone van het profiel van elke ontvanger
      * **Specifieke timezone**: Pas een vaste timezone (b.v., Oost, Centraal) toe

   * **Actie**: Kies wat aan berichten tijdens stille uren gebeurt:
      * **verwerping**: De berichten worden permanent onderdrukt
      * **Rij**: De berichten worden gehouden en verzonden wanneer het stil uureind

1. Klik op **[!UICONTROL Save]** om de regel te maken.

## Quiet uren toepassen op campagnes en reizen {#apply-quiet-hours}

Als u eenmaal een regel voor stille uren hebt gemaakt, moet u deze toepassen op uw campagnes of reizen:

1. Open de campagne of de reis waar u rustige uren wilt toepassen.

1. Navigeer naar de handeling (E-mail, SMS, Push of WhatsApp) die u wilt besturen.

1. Zoek in de actieconfiguratie de sectie **[!UICONTROL Rule set]** .

1. Selecteer de regelreeks die uw rustige urenregel bevat.

1. Sla uw wijzigingen op.

De rustige urenregel is nu van toepassing op die specifieke handeling. Alle berichten die via deze actie worden verzonden, respecteren de configuratie van de stille uren.

>[!NOTE]
>
>De stille urenregels zijn op zowel geplande als gebeurtenis-teweeggebrachte mededelingen van toepassing. Zorg ervoor uw regelreeks behoorlijk wordt gevormd om uw gebruiksgeval te behandelen.

## Tijdzoneoverwegingen {#timezone-considerations}

Wanneer het gebruiken van de **lokale timezone van de Gebruiker** optie, [!DNL Adobe Journey Optimizer] zoekt timezone informatie in de volgende orde:

1. **tijdzonekenmerk van het Profiel**: De timezone uitdrukkelijk gespecificeerd in het profiel van de klant
2. **Overgenomen timezone**: Een tijdzone die op andere profielgegevens en gedragssignalen wordt berekend wordt gebaseerd

Als geen van beide beschikbaar is, kan het systeem rustige uren niet correct toepassen. Zorg ervoor dat uw klantprofielen informatie over de tijdzone bevatten voor optimale resultaten.

Wanneer het gebruiken van a **Specifieke timezone**, ontvangen alle ontvangers (of ontvangen niet) berichten die op die enige tijdzone, ongeacht hun daadwerkelijke plaats worden gebaseerd.

## Afvoerkanalen en beperkingen {#guardrails-limitations}

Houd rekening met het volgende wanneer u stille uren gebruikt:

* **de tijd van de Activering**: Het kan tot 20 minuten voor een regel of een regel nemen die wordt geplaatst om volledig worden geactiveerd. Plan dienovereenkomstig wanneer het creëren van of het wijzigen van regels.

* **de activeringsvertraging van de Campagne**: Na het associëren van bedrijfsregels, wacht minstens 10 minuten alvorens een reis te activeren of een campagne te verzenden om ervoor te zorgen de regels behoorlijk worden toegepast.

* **de vastgestelde grenzen van de Regel**: Momenteel, kunt u tot 3 actieve regelreeksen voor het kanaaldomein en 5 voor het reisdomein hebben.

* **de versietarief van het Bericht**: Wanneer het rustige uren en een rij gevormde berichten worden vrijgegeven, worden zij verzonden aan een tarief van maximaal 5.000 berichten per seconde per organisatie.

* **niet gesteund in**: De stille urenregels zijn momenteel niet beschikbaar voor de Orchestratie van de Campagne.

* **Droog looppas**: De stille urenregels worden niet geëvalueerd tijdens de runtime van de reis droge uitvoeringen.

## Rapportage {#reporting}

U kunt de standaardrapportfuncties gebruiken om te zien hoe rustige uren invloed hebben op uw campagnes en reizen:

* **All-time rapport**: De &quot;Uitgesloten sectie van Redenen&quot;toont het volume van klanten die geen mededelingen wegens stille urenregels, samen met de specifieke naam van de regelreeks ontvingen.

* **Levend rapport**: (Als beschikbaar) toont statistieken in real time over profielen die momenteel wegens stille uren wachten of wegens stille uren worden verworpen.

## Volgende stappen {#next-steps}

Zodra uw rustige urenregels worden gevormd en toegepast, kunt u:

* Controleer uw campagne of reis om ervoor te zorgen dat de regels correct worden gekoppeld
* Uw campagne of reis activeren
* De impact van stille uren in uw rapporten controleren

