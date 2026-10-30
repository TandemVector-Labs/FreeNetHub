# FreeNet Hub — Public Windows R53 and Linux R21

<p align="center">
  <a href="evidence/R37_INSTALLED_UI_DASHBOARD_20260929.png"><img src="evidence/R37_INSTALLED_UI_DASHBOARD_20260929.png" alt="FreeNet Hub — authentic installed dashboard screenshot captured from R37" width="1000"></a>
</p>
<p align="center"><sub>Historical installed-interface evidence (R37, September 2026), not a screenshot of the current R53 release or proof of a live protected connection.</sub></p>

FreeNet Hub controls connectivity on Windows and Linux with explicit Browser, Full System, and Console capabilities. Availability differs by provider and platform.

## Installation authority

**Official release and install authority:** [FreeNet Hub 4.3.9 R53 (Windows R53 and Linux R21 assets)](https://github.com/GOD13emad/FreeNetHub/releases/tag/v4.3.9-r53-windows-stable). See the [canonical upstream README](https://github.com/GOD13emad/FreeNetHub#readme) for current assets, limitations and verification.

### Windows R53 (v4.3.9) — public

- Asset: `FreeNetHub_4.3.9_R53_Setup.exe`
- SHA-256: `34A1A45383F8E35F7D23CBD12A76440D063CE43D49E3A5CC23A3518F947353A2`
- Release revision: `4.3.9-r53-inno-root-guard`.
- Upgrade: R51/R52 may upgrade in place under the original Inno AppId only when the registered uninstall root agrees with the selected existing installation and the safe-upgrade preflight passes. Conflicting canonical and temporary install roots **fail closed before file replacement or provider shutdown**; they are not automatically merged or deleted.
- Verified: exact public-main commit `17daff34805b82bcae0c6e8d5e6cbed6258c50ff` passed [postmerge CI 10/10](https://github.com/GOD13emad/FreeNetHub/actions/runs/38521651247), including fresh Windows install, R51/R52 upgrade, pinned rollback, data/settings preservation, split-root denial, Android/iOS simulator runtime and virtual acceptance.
- Live Windows R51 `UpdateCheck` independently discovered public R53 and its SHA-256 with `updateAvailable=true`, without disconnecting an active CFON listener. **This does not constitute installing R53 on that owner host.**
- The Windows installer is **unsigned by publisher choice**. Windows SmartScreen or Smart App Control may warn or block it. Do not disable security protections merely to install.

### Linux R21 — current public package

- Asset: `FreeNetHub_4.2.0_Linux_R21.zip`
- SHA-256: `82305E1A15684662B7711B53A84522122C6A11D618366314D9DD297B3A7FEC1A`
- Accepted installed revision: `4.2.0-linux.21-r54`.
- The [upstream release documentation](https://github.com/GOD13emad/FreeNetHub#linux-r21--current-public-package) records owner-host GTK, integrity, data-preserving R20→R21 upgrade, and browser-scoped CFON checks. These do **not** establish whole-system VPN or DNS-leak protection.
- R20 remains a historical rollback/reference asset in the same GitHub Release; **it is not the latest public Linux package**. Avoid updates while an active tunnel/session is running.

### Windows R52 and R51 — previous releases

- R52 (`4.3.8`) and R51 (`4.3.7`) remain historical/rollback authorities, not the Latest Windows installer. Published assets and SHA-256 digests are retained unchanged.
- Do not force an R53 upgrade while a provider listener is active or if two installs share one AppId with conflicting uninstall history. Preserve user data and use controlled recovery with verified rollback.

## Current capabilities

- Dashboard / Methods / Nodes / Tools / Settings desktop UI
- Browser, Full System, and Console scopes with explicit boundaries
- AUTO, Node Pool, WARP, GOOL, CFON, Tor/obfs4/Snowflake, Custom, and Direct paths where platform/runtime support is validated
- Node imports for SS, VMess, VLESS, Trojan, Hysteria v1/v2, TUIC, AnyTLS, plus validated standalone sing-box JSON imports for ShadowTLS, SSH, Snell, SOCKS, HTTP CONNECT, and Naive
- fail-closed handling for unsupported or unsafe imported local credential/certificate paths
- explicit node refresh, endpoint testing, performance testing, ranking, favorites/pins, metadata, filtering/sorting, and export
- revision-aware online update checks with downgrade protection
- normal application launch does not auto-connect networking

## Validation boundary

The published Windows R53 and Linux R21 assets are accepted only within the scopes verified by their own tests. Linux whole-system DNS-leak prevention, unsigned-Windows compatibility with Smart App Control, user-host installed R53 field GUI acceptance, physical console testing, production mobile forwarding/signing, and interactive Cloudflare challenge/login remain OPEN. A command-line HTTP 403 with cf-mitigated: challenge is not proof of a broken proxy or successful browser login.

No software can promise Internet access if all underlying paths are unavailable.

## Source and release authority

The exact asset names and SHA-256 digests of the official v4.3.9-r53-windows-stable release govern current installation; later source commits may update documentation without rebuilding the published installers. The repository has **no project-wide software license** (see `THIRD_PARTY_NOTICES.md`); third-party licenses are not a license grant for FreeNet Hub's own source. License choice is an owner/legal gate.

See SECURITY.md, issues #30/#32 and evidence/ for accepted and outstanding proof.
