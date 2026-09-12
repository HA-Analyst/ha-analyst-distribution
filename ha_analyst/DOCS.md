# HA Analyst – Private Beta Installation

Für den ersten Realtest bleibt alles privat. Home Assistant lädt das bereits gebaute Multi-Arch-Image `ghcr.io/ha-analyst/ha-analyst:1.0.17.75`; auf dem Home-Assistant-System findet dabei kein Native-/Nuitka-Build mehr statt.

## 1. GHCR-Zugriff in Home Assistant hinterlegen

GitHub Container Registry benötigt für private Images ein Personal Access Token (classic) mit mindestens `read:packages`.

In Home Assistant mit aktiviertem Erweiterten Modus:

1. Einstellungen → Apps/Add-ons → App-/Add-on-Store öffnen.
2. Drei-Punkte-Menü → Registries/Registrierungen.
3. Neue Registry hinzufügen:
   - Registry: `ghcr.io`
   - Benutzername: der GitHub-Benutzer mit Zugriff auf die private Organisation/package
   - Passwort: PAT (classic) mit `read:packages`

Das Token gehört ausschließlich in Home Assistant und niemals in dieses Repository.

## 2. Sourcefreie lokale Staging-Definition verwenden

Das Distributionsrepository bleibt für diesen Test privat und wird deshalb nicht als Remote-Custom-Repository geklont. Die Dateien aus diesem Ordner werden stattdessen als lokale App/Add-on-Definition unter dem lokalen Supervisor-App-Verzeichnis bereitgestellt (`addons/local/ha_analyst` bzw. der von Home Assistant dafür eingeblendete lokale App/Add-on-Pfad).

Benötigt werden nur:

- `config.yaml`
- `README.md`
- `DOCS.md`
- `CHANGELOG.md`

`config.yaml` enthält bereits:

```yaml
image: ghcr.io/ha-analyst/ha-analyst
version: 1.0.17.75
```

Home Assistant ergänzt den Versions-Tag und löst über das Multi-Arch-Manifest automatisch `amd64` bzw. `aarch64` auf.

## 3. Realtest

1. App-/Add-on-Store neu laden, bis die lokale HA-Analyst-Definition erscheint.
2. HA Analyst installieren.
3. Prüfen, dass Home Assistant das Image herunterlädt und nicht lokal baut.
4. HA Analyst starten.
5. Falls die Bridge neu installiert wurde, dem sichtbaren Hinweis folgen und Home Assistant einmal manuell neu starten.
6. Nach vollständiger Analyst-Readiness muss das verwaltete Dashboard automatisch erscheinen und echte Daten zeigen.
7. Zentralen HA-Analyst-Test-Runner ausführen.

Erwartung: Installation und Start sind deutlich schneller als beim früheren lokalen Build, weil ausschließlich das fertige private GHCR-Image geladen wird.

Staging-Dokumentation: https://github.com/HA-Analyst/ha-analyst-distribution  
Support / Feedback: https://github.com/HA-Analyst/ha-analyst-distribution/issues
