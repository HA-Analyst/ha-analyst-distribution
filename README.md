# HA Analyst – Private Distribution Staging

Dieses Repository ist die sourcefreie Staging-Distribution für HA Analyst. Es enthält keinen Analyst-Core-Quellcode und verweist auf das vorgebaute Multi-Arch-Image `ghcr.io/ha-analyst/ha-analyst`.

Aktueller Stand: HA Analyst 1.0.17.75 / B0.0.98. Der Multi-Arch-Build für `amd64` und `aarch64` ist real validiert. Der private GHCR-Publish ist vorbereitet, aber noch nicht ausgeführt.

Wichtig: Das Repository bleibt vorerst privat. Für einen Home-Assistant-Installationstest gegen private GitHub-/GHCR-Ziele ist zusätzliche Authentifizierung nötig; dieser Schritt wird erst nach dem ersten privaten Registry-Publish festgelegt.
