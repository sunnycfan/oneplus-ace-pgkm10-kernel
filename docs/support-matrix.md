# Support matrix: OnePlus Ace PGKM10

Checked against:

- Bouteillepleine/ReSukiSu_Oneplus-
- WildKernels/OnePlus_KernelSU_SUSFS
- current build artifact from run 28654742256

## Current build

```text
AK3_OP-ACE-PGKM10-1800_OOS15_android12-5.10.236_RSKSU_35001_SuSFS_v2.2.0.zip
Kernel: 5.10.236-android12-OP-ACE-PGKM10
ReSukiSU: 35001
SuSFS: v2.2.0
```

## Feature status

```text
ReSukiSU: yes
SuSFS: yes
KPM: not enabled / not provided by the current OnePlus Ace build framework
```

## Evidence

SuSFS:

- `configs/oos15/OP-ACE-PGKM10-1800.json` sets `susfs: true`.
- Build metadata contains `v2.2.0`.
- AK3 zip contains `ksu_module_susfs_1.5.2+_CI.zip`.
- Image strings include `susfs is initialized! version: v2.2.0` and SUSFS config symbols.

KPM:

- The inspected OnePlus/Oppo/Realme build frameworks do not expose a `kpm` option in device configs or workflow inputs.
- No `CONFIG_KPM` / `CONFIG_KSU_KPM` configuration is written by the workflow.
- The current AK3 zip does not include a KPM loader or `.kpm` payload.
- Any incidental `lkpm` strings in the Image are not treated as KPM support evidence.

Conclusion: this PGKM10 line currently supports ReSukiSU + SuSFS, but should be treated as not KPM-capable unless a separate SukiSU/KPM integration path is added and verified.
