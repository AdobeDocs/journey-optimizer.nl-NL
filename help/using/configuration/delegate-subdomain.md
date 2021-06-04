---
title: Subdomeinen delegeren
description: Leer hoe u uw subdomeinen kunt delegeren
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: e569e992530df5429ffb96f78ba28b53de0ded81
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 8%

---


# Een subdomein delegeren

Domeinnaamdelegatie is een methode die de eigenaar van een domeinnaam toestaat (technisch: een DNS-zone) om een onderverdeling ervan te delegeren (technisch gezien: een DNS-zone eronder, die een subzone kan worden genoemd) aan een andere entiteit. In feite, als een klant de streek &quot;example.com&quot;behandelt, kan hij subzone &quot;marketing.example.com&quot;aan Adobe afvaardigen.

Door subdomain voor gebruik met Adobe Optimizer te delegeren, kunnen de cliënten op Adobe vertrouwen om de DNS infrastructuur te handhaven die wordt vereist om industrie-standaardleveringsvereisten voor hun e-mailmarketing te ontmoeten verzendende domeinen, terwijl het blijven handhaven en DNS voor hun controleren
interne e-maildomeinen.

Met Journey Optimizer kunt u de subdomeinen volledig delegeren aan Adobe. Door dit te doen, zal Adobe berichten als beheerde dienst kunnen leveren door alle aspecten van DNS te controleren en te handhaven die voor het leveren, het teruggeven en het volgen van e-mailcampagnes worden vereist.

>[!NOTE]
>
>Door gebrek, [!DNL Journey Optimizer] staat het vergunningscontract u toe om tot 10 subdomeinen te delegeren. Neem contact op met uw Adobe als u deze beperking wilt verhogen.
>
>Het gebruik van CNAMEs voor subdomain delegatie wordt momenteel niet gesteund door Journey Optimizer.

Voer de volgende stappen uit om een nieuw subdomein te delegeren:

1. Open het menu **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** en klik vervolgens op **[!UICONTROL Delegate subdomain]**.

   ![](../assets/subdomain-delegate.png)

1. Geef de naam op van het subdomein dat u wilt delegeren.

   ![](../assets/subdomain-name.png)

1. De lijst van records die in uw DNS-serverweergaven moeten worden geplaatst. Kopieer deze records één voor één of download een CSV-bestand en navigeer vervolgens naar uw domeinhostingoplossing om de overeenkomende DNS-records te genereren.

   Zorg ervoor dat alle DNS verslagen in uw domein het ontvangen oplossing zijn geproduceerd. Als alles behoorlijk wordt gevormd, controleer de doos &quot;I bevestig...&quot;, dan klik **[!UICONTROL Submit]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >U kunt de verslagen tot stand brengen en de subdomeinconfiguratie voorleggen later op het gebruiken van **[!UICONTROL Save as draft]** knoop. Vervolgens kunt u de subdomeindelegatie hervatten door deze te openen vanuit de lijst met subdomeinen.

1. Nadat de subdomeindelegatie is verzonden, wordt het subdomein in de lijst weergegeven met de status **[!UICONTROL Processing]**. Raadpleeg [deze sectie](access-subdomains.md) voor meer informatie over de status van subdomeinen.

   De onderstaande controles en acties worden uitgevoerd totdat het subdomein is geverifieerd en kunnen worden gebruikt om berichten te verzenden.

   Deze stap wordt uitgevoerd door Adobe en kan tot 3 uur duren.

   1. Controleer of het subdomein is gedelegeerd aan Adobe DNS (NS-record, SOA-record, Zone-instelling, eigendomsrecord).
   1. Vorm DNS voor het domein,
   1. URL&#39;s voor bijhouden en spiegelen maken,
   1. Providing CDN Cloud Front,
   1. CDN SSL-certificaat maken, valideren en koppelen;
   1. Voorwaartse DNS maken,
   1. PTR-record maken.

   ![](../assets/subdomain-processing.png)

1. Zodra de controles succesvol zijn, krijgt subdomain de **[!UICONTROL Success]** status. Het is klaar om te worden gebruikt om berichten te leveren.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)


