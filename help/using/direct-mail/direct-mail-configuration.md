---
title: Directe-mailconfiguratie
description: Leer hoe u direct-mailkanaal kunt configureren in Journey Optimizer
feature: Direct Mail, Surface
topic: Content Management
role: User
level: Experienced
keyword: direct, mail, configuration, direct-mail, provider
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
source-git-commit: c7d8dd94bde49e8d02fe553fbac3942f55bf73fe
workflow-type: tm+mt
source-wordcount: '1194'
ht-degree: 1%

---

# Directe-mailconfiguratie {#direct-mail-configuration}

[!DNL Journey Optimizer] staat u toe om de dossiers te personaliseren en te produceren die door directe postleveranciers worden vereist om post naar uw klanten te verzenden.

Wanneer [een direct-mailbericht maken](../direct-mail/create-direct-mail.md), definieert u de doelpublieksgegevens, inclusief de gekozen contactgegevens (bijvoorbeeld het postadres). Er wordt dan automatisch een bestand met deze gegevens gegenereerd en geëxporteerd naar een server, waar uw directe-mailprovider het bestand kan ophalen en de daadwerkelijke verzending kan verzorgen.

Voordat u dit bestand kunt genereren, moet u het volgende maken:

1. A [bestand dat configuratie verplettert](#file-routing-configuration) om de server op te geven waar het bestand wordt geëxporteerd en het bestand indien nodig te coderen.

   >[!CAUTION]
   >
   >Om een dossier te creëren dat configuratie verplettert, moet u hebben **[!DNL Manage file routing]** ingebouwde machtiging. [Meer informatie](../administration/ootb-product-profiles.md#content-library-manager).

1. A [direct-mailoppervlak](#direct-mail-surface) dat het dossier zal van verwijzingen voorzien dat configuratie verplettert. Als u geen dossier gevormd hebt dat optie verplettert, zult u geen direct-mailoppervlak kunnen tot stand brengen.

## Bestands-routering configureren {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Definieer het bestand dat de configuratie verplettert"
>abstract="Nadat u een direct-mailbericht hebt gemaakt, wordt het bestand met de doelpublieksgegevens gegenereerd en geëxporteerd naar een server. U moet de serverdetails specificeren zodat uw direct-mailleverancier tot dat dossier voor levering direct-mail kan toegang hebben en gebruiken."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/create-direct-mail.html" text="Een direct-mailbericht maken"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Definieer het bestand dat de configuratie verplettert"
>abstract="U moet definiëren waar het bestand wordt geëxporteerd voordat uw direct-mailprovider het kan gebruiken."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configuratie van bestandsroutering"
>abstract="Selecteer het dossier dat configuratie van uw keus verplettert, die bepaalt waar het dossier voor uw direct-mailleverancier aan gebruik zal worden uitgevoerd."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Selecteer het servertype voor uw bestand"
>abstract="Kies welk type server u wilt gebruiken voor het exporteren van uw bestanden voor directe e-mail. Momenteel worden alleen Amazon S3 en SFTP ondersteund door Journey Optimizer."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Kies het AWS-gebied"
>abstract="Selecteer het geografische gebied van de AWS-server waarop u uw bestanden voor directe e-mail wilt exporteren. In het algemeen verdient het de voorkeur het gebied te kiezen dat het dichtst bij de locatie van uw directe-mailprovider ligt."

>[!NOTE]
>
>Amazon S3, SFTP en Azure worden momenteel ondersteund in [!DNL Journey Optimizer].

Een direct-mailbericht verzenden [!DNL Journey Optimizer] Hiermee genereert en exporteert u het bestand met de doelgegevens naar een server.

U moet die serverdetails specificeren zodat uw direct-mailleverancier tot dat dossier voor het leveren van post kan toegang hebben en gebruiken.

Om het dossier te vormen dat, volg de stappen hieronder verplettert.

>[!BEGINTABS]

>[!TAB Amazon S3]

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL File routing configuration]** > **[!UICONTROL File Routing]** en klik vervolgens op **[!UICONTROL Create routing configuration]**.

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. Plaats een naam voor uw configuratie.

1. Selecteren **Amazon S3** als de **[!UICONTROL Server type]** gebruiken voor het exporteren van de direct-mailbestanden.

   ![](assets/file-routing-config-type.png){width="800" align="center"}

1. Voer de gegevens en referenties voor de server in

   * **AWS bucket name**:Als u wilt weten waar u de naam van uw AWS-emmertje vindt, raadpleegt u [deze pagina](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBucket.html).

   * **AWS-toegangstoets**: Als u wilt weten waar u de AWS-toegangstoets-id vindt, raadpleegt u [deze pagina](https://docs.aws.amazon.com/IAM/latest/UserGuide/security-creds.html#access-keys-and-secret-access-keys).

   * **AWS geheime sleutel**: Als je wilt weten waar je de geheime sleutel van AWS vindt, raadpleegt u [deze pagina](https://aws.amazon.com/fr/blogs/security/wheres-my-secret-access-key/).

   * **AWS**: kies de optie **[!UICONTROL AWS region]** waar de serverinfrastructuur zal worden gevestigd. AWS-regio&#39;s zijn geografische gebieden die AWS gebruikt om haar cloudinfrastructuur te hosten. In het algemeen verdient het de voorkeur het gebied te kiezen dat het dichtst bij de locatie van uw directe-mailprovider ligt.

   ![](assets/file-routing-config-aws-region.png){width="800" align="center"}

1. Als u het bestand wilt versleutelen, kopieert en plakt u de coderingssleutel in de **[!UICONTROL PGP/GPG encryption key]** veld.

1. Selecteer **[!UICONTROL Submit]**. Het dossier dat configuratie verplettert wordt gecreeerd met **[!UICONTROL Active]** status. Het is nu klaar om in een [direct-mailoppervlak](#direct-mail-surface).

   U kunt ook **[!UICONTROL Save as draft]** om het dossier tot stand te brengen dat configuratie verplettert, maar u zult niet het in een oppervlakte kunnen selecteren tot het is **[!UICONTROL Active]**.

>[!TAB SFTP]

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL File routing configuration]** > **[!UICONTROL File Routing]** en klik vervolgens op **[!UICONTROL Create routing configuration]**.

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. Plaats een naam voor uw configuratie.

1. SFTP selecteren als **[!UICONTROL Server type]** gebruiken voor het exporteren van de direct-mailbestanden.

   ![](assets/file-routing-config-type-sftp.png){width="800" align="center"}

1. Voer de gegevens en referenties voor uw server in:

   * **Account**: Accountnaam gebruikt om verbinding te maken met de SFTP-server.

   * **Serveradres**: &#x200B; URL van de SFTP-server.

   * **Poort**: FTP-poortnummer.

   * **Wachtwoord**: &#x200B; Wachtwoord gebruikt om verbinding te maken met de SFTP-server.

   ![](assets/file-routing-config-sftp-detail.png)

1. Als u het bestand wilt versleutelen, kopieert en plakt u de coderingssleutel in de **[!UICONTROL PGP/GPG encryption key]** veld.

1. Selecteer **[!UICONTROL Submit]**. Het dossier dat configuratie verplettert wordt gecreeerd met **[!UICONTROL Active]** status. Het is nu klaar om in een [direct-mailoppervlak](#direct-mail-surface).

   U kunt ook **[!UICONTROL Save as draft]** om het dossier tot stand te brengen dat configuratie verplettert, maar u zult niet het in een oppervlakte kunnen selecteren tot het is **[!UICONTROL Active]**.

>[!TAB Azure]

1. Toegang krijgen tot de **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL File routing configuration]** > **[!UICONTROL File Routing]** en klik vervolgens op **[!UICONTROL Create routing configuration]**.

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. Plaats een naam voor uw configuratie.

1. Azure selecteren **[!UICONTROL Server type]** gebruiken voor het exporteren van de direct-mailbestanden.

   ![](assets/file-routing-config-type-azure.png){width="800" align="center"}

1. Voer de gegevens en referenties voor uw server in:

   * **Azure Connection String**: Als u uw **Azure Connection String**, zie [deze pagina](https://learn.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string#configure-a-connection-string-for-an-azure-storage-account).

     De **Azure Connection String** moet de volgende notatie volgen:

     `DefaultEndpointsProtocol=[http|https];AccountName=myAccountName;AccountKey=myAccountKey`

   * **Containernaam**: Als u uw **Containernaam**, zie [deze pagina](https://learn.microsoft.com/en-us/azure/storage/blobs/blob-containers-portal).

     De **Containernaam** moet alleen de naam van de container zonder slashes bevatten. Als u een pad in de container voor het opslaan van het bestand wilt opgeven, werkt u de bestandsnaam van de Direct Mail Campaign bij en voegt u het gewenste pad in.

1. Als u het bestand wilt versleutelen, kopieert en plakt u de coderingssleutel in de **[!UICONTROL PGP/GPG encryption key]** veld.

1. Selecteer **[!UICONTROL Submit]**. Het dossier dat configuratie verplettert wordt gecreeerd met **[!UICONTROL Active]** status. Het is nu klaar om in een [direct-mailoppervlak](#direct-mail-surface).

   U kunt ook **[!UICONTROL Save as draft]** om het dossier tot stand te brengen dat configuratie verplettert, maar u zult niet het in een oppervlakte kunnen selecteren tot het is **[!UICONTROL Active]**.

>[!ENDTABS]

## Een direct-mailoppervlak maken {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Instellingen voor direct mail definiëren"
>abstract="Een direct-mailoppervlak bevat de instellingen voor de opmaak van het bestand dat de doelpublieksgegevens bevat en wordt gebruikt door de mailprovider. U moet ook bepalen waar het dossier door het dossier te selecteren verplettert configuratie zal worden uitgevoerd."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/direct-mail-configuration.html#file-routing-configuration" text="Bestands-routering configureren"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="De drempelwaarde voor het splitsen van bestanden definiëren"
>abstract="U moet het maximumaantal records instellen voor elk bestand dat publieksgegevens bevat. U kunt een willekeurig getal tussen 1 en 200.000 records selecteren. Nadat de opgegeven drempelwaarde is bereikt, wordt een ander bestand gemaakt voor de resterende records."

Direct mailen met [!DNL Journey Optimizer], moet u een kanaaloppervlak maken om de instellingen te definiëren voor de opmaak van het bestand dat wordt gebruikt door de mailprovider.

Een direct-mailoppervlak moet ook het bestand bevatten dat de configuratie verplettert die de server definieert waar het direct-mailbestand wordt geëxporteerd.

1. Maak een kanaaloppervlak. [Meer informatie](../configuration/channel-surfaces.md)

1. Selecteer de **[!UICONTROL Direct mail]** kanaal.

   ![](assets/surface-direct-mail-channel.png){width="800" align="center"}

1. Bepaal de direct-mailmontages in de specifieke sectie van de configuratie van de kanaaloppervlakte.

   ![](assets/surface-direct-mail-settings.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. Selecteer de bestandsindeling: **[!UICONTROL CSV]** of **[!UICONTROL Text delimited]**.

1. Als u **[!UICONTROL Text delimited]** definieert u het kolomscheidingsteken van uw keuze: tabulatie, puntkomma, verticale balk of ampersand.

   ![](assets/surface-direct-mail-column-separator.png)

1. Selecteer de **[!UICONTROL File routing configuration]** onder de mensen die je creëerde. Hiermee bepaalt u waar het bestand wordt geëxporteerd zodat uw direct-mailprovider het kan gebruiken.

   >[!CAUTION]
   >
   >Als u geen dossier gevormd hebt dat optie verplettert, zult u geen direct-mailoppervlak kunnen tot stand brengen. [Meer informatie](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. Verzend het direct-mailoppervlak.

U kunt nu [een direct-mailbericht maken](../direct-mail/create-direct-mail.md) in een campagne. Nadat de campagne is gestart, wordt het bestand met de doelgegevens van het publiek automatisch geëxporteerd naar de server die u hebt gedefinieerd. De direct-mailprovider kan dat bestand vervolgens ophalen en doorgaan met de directe-maillevering.

>[!NOTE]
>
>Dubbele rijen waarbij alle waarden in de rij gelijk zijn, worden automatisch uit het bestand verwijderd.

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->