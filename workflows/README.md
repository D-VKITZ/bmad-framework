<div align="center">

# 🔄 Workflows

### Session-Management, Übergabe & Ralph-Loop™ Orchestrierung

![Startup](https://img.shields.io/badge/Startup-Workflow-fa1e4e?style=for-the-badge&logo=rocket&logoColor=white)
![Handoff](https://img.shields.io/badge/Handoff-7_Punkte-00ff88?style=for-the-badge&logo=handshake&logoColor=white)
![Ralph-Loop](https://img.shields.io/badge/Ralph--Loop™-6_Phasen-ffb800?style=for-the-badge&logo=loop&logoColor=black)
![Session](https://img.shields.io/badge/Session-Managed-3b82f6?style=for-the-badge&logo=timer&logoColor=white)
![Context](https://img.shields.io/badge/Context-Fresh-6366f1?style=for-the-badge&logo=sparkles&logoColor=white)
![Recovery](https://img.shields.io/badge/Recovery-Auto-00ff88?style=for-the-badge&logo=shield&logoColor=white)
![Pre-Session](https://img.shields.io/badge/Pre--Session-Init-3b82f6?style=for-the-badge&logo=play&logoColor=white)
![Active](https://img.shields.io/badge/Active-Execute-fa1e4e?style=for-the-badge&logo=code&logoColor=white)
![Post-Session](https://img.shields.io/badge/Post--Session-Handoff-ffb800?style=for-the-badge&logo=save&logoColor=black)
![Git Hooks](https://img.shields.io/badge/Git_Hooks-Active-00ff88?style=for-the-badge&logo=git&logoColor=white)
![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub_Actions-6366f1?style=for-the-badge&logo=githubactions&logoColor=white)
![Auto-Save](https://img.shields.io/badge/Auto--Save-60s-3b82f6?style=for-the-badge&logo=save&logoColor=white)
![Health](https://img.shields.io/badge/Health_Check-30s-00ff88?style=for-the-badge&logo=heart&logoColor=white)
![Validated](https://img.shields.io/badge/Validated-✓-00ff88?style=for-the-badge&logo=checkmarx&logoColor=white)
![Documented](https://img.shields.io/badge/Documented-Complete-3b82f6?style=for-the-badge&logo=readme&logoColor=white)
![Versioned](https://img.shields.io/badge/Versioned-Git-ffb800?style=for-the-badge&logo=git&logoColor=black)
![Reproducible](https://img.shields.io/badge/Reproducible-100%25-6366f1?style=for-the-badge&logo=repeat&logoColor=white)
![BMAD](https://img.shields.io/badge/BMAD™-Workflows-fa1e4e?style=for-the-badge&logo=robot&logoColor=white)

---

*Session-Workflows des [BMAD™ Frameworks](https://github.com/D-VKITZ/bmad-framework) · DEVKiTZ™ Ökosystem*

</div>

---

## 📖 Übersicht

Der **Workflows-Ordner** enthält die drei zentralen Ablauf-Definitionen des BMAD™ Frameworks: den **Startup-Workflow** (Session-Beginn), den **Handoff-Workflow** (Session-Übergabe) und das **Ralph-Loop™ Diagramm** (Task-Execution). Zusammen bilden sie das Rückgrat für konsistente, reproduzierbare Entwicklungs-Sessions — ohne Context-Drift und ohne Wissensverlust.

---

## 📋 Workflow-Übersicht

| Workflow | Datei | Trigger | Phase | Beschreibung |
|:---------|:------|:--------|:------|:-------------|
| 🚀 **Startup** | `startup.md` | Session-Beginn | Pre-Session | Pflichtdateien lesen, Context laden, Agenten init |
| 🤝 **Handoff** | `handoff.md` | Session-Ende | Post-Session | 7-Punkte Checkliste, R24, Dreifach-Verankerung |
| 🔄 **Ralph-Loop** | `ralph-loop-diagram.md` | Jeder Task | Active | 6 Phasen, Entscheidungspunkte, Rollback |

---

## 🔄 Workflow-Lifecycle

```mermaid
flowchart LR
    subgraph PRE["🚀 Pre-Session"]
        S1["📄 Pflichtdateien lesen"]
        S2["🧠 Context laden"]
        S3["🤖 Agenten initialisieren"]
        S4["📊 Status prüfen"]
        S1 --> S2 --> S3 --> S4
    end

    subgraph ACTIVE["⚡ Active Session"]
        A1["📋 Tasks aus Queue"]
        A2["🔄 Ralph-Loop™"]
        A3["💾 Auto-Save"]
        A4["🏥 Health-Check"]
        A1 --> A2
        A2 -.-> A3
        A2 -.-> A4
    end

    subgraph POST["🤝 Post-Session"]
        P1["✅ 7-Punkte Checkliste"]
        P2["⚠️ R24 ALARM prüfen"]
        P3["⚓ Dreifach-Verankerung"]
        P4["📦 Git Commit"]
        P1 --> P2 --> P3 --> P4
    end

    S4 --> A1
    A2 -->|"Session Ende"| P1

    style PRE fill:#060608,stroke:#3b82f6,stroke-width:2px,color:#fff
    style ACTIVE fill:#060608,stroke:#fa1e4e,stroke-width:3px,color:#fff
    style POST fill:#060608,stroke:#00ff88,stroke-width:2px,color:#fff
```

---

## 🚀 startup.md — Session-Start

### Pflichtdateien-Kaskade

Beim Start jeder DEVKiTZ™-Session müssen diese Dateien in **exakter Reihenfolge** gelesen werden:

| Priorität | Datei | Pfad | Inhalt |
|:----------|:------|:-----|:-------|
| 1 | `CLAUDE.md` | `C:\DEVKiTZ\CLAUDE.md` | Regelwerk für Claude-basierte Agenten |
| 2 | `GEMINI.md` | `C:\DEVKiTZ\GEMINI.md` | Gedächtnis + Regelwerk für Gemini |
| 3 | `REGELWERK.md` | `C:\DEVKiTZ\REGELWERK.md` | Eiserne Regeln + Standards |
| 4 | `BLAUPAUSE.md` | `01_PROJECTS\01_dashboard\BLAUPAUSE.md` | Dashboard-Architektur |

### 5-Schritt Startup-Sequenz

```javascript
// Session-Start Protokoll
async function startSession() {
  // Schritt 1: Pflichtdateien laden
  const claude = await readFile('C:/DEVKiTZ/CLAUDE.md');
  const gemini = await readFile('C:/DEVKiTZ/GEMINI.md');
  const regelwerk = await readFile('C:/DEVKiTZ/REGELWERK.md');
  const blaupause = await readFile('01_PROJECTS/01_dashboard/BLAUPAUSE.md');

  // Schritt 2: Agenten-Registry prüfen
  const agents = await loadJSON('AGENTS.md');
  
  // Schritt 3: Letzte Session-Artefakte laden
  const lastSession = await iceberg.getLatest('session');
  
  // Schritt 4: Offene Tasks aus prd.json
  const prd = await loadJSON('prd.json');
  const openTasks = prd.tasks.filter(t => t.status !== 'completed');
  
  // Schritt 5: Health-Check aller Systeme
  const health = await checkAllSystems();
  
  return {
    context: { claude, gemini, regelwerk, blaupause },
    agents,
    openTasks,
    health
  };
}
```

---

## 🤝 handoff.md — Session-Übergabe

### 7-Punkte Checkliste

Bei **jedem** Session-Ende muss diese Checkliste abgearbeitet werden. James™ überwacht die Einhaltung.

| # | Prüfpunkt | Verantwortlich | Beschreibung |
|:--|:----------|:---------------|:-------------|
| 1 | ☐ `CLAUDE.md` aktuell? | James™ | Neue Regeln, Erkenntnisse eingetragen? |
| 2 | ☐ `GEMINI.md` aktuell? | James™ | Gedächtnis ergänzt? |
| 3 | ☐ Artefakte dreifach verankert? | Dokumentar™ | Iceberg + Hub + Copilot |
| 4 | ☐ `features.json` aktualisiert? | Developer™ | Neue/geänderte Module registriert? |
| 5 | ☐ Git committed? | Developer™ | Conventional Commit erstellt? |
| 6 | ☐ Walkthrough/Notes gespeichert? | Dokumentar™ | Zusammenfassung der Arbeit |
| 7 | ☐ Neue §-Einträge für Features? | PM™ | Neue Regeln dokumentiert? |

### R24 ALARM Protokoll

Vor jeder Verschiebung nach `99_ARCHIVE/`:

```
1. 🚨 R24 ALARM aktivieren
2. 📋 Liste der betroffenen Dateien erstellen
3. 👤 777 informieren und Bestätigung abwarten
4. ✅ Erst nach expliziter Genehmigung verschieben
5. ⚓ Dreifach-Verankerung der archivierten Artefakte
6. 📝 Walkthrough der Archivierung erstellen
```

---

## 🔄 ralph-loop-diagram.md — Ralph-Loop™

### 6-Phasen mit Entscheidungspunkten

```mermaid
flowchart TD
    START(("🎯 Task aus<br/>prd.json")) --> P1

    P1["📖 Phase 1: LESEN<br/>────────────<br/>• prd.json laden<br/>• Constitution lesen<br/>• AGENTS.md prüfen<br/>• Relevante Artefakte filtern"]
    P1 --> D1{"Context<br/>gültig?"}
    D1 -->|"✅ Ja"| P2
    D1 -->|"❌ Nein"| ERR1["⚠️ Fallback:<br/>Cache nutzen"]
    ERR1 --> P2

    P2["🚀 Phase 2: SPAWN<br/>────────────<br/>• Neue Agent-Instanz<br/>• Frischer Kontext<br/>• Timeout: 30min<br/>• Retry-Counter: 3"]
    P2 --> D2{"Agent<br/>gestartet?"}
    D2 -->|"✅ Ja"| P3
    D2 -->|"❌ Nein"| ERR2["🔄 Retry mit<br/>Backoff"]
    ERR2 --> P2

    P3["⚡ Phase 3: EXECUTE<br/>────────────<br/>• Developer™ coded<br/>• Atomarer Task<br/>• Shared Scripts nutzen<br/>• esc() enforced"]
    P3 --> D3{"Timeout<br/>erreicht?"}
    D3 -->|"❌ Nein"| P4
    D3 -->|"⏰ Ja"| ERR3["⏸️ Task<br/>pausieren"]

    P4["✅ Phase 4: VERIFY<br/>────────────<br/>• Reviewer™ prüft<br/>• Tester™ testet<br/>• Quality Gates<br/>• Screenshots"]
    P4 --> D4{"Alle Tests<br/>bestanden?"}
    D4 -->|"✅ Ja"| P5
    D4 -->|"❌ Nein"| RB["↩️ Rollback<br/>→ zurück zu P3"]
    RB --> P3

    P5["📦 Phase 5: COMMIT<br/>────────────<br/>• Git Commit<br/>• prd.json Update<br/>• ⚓ Dreifach-Verankerung<br/>• features.json Update"]
    P5 --> P6

    P6{"🔄 Phase 6: LOOP<br/>────────────<br/>Weitere Tasks<br/>in der Queue?"}
    P6 -->|"✅ Ja"| P1
    P6 -->|"❌ Nein"| DONE(("✅ Fertig"))

    style P1 fill:#3b82f6,color:#fff,stroke:#3b82f6
    style P2 fill:#6366f1,color:#fff,stroke:#6366f1
    style P3 fill:#fa1e4e,color:#fff,stroke:#fa1e4e
    style P4 fill:#00ff88,color:#060608,stroke:#00ff88
    style P5 fill:#ffb800,color:#060608,stroke:#ffb800
    style P6 fill:#fa1e4e,color:#fff,stroke:#fa1e4e
    style DONE fill:#00ff88,color:#060608,stroke:#00ff88
```

---

## 🏥 Background-Loops

Während der aktiven Session laufen 8 Background-Loops parallel:

| # | Loop | Intervall | Funktion | Ampel |
|:--|:-----|:----------|:---------|:------|
| 1 | 🔄 Ralph-Loop | Pro Task | Task-Execution Pipeline | 🟢 |
| 2 | 💡 Copilot Suggest | 30s | Kontextbezogene Vorschläge | 🟢 |
| 3 | 💾 Auto-Save | 60s | Änderungen automatisch speichern | 🟢 |
| 4 | 📦 Backup | 5min | Incremental Backup → Iceberg™ | 🟢 |
| 5 | 🏥 Health | 30s | System-Health aller Komponenten | 🟢 |
| 6 | 🔄 Update | 10min | Feature-Updates + Sync prüfen | 🟢 |
| 7 | 🎫 Triage | 5min | Issue-Triage + Auto-Labeling | 🟢 |
| 8 | 🤝 Dual-Agent | Realtime | Dual-Agent Koordination | 🟢 |

---

## 🛡️ Recovery & Rollback

| Szenario | Recovery-Strategie | Kommando |
|:---------|:-------------------|:---------|
| Context Drift | Frischen SPAWN erzwingen | Ralph-Loop Phase 2 |
| Git-Konflikt | Rebase + Retry | `git rebase --continue` |
| Agent-Timeout | Task pausieren, nächsten starten | Orchestrator Auto |
| Regelverstoß | Sofort-Stopp, James™ Alert | R24 ALARM |
| Datenverlust | Iceberg™ Restore | `iceberg restore --latest` |
| Session-Crash | Letzte Auto-Save wiederherstellen | Auto-Recovery |

---

## 🧠 Best Practices

- ✅ **Immer** mit Startup-Workflow beginnen — keine Abkürzungen
- ✅ **Frischer Kontext** pro Ralph-Loop — niemals alten State wiederverwenden
- ✅ **7-Punkte Checkliste** bei Session-Ende — kein Punkt auslassen
- ✅ **R24 vor Archivierung** — 777 muss explizit genehmigen
- ✅ **Dreifach-Verankerung** für alle Artefakte

### ❌ Anti-Patterns

- ❌ Session starten ohne Pflichtdateien zu lesen
- ❌ Tasks ohne prd.json-Eintrag ausführen
- ❌ Context aus vorheriger Session weiterverwenden
- ❌ Archivierung ohne R24 ALARM
- ❌ Handoff ohne Git Commit

---

<div align="center">

---

**🔄 Workflows** · Teil des [BMAD™ Frameworks](https://github.com/D-VKITZ/bmad-framework)

Gebaut mit 🖤 von **DEVKiTZ™** · `#060608` · Konsistente Sessions. Kein Wissensverlust.

![DEVKiTZ](https://img.shields.io/badge/DEVKiTZ™-Ökosystem-fa1e4e?style=for-the-badge&logo=dev.to&logoColor=white)

</div>
