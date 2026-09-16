# HA Analyst – Installation / Setup

**Deutsch** · [English version](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/DOCS.md#english)

## Deutsch

### Voraussetzungen

- Home Assistant `2026.9.0` oder neuer.
- Unterstützte Architektur: `amd64` oder `aarch64`.
- Administrativer Zugriff auf den Home-Assistant-App-Store.

### Installation

> HA Analyst wird als **Home-Assistant-App** (früher Add-on) installiert. Es handelt sich nicht um eine HACS-Integration; HACS wird für die Installation nicht verwendet.

1. Das HA-Analyst-Distributionsrepository im Home-Assistant-App-Store hinzufügen.
2. **HA Analyst** als App installieren und starten.
3. Falls die Bridge neu installiert oder aktualisiert wurde, dem sichtbaren Hinweis folgen und Home Assistant einmal manuell neu starten.
4. Nach vollständiger Analyst-Readiness wird das verwaltete Dashboard automatisch synchronisiert.
5. Das Dashboard erst dann als betriebsbereit bewerten, wenn die Analyst-Karten echte Daten anzeigen.

### Update

- Updates werden über dasselbe Repository angeboten.
- Während der Beta werden unveränderliche Versions-Tags verwendet; es gibt keinen beweglichen `latest`-Tag.
- Bei Bridge-Änderungen kann erneut ein Home-Assistant-Neustart erforderlich sein. Der Analyst weist sichtbar darauf hin.

### Wechsel von einem lokalen Entwicklungsstand

Wenn zuvor ein lokaler App-Ordner mit demselben Slug `ha_analyst` verwendet wurde, muss dieser lokale Bestand entfernt werden, bevor die Repository-Version eindeutig verwendet werden kann. Ein lokaler Bestand kann die Repository-Version im App-Store überlagern.

### Support & Diagnosepaket

HA Analyst enthält im Ingress-Konfigurator den Bereich **Support & Beta-Diagnose**. Bei einem Problem zuerst den **Runtime-Selbsttest** ausführen und danach **Diagnosepaket herunterladen** wählen. Das ZIP enthält technische Release-, Installations-, Readiness-, Capability-, Integrations-, Konsistenz- und Dashboard-Zusammenfassungen sowie Runtime-Dateimetadaten. Es enthält keine Rohzustände, Entity-/Device-IDs, Benutzerkonfiguration, Home-Assistant-/Zigbee2MQTT-Tokens, Lizenzschlüssel oder signierte Lease-Tokens.

Für einen Beta-Fehlerbericht bitte HA-Analyst-Version/Build, Home-Assistant-Version, Architektur (`amd64`/`aarch64`), Testart (Fresh Install/Update/Recovery), sichtbaren Bridge-Neustartstatus, Ergebnis des Runtime-Selbsttests, ungefähren Fehlerzeitpunkt und das Diagnosepaket angeben. Keine zusätzlichen Logs oder Screenshots veröffentlichen, wenn darin Zugangsdaten, interne URLs oder persönliche Hausdaten sichtbar sind.

Für geplante Abnahmeläufe steht im öffentlichen Support-Bereich zusätzlich das strukturierte **HA Analyst beta acceptance report**-Formular bereit. Es trennt Fresh Install, Update, Recovery, Runtime und Diagnose-Abnahme und verlangt keine geheimen oder hausbezogenen Daten.

### Was bei Problemen hilfreich ist

1. App-Protokoll öffnen und den Zeitpunkt des Fehlers notieren.
2. Prüfen, ob ein Home-Assistant-Neustart für die Bridge noch aussteht.
3. Prüfen, ob Dashboard und Karten nach Analyst-Readiness echte Daten anzeigen.
4. Runtime-Selbsttest ausführen und das vorgesehene Diagnosepaket erzeugen.
5. Diagnose-/Supportinformationen nur über die vorgesehenen Analyst-Funktionen weitergeben; keine Home-Assistant-Zugangsdaten oder Tokens veröffentlichen.

📘 [Dokumentation](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/DOCS.md) · 🧾 [Changelog](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/CHANGELOG.md) · 💬 [Support / Feedback](https://github.com/HA-Analyst/ha-analyst-distribution/issues)

---

## English

### Requirements

- Home Assistant `2026.9.0` or newer.
- Supported architecture: `amd64` or `aarch64`.
- Administrative access to the Home Assistant app store.

### Installation

> HA Analyst is installed as a **Home Assistant app** (formerly add-on). It is not a HACS integration, and HACS is not used for installation.

1. Add the HA Analyst distribution repository to the Home Assistant app store.
2. Install and start **HA Analyst** as an app.
3. If the Bridge was newly installed or updated, follow the visible notice and restart Home Assistant once.
4. After full Analyst readiness, the managed dashboard is synchronized automatically.
5. Treat the dashboard as operational only after the Analyst cards display real data.

### Update

- Updates are delivered through the same repository.
- During beta, immutable version tags are used; there is no moving `latest` tag.
- Bridge changes may require another Home Assistant restart. HA Analyst provides a visible notice when this is required.

### Migrating from a local development installation

If a local app folder with the same `ha_analyst` slug was used previously, remove that local copy before relying on the repository-managed version. A local copy can shadow the repository version in the app store.

### Support & diagnostics package

HA Analyst provides **Support & beta diagnostics** in its Home Assistant Ingress configuration UI. When reporting a problem, run the **runtime self-test** first and then choose **Download diagnostics package**. The ZIP contains technical release, installation, readiness, capability, integration, consistency and dashboard summaries plus runtime-file metadata. It does not contain raw states, entity/device IDs, user configuration, Home Assistant or Zigbee2MQTT tokens, license keys or signed lease tokens.

For a beta issue report, include the HA Analyst version/build, Home Assistant version, architecture (`amd64`/`aarch64`), test type (fresh install/update/recovery), visible Bridge restart state, runtime self-test result, approximate failure time and the diagnostics package. Do not publish additional logs or screenshots if they expose credentials, internal URLs or private household data.

For planned acceptance runs, the public support area also provides the structured **HA Analyst beta acceptance report** form. It separates fresh install, update, recovery, runtime and diagnostics acceptance without requesting secrets or household data.

### Useful information when reporting a problem

1. Open the app log and note when the problem occurred.
2. Check whether a Home Assistant restart for the Bridge is still pending.
3. Verify that the dashboard and cards show real data after Analyst readiness.
4. Run the runtime self-test and create the intended diagnostics package.
5. Share diagnostic/support information only through the intended Analyst mechanisms; never publish Home Assistant credentials or tokens.

📘 [Documentation](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/DOCS.md#english) · 🧾 [Changelog](https://github.com/HA-Analyst/ha-analyst-distribution/blob/main/ha_analyst/CHANGELOG.md) · 💬 [Support / Feedback](https://github.com/HA-Analyst/ha-analyst-distribution/issues)
