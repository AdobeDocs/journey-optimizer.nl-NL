---
source-git-commit: 505810d58d7db1682cc434b0df6d1ec5f5edd23e
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---
# 🚀 Cursoragents installeren

De Agenten van de curseur zijn gedeelde hulpmiddelen die u helpen documentatie tot stand brengen en handhaven efficiënter.

## Eerste keer instellen

U moet slechts dit **eens** per bewaarplaats doen.

### Optie 1: Cursor gebruiken (aanbevolen ⭐)

1. Cursorchat openen (`Cmd+L` of `Ctrl+L`)
2. Type:

   ```
   @setup-agents
   ```

3. De agent zal automatisch:
   - Toegang tot SSH en HTTPS testen
   - De werkmethode gebruiken
   - Volg zo nodig de instructies
4. Gereed! ✨

**Nota:** de agent ontdekt automatisch als u SSH of HTTPS toegang tot `git.corp.adobe.com` hebt en gebruikt de aangewezen methode. Als geen van beide werkt, is er een instructies-instelling beschikbaar.

### Optie 2: Terminal gebruiken

1. Open uw terminal in de opslagplaats.
2. Uitvoeren:

   ```bash
   ./setup-agents.sh
   ```

   Het script wordt automatisch uitgevoerd:
   - Toegang tot SSH en HTTPS testen
   - De werkmethode gebruiken
   - Indien nodig installatie-instructies tonen

   Of handmatig (als u weet dat uw it is geconfigureerd):

   ```bash
   git submodule update --init --recursive
   ```

3. Gereed! ✨

## Verificatie

Controleer de installatie na de installatie:

```bash
ls .cursor-agents/agents/
```

U zou moeten zien:
- `draft-page-generator.md`
- `fix-grammar.md`
- enz.

## Gebruik

Na installatie kunt u agenten in Cursor gebruiken:

```
@draft-page      # Generate a new documentation page
@fix-grammar     # Fix grammar in current file
```

Zie [&#x200B; AGENTS.md &#x200B;](AGENTS.md) voor volledige lijst van beschikbare agenten.

## Bijwerken van agents

Om de recentste versie van alle agenten te krijgen:

### Optie 1: Cursor gebruiken

```
@update-agents
```

### Optie 2: Terminal gebruiken

```bash
git submodule update --remote
```

## Problemen oplossen

### Fout &quot;Agent niet gevonden&quot;

Als u deze fout ziet, zijn de agenten nog niet geïnstalleerd. Uitvoeren:

```
@setup-agents
```

### Submodule is leeg

Als `.cursor-agents/` bestaat maar leeg is:

```bash
git submodule update --init --recursive --remote
```

### Toestemming geweigerd

Zorg ervoor dat het opstellingsscript uitvoerbaar is:

```bash
chmod +x setup-agents.sh
```

### Netwerk-/VPN-problemen

- Zorg ervoor dat u verbinding hebt met Adobe VPN
- Netwerkconnectiviteit controleren
- Toegang tot it verifiëren:

  ```bash
  git ls-remote https://git.corp.adobe.com/AdobeDocs/CursorAgents
  ```

## Hoe het werkt

De Agenten van de curseur worden verdeeld als submodule van de a **it**:

```
your-repo/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  └── your-content/
```

De submodule verwijst naar:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Dit verzekert iedereen het zelfde, bijgewerkte agenten gebruikt.

## Voor onderhoudspersoneel

### Toevoegen aan een nieuwe opslagplaats

1. Voeg de submodule toe:

   ```bash
   git submodule add https://git.corp.adobe.com/AdobeDocs/CursorAgents.git .cursor-agents
   ```

2. Installatiebestanden kopiëren:
   - `setup-agents.sh`
   - `setup-agent.md` (plaatsen in hoofdmap, niet in submodule)
   - `INSTALL.md`

3. Vastleggen:

   ```bash
   git add .gitmodules .cursor-agents setup-agents.sh
   git commit -m "Add Cursor Agents submodule"
   ```

### De centrale gegevensbank bijwerken

Wijzigingen in agenten moeten worden aangebracht in:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Alle repositories ontvangen updates via `git submodule update --remote` .

&#x200B;---

**Hulp nodig?** Neem contact op met de leider van het documentatieteam of controleer de interne wiki.
