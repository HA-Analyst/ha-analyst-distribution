# HA Analyst – Beta Distribution

HA Analyst ist eine Informations-, Analyse- und Wissensschicht für Home Assistant. Dieses Repository ist die sourcefreie Distribution: Der proprietäre Analyst-Core ist nicht Bestandteil des Repositories; Home Assistant bezieht stattdessen ein vorgebautes Multi-Arch-Image.

## Beta-Status

Die Distribution befindet sich in Vorbereitung für die externe Beta. `amd64` und `aarch64` werden unterstützt. Der Native-Runtime-, Source-Free-, Security-, Restart- und Multi-Arch-Pfad wurde vor der externen Freigabe real validiert.

Aktuelles Distributionsimage: `ghcr.io/ha-analyst/ha-analyst`.

## Installation

Nach der öffentlichen Beta-Freigabe kann dieses Repository als Home-Assistant-App-/Add-on-Repository eingebunden werden. HA Analyst installiert seine Home-Assistant-Bridge und das verwaltete Analyst-Dashboard über den vorgesehenen Onboarding-Ablauf. Falls nach einer Bridge-Installation ein Home-Assistant-Neustart erforderlich ist, fordert HA Analyst diesen ausdrücklich an; ein Neustart wird nicht automatisch ausgelöst.

Die detaillierte Installationsanleitung befindet sich in `ha_analyst/DOCS.md`.

## Support und Feedback

Fehlerberichte und Beta-Feedback werden über die GitHub Issues dieses Distributionsrepositories gesammelt. Vor einem Bericht bitte prüfen, ob Home Assistant und HA Analyst auf dem jeweils aktuellen Beta-Stand laufen.

## Datenschutz und Lizenz

HA Analyst analysiert Home-Assistant-Daten innerhalb der Installation. Die endgültigen Bedingungen für externe Beta, Lizenzierung, optionale Aktivierung/Entitlements und die dazugehörigen Datenschutzangaben werden vor der öffentlichen Freigabe separat festgelegt und dokumentiert.

Bis zur ausdrücklichen öffentlichen Beta-Freigabe ist dieses Repository als Release-Vorbereitung zu verstehen.
