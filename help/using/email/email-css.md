---
solution: Journey Optimizer
product: journey optimizer
title: Aangepaste CSS toevoegen aan uw e-mailinhoud
description: Leer hoe u aangepaste CSS rechtstreeks in de e-mailDesigner in Journey Optimizer toevoegt aan uw e-mailinhoud
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: css, editor, summary, email
source-git-commit: feb3576c230f2fb28ab031f87cc5f99263329b57
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Metagegevens toevoegen aan uw e-mailinhoud {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="Aangepaste CSS toevoegen"
>abstract="xxx."

Wanneer het ontwerpen van uw e-mails, kunt u uw eigen douaneCSS direct binnen [!DNL Journey Optimizer] [ E-mailDesigner ](get-started-email-design.md) toevoegen.

In het tekstgebied Aangepaste CSS toevoegen wordt een geldige CSS-tekenreeks verwacht.

![](assets/email-body-css.png)

Voorwaarden voor beschikbaarheid

De functie Aangepaste CSS toevoegen is alleen beschikbaar wanneer er inhoud is gedefinieerd in de editor. De gebruiker moet inhoud toevoegen in de editor om de sectie Aangepaste CSS toevoegen te kunnen zien. Als de gebruiker al zijn inhoud verwijdert, verdwijnt de sectie en wordt de aangepaste CSS niet toegepast. Als de gebruiker inhoud weer toevoegt, is de sectie beschikbaar en wordt de aangepaste css toegepast.

**Voorbeelden van ongeldige CSS input**

Ongeldige CSS kan niet worden opgeslagen en als de CSS ongeldig is, wordt een rode toast weergegeven om aan te geven dat de CSS niet kan worden opgeslagen.

`<style>` wordt niet geaccepteerd


```
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```


ontbrekende accolade is ongeldig

```
body {
 background: red; 
```
