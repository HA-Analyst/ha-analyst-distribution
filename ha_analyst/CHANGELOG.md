# HA Analyst – Changelog

## 1.0.17.75 – B0.0.98 – Multi-Arch Release Pipeline Candidate

### Was beinhaltet das Update?

- B0.0.97 ist real vollständig sourcefrei und mit Fast-Build-Cache validiert; diese Gates sind abgeschlossen.
- Der externe Compile-Pfad für vorgebaute `amd64`- und `aarch64`-Images ist geöffnet und real als lokaler GitHub-Runner-Build inklusive Architektur-, Versions- und Label-Prüfung validiert.
- Build und Publish sind getrennt: `Build Beta` enthält keine Registry-Publish-Schritte; `Publish Private Beta` ist separat bestätigt und auf den privaten GHCR-Namespace `ghcr.io/ha-analyst` begrenzt.
- Der öffentliche/externe Publish bleibt weiterhin fail-closed, bis Repository-, Dokumentations-, Support- und Lizenzangaben final gesetzt sind.
- Das Distributionsrepository bleibt sourcefrei und verweist auf das generische Multi-Arch-Image `ghcr.io/ha-analyst/ha-analyst`.
- Beta-Tags bleiben unveränderlich: kein `latest`-Tag während der Beta und kein stilles Überschreiben bereits veröffentlichter Versionen.
- Native-Core, Bridge 1.3.6, Frontend 1.8.5 (Build `3c0cdd1d9175`), Dashboard 1.4.1 und AppArmor bleiben fachlich unverändert gegenüber dem real validierten B0.0.98-Produktstand.
