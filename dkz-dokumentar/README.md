<div align="center">

# 📚 DkZ Dokumentar™

### *Das Gedächtnis des DEVKiTZ™ Ökosystems*

**README · Wiki · Walkthroughs · Learnings · Mermaid Diagramme · Persistenz**

---

![Role](https://img.shields.io/badge/Role-Documentation-fa1e4e?style=for-the-badge&logo=book&logoColor=white)
![Output](https://img.shields.io/badge/Output-README+Wiki-00ff88?style=for-the-badge&logo=markdown&logoColor=white)
![Format](https://img.shields.io/badge/Format-Markdown-3b82f6?style=for-the-badge&logo=markdown&logoColor=white)
![Diagrams](https://img.shields.io/badge/Diagrams-Mermaid-6366f1?style=for-the-badge&logo=mermaid&logoColor=white)
![Screenshots](https://img.shields.io/badge/Screenshots-3608+-ffb800?style=for-the-badge&logo=camera&logoColor=black)
![Walkthroughs](https://img.shields.io/badge/Walkthroughs-46+-00ff88?style=for-the-badge&logo=footsteps&logoColor=white)
![Learnings](https://img.shields.io/badge/Learnings-Captured-3b82f6?style=for-the-badge&logo=lightbulb&logoColor=white)
![Templates](https://img.shields.io/badge/Templates-Standardized-6366f1?style=for-the-badge&logo=template&logoColor=white)
![Changelog](https://img.shields.io/badge/Changelog-Updated-00ff88?style=for-the-badge&logo=history&logoColor=white)
![API](https://img.shields.io/badge/API-Documented-ffb800?style=for-the-badge&logo=openapi&logoColor=black)
![Tutorials](https://img.shields.io/badge/Tutorials-Written-3b82f6?style=for-the-badge&logo=graduationcap&logoColor=white)
![Onboarding](https://img.shields.io/badge/Onboarding-Guide-fa1e4e?style=for-the-badge&logo=rocket&logoColor=white)
![i18n](https://img.shields.io/badge/i18n-Deutsch-ffb800?style=for-the-badge&logo=translate&logoColor=black)
![Links](https://img.shields.io/badge/Links-File_Links-6366f1?style=for-the-badge&logo=link&logoColor=white)
![Version](https://img.shields.io/badge/Version-Tracked-00ff88?style=for-the-badge&logo=semver&logoColor=white)
![BMAD](https://img.shields.io/badge/BMAD™-Agent_7%2F7-6366f1?style=for-the-badge&logo=robot&logoColor=white)

---

*Teil des [DEVKiTZ™ Ökosystems](https://github.com/777/devkitz-ecosystem) · BMAD™ Methodik Agent #7*

</div>

---

## 📖 Übersicht

**DkZ Dokumentar™** ist das **lebende Gedächtnis** des DEVKiTZ™ Ökosystems. Er erstellt READMEs, pflegt das Wiki, archiviert Walkthroughs und fängt Learnings ein, damit kein Wissen verloren geht. Mit über 7.700 Dateien, 3.600+ Screenshots und 46+ Walkthroughs verwaltet er das größte Wissensarchiv im gesamten System.

Der Dokumentar™ arbeitet nach dem Prinzip der **Dreifach-Verankerung**: Jedes Artefakt wird in Iceberg, Hub und Copilot persistiert — dreifach gesichert, immer auffindbar.

---

## 🔄 Dokumentations-Workflow

```mermaid
flowchart TD
    subgraph SOURCES["📥 Quellen"]
        A["👨‍💻 Developer™<br/>Code + JSDoc"]
        B["🏗️ Architekt™<br/>plan.md + Diagramme"]
        C["📋 PM™<br/>PRD + Stories"]
        D["🔍 Reviewer™<br/>Review-Ergebnisse"]
        E["🧪 Tester™<br/>Test-Reports"]
    end

    subgraph DOC["📚 DkZ Dokumentar™"]
        F["📝 README erstellen"]
        G["📖 Wiki pflegen"]
        H["🎬 Walkthroughs"]
        I["💡 Learnings erfassen"]
        J["📊 Changelog"]
    end

    subgraph PERSIST["🔒 Dreifach-Verankerung"]
        K["🧊 Iceberg<br/>Langzeit-Archiv"]
        L["🔍 WissenHub<br/>Suchbar + Filterbar"]
        M["🤖 Copilot<br/>KI-Zugriff"]
    end

    A --> F
    B --> F
    B --> G
    C --> G
    D --> I
    E --> H

    F --> K
    G --> K
    H --> K
    I --> L
    J --> L

    K --> M
    L --> M

    style SOURCES fill:#060608,stroke:#3b82f6,stroke-width:2px,color:#ffffff
    style DOC fill:#060608,stroke:#fa1e4e,stroke-width:3px,color:#ffffff
    style PERSIST fill:#060608,stroke:#00ff88,stroke-width:2px,color:#ffffff
```

---

## 📊 Input / Output Matrix

| Richtung | Typ | Beschreibung |
|:---------|:----|:-------------|
| 📥 Input | Code + JSDoc | Quellcode-Kommentare vom Developer™ |
| 📥 Input | `plan.md` | Architektur-Beschreibungen vom Architekt™ |
| 📥 Input | PRD + Stories | Produktanforderungen vom PM™ |
| 📥 Input | Review-Ergebnisse | Quality-Reports vom Reviewer™ |
| 📥 Input | Test-Reports | HTML-Reports und Screenshots vom Tester™ |
| 📤 Output | `README.md` | Modul-Dokumentation mit Badges + Mermaid |
| 📤 Output | Wiki-Seiten | `04_SYSTEM/DEVKITZ_WIKI/` Einträge |
| 📤 Output | Walkthroughs | Schritt-für-Schritt-Anleitungen mit Screenshots |
| 📤 Output | Learnings | Gelerntes aus Bugs, Reviews, Entscheidungen |
| 📤 Output | CHANGELOG.md | Versionierte Änderungsliste |

---

## 🤝 Interaktions-Matrix

| Agent | Interaktion | Beschreibung |
|:------|:------------|:-------------|
| 🎯 James™ | `Compliance` | Doku-Standards einhalten, Spiegel-Sync prüfen |
| 📋 DkZ PM™ | `Spezifikation` | Feature-Doku aus PRD generieren |
| 🏗️ DkZ Architekt™ | `Architektur-Doku` | Diagramme und Patterns dokumentieren |
| 👨‍💻 DkZ Developer™ | `Code-Doku` | JSDoc-Kommentare in README übertragen |
| 🔍 DkZ Reviewer™ | `Doku-Check` | Vollständigkeit der Dokumentation verifizieren |
| 🧪 DkZ Tester™ | `Reports` | Test-Ergebnisse und Screenshots archivieren |

---

## 📝 README Template

```markdown
<div align="center">

# [Emoji] Modul-Name

### *Kurzbeschreibung*

![Badge1](url) ![Badge2](url) ...

</div>

---

## 📖 Übersicht
[2-3 Absätze Beschreibung]

## 🔄 Workflow / Architektur
[Mermaid Diagramm]

## 📊 Features
[Feature-Tabelle]

## ⚙️ Konfiguration
[Config-Tabelle oder JSON-Beispiel]

## 🚀 Verwendung
[Code-Beispiele]

## 📈 Metriken
[Status-Tabelle]

---

<div align="center">
**DEVKiTZ™ Ökosystem** · Footer
</div>
```

---

## 💡 Learnings Template

```json
{
  "id": "LEARN-2026-0528-001",
  "type": "learning",
  "title": "Beschreibender Titel",
  "date": "2026-05-28",
  "module": "modul-name",
  "category": "bug|architecture|performance|security|dx",
  "context": "Was war die Situation?",
  "problem": "Was war das Problem?",
  "solution": "Was war die Lösung?",
  "takeaway": "Was lernen wir daraus?",
  "tags": ["relevant", "tags"]
}
```

---

## 📖 Wiki-Struktur

```
04_SYSTEM/DEVKITZ_WIKI/
├── 00_INDEX.md              # Inhaltsverzeichnis
├── 01_ARCHITEKTUR/          # System-Architektur
│   ├── tech-stack.md
│   ├── modul-patterns.md
│   └── daten-schicht.md
├── 02_AGENTEN/              # BMAD™ Agenten
│   ├── james-guardian.md
│   ├── dkz-pm.md
│   └── ...
├── 03_MODULE/               # 132+ Modul-Docs
├── 04_WORKFLOWS/            # Ralph-Loop, CI/CD
├── 05_LEARNINGS/            # Gesammeltes Wissen
└── 06_ONBOARDING/           # Neue Agenten einarbeiten
```

---

## 📸 Walkthrough-Persistenz

Walkthroughs dokumentieren komplexe Prozesse mit Screenshots und werden dreifach verankert:

| Metrik | Wert |
|:-------|:-----|
| Walkthroughs gesamt | 46+ |
| Screenshots archiviert | 3.608+ |
| Conversations dokumentiert | 76+ |
| Artefakte verwaltet | 7.708+ |
| Plans erstellt | 59 |
| Tasks getrackt | 63 |

---

## ✍️ Format-Standards

| Element | Standard | Beispiel |
|:--------|:---------|:---------|
| Überschriften | `#` = 1× Titel, `##` Sektionen | `## 📖 Übersicht` |
| Code-Blöcke | Immer mit Sprachkennung | ` ```javascript ` |
| Tabellen | Ausgerichtete Spalten | `\|:--|:--\|` |
| Trennlinien | Zwischen Haupt-Sektionen | `---` |
| Links | Markdown-Links | `[Text](pfad)` |
| Emojis | Bei allen Überschriften | ✅ |
| Sprache | Deutsch | Pflicht |

---

## 🧠 Best Practices

- **Kein Platzhalter-Text** — Jede Beschreibung ist vollständig und spezifisch
- **Mermaid statt Bilder** — Diagramme als Code, nicht als PNG
- **File-Links** statt nackte URLs — `[config](./config.json)`
- **Dreifach-Verankerung** — Iceberg + WissenHub + Copilot
- **Versionierung** — Jede Doku-Änderung wird committet
- **Screenshots** — Immer mit Zeitstempel und Kontext archiviert
- **Onboarding-First** — Neue Agenten müssen die Doku sofort verstehen

---

<div align="center">

---

**📚 DkZ Dokumentar™** · Teil der [BMAD™ Methodik](https://github.com/777/devkitz-ecosystem)

Gebaut mit 🖤 von **DEVKiTZ™** · `#060608` · Keine Frameworks. Kein Kompromiss.

![DEVKiTZ](https://img.shields.io/badge/DEVKiTZ™-Ökosystem-fa1e4e?style=for-the-badge&logo=dev.to&logoColor=white)

</div>
