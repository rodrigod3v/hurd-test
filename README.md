# Hurd App - QA Assessment Greenhouse 🌿

Professional QA testing suite for the Hurd Android application, featuring manual exploratory charters and automated E2E Maestro flows.

## 🏗️ Project Architecture

```
.
├── .github/workflows/       # CI/CD - GitHub Actions
├── docs/                    # Technical & Strategy Documentation
├── evidence/                # Test artifacts (logs, hierarchy, screenshots)
├── reports/                 # Final QA and Bug reports
└── tests/                   
    ├── e2e/                 # Maestro E2E Automation Flows
    └── manual/              # Manual Test Cases & Exploratory Charters
```

## 🛠️ Tech Stack
- **Framework**: [Maestro](https://maestro.mobile.dev/)
- **Android Tools**: `adb`, `logcat`, `dumpsys`
- **CI**: GitHub Actions
- **Language**: YAML (for tests), Markdown (for docs)

## 🚀 How to Run Tests

### 1. Prerequisites
- Install Maestro: `curl -Ls "https://get.maestro.mobile.dev" | bash`
- Connect an Android Emulator or Device via ADB.

### 2. Running Automation
To run the full suite:
```bash
maestro test tests/e2e/
```

To run a specific flow:
```bash
maestro test tests/e2e/feed_interactions.yaml
```

### 3. Manual Testing
Refer to [tests/manual/manual_scenarios.md](tests/manual/manual_scenarios.md) for detailed test cases and exploratory missions.

## 🐞 Bug Reporting
All identified bugs are documented in [reports/qa_report.md](reports/qa_report.md). Debugging evidence (crashes, layouts) can be found in the `evidence/` folder.

---
**Maintained by**: Rodrigo & Antigravity AI
