# Robust QA Architecture Expansion

This plan details the reorganization of the Hurd App QA project to ensure professional standards, scalability, and clarity.

## 📁 Proposed Folder Structure
- `tests/e2e/`: Maestro YAML flows organized by feature.
- `tests/manual/`: Markdown files for manual test cases and exploratory charters.
- `docs/`: Comprehensive technical documentation.
- `evidence/`: Artifacts from test runs (`errors.log`, `hierarchy.json`, screenshots).
- `reports/`: Final QA reports and summaries.

## 🛠️ Planned Improvements
1. **E2E Tests**: Implement flows for:
    - Post creation (Text/Image).
    - Engagement (Like/Comment).
    - Learning path completion.
    - Profile navigation and verification.
2. **Git/CI**: Update `.gitignore` to allow specific debugging files while excluding heavy binary assets.
3. **Documentation**: Create a master `README.md` explaining the stack, architecture, and how to replicate the tests.

## 🚀 Verification Plan
- Validate that all Maestro flows run in the new directory structure.
- Ensure GitHub Actions correctly triggers on the new structure.
