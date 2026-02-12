# Robust QA Architecture

This document details the organization of the Hurd App QA project, ensuring professional standards, scalability, and clarity.

## 📁 Current Project Structure
- `tests/e2e/`: Maestro YAML flows organized by feature.
- `tests/manual/`: Markdown files for manual test cases and exploratory charters.
- `docs/`: Technical documentation and setup guides.
- `evidence/`: Artifacts from test runs (`errors.log`, `hierarchy.json`).
- `reports/`: Final QA reports and summaries.

## 🛠️ Core Features & Coverage
1. **E2E Automation**: Comprehensive flows implemented for:
    - Post exploration and deep dives.
    - Engagement (Feed interactions).
    - Learning path completion.
    - Profile verification.
    - Scores and Leaderboard.
2. **CI/CD**: Integrated GitHub Actions for automated Maestro test runs.
3. **Evidence System**: Dual reporting with persistent logs and latest run artifacts for rapid debugging.

## 🚀 Verification Standards
- All Maestro flows are verified to run against the provided APK.
- GitHub Actions environment is configured to monitor regression on main branches.

