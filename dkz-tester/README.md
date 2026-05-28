<div align="center">

# 🧪 DkZ Tester™

### *Der Qualitätssicherer des DEVKiTZ™ Ökosystems*

**Playwright E2E · Unit Tests · Visual Regression · Performance Validation**

---

![Role](https://img.shields.io/badge/Role-Tester-fa1e4e?style=for-the-badge&logo=flask&logoColor=white)
![Framework](https://img.shields.io/badge/Framework-Playwright-00ff88?style=for-the-badge&logo=playwright&logoColor=white)
![Browser](https://img.shields.io/badge/Browser-Chromium-3b82f6?style=for-the-badge&logo=googlechrome&logoColor=white)
![Type](https://img.shields.io/badge/Type-E2E+Unit-6366f1?style=for-the-badge&logo=testing&logoColor=white)
![Coverage](https://img.shields.io/badge/Coverage-80%25+-00ff88?style=for-the-badge&logo=codecov&logoColor=white)
![Smoke](https://img.shields.io/badge/Smoke-Dashboard-ffb800?style=for-the-badge&logo=fire&logoColor=black)
![Regression](https://img.shields.io/badge/Regression-Full-3b82f6?style=for-the-badge&logo=regression&logoColor=white)
![Visual](https://img.shields.io/badge/Visual-Screenshots-6366f1?style=for-the-badge&logo=camera&logoColor=white)
![Performance](https://img.shields.io/badge/Performance-Metrics-00ff88?style=for-the-badge&logo=speedtest&logoColor=white)
![A11y](https://img.shields.io/badge/A11y-Audit-ffb800?style=for-the-badge&logo=accessibility&logoColor=black)
![Mobile](https://img.shields.io/badge/Mobile-Responsive-3b82f6?style=for-the-badge&logo=mobile&logoColor=white)
![CI](https://img.shields.io/badge/CI-Automated-00ff88?style=for-the-badge&logo=githubactions&logoColor=white)
![Reports](https://img.shields.io/badge/Reports-HTML-6366f1?style=for-the-badge&logo=html5&logoColor=white)
![Artifacts](https://img.shields.io/badge/Artifacts-Saved-ffb800?style=for-the-badge&logo=archive&logoColor=black)
![Validation](https://img.shields.io/badge/Validation-Rules-fa1e4e?style=for-the-badge&logo=checkmarx&logoColor=white)
![BMAD](https://img.shields.io/badge/BMAD™-Agent_6%2F7-6366f1?style=for-the-badge&logo=robot&logoColor=white)

---

*Teil des [DEVKiTZ™ Ökosystems](https://github.com/777/devkitz-ecosystem) · BMAD™ Methodik Agent #6*

</div>

---

## 📖 Übersicht

**DkZ Tester™** validiert jede Code-Änderung im DEVKiTZ™ Ökosystem durch automatisierte Tests. Von Smoke-Tests über Full Regression bis hin zu Visual Snapshots — der Tester™ stellt sicher, dass alle 132+ Module korrekt funktionieren, bevor Code in den `main`-Branch gelangt.

Als Playwright-Spezialist erstellt der Tester™ E2E-Tests, die das Dashboard in realen Browser-Szenarien durchspielen, und liefert HTML-Reports mit Screenshots und Performance-Metriken an das Team.

---

## 🔄 Test-Workflow im Ralph-Loop

```mermaid
flowchart TD
    subgraph TRIGGER["Trigger"]
        A["👨‍💻 Developer™<br/>pusht Code"]
        B["🔍 Reviewer™<br/>fordert Tests an"]
    end

    subgraph PIPELINE["🧪 Test-Pipeline"]
        C["🔥 Smoke Tests<br/>Dashboard lädt?"]
        D["🧩 Unit Tests<br/>Funktions-Logik"]
        E["🔗 E2E Tests<br/>User Journeys"]
        F["📸 Visual Tests<br/>Screenshot Diff"]
        G["⚡ Performance<br/>Lighthouse Scores"]
        H["♿ A11y Tests<br/>WCAG Compliance"]
        I["📱 Mobile Tests<br/>Responsive Check"]
    end

    subgraph REPORT["📊 Ergebnis"]
        J{"Alle Tests grün?"}
        K["✅ Test-Report<br/>an Reviewer™"]
        L["❌ Fehlerbericht<br/>an Developer™"]
    end

    A --> C
    B --> C
    C --> D --> E --> F --> G --> H --> I
    I --> J
    J -->|Ja| K
    J -->|Nein| L
    L -.->|Fix| A

    style TRIGGER fill:#060608,stroke:#3b82f6,stroke-width:2px,color:#ffffff
    style PIPELINE fill:#060608,stroke:#00ff88,stroke-width:3px,color:#ffffff
    style REPORT fill:#060608,stroke:#fa1e4e,stroke-width:2px,color:#ffffff
```

---

## 📊 Input / Output Matrix

| Richtung | Typ | Beschreibung |
|:---------|:----|:-------------|
| 📥 Input | Code-Änderungen | Neue oder geänderte Module vom Developer™ |
| 📥 Input | Akzeptanzkriterien | Testbare Kriterien aus User Stories |
| 📥 Input | `data-testid` Attribute | Stabile Selektoren für Playwright |
| 📥 Input | Baseline-Screenshots | Referenz-Bilder für Visual Regression |
| 📤 Output | Test-Reports (HTML) | Detaillierte Ergebnisse mit Screenshots |
| 📤 Output | Coverage-Reports | Zeilen- und Branch-Coverage |
| 📤 Output | Performance-Metriken | Lighthouse Scores pro Modul |
| 📤 Output | Bug-Reports | Fehlerbeschreibung mit Reproduktionsschritten |

---

## 🤝 Interaktions-Matrix

| Agent | Interaktion | Beschreibung |
|:------|:------------|:-------------|
| 🎯 James™ | `Reporting` | Test-Ergebnisse an Guardian melden |
| 📋 DkZ PM™ | `Akzeptanz` | Tests aus Akzeptanzkriterien ableiten |
| 🏗️ DkZ Architekt™ | `Testbarkeit` | Modul-Design für Tests optimieren |
| 👨‍💻 DkZ Developer™ | `Bugs` | Fehler melden, Test-Hooks anfordern |
| 🔍 DkZ Reviewer™ | `Verifikation` | Coverage-Reports für Review-Gate |
| 📚 DkZ Dokumentar™ | `Reports` | Test-Ergebnisse für Wiki archivieren |

---

## 🧪 Playwright E2E Test — Beispiel

```javascript
// tests/dashboard.spec.js
import { test, expect } from '@playwright/test';

test.describe('DEVKiTZ™ Dashboard', () => {

  test.beforeEach(async ({ page }) => {
    await page.goto('/01_PROJECTS/01_dashboard/index.html');
  });

  test('Dashboard lädt korrekt', async ({ page }) => {
    // Smoke Test — Grundfunktionalität
    await expect(page).toHaveTitle(/DEVKiTZ/);
    await expect(page.locator('[data-testid="navbar"]')).toBeVisible();
    await expect(page.locator('[data-testid="module-grid"]')).toBeVisible();
  });

  test('Module sind navigierbar', async ({ page }) => {
    // E2E — Modul-Navigation
    const moduleCards = page.locator('[data-testid="module-card"]');
    await expect(moduleCards).toHaveCount({ minimum: 10 });

    await moduleCards.first().click();
    await expect(page).toHaveURL(/modules\//);
  });

  test('Dark Mode nutzt DkZ Farben', async ({ page }) => {
    // Visual — CSS Variables aktiv
    const bg = await page.evaluate(() =>
      getComputedStyle(document.body).getPropertyValue('--bg').trim()
    );
    expect(bg).toBe('#060608');
  });

  test('Kein console.error auf der Seite', async ({ page }) => {
    // Qualität — Keine JS-Fehler
    const errors = [];
    page.on('console', msg => {
      if (msg.type() === 'error') errors.push(msg.text());
    });
    await page.waitForLoadState('networkidle');
    expect(errors).toHaveLength(0);
  });

  test('Responsive Layout ab 320px', async ({ page }) => {
    // Mobile — Breakpoint-Test
    await page.setViewportSize({ width: 320, height: 568 });
    await expect(page.locator('[data-testid="navbar"]')).toBeVisible();
    await expect(page.locator('[data-testid="module-grid"]')).toBeVisible();
  });
});
```

---

## 📋 Test-Plan Template

| Test-Typ | Scope | Frequenz | Schwelle |
|:---------|:------|:---------|:---------|
| 🔥 Smoke | Dashboard Core | Jeder Push | 100% Pass |
| 🧩 Unit | Utility-Funktionen | Jeder Push | ≥ 80% Coverage |
| 🔗 E2E | User Journeys | Jeder PR | ≥ 90% Pass |
| 📸 Visual | Screenshots | Wöchentlich | < 0.1% Diff |
| ⚡ Performance | Lighthouse | Jeder PR | Score ≥ 90 |
| ♿ A11y | WCAG 2.1 AA | Jeder PR | 0 Violations |
| 📱 Mobile | 320px–1440px | Jeder PR | Kein Overflow |

---

## 📸 Screenshot-Archiv

Der Tester™ verwaltet das umfangreichste visuelle Archiv im DEVKiTZ™ Ökosystem:

| Metrik | Wert |
|:-------|:-----|
| Screenshots gesamt | 3.608+ |
| Baseline-Sets | Pro Modul |
| Diff-Schwelle | 0.1% |
| Format | PNG, 1920×1080 + 375×812 |
| Speicherort | `tests/screenshots/` |

---

## 🧠 Best Practices

- **Stabile Selektoren** — `data-testid` statt CSS-Klassen oder Textinhalt
- **Unabhängige Tests** — Kein Test hängt von einem anderen ab
- **Deterministisch** — Gleicher Input = Gleicher Output, immer
- **Screenshots bei Fehlern** — Automatisch gespeichert für Debugging
- **CI-Integration** — Tests laufen in GitHub Actions auf jedem PR
- **Flaky Test = Bug** — Instabile Tests werden sofort repariert

---

<div align="center">

---

**🧪 DkZ Tester™** · Teil der [BMAD™ Methodik](https://github.com/777/devkitz-ecosystem)

Gebaut mit 🖤 von **DEVKiTZ™** · `#060608` · Keine Frameworks. Kein Kompromiss.

![DEVKiTZ](https://img.shields.io/badge/DEVKiTZ™-Ökosystem-fa1e4e?style=for-the-badge&logo=dev.to&logoColor=white)

</div>
