---
solution: Journey Optimizer
product: journey optimizer
title: Gegevenssets exporteren naar opslaglocaties in de cloud
description: Leer hoe u uw gegevenssets exporteert met Adobe Experience Platform-cloudopslagbestemmingen.
role: User
level: Beginner
keywords: platform, data Lake, create, Lake, datasets, profile
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: 08f24547237c01c581248d675c55c834c261b173
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 1%

---

# Gegevenssets exporteren naar opslaglocaties in de cloud {#export-datasets}

Met Journey Optimizer kunt u een live verbinding maken met opslaglocaties in de cloud om de inhoud van uw gegevenssets te exporteren.

Door uw gegevens periodiek te exporteren, kunt u ervoor zorgen dat u een volledig en bijgewerkt overzicht hebt van de interactie van uw klant, zodat u deze direct kunt gebruiken voor rapportage, archivering of gegevensanalyse.

## Beschikbare cloudopslagbestemmingen {#destinations}

U kunt gegevenssets exporteren naar 6 cloudopslagdoelen die toegankelijk zijn vanuit de **[!UICONTROL Destinations]** in het menu **[!UICONTROL Catalog]** tab.

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>Deze bestemmingen zijn allemaal beschikbaar in bèta en kunnen worden gewijzigd.

Gedetailleerde informatie over elke bestemming is beschikbaar in de documentatie van Adobe Experience Platform:

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [Gegevenslandingszone](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Google Cloud Storage](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## Journey Optimizer-gegevenssets beschikbaar voor exporteren {#datasets}

Begrijp van de lijst hieronder welke datasets van Journey Optimizer u afhankelijk van uw productrij kunt uitvoeren (zie [Journey Optimizer-productbeschrijving](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}) |Gegevensset|Beschrijving|Niveau| | — | — | — | | Gegevensset voor AJO BCC-feedbackgebeurtenis | Gegevensset voor AJO BCC-feedbackgebeurtenis | Eerste | | Gegevensset AJO-indeling | Gegevensset voor het invoeren van feedback over e-mail- en pushgebeurtenissen van Journey Optimizer. Gemaakt met SDK. | Eerste | | Dataset AJO-service voor instemming | Hiermee wordt informatie over de toestemming van een profiel opgeslagen. | Eerste | | Dataset voor AJO Email Tracking Experience Event | Interactielogboeken voor e-mailkanaal die worden gebruikt voor rapportage en het creëren van publiek.  | Eerste | | Gegevensset AJO Entiteit | Gegevensset voor het opslaan van metagegevens van entiteiten voor berichten die naar de eindgebruiker worden verzonden.  | Eerste | | Dataset voor AJO Inbound Activity Event | Gegevensset voor Journey Optimizer-webkanalen en inApp-kanalen voor levering- en interactiegebeurtenissen. | Eerste | | Gegevensset van AJO Interactive Messaging Profile | Profielen voor opslag die zijn gemaakt ter ondersteuning van door API&#39;s geactiveerde campagnes | Eerste | | Dataset voor AJO-feedbackgebeurtenis | Berichtenleveringslogboeken. Informatie over alle berichtlevering van Journey Optimizer voor rapportage en het creëren van publiek. De terugkoppeling van e-mailISPs op grenzen wordt ook geregistreerd in deze dataset. | Eerste | | Uitbreiding AJO-profieltellers | Bevat een kaart met objecten die counter_value en endDate bevatten, afgesloten door counter_id | Eerste | | Gegevensset van AJO-pushprofiel | Hiermee worden push-tokens van een profiel opgeslagen. | Eerste | | Dataset voor AJO-gebeurtenis voor het bijhouden van push | Interactielogboeken voor pushkanaal die worden gebruikt voor rapportage en het maken van publiek.  | Eerste | | Gegevensset AJO-oppervlakken | Lege gegevensset met betrekking tot het schema voor binnenkomende oppervlakken van Journey Optimizer | Eerste | | AOOutputForUPSDataset | Bevat alle AO-publiekslidmaatschappen die naar UPS moeten worden geschreven | Eerste | | Gegevensset van publiek orkestprofiel | Gegenereerd door publiekscompositie voor publiek publiek in compositie. Bevat alle publiek van de Audience COmposition, hun attributen en verrijkingsgegevens | Eerste | | Beslissingsobjectrepositofaciliteit - Activiteiten | Ook bekend als Besluiten in de gebruikersinterface. Maar dit zijn de objecten die een gebruiker maakt die alle bouwstenen samenbrengt, inclusief de beslissingslogica. Bijvoorbeeld, voor een bepaalde plaatsing (plaats), die zou moeten worden overwogen (de inzameling van de aanbieding), en welke rangschikkingsmethode aan gebruik op die aanbiedingen. | Ultieme | | Beslissingsobjectrepository - Terugvalvoorstellen | dit is de opslagplaats voor het andere type aanbieding dat een gebruiker maakt. Als zij niet in aanmerking komen voor een gepersonaliseerd aanbod en als zij iets moeten zien, zullen zij tenminste het terugvalaanbod zien. Deze dataset bevat de attributen voor dit type aanbieding | Ultieme | | Beslissingsobjectrepository - Aangepaste aanbiedingen | dit is de opslagplaats voor een soort aanbieding die een gebruiker maakt. Deze dataset bevat dus de kenmerken van dit type aanbieding | Ultieme | | Beslissingsobjectrepository - Plaatsingen | dit is de opslagplaats van objecten die bepalen waar een aanbieding moet worden weergegeven. | Ultieme | | Reisstapgebeurtenissen | Hiermee legt u alle ervaringsgebeurtenissen voor de stappen die door Journey Optimizer worden gegenereerd en die door services zoals Reporting worden verbruikt. | Eerste | | Reizen | Behuizing-informatie van metagegevensreeksen voor elke stap van de reis | Eerste | | ODE-besluitGebeurtenissen - snelle besluitvorming | Telkens wanneer we een besluit nemen op basis van een verzoek, tellen we dat als een beslissingsgebeurtenis | Ultieme |

## Vereisten {#prerequisites}

Om datasets uit te voeren, hebt u nodig [toegangsbeheermachtigingen](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions) hieronder weergegeven. Lees de [toegangsbeheeroverzicht](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) of neem contact op met de productbeheerder om de vereiste machtigingen te verkrijgen.

| Categorie | Machtiging |
|--|--|
| Doelen | Dataset-doelen beheren en activeren |
| Data management | Gegevensbestanden weergeven |
| Doelen | Doelen weergeven |

## Belangrijkste stappen om gegevenssets te exporteren {#main-steps}

De belangrijkste stappen om een dataset naar een plaats van de wolkenopslag uit te voeren zijn als volgt:

![](assets/dataset-export-process.png)

Gedetailleerde informatie over elke stap is beschikbaar in de documentatie van Adobe Experience Platform: [Gegevenssets exporteren naar cloudopslagbestemmingen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html).

1. **De bestemming voor cloudopslag instellen**. Als u dit nog niet hebt gedaan, maakt u verbinding met een bestemming voor cloudopslag vanuit de doelcatalogus. [Leer hoe u een nieuwe doelverbinding maakt](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html#setup)

   <!--![](assets/dataset-export-setup.png)-->

1. **Selecteer de bestemming voor cloudopslag** waar u uw datasets wilt uitvoeren. Klik in de catalogus met doelen op de knop **[!UICONTROL Export datasets]** op de gewenste kaart en selecteer de te gebruiken verbinding.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >Als u Adobe Journey Optimizer samen met de profielen van de Klant in real time gebruikt, zullen de bestemmingskaarten een &quot;Activate&quot;knoop tonen, die u toestaat om datasets zowel uit te voeren als publiek voor deze bestemming te activeren, afhankelijk van de toestemmingen u hebt toegelaten.

1. **Selecteer de gegevensset(s)** die u naar het geselecteerde doel wilt exporteren. [Meer informatie over Journey Optimizer-gegevenssets beschikbaar voor exporteren](#datasets)

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Het exporteren plannen** van uw gegevensset. Geef aan wanneer het exporteren moet beginnen en met welke frequentie dit moet gebeuren.

   <!--![](assets/dataset-export-schedule.png)-->

1. **De export controleren en bevestigen** door de samenvatting te controleren die aan het eind van de configuratie toont.

   <!--![](assets/dataset-export-review.png)-->

Zodra het exporteren is voltooid, wordt de inhoud van uw gegevensset op de locatie van uw cloudopslag gedeponeerd volgens het schema dat u hebt geconfigureerd. [Leer hoe u succesvolle gegevenssetexport kunt controleren](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
