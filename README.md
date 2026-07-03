# OnePlus Ace PGKM10 Kernel

OnePlus Ace / PGKM10 / Dimensity 8100-MAX kernel research and build workspace.

Target recorded from device screenshots:

```text
Device: OnePlus Ace (PGKM10)
SoC: MediaTek Dimensity 8100-MAX / MT6895 family
ROM: PGKM10_15.0.0.1800(CN01B80P02)
Android: 15
Kernel shown on device: 5.10.236-android12-9-o-g6973d81cd2ac
Security patch: 2026-04-01
```

## Current status

- Repository scaffold created.
- GitHub reference projects found for OnePlus/Oppo MT6895 OOS/COS 15 ReSukiSU/SUSFS builds.
- Official OnePlusOSS branches for `PGKM10_15.0.0.1800(CN01)` found and pinned in `manifests/oos15/oneplus_ace_pgkm10_15.0.0.1800_v.xml`.
- First build target config is `configs/oos15/OP-ACE-PGKM10-1800.json`.

## Important safety note

The earlier downloaded reference AK3 package was `5.10.226-android12-oki-xiaoxiaow`, while this device reports `5.10.236-android12-9-o-g6973d81cd2ac`. It is useful as an AK3 structure reference, but it is not treated as a matching kernel for this phone.

## Build approach

1. Reproduce a clean PGKM10 ColorOS 15 kernel build from OnePlusOSS sources.
2. Verify the produced Image version and KMI baseline.
3. Add ReSukiSU/SUSFS via the copied ReSukiSU OnePlus build framework.
4. Package as AnyKernel3 zip.
5. Do not flash automatically; final flashing remains user-controlled.
