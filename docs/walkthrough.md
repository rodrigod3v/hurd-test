# QA Assessment Guide - Hurd App

This document serves as your guide to executing a high-impact QA assessment for the Hurd app.

## 📋 What's Inside
- **Manual Scenarios**: Focus on core features (Feed & Learning). See [manual_scenarios.md](../tests/manual/manual_scenarios.md).
- **Exploratory Charter**: Deep dive into UX and edge cases.
- **E2E Scripts**: Automation using Maestro for quick regression.

## 🛠️ Setup Instructions

### 1. Environment
- Install **Android Studio** and create a Pixel 6/7 Emulator (API 33+).
- Enable **USB Debugging** (if using a physical device).
- Install the APK: `adb install hurd-qa-assessment.apk`.

### 2. Maestro (Optional)
- Install Maestro: `curl -Ls "https://get.maestro.mobile.dev" | bash`.
- Verify installation: `maestro --version`.

## 🚀 Execution Steps

### Step 1: Manual & Exploratory Testing
Follow the [manual_scenarios.md](../tests/manual/manual_scenarios.md) to validate the core features.
> [!TIP]
> Keep `adb logcat` running in the background to catch hidden errors:
> `adb logcat *:E > evidence/errors.log`

### Step 2: Automated Testing
Run the Maestro flows provided in the `tests/e2e/` directory.
```bash
# Run all tests
maestro test tests/e2e/

# Run specific flows
maestro test tests/e2e/explore.yaml
maestro test tests/e2e/learning_path.yaml
```

### Step 3: Bug Reporting
When you find a bug, document it with:
1.  **Summary**: [Area] Short description.
2.  **Steps**: 1, 2, 3...
3.  **Visuals**: Attach screenshot or screen record.
4.  **Priority**: Critical (Crash), Major (Broken flow), Minor (UI alignment).

## 🏁 Final Objective
Your goal is to show a **methodical approach**, the ability to **automate repetitive tasks**, and a **keen eye for UX**.

Good luck! 🎯

