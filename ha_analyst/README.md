# HA Analyst Beta

![Beta](https://img.shields.io/badge/channel-Beta-orange)
![Version](https://img.shields.io/badge/version-1.0.17.81-blue)
![Home Assistant](https://img.shields.io/badge/Home%20Assistant-2026.9%2B-41BDF5)
![Architectures](https://img.shields.io/badge/arch-amd64%20%7C%20aarch64-6E56CF)
![Runtime](https://img.shields.io/badge/runtime-source--free-success)

**Deutsch** · [English](#english)

HA Analyst ist eine Informations-, Analyse- und Wissensschicht für Home Assistant. Er strukturiert den vorhandenen Hauszustand automatisch und stellt daraus verständliche Übersichten, Zusammenhänge und Diagnoseinformationen bereit.

### Was HA Analyst abdeckt

- 👁️ **Beobachten** – automatischer Überblick über Haus, Bereiche, Geräte und relevante Zustände.
- 🧭 **Verstehen** – kontextreiche Analyst-Karten und fachliche Drill-downs statt reiner Entity-Listen.
- ⚡ **Handeln** – Grundlage für optionale, kontextbezogene Bedienung auf Basis fachlicher Objekte und Absichten.
- 📈 **Verbessern** – Diagnose, Qualitätsbewertung und schrittweise tiefere Analysen.

### Beta-Status

| Merkmal | Stand |
| --- | --- |
| Version | `1.0.17.81` |
| Kanal | Beta |
| Home Assistant | `2026.9.0+` |
| Architektur | `amd64`, `aarch64` |
| Dashboard | Automatisch nach vollständiger Analyst-Readiness |
| Runtime | Vorgebautes, sourcefreies Multi-Arch-Image |

> **Hinweis:** Diese Distribution enthält keinen offenen Analyst-Core-Quellcode. Home Assistant bezieht das vorgebaute Multi-Arch-Image für die passende Plattform.

### Schnellstart

1. Distributionsrepository in Home Assistant hinzufügen.
2. **HA Analyst** installieren und starten.
3. Wenn Home Assistant einen Neustart für die Bridge verlangt, den sichtbaren Hinweis befolgen und Home Assistant einmal neu starten.
4. Nach vollständiger Analyst-Readiness wird das verwaltete Dashboard automatisch synchronisiert.

📘 [Dokumentation](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/DOCS.md) · 🧾 [Changelog](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/CHANGELOG.md) · 💬 [Support / Feedback](https://github.com/HA-Analyst/ha-analyst-distribution/issues)

---

## English

HA Analyst is an information, analysis and knowledge layer for Home Assistant. It automatically structures the current state of a home and turns it into understandable overviews, relationships and diagnostic information.

### What HA Analyst covers

- 👁️ **Observe** – automatic overview of the home, areas, devices and relevant states.
- 🧭 **Understand** – context-rich Analyst cards and domain-oriented drill-downs instead of raw entity lists.
- ⚡ **Act** – foundation for optional context-aware control based on domain objects and user intent.
- 📈 **Improve** – diagnostics, quality assessment and progressively deeper analysis.

### Beta status

| Item | Status |
| --- | --- |
| Version | `1.0.17.81` |
| Channel | Beta |
| Home Assistant | `2026.9.0+` |
| Architectures | `amd64`, `aarch64` |
| Dashboard | Automatically synchronized after full Analyst readiness |
| Runtime | Prebuilt source-free multi-arch image |

> **Note:** This distribution does not contain the open Analyst Core source code. Home Assistant pulls the prebuilt multi-arch image for the matching platform.

### Quick start

1. Add the distribution repository to Home Assistant.
2. Install and start **HA Analyst**.
3. If Home Assistant requests a restart for the Bridge, follow the visible notice and restart Home Assistant once.
4. After full Analyst readiness, the managed dashboard is synchronized automatically.

📘 [Documentation](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/DOCS.md) · 🧾 [Changelog](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/CHANGELOG.md) · 💬 [Support / Feedback](https://github.com/HA-Analyst/ha-analyst-distribution/issues)
