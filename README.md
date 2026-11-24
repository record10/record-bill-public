# Record Bill Releases
Public repository for releases of the Record Bill application.

## Running a build

Actions → **Release** → Run workflow. Inputs: `branch` of the private source repo (`qa` or `main`), and one switch each for macOS, Windows, Linux and Android. The workflow clones the private repo with the `PRIVATE_REPO_PAT` secret (read-only, kept masked), reads the version from `tauri.conf.json`, and attaches the installers to a **draft** release here: production builds are tagged `v<version>`, `qa` builds `v<version>-qa.<run number>` and marked pre-release. The release page is public once you publish the draft; the source stays private.
