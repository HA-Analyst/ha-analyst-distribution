# HA Analyst – Private Distribution Staging

Dieses Repository ist die sourcefreie Staging-Distribution für HA Analyst. Es enthält keinen Analyst-Core-Quellcode und verweist auf das vorgebaute Multi-Arch-Image `ghcr.io/ha-analyst/ha-analyst`.

Aktueller Stand: HA Analyst 1.0.17.75 / B0.0.98. `amd64` und `aarch64` wurden real gebaut und validiert. Der private GHCR-Publish ist erfolgreich abgeschlossen; das generische Multi-Arch-Manifest `ghcr.io/ha-analyst/ha-analyst:1.0.17.75` ist veröffentlicht und signiert.

Das GitHub-Repository und die GHCR-Pakete bleiben für diesen Staging-Test privat. Für den Pull eines privaten GHCR-Images muss Home Assistant Supervisor einmalig Registry-Zugangsdaten für `ghcr.io` erhalten. Dafür genügt ein GitHub Personal Access Token (classic) mit `read:packages`; Schreib- oder Repository-Rechte sind für den Image-Pull nicht erforderlich.

Da dieses Distributionsrepository selbst privat bleibt, wird es für den ersten Realtest nicht als Remote-Custom-Repository eingebunden. Stattdessen wird die kleine sourcefreie `ha_analyst/`-Struktur als lokales Home-Assistant-App-/Add-on-Staging verwendet. Damit testen wir ausschließlich den Pull und Start des vorgebauten GHCR-Images, ohne den Source-Code oder das Distributionsrepository öffentlich zu machen.
