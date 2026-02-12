# Hurd App - QA Assessment Greenhouse 🌿

Professional QA testing suite for the Hurd Android application.

## 🏗️ Project Architecture

```
.
├── .github/workflows/       # CI/CD - GitHub Actions
├── docs/                    # Technical & Strategy Documentation
├── evidence/                # Test artifacts (logs, hierarchy, screenshots)
│   ├── home.png, learn.png, contribute.png, scores.png, profile.png
│   └── errors.log, hierarchy.json
├── reports/                 # Final QA and Bug reports
└── tests/                   
    ├── e2e/                 # Maestro E2E Automation (4 flows)
    └── manual/              # Manual Test Cases & Advanced Scenarios
```

## 🛠️ Tech Stack
- **Framework**: [Maestro](https://maestro.mobile.dev/)
- **Android Tools**: `adb`, `logcat`, `dumpsys`
- **CI**: GitHub Actions
- **Language**: YAML (for tests), Markdown (for docs)

## 🚀 Cómo ejecutar las pruebas

### 1. Requisitos previos
- Instalar Maestro: `curl -Ls "https://get.maestro.mobile.dev" | bash`
- Conectar un emulador o dispositivo Android vía ADB.

### 2. Ejecutar Automatización
```bash
maestro test tests/e2e/
```

## 🐞 Reporte de Errores
Todos los hallazgos críticos están en [reports/qa_report.md](reports/qa_report.md) y las evidencias visuales en la carpeta `evidence/`.

---
**Maintained by**: Rodrigo & Antigravity AI
