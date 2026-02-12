# QA Assessment Guide - Hurd App

This document serves as your guide to executing a high-impact QA assessment for the Hurd app.

## 📋 What's Inside
- **Manual Scenarios**: Focus on core features (Feed & Learning).
- **Exploratory Charter**: Deep dive into UX and edge cases.
- **E2E Scripts**: Automation using Maestro for quick regression.

## 🛠️ Setup Instructions

### 1. Environment
- Install **Android Studio** and create a Pixel 6/7 Emulator (API 33+).
- Enable **USB Debugging** (if using a physical device).
- Install the APK: `adb install hurd-qa-assessment.apk`.

### 2. Maestro (Optional but Recommended for "Extra Points")
- Install Maestro: `curl -Ls "https://get.maestro.mobile.dev" | bash`.
- Verify installation: `maestro --version`.

## 🚀 Execution Steps

### Step 1: Manual & Exploratory Testing
Follow the [manual_scenarios.md](file:///C:/Users/777/.gemini/antigravity/brain/3a42dd40-c5ef-4457-9849-597f801b83f9/manual_scenarios.md) to validate the core features.
> [!TIP]
> Keep `adb logcat` running in the background to catch hidden errors:
> `adb logcat *:E > errors.log`

### Step 2: Automated Testing
Run the Maestro flows provided in [maestro_scripts.md](file:///C:/Users/777/.gemini/antigravity/brain/3a42dd40-c5ef-4457-9849-597f801b83f9/maestro_scripts.md).
```bash
maestro test flow-feed.yaml
maestro test flow-learning.yaml
```

### Step 3: Bug Reporting
When you find a bug, document it with:
1.  **Summary**: [Area] Short description.
2.  **Steps**: 1, 2, 3...
3.  **Visuals**: Attach screenshot or screen record.
4.  **Priority**: Critical (Crash), Major (Broken flow), Minor (UI alignment).

## 🏁 Final Objective
Your goal is to show the recruiters that you have a **methodical approach**, can **automate repetitive tasks**, and have a **keen eye for UX**.

Good luck with the assessment! 🎯
