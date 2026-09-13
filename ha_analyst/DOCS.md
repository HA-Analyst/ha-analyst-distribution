# HA Analyst – Beta-Installation

## Voraussetzungen

- Home Assistant OS mit Supervisor/App-Unterstützung
- Home Assistant Core 2026.9.0 oder neuer
- Unterstützte Architektur: `amd64` oder `aarch64`
- Administratorzugriff für Installation und Konfiguration

## Installation

1. Das HA-Analyst-Distributionsrepository in Home Assistant als App-/Add-on-Repository hinzufügen.
2. **HA Analyst** auswählen und installieren.
3. HA Analyst starten und den Einrichtungsstatus im Analyst-Panel verfolgen.
4. Falls die Bridge neu installiert oder aktualisiert wurde und HA Analyst einen Home-Assistant-Neustart anfordert, Home Assistant einmal manuell neu starten. HA Analyst startet Home Assistant nicht selbstständig neu.
5. Warten, bis der Analyst seine Daten vollständig aufgebaut hat. Das verwaltete Dashboard wird erst nach bestätigter Data-Readiness automatisch aktiviert bzw. synchronisiert.
6. Sollte ein bereits geöffnetes Browserfenster danach noch alte oder fehlende Custom-Cards anzeigen, einmal `Strg+F5` ausführen. Wiederholte Hard-Reloads während noch laufender Dashboard-Registrierung sind nicht erforderlich.

## Was HA Analyst einrichtet

HA Analyst stellt seine eigene Home-Assistant-Bridge, das Analyst-Konfigurationspanel und ein verwaltetes Analyst-Dashboard bereit. Die fachliche Analyse bleibt zentral im Analysten; das Dashboard konsumiert die daraus erzeugten strukturierten Hausinformationen.

## Beta-Feedback

Für einen Fehlerbericht bitte möglichst folgende Angaben beifügen:

- HA-Analyst-Version
- Home-Assistant-Core-Version
- Architektur (`amd64` oder `aarch64`)
- kurze Beschreibung des erwarteten und tatsächlichen Verhaltens
- relevante Analyst-Diagnoseinformationen oder Logs ohne Zugangsdaten, Tokens oder andere Geheimnisse

Support und Beta-Feedback: GitHub Issues dieses Distributionsrepositories.

## Beta-Hinweis

Die externe Beta ist für reale Installationen gedacht, bleibt aber Vorabsoftware. Lizenz-, Aktivierungs-/Entitlement- und Datenschutzbedingungen werden vor der öffentlichen Freigabe verbindlich dokumentiert.
