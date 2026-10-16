# PumpSaver firmware releases

Compiled firmware for PumpSaver pump controllers. This repository holds
**release binaries only**; the source is kept elsewhere.

A controller installs from here only when an operator presses
**System › Firmware › Check for update** and then **Install**. It never
updates on its own.

Each release is tagged `v<version>` and carries exactly one file,
`pumpsaver-firmware.bin`, which is the real-drive build. Before a controller
boots it, the file must pass the ESP image check, match the SHA-256 GitHub
publishes for it, and carry a build marker naming that version.

Releases are published by `tools/release.ps1` in the source repository.
Do not upload other files under that name, and do not re-use a version
number. Controllers compare versions, so a re-used number is never offered.
