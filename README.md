<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="/program_info/org.prismlauncher.PrismLauncher.logo-darkmode.svg">
    <source media="(prefers-color-scheme: light)" srcset="/program_info/org.prismlauncher.PrismLauncher.logo.svg">
    <img alt="FractalLauncher" src="/program_info/org.prismlauncher.PrismLauncher.logo.svg" width="40%">
  </picture>
</p>

<p align="center">
  <b>Fractal Launcher</b> is an advanced, privacy-focused and smart custom launcher for Minecraft.<br />
  Designed for power users, developers, and pack creators with enhanced security, split-screen mod platforms, and memory optimization.<br />
  <br />This is a custom fork, independent and <b>not</b> endorsed by or affiliated with Prism Launcher or MultiMC.
</p>

---

## ✨ Key Features & Unique Improvements

Fractal Launcher builds upon a robust core, introducing features tailored for maximum performance, privacy, and utility:

1. **Split-Screen Mod Browser:** Parallel, isolated `OffTheRecord` (Incognito) browsing of **Modrinth** (left) and **CurseForge** (right) with a unified search bar and direct link auto-detection. No cookies or local storage saved.
2. **Smart File Interceptor:** Auto-detects downloaded `.mrpack`/`.zip` packs, prompts for target instances on `.jar` mod downloads, and stores resource packs in a central folder linked via system symlinks.
3. **Paranoid Account Security:** Zero plain-text `accounts.json`. Token data uses a multi-step binary obfuscation pipeline (binary $\rightarrow$ JSON chunks $\rightarrow$ Base64 $\rightarrow$ binary storage) saved under a randomized filename in a user-defined path, with sessions wiped on exit by default.
4. **Dynamic Ephemeral Accounts:** Built-in guest profile option generating a random temporary username (3–16 chars) on-the-fly right before Java launch (`LaunchTask`) with zero disk footprint.
5. **Proprietary `.ssp` Containers:** Custom obfuscated container format for modpacks and pre-configured Minecraft versions protected by a 4-byte flag, optional password encryption, and embedded access policies (`pack_manifest.json`).
6. **Instance Locks & Version Control:** `AccountLockMode` locks (`instance.cfg`) restricting instances to online or offline modes only, plus a local `versionsmod` manifest system for snapshots and rollbacks.
7. **Local Skins Anywhere:** Optional automated injection of your custom skin mod at instance creation, mapping to a central `shared_skins/` folder to render local skins on vanilla servers.
8. **Power-User Utilities:** Built-in mod duplicate scanner (`mod_id`), config syntax analyzer (`.toml`/`.json`), and log stealth anonymizer (`[REDACTED]` paths).
9. **Memory Snapshot & Sentinel Watcher:** Total RAM liberation during gameplay—the heavy UI process dumps its state to a temporary snapshot and exits (`exit(0)`), leaving a lightweight background sentinel (`--restore-from`) to wake the launcher up instantly once Minecraft closes.

---

## Installation & Development Builds

- Check our repository releases for stable builds.
- Development builds can be compiled directly from the source code.

Prebuilt binaries are target-oriented for **Linux**, **Windows**, and **macOS**.

## Building

If you want to build Fractal Launcher yourself, clone the repository and configure it via CMake:

```bash
git clone [https://github.com/NoizeLoser/FractalLauncher.git](https://github.com/NoizeLoser/FractalLauncher.git)
cd FractalLauncher
cmake -B build -S .
cmake --build build

```

*Note: Make sure to clear or set your own API keys in [CMakeLists.txt](https://www.google.com/search?q=CMakeLists.txt) if you are distributing custom builds.*

## Forking & Redistribution Policy

You are free to fork and redistribute as long as you follow the terms of the [license](https://www.google.com/search?q=LICENSE):

* Make it clear that your fork is not FractalLauncher and is not endorsed by or affiliated with the FractalLauncher project.
* Modify or clear out API keys in [CMakeLists.txt](https://www.google.com/search?q=CMakeLists.txt) if necessary.

## License [](https://www.google.com/search?q=LICENSE)

All launcher code is available under the GPL-3.0-only license.

```
