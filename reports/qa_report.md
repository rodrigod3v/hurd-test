# Hurd App - QA Assessment Report

**Date**: 2026-02-12
**Tester**: Antigravity (Autonomous QA Agent)
**Build**: `hurd-qa-assessment.apk`
**Platform**: Android Emulator (API 33)

---

## 🚀 Execution Summary
I performed a mix of automated exploration (Maestro) and manual inspection (ADB screenshots/taps) focusing on the **Community Feed**, **Learning Content**, and **Contribute** features.

---

## 🐞 Identified Bug Reports

### 1. [CRITICAL] Multiple App Crashes (Fatal Exceptions)
- **Description**: The app experienced multiple fatal exceptions on the main thread during navigation and background sync.
- **Evidence**: `adb logcat` shows `FATAL EXCEPTION: main` at various timestamps (e.g., 2026-02-12 12:06:22.672).
- **Severity**: Critical (Impacts app stability).

### 2. [MAJOR] Learning Section - Infinite Loading Spinner
- **Description**: Navigating to the "Learn" tab results in a persistent loading spinner that never resolves, preventing users from accessing learning content.
- **Evidence**: Captured in `screen_learn.png` and `learn_retry.png`.
- **Severity**: Major (Blocks a core feature).

### 3. [MAJOR] Navigation - Unresponsive Back Button in Contribute
- **Description**: The back button (`<`) in the "Create Post" flow is unresponsive to UI taps, forcing users to use the system back gesture or button.
- **Evidence**: Manually verified via ADB taps (coordinates 80, 80 failed, `keyevent 4` required).
- **Severity**: Major (UX Friction / Broken Navigation).

### 4. [MINOR] UI - Text Overlap/Clipping in Contribute Prompts
- **Description**: The prompt list in the "Contribute" section has items where text is extremely close to the edge or bottom navigation bar, suggesting layout calculation issues.
- **Evidence**: Visual inspection of `after_gotit.png`.
- **Severity**: Minor (Visual Polish).

---

## 🛠️ Performance & UX Observations
- **Initial Load**: The app takes ~10s to be fully interactive on an emulator with 4GB RAM.
- **Onboarding UX**: The "Not sure what to post?" screen is helpful but lacks a "Skip" or "Don't show again" flag, making it repetitive for frequent contributors.

---

## 🧪 Automation Artifacts
The following Maestro flows were created and tested:
- `explore.yaml`: Full app navigation.
- `explore_deep.yaml`: Focused on onboarding dismissal.

*Note: Automation stability was affected by the unresponsive buttons mentioned above.*
