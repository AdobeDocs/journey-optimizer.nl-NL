---
title: Directe-mailconfiguratie
description: Leer hoe u direct-mailkanaal kunt configureren in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 1f6b29d781abc17e238e4a3e051dc61d250b37a0
workflow-type: tm+mt
source-wordcount: '794'
ht-degree: 3%

---

# Directe-mailconfiguratie {#direct-mail-configuration}

[!DNL Journey Optimizer] staat u toe om de dossiers te personaliseren en te produceren die door directe postleveranciers worden vereist om post naar uw klanten te verzenden.

Wanneer u een directe postlevering voorbereidt, [!DNL Journey Optimizer] genereert een bestand met alle doelprofielen en de gekozen contactgegevens (bijvoorbeeld het postadres). U kunt dit bestand dan naar uw direct-mailprovider sturen, die voor de werkelijke verzending zorgt.

Als u een direct-mailbericht wilt verzenden, moet u een bestand maken en uploaden naar een server. Voordat u dit kunt doen, moet u een [bestand dat configuratie verplettert](#file-routing-configuration) en [direct-mailoppervlak](#direct-mail-surface) dat het dossier zal van verwijzingen voorzien dat configuratie verplettert.

## Bestands-routering configureren {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Bepaal de montages van het dossier dat configuratie verplettert"
>abstract="Wanneer u het directe-mailbericht maakt, genereert u het bestand met alle vereiste profielgegevens. Dit bestand moet worden geëxporteerd en geüpload naar een server, zodat uw direct-mailprovider dat bestand kan openen en gebruiken voor het verzenden van direct mail."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Bepaal de montages van het dossier dat configuratie verplettert"
>abstract="U moet definiëren waar het bestand wordt geëxporteerd en geüpload, zodat uw direct-mailprovider dit kan gebruiken."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configuratie van bestandsroutering"
>abstract="Selecteer het dossier dat configuratie van uw keus verplettert, die bepaalt waar het dossier zal worden uitgevoerd en voor uw direct-mailleverancier aan gebruik geupload."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Selecteer het servertype voor uw dossier het verpletteren"
>abstract="Kies welke server u wilt gebruiken voor het uploaden en opslaan van de bestanden voor directe e-mail. Momenteel worden alleen Amazon S3 en SFTP ondersteund."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Kies het AWS-gebied"
>abstract="Selecteer het geografische gebied waar u uw bestanden voor directe e-mail wilt exporteren en uploaden. Voor optimaal gebruik wordt aanbevolen het dichtstbijzijnde gebied te kiezen dat uw cloudinfrastructuur host."

1. Toegang krijgen tot **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL File routing configuration]** > **[!UICONTROL File Routing]** en klik vervolgens op **[!UICONTROL Create routing configuration]**.

   ![](assets/file-routing-config-button.png)

1. Plaats een naam voor uw configuratie.

1. Selecteer de configuratie **[!UICONTROL Server type]**, d.w.z. de server die u wilt gebruiken voor het uploaden en opslaan van de direct-mailbestanden.

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >Momenteel zijn alleen Amazon S3 en SFTP beschikbaar.

   Wanneer u het directe-mailbericht maakt, genereert u het bestand met alle vereiste profielgegevens. Dit bestand moet worden geëxporteerd en geüpload naar een server, zodat uw direct-mailprovider dat bestand kan openen en gebruiken voor het verzenden van direct mail.

1. Vul de details en de geloofsbrieven in specifiek voor het geselecteerde configuratietype, zoals serveradres, toegangssleutel, enz.

   ![](assets/file-routing-config-sftp-details.png)

1. Als u **[!UICONTROL Amazon S3]**, kiest u het AWS-gebied waar u uw bestanden voor directe e-mail wilt exporteren en uploaden.

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >AWS-regio&#39;s zijn afzonderlijke geografische gebieden over de hele wereld die AWS gebruikt om zijn infrastructuur te huisvesten. Voor optimaal gebruik wordt aanbevolen het dichtstbijzijnde gebied te kiezen dat uw cloudinfrastructuur host.

1. Selecteer **[!UICONTROL Submit]**. Het dossier dat configuratie verplettert wordt gecreeerd met **[!UICONTROL Active]** status. Het is nu klaar om in een direct-mailoppervlak te worden gebruikt om direct-mail van te leveren [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >U kunt ook **[!UICONTROL Save as draft]** om het dossier tot stand te brengen dat configuratie verplettert, maar u zult niet het in een oppervlakte kunnen selecteren tot het is **[!UICONTROL Active]**.

## Een direct-mailoppervlak maken {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Instellingen voor direct mail definiëren"
>abstract="Een direct-mailoppervlak bevat de instellingen die betrekking hebben op de opmaak van het bestand met profielgegevens voor direct-mail. U moet ook bepalen waar het dossier door het dossier te selecteren verplettert configuratie zal worden uitgevoerd."

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="De drempelwaarde voor het splitsen van bestanden definiëren"
>abstract="U moet het maximumaantal records instellen voor elk bestand dat profielgegevens bevat. Nadat de opgegeven drempelwaarde is bereikt, wordt een ander bestand gemaakt voor de resterende records."

Zodra het dossier verpletteren is gevormd, moet u een kanaaloppervlakte tot stand brengen om directe post van te kunnen leveren [!DNL Journey Optimizer]. In elk oppervlak, zult u een dossier moeten selecteren dat configuratie verplettert.

1. Maak een kanaaloppervlak. [Meer informatie](channel-surfaces.md)

1. Selecteer **[!UICONTROL Direct mail]** kanaal.

   ![](assets/surface-direct-mail-channel.png)

1. Bepaal de direct-mailmontages in de specifieke sectie van de configuratie van de kanaaloppervlakte.

   ![](assets/surface-direct-mail-settings.png)

1. Selecteer de bestandsindeling: **[!UICONTROL CSV]** of **[!UICONTROL Text delimited]**.

1. In de **[!UICONTROL Insertion]** kunt u dubbele rijen automatisch verwijderen.

1. Definieer het maximumaantal records (dat wil zeggen rijen) voor elk bestand dat profielgegevens bevat. Nadat de opgegeven drempelwaarde is bereikt, wordt een ander bestand gemaakt voor de resterende records.

   ![](assets/surface-direct-mail-split.png)

   Als het bestand bijvoorbeeld 100.000 records bevat en de drempellimiet is ingesteld op 60.000, worden de records gesplitst in twee bestanden. Het eerste bestand bevat 60.000 rijen en het tweede bestand bevat de resterende 40.000 rijen.

   >[!NOTE]
   >
   >U kunt een willekeurig getal tussen 1 en 200.000 records instellen. Dit betekent dat elk bestand ten minste 1 rij en maximaal 200.000 rijen moet bevatten.

1. Tot slot selecteert u **[!UICONTROL File routing configuration]** onder de mensen die je creëerde. Hiermee bepaalt u waar het bestand wordt geëxporteerd en geüpload zodat uw direct-mailprovider het kan gebruiken.

   >[!CAUTION]
   >
   >Als u geen dossier gevormd hebt dat optie verplettert, zult u geen direct-mailoppervlak kunnen tot stand brengen. [Meer informatie](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)