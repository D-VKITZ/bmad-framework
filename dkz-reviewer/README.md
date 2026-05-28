<div align="center">

# 🔍 DkZ Reviewer™ — CodeRabbit QA

### *Der Qualitätswächter des DEVKiTZ™ Ökosystems*

**Code Reviews · Quality Gates · Security Audits · Performance Checks**

---

![Role](https://img.shields.io/badge/Role-Reviewer-fa1e4e?style=for-the-badge&logo=search&logoColor=white)
![Tool](https://img.shields.io/badge/Tool-CodeRabbit-00ff88?style=for-the-badge&logo=coderabbit&logoColor=white)
![Quality](https://img.shields.io/badge/Quality-Gates-3b82f6?style=for-the-badge&logo=qualitygate&logoColor=white)
![Coverage](https://img.shields.io/badge/Coverage-80%25+-00ff88?style=for-the-badge&logo=codecov&logoColor=white)
![Patterns](https://img.shields.io/badge/Patterns-Anti_Pattern_Detection-ffb800?style=for-the-badge&logo=radar&logoColor=black)
![Security](https://img.shields.io/badge/Security-OWASP-fa1e4e?style=for-the-badge&logo=owasp&logoColor=white)
![Performance](https://img.shields.io/badge/Performance-Lighthouse-00ff88?style=for-the-badge&logo=lighthouse&logoColor=white)
![A11y](https://img.shields.io/badge/A11y-Audit-6366f1?style=for-the-badge&logo=accessibility&logoColor=white)
![SEO](https://img.shields.io/badge/SEO-Check-ffb800?style=for-the-badge&logo=google&logoColor=black)
![CSS](https://img.shields.io/badge/CSS-Variables_Only-6366f1?style=for-the-badge&logo=css3&logoColor=white)
![XSS](https://img.shields.io/badge/XSS-esc()_Enforced-fa1e4e?style=for-the-badge&logo=shield&logoColor=white)
![Console](https://img.shields.io/badge/Console-No_Logs-00ff88?style=for-the-badge&logo=terminal&logoColor=white)
![Dependencies](https://img.shields.io/badge/Dependencies-Audited-3b82f6?style=for-the-badge&logo=dependabot&logoColor=white)
![PR](https://img.shields.io/badge/PR-Required-ffb800?style=for-the-badge&logo=gitpullrequest&logoColor=black)
![Approval](https://img.shields.io/badge/Approval-Mandatory-fa1e4e?style=for-the-badge&logo=checkmarx&logoColor=white)
![BMAD](https://img.shields.io/badge/BMAD™-Agent_5%2F7-6366f1?style=for-the-badge&logo=robot&logoColor=white)

---

*Teil des [DEVKiTZ™ Ökosystems](https://github.com/777/devkitz-ecosystem) · BMAD™ Methodik Agent #5*

</div>

---

## 📖 Übersicht

**DkZ Reviewer™** ist der **Qualitätswächter** im BMAD™-System und arbeitet in Ralph-Loop Phase 4 (VERIFY). Ausgestattet mit CodeRabbit-Integration prüft er jeden Code-Beitrag gegen die Quality Gates des DEVKiTZ™ Ökosystems. Kein Code erreicht den `main`-Branch ohne seine Freigabe.

Der Reviewer™ kombiniert automatisierte Checks (Lint, Security, Performance) mit manueller Architektur-Bewertung und stellt sicher, dass die eisernen Regeln eingehalten werden — von `esc()` über CSS Variables bis hin zum Framework-Verbot.

---

## 🔄 Review-Workflow

```mermaid
flowchart TD
    subgraph PR["Pull Request eingeht"]
        A["👨‍💻 Developer™ pusht Code"]
    end

    subgraph AUTO["🤖 Automatisierte Checks"]
        B["Lint · ESLint Clean"]
        C["Security · OWASP Scan"]
        D["Performance · Lighthouse"]
        E["A11y · Accessibility Audit"]
        F["CSS · Variable Check"]
    end

    subgraph MANUAL["🔍 Manuelle Review"]
        G["Architektur-Patterns"]
        H["esc() Nutzung prüfen"]
        I["Shared Scripts vorhanden?"]
        J["Console.log entfernt?"]
        K["features.json aktuell?"]
    end

    subgraph RESULT["Ergebnis"]
        L{"Alle Gates bestanden?"}
        M["✅ APPROVED"]
        N["❌ CHANGES REQUESTED"]
    end

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F

    B & C & D & E & F --> G
    G --> H --> I --> J --> K

    K --> L
    L -->|Ja| M
    L -->|Nein| N
    N -.->|Feedback| A

    style PR fill:#060608,stroke:#3b82f6,stroke-width:2px,color:#ffffff
    style AUTO fill:#060608,stroke:#00ff88,stroke-width:2px,color:#ffffff
    style MANUAL fill:#060608,stroke:#ffb800,stroke-width:2px,color:#ffffff
    style RESULT fill:#060608,stroke:#fa1e4e,stroke-width:3px,color:#ffffff
```

---

## 📊 Input / Output Matrix

| Richtung | Typ | Beschreibung |
|:---------|:----|:-------------|
| 📥 Input | Pull Request | Code-Änderungen vom Developer™ |
| 📥 Input | `plan.md` | Architektur-Referenz für Pattern-Checks |
| 📥 Input | Eiserne Regeln | 10 Pflicht-Regeln als Checkliste |
| 📥 Input | Lighthouse Reports | Automatisierte Performance-Metriken |
| 📤 Output | Review-Kommentare | Inline-Feedback mit Korrekturvorschlägen |
| 📤 Output | Approval / Rejection | Freigabe oder Änderungsanforderung |
| 📤 Output | Quality-Report | Zusammenfassung aller Checks |
| 📤 Output | Regel-Verstoß-Meldung | Eskalation an James™ bei kritischen Verstößen |

---

## 🤝 Interaktions-Matrix

| Agent | Interaktion | Beschreibung |
|:------|:------------|:-------------|
| 🎯 James™ | `Eskalation` | Kritische Verstöße melden, Freigabe-Blockade |
| 📋 DkZ PM™ | `Feedback` | Qualitäts-Metriken für Sprint-Retrospektiven |
| 🏗️ DkZ Architekt™ | `Pattern-Check` | Architektur-Konformität validieren |
| 👨‍💻 DkZ Developer™ | `Review` | Code prüfen, Feedback geben, Approval |
| 🧪 DkZ Tester™ | `Koordination` | Test-Coverage vor Approval prüfen |
| 📚 DkZ Dokumentar™ | `Doku-Check` | README + JSDoc Vollständigkeit prüfen |

---

## ✅ Review-Checkliste

### 🔴 Kritisch (Blocker)

| # | Check | Regel |
|:--|:------|:------|
| 1 | `esc()` bei jedem User-Input vor `innerHTML` | XSS-Schutz |
| 2 | Keine Frameworks (React, Vue, Angular) | Vanilla Only |
| 3 | Kein `console.log` in Produktion | Console Clean |
| 4 | `99_ARCHIVE/` wird nicht gelöscht | Archiv Protected |

### 🟡 Hoch (Muss vor Merge)

| # | Check | Regel |
|:--|:------|:------|
| 5 | CSS Custom Properties statt Hardcoded | DkZ Variables |
| 6 | Shared Scripts eingebunden | dkz-navbar, dkz-debug, dkz-guide |
| 7 | `features.json` aktualisiert | Feature-Tracking |
| 8 | Git Commit Message = Conventional | feat/fix/refactor(scope) |

### 🟢 Standard (Best Practice)

| # | Check | Regel |
|:--|:------|:------|
| 9 | Semantic HTML | Heading-Hierarchie, ARIA |
| 10 | Performance Budget | Lighthouse > 90 |
| 11 | Mobile-First Responsive | Ab 320px |
| 12 | Test-Hooks vorhanden | data-testid Attribute |

---

## 🛡️ Security-Checks (OWASP)

```javascript
// Review-Pattern: XSS-Erkennung
const xssPatterns = [
  /\.innerHTML\s*=\s*(?!.*esc\()/, // innerHTML ohne esc()
  /\.outerHTML\s*=/,                // outerHTML Zuweisung
  /document\.write\(/,             // document.write
  /eval\(/,                        // eval() Nutzung
  /setTimeout\(\s*["']/,           // setTimeout mit String
  /setInterval\(\s*["']/           // setInterval mit String
];

// Automatisierter Check
const auditFile = (content) => {
  const violations = [];
  xssPatterns.forEach((pattern, i) => {
    if (pattern.test(content)) {
      violations.push({
        rule: `XSS-${i + 1}`,
        severity: 'CRITICAL',
        action: 'BLOCK_MERGE'
      });
    }
  });
  return violations;
};
```

---

## 📈 Quality Gates

| Gate | Schwelle | Tool |
|:-----|:---------|:-----|
| Test Coverage | ≥ 80% | Playwright |
| Lighthouse Performance | ≥ 90 | Lighthouse CI |
| Lighthouse Accessibility | ≥ 95 | Lighthouse CI |
| Security Vulnerabilities | 0 kritisch | OWASP Scanner |
| CSS Variable Compliance | 100% | Custom Linter |
| Console.log Statements | 0 | ESLint Rule |
| Framework Imports | 0 | Import Scanner |

---

## 🧠 Best Practices

- **Jede Zeile** mit User-Input-Kontakt wird auf `esc()` geprüft
- **Review-Kommentare** sind konstruktiv und enthalten Code-Vorschläge
- **Pattern-Verstöße** werden mit Referenz auf Architektur-Docs dokumentiert
- **Performance-Regression** blockiert den Merge automatisch
- **Pair-Review** bei Security-relevantem Code mit James™

---

<div align="center">

---

**🔍 DkZ Reviewer™ CodeRabbit QA** · Teil der [BMAD™ Methodik](https://github.com/777/devkitz-ecosystem)

Gebaut mit 🖤 von **DEVKiTZ™** · `#060608` · Keine Frameworks. Kein Kompromiss.

![DEVKiTZ](https://img.shields.io/badge/DEVKiTZ™-Ökosystem-fa1e4e?style=for-the-badge&logo=dev.to&logoColor=white)

</div>
