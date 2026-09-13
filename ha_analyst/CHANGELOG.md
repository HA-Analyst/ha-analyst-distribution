# HA Analyst – Changelog

## 1.0.17.79 – B0.1.01 – External Beta Distribution Preparation

### Deutsch

- Der sourcefreie Native-Core-Stand wird als vorgebautes Multi-Arch-Image für `amd64` und `aarch64` verteilt.
- Das generische Image `ghcr.io/ha-analyst/ha-analyst:1.0.17.79` wurde als Multi-Arch-Manifest veröffentlicht und mit dem Release-Manifest verknüpft.
- Das Distributionsrepository ist für Home Assistant anonym lesbar und enthält ausschließlich sourcefreie Distributionsmetadaten.
- Der Wechsel von einem alten lokalen `addons/ha_analyst`-Entwicklungsstand auf die Repository-Version ist dokumentiert; ein lokaler Bestand mit demselben Slug kann die Repository-Version im App-Store überlagern.
- Der Release-/Distribution-Vertrag wurde gehärtet: Versionsmetadaten werden aus `data/release.json` abgeleitet, sodass veraltete Template-Versionen den nächsten Publish nicht erneut blockieren.
- Die App-Konfiguration erhält native Home-Assistant-Übersetzungen für Deutsch und Englisch.
- README und Installationsdokumentation wurden als zweisprachige Beta-Oberfläche mit sichtbaren Angaben zu Version, Beta-Kanal, Home-Assistant-Mindestversion, Architekturen und sourcefreier Runtime überarbeitet.
- Analyst-Core, Dashboard-Lifecycle und bestehende Runtime-Sicherheitslogik werden durch diesen Distribution-/Dokumentationsblock nicht fachlich verändert.

### English

- The source-free native core is distributed as a prebuilt multi-arch image for `amd64` and `aarch64`.
- The generic image `ghcr.io/ha-analyst/ha-analyst:1.0.17.79` was published as a multi-arch manifest and recorded in the release manifest.
- The distribution repository is anonymously readable by Home Assistant and contains source-free distribution metadata only.
- Migration from an old local `addons/ha_analyst` development copy to the repository-managed version is documented; a local copy with the same slug can shadow the repository version in the app store.
- The release/distribution contract was hardened: version metadata is derived from `data/release.json`, preventing stale template versions from blocking a future publish again.
- App configuration now ships native Home Assistant translations for German and English.
- README and installation documentation were redesigned as a bilingual beta surface with visible version, beta channel, minimum Home Assistant version, architectures and source-free runtime information.
- Analyst Core, dashboard lifecycle and existing runtime security logic are not functionally changed by this distribution/documentation block.

## 1.0.17.76 – B0.0.99 – Fresh-Install Restart Observation Fix

### Deutsch

- Der erste echte private GHCR-/Multi-Arch-Installationspfad aus B0.0.98 wurde real bestätigt: Home Assistant konnte das vorgebaute `ghcr.io/ha-analyst/ha-analyst:1.0.17.75` installieren und starten, ohne den Analyst-Core lokal zu kompilieren.
- Beim vollständigen Clean-/Reinstall-Test wurde ein Fresh-Install-Race reproduziert: Eine bereits im laufenden Home Assistant geladene Bridge 1.3.6 konnte vor dem geforderten Core-Neustart dieselbe erwartete Versionsnummer melden. Dadurch wurde die Dashboard-Aktivierung zu früh freigegeben; der unmittelbar folgende Home-Assistant-Neustart hinterließ zunächst nur den Dashboard-Shell ohne sichtbare Karten.
- `discovery.sh` 1.5.0 akzeptiert einen offenen `core_restart_required`-Zustand nicht mehr allein aufgrund eines vorhandenen Config-Flows oder einer passenden Bridge-Version. Vor Discovery/Runtime-Verifikation muss ein tatsächlicher Neustart beobachtet werden.
- Ein normaler Home-Assistant-Core-Neustart wird als `Core down → Core up` erkannt und persistent in `bridge_install.json` markiert. Ein kompletter Host-Neustart wird zusätzlich über einen geänderten Supervisor-`host/info`-`boot_timestamp` erkannt.
- Analyst-Core, Native-Binary, Bridge 1.3.6, Frontend 1.8.5 und Dashboard 1.4.1 blieben fachlich unverändert.

### English

- The first real private GHCR/multi-arch installation path from B0.0.98 was validated: Home Assistant installed and started the prebuilt image without compiling Analyst Core locally.
- A fresh-install restart race was reproduced and fixed: an already loaded Bridge could report the expected version before the required Home Assistant Core restart had actually happened, allowing dashboard activation too early.
- `discovery.sh` 1.5.0 now requires evidence of an actual Home Assistant restart before Bridge discovery/runtime verification can close an outstanding restart requirement.
- Normal Core restart and full host restart paths are both observed persistently so an Analyst app restart alone cannot incorrectly satisfy the gate.
- Analyst Core, native binary, Bridge 1.3.6, Frontend 1.8.5 and Dashboard 1.4.1 remained functionally unchanged.

## 1.0.17.75 – B0.0.98 – Multi-Arch Release Pipeline Candidate

### Deutsch

- B0.0.97 ist real vollständig sourcefrei und mit Fast-Build-Cache validiert; diese Gates sind abgeschlossen.
- Der externe Compile-Pfad für vorgebaute `amd64`- und `aarch64`-Images wurde geöffnet, während der öffentliche Produkt-Publish fail-closed blieb.
- Ein privater GitHub-Actions-Workflow nutzt Home Assistants BuildKit-basierte Builder-Actions für Build-Matrix, Einzelarchitektur-Images und das generische Multi-Arch-Manifest.
- Beta-Tags bleiben unveränderlich: kein `latest`-Tag und kein stilles Überschreiben bereits veröffentlichter Versionen.
- Native-Core, Bridge 1.3.6, Frontend 1.8.5, Dashboard 1.4.1 und AppArmor blieben fachlich unverändert gegenüber dem real validierten B0.0.97-Stand.

### English

- B0.0.97 had already been fully validated as source-free with the fast-build cache; those gates were complete.
- The external compile path for prebuilt `amd64` and `aarch64` images was opened while the public product publish gate remained fail-closed.
- A private GitHub Actions workflow uses Home Assistant's BuildKit-based builder actions for the build matrix, architecture-specific images and the generic multi-arch manifest.
- Beta tags remain immutable: no `latest` tag and no silent overwrite of an already published version.
- Native Core, Bridge 1.3.6, Frontend 1.8.5, Dashboard 1.4.1 and AppArmor remained functionally unchanged from the real-world validated B0.0.97 baseline.
