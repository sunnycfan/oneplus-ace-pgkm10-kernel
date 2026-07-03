# Resource search log

Relevant hits:

```text
WildKernels/OnePlus_KernelSU_SUSFS
- configs/a15/OP-ACE-5.10.226.json
- manifests/a15/oneplus_ace_5.10.226_v.xml

Bouteillepleine/ReSukiSu_Oneplus-
- configs/oos15/OP-ACE.json
- manifests/oos15/oneplus_ace_v.xml
- ReSukiSU/SUSFS focused workflow; copied as initial build framework.

p0s3id0nVN/OnePlus_OKI_SUSFS
- .back/configs/oos15/OP-ACE.json

OnePlusOSS/android_kernel_5.10_oneplus_mt6895
- official kernel source branches, including oneplus/mt6895_v_15.0.0_ace.

OnePlusOSS/android_vendor_mediatek_kernel_modules_mt6895
- official vendor MTK kernel modules branch matching PGKM10_15.0.0.1800(CN01).
```

Exact source match:

```text
kernel commit: 8baa5a377e2776402de745579cc3835d08ee1cca
vendor modules commit: 0c04020c19a68356afd49ce24f2ff95ee56c37e0
Both commit messages say: Synchronize code for OnePlus PGKM10_15.0.0.1800(CN01)
```

Existing AK3 package inspected:

```text
/storage/emulated/0/Android/data/org.telegram.plus/files/Telegram/Telegram Files/5.10.226_ReSukiSU_lz4kd_34967.zip
sha256: 989d8334a1f0c427c46ce148c4a4fe0a8d65bbb064ef4d53b77e5580482a537b
Image version: Linux version 5.10.226-android12-oki-xiaoxiaow
```

Conclusion: same broad `5.10 android12` GKI family, not an exact match for `5.10.236-android12-9-o-g6973d81cd2ac`.
