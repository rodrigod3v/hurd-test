# Hurd App - QA Assessment Greenhouse 🌿

Professional QA testing suite for the Hurd Android application. Structured to provide a clear, technical, and high-impact assessment of the application's stability and usability.

## 🏗️ Project Architecture

```
.
├── .github/workflows/       # CI/CD - GitHub Actions
├── docs/                    # Technical & Strategy Documentation
│   ├── architecture.md      # Robust QA Architecture overview
│   └── walkthrough.md       # Setup and Execution walkthrough
├── evidence/                # Technical Artifacts (Text-only)
│   ├── errors.log           # ADB logcat fatal exceptions
│   ├── latest_errors.log    # Latest run exceptions
│   ├── hierarchy.json       # UI Component tree (Maestro)
│   └── latest_hierarchy.json # Latest run UI tree
├── reports/                 # Final QA and Bug reports
│   └── qa_report.md         # Main QA findings and analysis
└── tests/                   
    ├── e2e/                 # Maestro E2E Automation (6 flows)
    │   ├── explore.yaml
    │   ├── explore_deep.yaml
    │   ├── feed_interactions.yaml
    │   ├── learning_path.yaml
    │   ├── profile_settings.yaml
    │   └── scores_leaderboard.yaml
    └── manual/              # Manual Test Cases & Advanced Scenarios
        ├── advanced_scenarios.md
        └── manual_scenarios.md
```

## 📂 Navigation Guide

- **[qa_report.md](reports/qa_report.md)**: **The main document**. Contains execution summary, critical findings (crashes), and technical observations.
- **[walkthrough.md](docs/walkthrough.md)**: Guide on how to reproduce the results and configure the environment.
- **[evidence/latest_errors.log](evidence/latest_errors.log)**: Current technical logs showing fatal exceptions.

## 🛠️ Tech Stack
- **E2E Framework**: [Maestro](https://maestro.mobile.dev/)
- **Diagnostics**: `adb logcat`, `dumpsys window`
- **CI**: GitHub Actions
- **Evidence Format**: Technical logs and UI hierarchy (JSON/Text)

## 🚀 Execution
To run the automated suite locally:
```bash
maestro test tests/e2e/
```

## 🐞 Status & Findings
The assessment is currently focused on identifying stability issues and feature implementation gaps. Key identified issues include:
- **Critical**: `FATAL EXCEPTION: main` crashes detected in multiple flows.
- **Major**: Infinite loading in the Learning module.
- **Major**: Navigation/Back-button interaction failures in specific flows.

Full details are documented in [reports/qa_report.md](reports/qa_report.md).

---
**Maintained by**: Rodrigo & Antigravity AI

