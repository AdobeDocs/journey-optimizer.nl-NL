---
source-git-commit: 80d5f294491b35dcdbfe4976cb3ec4cf14384858
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

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

3. Volg de aanwijzingen
4. Gereed! ✨

### Optie 2: Terminal gebruiken

1. Open uw terminal in de opslagplaats.
2. Uitvoeren:

   ```bash
   ./setup-agents.sh
   ```

   Of handmatig:

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

Zie `.cursor-agents/AGENTS.md` voor een volledige lijst met beschikbare agents.

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
journey-optimizer.en/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  ├── setup-agent.md           ← Bootstrap agent
  └── help/                    ← Your documentation
```

De submodule verwijst naar:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Dit verzekert iedereen het zelfde, bijgewerkte agenten gebruikt.

**Hulp nodig?** Neem contact op met de leider van het documentatieteam of controleer de interne wiki.

