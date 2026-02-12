# Hurd App - QA Assessment Greenhouse 🌿

Professional QA testing suite for the Hurd Android application.

## 🏗️ Project Architecture

```
.
├── .github/workflows/       # CI/CD - GitHub Actions
├── docs/                    # Technical & Strategy Documentation
├── evidence/                # Technical Artifacts (Text-only)
│   └── errors.log           # ADB logcat fatal exceptions
│   └── hierarchy.json       # UI Component tree (Maestro)
├── reports/                 # Final QA and Bug reports
└── tests/                   
    ├── e2e/                 # Maestro E2E Automation (4 flows)
    └── manual/              # Manual Test Cases & Advanced Scenarios
```

## 🛠️ Tech Stack
- **E2E Framework**: [Maestro](https://maestro.mobile.dev/)
- **Diagnostics**: `adb logcat`, `dumpsys window`
- **CI**: GitHub Actions
- **Evidence Format**: Raw technical logs (JSON/Text)

## 🚀 Execution
To run the automated suite:
```bash
maestro test tests/e2e/
```

## 🐞 Findings
Critical bugs, performance regressions, and architectural observations are documented in [reports/qa_report.md](reports/qa_report.md).

---
**Maintained by**: Rodrigo & Antigravity AI
