# HA Analyst – Changelog

## 1.0.17.76 – B0.0.99 – Fresh-Install Restart Observation Fix

### Was beinhaltet das Update?

- Der erste echte private GHCR-/Multi-Arch-Installationspfad aus B0.0.98 wurde real bestätigt: Home Assistant konnte das vorgebaute `ghcr.io/ha-analyst/ha-analyst:1.0.17.75` installieren und starten, ohne den Analyst-Core lokal zu kompilieren.
- Beim vollständigen Clean-/Reinstall-Test wurde ein Fresh-Install-Race reproduziert: Eine bereits im laufenden Home Assistant geladene Bridge 1.3.6 konnte vor dem geforderten Core-Neustart dieselbe erwartete Versionsnummer melden. Dadurch wurde die Dashboard-Aktivierung zu früh freigegeben; der unmittelbar folgende Home-Assistant-Neustart hinterließ zunächst nur den Dashboard-Shell ohne sichtbare Karten.
- `discovery.sh` 1.5.0 akzeptiert einen offenen `core_restart_required`-Zustand nicht mehr allein aufgrund eines vorhandenen Config-Flows oder einer passenden Bridge-Version. Vor Discovery/Runtime-Verifikation muss ein tatsächlicher Neustart beobachtet werden.
- Ein normaler Home-Assistant-Core-Neustart wird als `Core down → Core up` erkannt und persistent in `bridge_install.json` markiert. Ein kompletter Host-Neustart wird zusätzlich über einen geänderten Supervisor-`host/info`-`boot_timestamp` erkannt, sodass der Schutz auch einen App-Prozessneustart überlebt.
- Erst nach dieser Neustartbeobachtung folgen Bridge-Discovery, Runtime-Verifikation und Dashboard-Aktivierung. Ein bloßer HA-Analyst-App-Neustart kann das Restart-Gate nicht mehr fälschlich schließen.
- Analyst-Core, Native-Binary, Bridge 1.3.6, Frontend 1.8.5 und Dashboard 1.4.1 bleiben fachlich unverändert. Die Änderung liegt ausschließlich im günstigen Discovery-/Payload-Pfad; der Native-Input-Fingerprint bleibt `84dd99590fad76f5afee3ae3f028555df26d69a3e6f0f71d31d1d9a98a83113c`.
- B0.0.99 verwendet den neuen unveränderlichen privaten Image-Tag `1.0.17.76`; B0.0.98 / `1.0.17.75` bleibt als erste real erfolgreiche private Multi-Arch-Publish-Referenz unverändert erhalten.

## 1.0.17.75 – B0.0.98 – Multi-Arch Release Pipeline Candidate

### Was beinhaltet das Update?

- B0.0.97 ist real vollständig sourcefrei und mit Fast-Build-Cache validiert; diese Gates sind abgeschlossen.
- Der externe Compile-Pfad für vorgebaute `amd64`- und `aarch64`-Images wird geöffnet. Der eigentliche Publish bleibt weiterhin fail-closed, bis Registry-, Repository-, Dokumentations-, Support- und Lizenzangaben final gesetzt sind.
- Ein produktionsnaher privater GitHub-Actions-Workflow nutzt Home Assistants aktuelle BuildKit-basierten Builder-Actions für Build-Matrix, Einzelarchitektur-Images und das generische Multi-Arch-Manifest.
- Für lokale/private Build-VMs kann `tools/release_pipeline.py plan` den vollständigen Image-/Tag-Plan ausgeben und `compile --arch ...` einzelne Architekturimages mit Docker Buildx bauen. Ohne explizites `--push` werden keine Registry-Artefakte veröffentlicht.
- Der öffentliche App-Repository-Pfad verwendet weiterhin nur ein sourcefreies Gerüst mit `image: ghcr.io/HA-Analyst/ha-analyst`; das generische Image wird später über das Multi-Arch-Manifest automatisch auf die passende Plattform aufgelöst.
- Beta-Tags bleiben unveränderlich: kein `latest`-Tag während der Beta und kein stilles Überschreiben bereits veröffentlichter Versionen.
- Native-Core, Bridge 1.3.6, Frontend 1.8.5 (Build `3c0cdd1d9175`), Dashboard 1.4.1 und AppArmor bleiben fachlich unverändert gegenüber dem real validierten B0.0.97-Stand.
- Der Native-Input-Fingerprint bleibt `84dd99590fad76f5afee3ae3f028555df26d69a3e6f0f71d31d1d9a98a83113c`; reine Release-/Pipeline-Metadaten dürfen keinen Native-Recompile auslösen.
