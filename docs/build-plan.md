# Build plan

## Phase 1: source/bootstrap

- Use official OnePlusOSS `PGKM10_15.0.0.1800(CN01)` commits pinned in manifest.
- Run GitHub Actions workflow with exact target `OP-ACE-PGKM10-1800`.
- First run may require toolchain cache/mirror initialization.

## Phase 2: clean build validation

- Confirm produced `Image` exists.
- Extract strings from Image and record Linux version.
- Compare against device kernel baseline: `5.10.236-android12-9-o-g6973d81cd2ac`.

## Phase 3: ReSukiSU/SUSFS AK3

- Build ReSukiSU/SUSFS package through copied ReSukiSU OnePlus workflow.
- Verify AK3 zip structure: `Image`, `anykernel.sh`, `META-INF`, `tools/`.
- Add explicit no-auto-flash policy.

## Phase 4: user-controlled flashing

- Provide generated AK3 zip and script/checklist only.
- User flashes manually; Hermes does not auto-flash this OnePlus Ace target unless separately requested and verified.
