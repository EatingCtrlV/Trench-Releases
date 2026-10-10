# Trench Releases

Downloads and updates for **Trench**, a Windows desktop workspace for real terminal sessions and text files, with agent and editor windows on shared canvases alongside tasks and sprints.

This repository only hosts the installers. The Trench source code is private.

## Download

1. Open the [latest release](../../releases/latest).
2. Download **Trench-Setup-&lt;version&gt;.exe** and run it. It installs for your Windows account only, with no administrator rights and no Node or npm needed.
3. Trench checks this page for newer versions and tells you when one is available.

The other files in a release (`latest.yml`, `*.blockmap`) are used by Trench's updater. You do not need to download them.

## Windows SmartScreen warning

The installer is **not code-signed yet**. Windows SmartScreen may show "Windows protected your PC". Choose **More info**, then **Run anyway**. You can check your download against the SHA-256 listed with each release.

## Verify your download

Each release includes a `.sha256` file. In PowerShell:

```powershell
(Get-FileHash .\Trench-Setup-<version>.exe -Algorithm SHA256).Hash.ToLower()
```

The output must match the hash in the `.sha256` file.

## Your data

Trench keeps your projects and settings in `%LOCALAPPDATA%\Trench`. Updating or uninstalling keeps them unless you tick "Also delete my Trench data" in the uninstaller.
