---
solution: Journey Optimizer
product: journey optimizer
title: De reis publiceren
description: Leer hoe u een reis publiceert
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publiceren, reizen, live, geldigheid, controle
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
source-git-commit: 5bdacef2196592776c6b37708b0df0986460ca1f
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 1%

---

# Uw reis publiceren {#publishing-the-journey}

Als u een reis wilt activeren en nieuwe profielen wilt toestaan deze in te voeren, moet u deze publiceren. De publicatie maakt de reis live en functioneel. Voordat u gaat publiceren, moet u controleren of de rit voltooid en geldig is en eventuele fouten verhelpen. Een reis kan namelijk niet worden gepubliceerd als deze fouten bevat.

➡️ [Ontdek deze functie in video](#video)

## Publicatieproces {#journey-publication}

De stappen om een reis te publiceren zijn hieronder gedetailleerd:

1. Voordat u uw reis publiceert, moet u controleren of deze geldig en foutloos is. De reizen kunnen niet worden gepubliceerd als zij om het even welke fouten bevatten.

   * Leer hoe te om uw reis op [ deze pagina ](testing-the-journey.md) te testen.
   * Leer hoe te om uw reisfouten in [ problemen op te lossen deze sectie ](../building-journeys/troubleshooting.md#checking-for-errors-before-testing).

1. Als u de rit wilt publiceren, klikt u op de optie **[!UICONTROL Publish]** in het keuzemenu rechtsboven.

   >[!NOTE]
   >
   > Als uw reis aan een goedkeuringsbeleid onderworpen is, moet u goedkeuring vragen alvorens u het kunt publiceren. [Meer informatie](../test-approve/gs-approval.md)


   ![](assets/journeyuc1_18.png)

Wanneer de reis wordt gepubliceerd, is het op **read-only** wijze. Als een reis alleen-lezen is, kunt u alleen de activiteitslabels en -beschrijvingen, de naam van de reis en de beschrijving van de reis wijzigen. Als u meer wijzigingen aan een gepubliceerde reis moet maken, creeer [ een nieuwe versie ](journey-ui.md#journey-versions) van uw reis.

Wanneer u een reis stopt, wordt deze permanent stopgezet: alle mensen die op de reis stromen, worden permanent gestopt en de reis houdt op nieuwe ingangen toe te staan. Als u de reis opnieuw moet leiden, moet u het dupliceren en de nieuwe reis publiceren.


>[!IMPORTANT]
>
>Als er wijzigingen worden aangebracht in een biedbesluit dat wordt gebruikt in een reisbericht, moet u de reis ongedaan maken en opnieuw publiceren.  Dit zal ervoor zorgen dat de veranderingen in het reisbericht worden opgenomen en dat de boodschap in overeenstemming is met de meest recente updates.


## Journeyversies {#journey-versions}

In de reislijst, worden alle reisversies getoond met het versieaantal. Wanneer u een reis zoekt, verschijnen de nieuwste versies bij de eerste keer dat de toepassing wordt geopend boven aan de lijst. Vervolgens kunt u de gewenste sortering definiëren en wordt deze door de toepassing als gebruikervoorkeur behouden. De versie van de reis wordt ook weergegeven boven aan de interface van de reiseditie, boven het canvas.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Doorgaans kan een profiel niet meerdere keren op dezelfde reis tegelijk aanwezig zijn voor alle actieve versies van de reis. Als de terugkeer wordt toegelaten, kan een profiel een reis opnieuw ingaan, maar kan het niet doen tot zij dat vorige geval van de reis volledig verlaten. [Meer informatie](entry-management.md).

### Een nieuwe versie van een reis maken {#journey-create-new-version}

Als u zich aan een levende reis moet aanpassen, creeer een nieuwe versie van uw reis. Volg onderstaande stappen om een nieuwe versie van een bestaande reis te maken:

1. Open de meest recente versie van uw livereis, klik op **[!UICONTROL Create a new version]** en bevestig deze.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >U kunt alleen een nieuwe versie maken van de meest recente versie van een reis.

1. Breng uw wijzigingen aan, klik op **[!UICONTROL Publish]** en bevestig de selectie.

Vanaf het moment dat de reis wordt gepubliceerd, zullen individuen naar de recentste versie van de reis gaan. Mensen die al een vorige versie hebben ingevoerd, blijven er totdat ze klaar zijn met de reis. Als ze later weer dezelfde reis maken, gaan ze naar de meest recente versie.

Reisversies kunnen afzonderlijk worden gestopt. Alle versies van reizen hebben dezelfde naam.

Wanneer u een nieuwe versie van een reis publiceert, beëindigt de vorige versie automatisch en schakelt aan de **Gesloten** status. Er kan geen toegang tot de reis plaatsvinden. Zelfs als u de laatste versie stopt, blijft de vorige versie gesloten.


>[!NOTE]
>
>Specifieke garanties en beperkingen zijn van toepassing op de versiering van de reizen. Leer meer op [ deze pagina ](../start/guardrails.md#journey-versions-journey-versions-g).


## Hoe kan ik-video {#video}

Leer hoe u een reis publiceert in deze video:

>[!VIDEO](https://video.tv.adobe.com/v/3424998?quality=12)