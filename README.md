<div align="center">

# 🤖 BMAD™ Framework

### **B**lueprint → **M**apping → **A**nalyse → **D**esign

*Die 7-Agenten KI-Methodik von DEVKiTZ™ — Systematische Softwareentwicklung mit autonomen Spezialisten*

---

![Version](https://img.shields.io/badge/Version-2.0-fa1e4e?style=for-the-badge&logo=semver&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-00ff88?style=for-the-badge&logo=statuspage&logoColor=white)
![Agenten](https://img.shields.io/badge/Agenten-7-6366f1?style=for-the-badge&logo=probot&logoColor=white)
![Phasen](https://img.shields.io/badge/Ralph--Loop™_Phasen-6-ffb800?style=for-the-badge&logo=loop&logoColor=white)
![Lizenz](https://img.shields.io/badge/Lizenz-MIT-3b82f6?style=for-the-badge&logo=opensourceinitiative&logoColor=white)

![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-Semantic-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-Custom_Props-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![DuckDB](https://img.shields.io/badge/DuckDB-Analytics-FFF000?style=for-the-badge&logo=duckdb&logoColor=black)

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI%2FCD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-Server-fa1e4e?style=for-the-badge&logo=fastapi&logoColor=white)
![OpenRouter](https://img.shields.io/badge/OpenRouter-Multi--LLM-6366f1?style=for-the-badge&logo=openai&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-Antigravity-4285F4?style=for-the-badge&logo=google&logoColor=white)

![CodeRabbit](https://img.shields.io/badge/CodeRabbit-Review-00ff88?style=for-the-badge&logo=coderabbit&logoColor=white)
![Tests](https://img.shields.io/badge/Tests-Passing-00ff88?style=for-the-badge&logo=vitest&logoColor=white)
![Docs](https://img.shields.io/badge/Docs-Complete-3b82f6?style=for-the-badge&logo=readthedocs&logoColor=white)
![Made with](https://img.shields.io/badge/Made_with-DEVKiTZ™-fa1e4e?style=for-the-badge&logo=heart&logoColor=white)

</div>

---

## 📖 Überblick

**BMAD™** ist die proprietäre Multi-Agenten-Methodik von [DEVKiTZ™](https://github.com/D-VKITZ), die Softwareentwicklung in vier strategische Phasen gliedert und durch sieben spezialisierte KI-Agenten autonom ausführen lässt. Jeder Agent hat eine klar definierte Rolle — vom strategischen Guardian bis zum Code-Executor — und operiert innerhalb des **Ralph-Loop™**, einem 6-Phasen-Zyklus, der kontextfrischen, fehlerfreien Output garantiert.

> **Kernprinzip:** Jeder Task bekommt frischen Kontext — kein Context Drift. Kein Agent arbeitet außerhalb seiner Rolle. James™ überwacht alles.

### 🧬 Was bedeutet BMAD?

| Phase | Name | Beschreibung |
|:------|:-----|:-------------|
| **B** | 🔵 Blueprint | Anforderungen erfassen, PRD erstellen, Ziele definieren |
| **M** | 🟣 Mapping | Architektur entwerfen, Module planen, Abhängigkeiten kartieren |
| **A** | 🟡 Analyse | Code-Review, Qualitätsprüfung, Testing, Metriken erheben |
| **D** | 🔴 Design | Implementation, Dokumentation, Deployment, Übergabe |

---

## 🤖 Die 7 Agenten

Das Herz von BMAD™ sind sieben spezialisierte Agenten, die im Zusammenspiel den gesamten Entwicklungszyklus abdecken. Kein Agent agiert isoliert — die Hierarchie wird durch James™ gesteuert.

| # | Agent | Rolle | Kernaufgabe | Output |
|:--|:------|:------|:------------|:-------|
| 1 | 🎯 **James™** | Guardian | Überwacht alle Agenten, coded **NICHT** | Steuerungsbefehle, Eskalationen |
| 2 | 📋 **DkZ PM™** | Product Manager | Spezifikation, User Stories, Priorisierung | `spec.md`, PRD, Backlog |
| 3 | 🏗️ **DkZ Architekt™** | Architekt | Technische Planung, Stack-Entscheidungen | `plan.md`, Architektur-Diagramme |
| 4 | 👨‍💻 **DkZ Developer™** | Coder | Ralph-Loop Executor, schreibt den Code | Module, Features, Bugfixes |
| 5 | 🔍 **DkZ Reviewer™** | CodeRabbit QA | Code-Review, Best Practices, Sicherheit | Review-Reports, Annotations |
| 6 | 🧪 **DkZ Tester™** | Tester | Tests schreiben, Validierung, Regression | Test-Suites, Coverage-Reports |
| 7 | 📚 **DkZ Dokumentar™** | Dokumentar | README, Wiki, Changelogs, Learnings | Dokumentation, Knowledge Base |

### 🏛️ Agenten-Hierarchie

```mermaid
graph TD
    J["🎯 James™<br/>Guardian"]
    PM["📋 DkZ PM™<br/>Product Manager"]
    AR["🏗️ DkZ Architekt™<br/>Architekt"]
    DEV["👨‍💻 DkZ Developer™<br/>Coder"]
    REV["🔍 DkZ Reviewer™<br/>CodeRabbit QA"]
    TEST["🧪 DkZ Tester™<br/>Tester"]
    DOC["📚 DkZ Dokumentar™<br/>Dokumentar"]

    J -->|steuert| PM
    J -->|steuert| AR
    J -->|steuert| DEV
    J -->|steuert| REV
    J -->|steuert| TEST
    J -->|steuert| DOC

    PM -->|spec.md| AR
    AR -->|plan.md| DEV
    DEV -->|Code| REV
    REV -->|Feedback| DEV
    DEV -->|Release| TEST
    TEST -->|Ergebnis| DOC

    style J fill:#fa1e4e,stroke:#fa1e4e,color:#fff
    style PM fill:#6366f1,stroke:#6366f1,color:#fff
    style AR fill:#3b82f6,stroke:#3b82f6,color:#fff
    style DEV fill:#00ff88,stroke:#00ff88,color:#060608
    style REV fill:#ffb800,stroke:#ffb800,color:#060608
    style TEST fill:#ff3b5c,stroke:#ff3b5c,color:#fff
    style DOC fill:#3b82f6,stroke:#3b82f6,color:#fff
```

---

## 🔄 Ralph-Loop™

Der **Ralph-Loop™** ist der Ausführungszyklus jedes Tasks. Er stellt sicher, dass jeder Agent mit frischem Kontext arbeitet und kein Context Drift entsteht. Der Loop besteht aus 6 Phasen und wird solange wiederholt, bis alle Tasks erledigt sind.

```mermaid
graph LR
    L["1️⃣ LESEN<br/>prd.json + constitution<br/>+ AGENTS.md"]
    S["2️⃣ SPAWN<br/>Neue Instanz<br/>frischer Kontext"]
    E["3️⃣ EXECUTE<br/>Developer™<br/>schreibt Code"]
    V["4️⃣ VERIFY<br/>Tester™ + Reviewer™<br/>prüfen"]
    C["5️⃣ COMMIT<br/>Git commit<br/>+ prd.json update"]
    LP["6️⃣ LOOP<br/>Nächster Task<br/>oder Done"]

    L --> S --> E --> V --> C --> LP
    LP -->|Nächster Task| L

    style L fill:#3b82f6,stroke:#3b82f6,color:#fff
    style S fill:#6366f1,stroke:#6366f1,color:#fff
    style E fill:#00ff88,stroke:#00ff88,color:#060608
    style V fill:#ffb800,stroke:#ffb800,color:#060608
    style C fill:#fa1e4e,stroke:#fa1e4e,color:#fff
    style LP fill:#ff3b5c,stroke:#ff3b5c,color:#fff
```

### 📋 Phasen im Detail

| Phase | Name | Agent(en) | Aktion |
|:------|:-----|:----------|:-------|
| 1 | **LESEN** | James™ | `prd.json`, Konstitution und `AGENTS.md` laden, relevante Artefakte injizieren |
| 2 | **SPAWN** | James™ | Neue Agent-Instanz mit frischem Kontext erstellen — kein Altlast-State |
| 3 | **EXECUTE** | Developer™ | Code schreiben, Module implementieren, Bugs fixen |
| 4 | **VERIFY** | Reviewer™ + Tester™ | Code-Review via CodeRabbit, Unit-Tests, Integration-Tests |
| 5 | **COMMIT** | Developer™ | `git commit` mit konventionellem Format, `prd.json` Status aktualisieren |
| 6 | **LOOP** | James™ | Prüfen ob weitere Tasks vorhanden — wenn ja: zurück zu Phase 1 |

---

## ⚠️ Eiserne Regeln (Top 10)

Diese Regeln gelten **ausnahmslos** für jeden Agenten und jede Codezeile innerhalb des DEVKiTZ™ Ökosystems.

| # | Regel | Begründung |
|:--|:------|:-----------|
| 1 | 🛡️ **`esc()` bei JEDEM User-Input** vor `innerHTML` | XSS-Schutz — keine Ausnahme |
| 2 | 🎨 **DkZ CSS Variables nutzen** — kein hardcoded `#fa1e4e` | Design-Konsistenz über alle Module |
| 3 | 📦 **Shared Scripts einbinden** (`dkz-debug.js`, `dkz-guide.js`, `dkz-navbar.js`) | DRY-Prinzip, zentrale Updates |
| 4 | 📄 **`features.json` nach Modul-Änderung aktualisieren** | Dashboard-Integrität sicherstellen |
| 5 | 💾 **Git Commit nach JEDER Änderung** | Lückenlose Nachvollziehbarkeit |
| 6 | 🚨 **R24 ALARM vor Archivierung** — 777 muss bestätigen | Kein versehentliches Archivieren |
| 7 | 📁 **`99_ARCHIVE/` nur ablegen, NIEMALS löschen** | Wissen geht nie verloren |
| 8 | 🖥️ **Desktop NIE verändern** — nur ablegen | Bestehende Dateien sind tabu |
| 9 | 🔇 **Kein `console.log` in Produktion** | Sauberer Production-Output |
| 10 | 🚫 **Kein jQuery ohne Rücksprache mit 777** | Vanilla JS ist Standard |

---

## 🗂️ Projektstruktur

```
C:\DEVKiTZ\
├── 01_PROJECTS/
│   └── 01_dashboard/
│       ├── modules/          # 81+ Module
│       ├── shared/           # Shared Scripts (dkz-*.js)
│       └── BLAUPAUSE.md      # Architektur-Blaupause
├── 04_SYSTEM/
│   └── DEVKITZ_WIKI/         # Wiki & Knowledge Base
├── 99_ARCHIVE/               # Nur ablegen, NIE löschen
├── .agents/
│   └── workflows/            # Agent-Workflows
├── CLAUDE.md                 # Pflichtlektüre #1
├── GEMINI.md                 # Pflichtlektüre #2
├── REGELWERK.md              # Pflichtlektüre #3
└── AGENTS.md                 # Agenten-Router
```

---

## 🚀 Schnellstart

### Voraussetzungen

```bash
# Node.js 18+ erforderlich
node --version   # v18.x oder höher

# Git muss konfiguriert sein
git --version
```

### Projekt einrichten

```bash
# Repository klonen
git clone https://github.com/D-VKITZ/bmad-framework.git
cd bmad-framework

# Abhängigkeiten installieren
npm install

# Agenten-Konfiguration prüfen
cat AGENTS.md
```

### Ersten Ralph-Loop™ starten

```javascript
// 1. PRD laden
const prd = await loadPRD('prd.json');

// 2. James™ initialisieren — Guardian übernimmt Steuerung
const james = new Guardian({ constitution: 'AGENTS.md' });

// 3. Ralph-Loop starten
await james.startLoop({
  tasks: prd.tasks,
  agents: ['pm', 'architekt', 'developer', 'reviewer', 'tester', 'dokumentar'],
  freshContext: true  // Kein Context Drift!
});
```

---

## 🔗 Session-Übergabe Checkliste

Bei **jedem** Session-Ende müssen folgende Punkte abgehakt werden:

- [ ] ✅ `CLAUDE.md` aktuell?
- [ ] ✅ `GEMINI.md` aktuell?
- [ ] ✅ Artefakte dreifach verankert? (Iceberg + Hub + Copilot)
- [ ] ✅ `features.json` aktualisiert?
- [ ] ✅ Git committed?
- [ ] ✅ Walkthrough / Notes gespeichert?
- [ ] ✅ Neue §-Einträge für neue Features?

---

## 🔗 Verwandte Repositories

| Repository | Beschreibung | Link |
|:-----------|:-------------|:-----|
| 🤖 **BMAD™ Framework** | Dieses Repository — 7-Agenten Methodik | [github.com/D-VKITZ/bmad-framework](https://github.com/D-VKITZ/bmad-framework) |
| 🐝 **Agent Swarm** | Multi-Agent Orchestrierung & Deployment | [github.com/D-VKITZ/agent-swarm](https://github.com/D-VKITZ/agent-swarm) |
| 🏠 **DEVKiTZ™ Ecosystem** | Haupt-Repository des Ökosystems | [github.com/777/devkitz-ecosystem](https://github.com/777/devkitz-ecosystem) |
| 📊 **Dashboard** | Fusion Dashboard mit 81+ Modulen | `01_PROJECTS/01_dashboard/` |
| 📚 **Wiki** | DEVKiTZ™ Knowledge Base | `04_SYSTEM/DEVKITZ_WIKI/` |

---

## 📊 Projekt-Metriken

| Metrik | Wert |
|:-------|:-----|
| 🤖 Agenten | 7 |
| 🔄 Loop-Phasen | 6 |
| 📦 Dashboard-Module | 81+ |
| 💬 Conversations | 76+ |
| 📐 Plans | 59+ |
| 📖 Walkthroughs | 46+ |
| 📋 Tasks | 63+ |
| 📸 Screenshots | 3.608+ |
| 📁 Total Files | 7.708+ |

---

<div align="center">

## 📄 Lizenz

MIT License — Siehe [LICENSE](LICENSE) für Details.

---

<img src="https://img.shields.io/badge/DEVKiTZ™-BMAD_Framework-fa1e4e?style=for-the-badge&logo=heart&logoColor=white" alt="DEVKiTZ™" />

**Built with ❤️ by [DEVKiTZ™](https://github.com/D-VKITZ)**

*Blueprint → Mapping → Analyse → Design — Systematisch. Autonom. Fehlerfrei.*

`--accent: #fa1e4e` · `--bg: #060608` · `--green: #00ff88` · `--yellow: #ffb800`

© 2026 DEVKiTZ™ · Alle Rechte vorbehalten

</div>
