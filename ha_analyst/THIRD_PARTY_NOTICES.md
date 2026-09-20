# HA Analyst - Third-Party Notices

**Produktversion:** `1.0.18.5`  
**Stand:** 19.09.2026

This file lists direct runtime dependencies, relevant transitive runtime dependencies, and build-only tools used by the HA Analyst build pipeline. The exact final container images require an additional image-level SBOM before external release.

## Runtime / shipped dependency inventory

| Component | Version | License | Project |
| --- | --- | --- | --- |
| websocket-client | 1.9.0 | Apache-2.0 | https://github.com/websocket-client/websocket-client |
| PyYAML | 6.0.3 | MIT | https://pyyaml.org/ |
| cryptography | 46.0.4 | Apache-2.0 OR BSD-3-Clause | https://github.com/pyca/cryptography |
| cffi | 2.1.1 | MIT | https://cffi.readthedocs.io/ |
| pycparser | 3.0 | BSD-3-Clause | https://github.com/eliben/pycparser |

## Build-only provenance

| Tool | Version | License | Project |
| --- | --- | --- | --- |
| Nuitka | 4.2.1 | AGPL-3.0-or-later WITH Nuitka-runtime-exception | https://nuitka.net/ |
| rjsmin | 1.2.2 | Apache-2.0 | https://pypi.org/project/rjsmin/1.2.2/ |
| patchelf-pypi | 0.17.2.4 | Apache-2.0 AND GPL-3.0-or-later | https://pypi.org/project/patchelf/0.17.2.4/ |

## Base image

- `ghcr.io/home-assistant/base:3.24-2026.08.0`
- The base-image and Alpine package licenses are finalized from the exact built amd64/aarch64 image SBOM, not guessed from the source tree.

## Distribution rule

The vendored Python runtime retains package metadata/license files produced by pip. Before Closed-Beta freeze, the exact image SBOM and notices must be archived with the immutable release digest.

## Sources used for build-tool license classification

- Nuitka 4.2.1: https://pypi.org/project/Nuitka/ (AGPL-3.0 with documented runtime exception).
- rjsmin 1.2.2: https://pypi.org/project/rjsmin/1.2.2/ (Apache-2.0).
- patchelf 0.17.2.4 PyPI wrapper: https://pypi.org/project/patchelf/0.17.2.4/ (wrapper Apache-2.0; bundled upstream patchelf GPL-3.0-or-later).
