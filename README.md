# HA Analyst – Beta Distribution

**Deutsch** · [English](#english)

## Deutsch

HA Analyst ist eine Informations-, Analyse- und Wissensschicht für Home Assistant. Dieses Repository ist die sourcefreie Distribution: Der proprietäre Analyst-Core ist nicht Bestandteil des Repositories; Home Assistant bezieht stattdessen ein vorgebautes Multi-Arch-Image.

### Beta-Status

Die Distribution befindet sich in Vorbereitung für die externe Beta. `amd64` und `aarch64` werden unterstützt. Native Runtime, Source-Free-Runtime, Security-, Restart- und Multi-Arch-Pfad wurden vor der externen Freigabe real validiert.

Aktuelles Distributionsimage: `ghcr.io/ha-analyst/ha-analyst`.

### Öffentliche Beta-Ressourcen

- [Installation und Beta-Dokumentation](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/DOCS.md)
- [Changelog](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/CHANGELOG.md)
- [Support und Beta-Feedback](https://github.com/HA-Analyst/ha-analyst-distribution/issues)
- [Strukturierter Beta-Abnahmebericht](https://github.com/HA-Analyst/ha-analyst-distribution/issues/new?template=beta-acceptance-report.yml)
- [Beta-Fehlerbericht](https://github.com/HA-Analyst/ha-analyst-distribution/issues/new?template=beta-bug-report.yml)

Diese Ziele liegen vollständig im öffentlichen Distributionsrepository und bleiben damit unabhängig vom privaten Entwicklungsrepository erreichbar.

### Installation

Nach der ausdrücklichen externen Beta-Freigabe kann dieses Repository als Home-Assistant-App-Repository eingebunden werden. HA Analyst ist eine **Home-Assistant-App** (früher Add-on) und keine HACS-Integration; die Installation erfolgt im Home-Assistant-App-Store, nicht über HACS. HA Analyst installiert seine Home-Assistant-Bridge und das verwaltete Analyst-Dashboard über den vorgesehenen Onboarding-Ablauf. Falls nach einer Bridge-Installation ein Home-Assistant-Neustart erforderlich ist, fordert HA Analyst diesen ausdrücklich an; ein Neustart wird nicht automatisch ausgelöst.

Die detaillierte Installationsanleitung befindet sich unter [ha_analyst/DOCS.md](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/DOCS.md).

### Support und Feedback

Fehlerberichte und Beta-Feedback werden über die [GitHub Issues dieses Distributionsrepositories](https://github.com/HA-Analyst/ha-analyst-distribution/issues) gesammelt. Für geplante Abnahmeläufe steht ein strukturierter Beta-Abnahmebericht bereit. Bitte vor einem Bericht prüfen, ob Home Assistant und HA Analyst auf dem jeweils aktuellen Beta-Stand laufen.

### Datenschutz und Lizenz

HA Analyst analysiert Home-Assistant-Daten innerhalb der Installation. Die Lizenzprüfung ist für die vorgesehenen Offline-Lizenzen lokal ausgelegt; eine Lizenzanfrage oder -erneuerung übermittelt nur dann Personen-/Bezugsdaten, wenn der Nutzer diesen Vorgang ausdrücklich auslöst. Die finalen Bedingungen und Datenschutzangaben für die externe Beta werden vor Freigabe veröffentlicht.

Bis zur ausdrücklichen externen Beta-Freigabe ist dieses Repository als Release-Vorbereitung zu verstehen.

---

## English

HA Analyst is an information, analysis and knowledge layer for Home Assistant. This repository is the source-free distribution: the proprietary Analyst Core source is not part of the repository; Home Assistant pulls a prebuilt multi-architecture image instead.

### Beta status

The distribution is being prepared for the external beta. `amd64` and `aarch64` are supported. The native runtime, source-free runtime, security, restart and multi-architecture paths were validated before external release.

Current distribution image: `ghcr.io/ha-analyst/ha-analyst`.

### Public beta resources

- [Installation and beta documentation](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/DOCS.md#english)
- [Changelog](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/CHANGELOG.md)
- [Support and beta feedback](https://github.com/HA-Analyst/ha-analyst-distribution/issues)
- [Structured beta acceptance report](https://github.com/HA-Analyst/ha-analyst-distribution/issues/new?template=beta-acceptance-report.yml)
- [Beta bug report](https://github.com/HA-Analyst/ha-analyst-distribution/issues/new?template=beta-bug-report.yml)

All of these resources live in the public distribution repository and therefore remain available independently of the private development repository.

### Installation

After the external beta is explicitly opened, this repository can be added to the Home Assistant app store. HA Analyst is a **Home Assistant app** (formerly add-on), not a HACS integration; install it from the Home Assistant app store, not through HACS. HA Analyst installs its Home Assistant Bridge and managed Analyst dashboard through the intended onboarding flow. If a Home Assistant restart is required after Bridge installation or update, HA Analyst shows an explicit notice; it does not restart Home Assistant automatically.

Detailed installation instructions are available in [ha_analyst/DOCS.md](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/DOCS.md#english).

### Support and feedback

Bug reports and beta feedback are collected through the [GitHub Issues of this distribution repository](https://github.com/HA-Analyst/ha-analyst-distribution/issues). A structured beta acceptance report is available for planned acceptance runs. Before reporting an issue, please verify that Home Assistant and HA Analyst are on the current beta versions.

### Privacy and licensing

HA Analyst analyses Home Assistant data inside the installation. The planned offline license model verifies licenses locally; personal or purchase-reference data is transmitted only when the user explicitly initiates a license request, extension or reissue. Final external-beta terms and privacy information will be published before the beta is opened.

Until the external beta is explicitly opened, this repository should be treated as release preparation.
