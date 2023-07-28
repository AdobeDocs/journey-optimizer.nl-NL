---
title: Een direct mailbericht testen en verzenden
description: Leer hoe u een direct-mailbericht test en verzendt in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
source-git-commit: 246205d13c1dd30b4f4769780f69e5acdd388e66
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 2%

---

# Een direct mailbericht testen en verzenden {#direct-mail-test-send}

## Een voorbeeld van het extractiebestand bekijken {#preview-dm}

Nadat de inhoud van het extractiebestand is gedefinieerd, kunt u er testprofielen voor gebruiken. Als u gepersonaliseerde inhoud hebt ingevoegd, kunt u met behulp van testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

1. Klik in het configuratiescherm voor de inhoud van het extractiebestand op **[!UICONTROL Simulate content]**.

   ![](assets/direct-mail-simulate-button.png){width="800" align="center"}

1. Klikken **[!UICONTROL Manage test profiles]** een testprofiel toevoegen.

1. Zoek uw testprofiel met de **[!UICONTROL Identity namespace]** en **[!UICONTROL Identity value]** velden. Klik vervolgens op **[!UICONTROL Add profile]**.

   ![](assets/direct-mail-test-profile.png){width="800" align="center"}

1. Nadat u het testprofiel hebt geselecteerd, kunt u het dialoogvenster **[!UICONTROL Add test profile]** venster.

1. Van de **Voorvertonen en testen** -venster, worden de testprofielgegevens toegevoegd aan de inhoud van het extractiebestand, zodat u kunt zien hoe het bestand wordt weergegeven.

   ![](assets/direct-mail-simulate.png){width="800" align="center"}

Als de bestandsinhoud klaar is om te worden verzonden, sluit u het simulatiescherm en klikt u op de knop **[!UICONTROL Review to activate]** knop.

## De campagne Direct mail valideren en activeren {#dm-validate}

Voordat u de campagne voor directe mail activeert, moet u controleren of de campagne en het extractiebestand op de juiste wijze zijn geconfigureerd. Om dit te doen, controleer alarm in de hogere sectie van de redacteur. Sommige zijn eenvoudige waarschuwingen, maar andere kunnen u verhinderen het bericht te verzenden. Er kunnen twee typen waarschuwingen optreden: waarschuwingen en fouten.

* **Waarschuwingen** verwijzen naar aanbevelingen en beste praktijken. Er wordt bijvoorbeeld een waarschuwingsbericht weergegeven als uw SMS-bericht leeg is.

* **Fouten** voorkomen dat u de campagne publiceert, zolang deze niet is opgelost. Er verschijnt bijvoorbeeld een foutbericht wanneer de onderwerpregel ontbreekt.

![](assets/direct-mail-review.png){width="800" align="center"}

Klik op de knop **[!UICONTROL Activate]** knop. Wanneer de campagne start, wordt het extractiebestand automatisch gegenereerd en geëxporteerd naar de server die in uw [bestand dat configuratie verplettert](../direct-mail/direct-mail-configuration.md).

Nadat u de campagne hebt verzonden, kunt u de impact van de campagne voor directe e-mail meten in de campagnerapporten. Raadpleeg deze sectie voor meer informatie over rapporten.
