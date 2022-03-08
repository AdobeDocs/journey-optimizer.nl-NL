---
title: Helpers
description: Helpers
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 3%

---

# Helpers {#gs-helpers}

## Standaardwaarde voor alternatieven{#default-value}

De `Default Fallback Value` helper wordt gebruikt om een standaardreservewaarde terug te keren als een attribuut leeg of ongeldig is. Dit mechanisme werkt voor Profielkenmerken en Reisgebeurtenissen.

**Syntaxis**

```sql
Hello {%=profile.personalEmail.name.firstName ?: 'there' %}!
```

In dit voorbeeld wordt de waarde `there` wordt weergegeven als de `firstName` Het kenmerk van dit profiel is leeg of null.

## Voorwaarden{#if-function}

De `if` helper wordt gebruikt om een voorwaardelijk blok te bepalen.
Als de uitdrukkingsevaluatie waar terugkeert, wordt het blok teruggegeven anders wordt het overgeslagen.

**Syntaxis**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Na de `if` helper, u kunt een `else` om een codeblok op te geven dat moet worden uitgevoerd als dezelfde voorwaarde onwaar is.
De `elseif` De instructie geeft een nieuwe voorwaarde op die moet worden getest als de eerste instructie false retourneert.


**Indeling**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Voorbeelden**

1. **Verschillende opslagkoppelingen renderen op basis van voorwaardelijke expressies**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **E-mailadresextensie bepalen**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Een voorwaardelijke koppeling toevoegen**

   Met de volgende bewerking voegt u een koppeling toe naar de website &#39;www.adobe.com/academia&#39; voor profielen met alleen de e-mailadressen &#39;.edu&#39;, naar de website &#39;www.adobe.com/org&#39; voor profielen met de e-mailadressen &#39;.org&#39; en de standaard-URL &#39;www.adobe.com/users&#39; voor alle andere profielen:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Voorwaardelijke inhoud gebaseerd op segmentlidmaatschap**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

1. **Bepalen of een profiel al lid is**

   ```sql
   {%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
       You're a member!
   {%else%}
       You should be a member! Sign up now!
   {%/if%}
   ```

>[!NOTE]
>
>Meer over segmentatie en segmentatie de dienst leren, verwijs naar dit [sectie](../../segment/about-segments.md).


## Tenzij{#unless}

De `unless` helper wordt gebruikt om een voorwaardelijk blok te bepalen. Door bezwaar aan te tekenen tegen de `if`  helper, als de uitdrukkingsevaluatie vals terugkeert, wordt het blok teruggegeven.

**Syntaxis**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Voorbeeld**

Enige inhoud renderen op basis van extensie e-mailadres:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## Elk{#each}

De `each` helper wordt gebruikt om over een serie te herhalen.
De syntaxis van de hulplijn is ```{{#each ArrayName}}``` YourContent {{/each}} We kunnen naar de afzonderlijke arrayitems verwijzen met het trefwoord **dit** in het blok. De index van het element van de array kan worden gerenderd met {{@index}}.

**Syntaxis**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

**Voorbeeld**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Voorbeeld**

Een lijst met producten weergeven die deze gebruiker in zijn winkelwagentje heeft:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## Met{#with}

De `with` helper wordt gebruikt om het evaluatietoken van malplaatje-deel te veranderen.

**Syntaxis**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

De `with` helper is nuttig om een kortere wegvariabele ook te bepalen.

**Voorbeeld**

Wordt gebruikt met voor het aliasing van lange variabelenamen naar kortere namen:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Laat{#let}

De `let` De functie staat een uitdrukking toe om als variabele worden opgeslagen die later in een vraag moet worden gebruikt.

**Syntaxis**

```sql
{% let variable = expression %} {{variable}}
```

**Voorbeeld**

In het volgende voorbeeld worden alle sommen met producttotalen bij de transactie in USD weergegeven als de som groter is dan $100 en kleiner dan $1000.

```sql
{% let variable = expression %} {{variable}}
```
