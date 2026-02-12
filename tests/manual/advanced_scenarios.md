# Hurd App - Advanced Manual Test Scenarios

## 🌐 1. Network Resilience & Connectivity
- **Scenario**: App behavior in Airplane Mode.
  - **Steps**: Open app -> Enable Airplane Mode -> Navigate to Feed.
  - **Expected**: Disconnected/Offline state message appeared. No crash.
- **Scenario**: Low Bandwidth Simulation.
  - **Steps**: Use 3G/Edge simulation -> Open Learn section.
  - **Expected**: Content loads with graceful placeholders/spinners.

## 💾 2. App State & Persistence
- **Scenario**: Cold Start Resilience.
  - **Steps**: Force Stop app -> Clear Cache -> Launch.
  - **Expected**: App re-initializes correctly without loss of session/onboarding state.
- **Scenario**: Foreground/Background Transition.
  - **Steps**: Start a lesson -> Minimize app -> Wait 2 mins -> Resume.
  - **Expected**: Lesson state is preserved exactly where user left off.

## ♿ 3. Accessibility & UX Edge Cases
- **Scenario**: Font Scaling.
  - **Steps**: System Settings -> Display -> Font Size: Largest -> Open Hurd.
  - **Expected**: UI elements scale correctly; no text overlapping or clipping.
- **Scenario**: Screen Reader (TalkBack) Labels.
  - **Steps**: Enable TalkBack -> Navigate Bottom Bar.
  - **Expected**: Each icon has a descriptive content description (e.g., "Home Tab", "Learn Tab").

## 🔒 4. Privacy & Permissions
- **Scenario**: Camera Permission Refusal.
  - **Steps**: Go to Post -> Click Photo -> Deny Permission.
  - **Expected**: App handles denial gracefully, offering an explanation or alternative.
