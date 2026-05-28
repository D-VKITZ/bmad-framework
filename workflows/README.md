# 🔄 Workflows

## Session-Start

1. **Pflicht-Dateien lesen:** CLAUDE.md → GEMINI.md → REGELWERK.md → BLAUPAUSE.md
2. **Context laden:** Relevante Artefakte aus Iceberg
3. **Task-Queue prüfen:** prd.json öffnen → nächsten Task identifizieren
4. **Ralph-Loop starten:** Phase 1 (LESEN) beginnen

## Session-Übergabe

1. ✅ CLAUDE.md aktuell?
2. ✅ GEMINI.md aktuell?
3. ✅ Artefakte dreifach verankert? (Iceberg + Hub + Copilot)
4. ✅ features.json aktualisiert?
5. ✅ Git committed?
6. ✅ Walkthrough/Notes gespeichert?
7. ✅ Neue §-Einträge für neue Features?

## Ralph-Loop™ Diagram

```mermaid
sequenceDiagram
    participant 777 as 777 (Owner)
    participant J as 🎯 James™
    participant PM as 📋 PM™
    participant A as 🏗️ Architekt™
    participant D as 👨‍💻 Developer™
    participant R as 🔍 Reviewer™
    participant T as 🧪 Tester™
    participant DOK as 📚 Dokumentar™

    777->>J: Feature Request
    J->>PM: PRD erstellen
    PM->>A: Spec → plan.md
    J->>J: LESEN (Phase 1)
    J->>D: SPAWN (Phase 2)
    D->>D: EXECUTE (Phase 3)
    D->>R: Code Review
    D->>T: Tests
    R-->>D: Feedback
    T-->>D: Test Results
    D->>J: COMMIT (Phase 5)
    J->>DOK: Dokumentation
    J->>J: LOOP (Phase 6)
```
