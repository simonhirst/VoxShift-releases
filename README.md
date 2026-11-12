# Vox Shift releases

Installers and update manifests for **Vox Shift**, by Simon Hirst: local dictation and British read-aloud for
Windows and macOS. Speech recognition and reading run entirely on your computer.

This repository holds releases only; there is no source code here.

## Install

Download `VoxShift-<version>-windows-x64-setup.exe` from the latest release and run it. It installs for your
user account, with no administrator prompt.

The installer is not code-signed yet, so Windows SmartScreen may warn on first run ("More info", then "Run
anyway"). To check the download, compare its SHA-256 with the one in the release notes:

```powershell
Get-FileHash .\VoxShift-<version>-windows-x64-setup.exe -Algorithm SHA256
```

## Updates

Vox Shift checks this repository's latest release once a day, if you allow it in Settings › General. It reads
`update-manifest.json`, which is signed by the author. An update installs only if that signature and the
download's SHA-256 both check out. The check sends nothing about you or what you dictate.
