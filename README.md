# Ch1p (`@Ch111p` / `@dhtfish-98`)

Independent C/C++ vulnerability researcher and binary analysis tool developer focusing on multimedia container parsers, Mach-O/ELF binary toolchains, and sanitizer-guided fuzzing.

- **Handles**: [`@Ch111p`](https://github.com/Ch111p) (**Ch1p**) / [`@dhtfish-98`](https://github.com/dhtfish-98)
- **Contact Email**: `bitfish886@gmail.com`

---

## Assigned CVEs (Vulnerability Disclosures)

| CVE ID | Target Software | CVSS v3.1 | Vulnerability Summary | Upstream Issue & Fix Commit |
| :--- | :--- | :--- | :--- | :--- |
| **[CVE-2020-19751](https://nvd.nist.gov/vuln/detail/CVE-2020-19751)** | **GPAC** (`v0.8.0` / `MP4Box`) | **9.1 Critical** (`CWE-125` / `CWE-126`) | Heap buffer over-read / heap overflow & invalid pointer free in `gf_odf_del_ipmp_tool` (`src/odf/odf_code.c:3295`) via `ipmpx_Delete` | [gpac/gpac#1272](https://github.com/gpac/gpac/issues/1272) · [Commit `c26b0aa`](https://github.com/gpac/gpac/commit/c26b0aa605aaea1f0ebe8d21fe1398d94680adf7) |
| **[CVE-2020-19750](https://nvd.nist.gov/vuln/detail/CVE-2020-19750)** | **GPAC** (`v0.8.0` / `MP4Box`) | **7.5 High** (`CWE-125` / `CWE-126`) | Heap-based buffer over-read in `txtc_Read` (`src/isomedia/box_code_base.c:8637`) via `gf_strdup` on un-terminated `TextConfigBox` payload | [gpac/gpac#1262](https://github.com/gpac/gpac/issues/1262) · [Commit `3fcf66c`](https://github.com/gpac/gpac/commit/3fcf66c6031da966cf33ee89bcbefa2f8bec4b02) |
| **[CVE-2020-19752](https://nvd.nist.gov/vuln/detail/CVE-2020-19752)** | **Gifsicle** (`v1.92`) | **7.5 High** (`CWE-476`) | NULL pointer dereference in `find_color_or_error` (`src/support.c:1110`) when processing GIF streams without local/global colormaps | [kohler/gifsicle#140](https://github.com/kohler/gifsicle/issues/140) · [Commit `eb9e083`](https://github.com/kohler/gifsicle/commit/eb9e083dcc0050996d79de2076ddc76011ad2f10) |

---

## Upstream Security & Tooling Patches

- **LLVM Project (`llvm/llvm-project`)**:
  - [PR #168925](https://github.com/llvm/llvm-project/pull/168925) — `[llvm-objcopy][MachO] Fix slice index bug when copying fat binaries` (Merged)
  - [PR #173503](https://github.com/llvm/llvm-project/pull/173503) — `[AArch64][Disassembler] Fix diagnostic for Wait instruction` (Merged)
- **Radare2 Reverse Engineering Framework (`radareorg/radare2`)**:
  - [PR #26748](https://github.com/radareorg/radare2/pull/26748) — Upstream binary analysis patch (Merged)
- **Go Mach-O Parser (`blacktop/go-macho`)**:
  - [PR #79](https://github.com/blacktop/go-macho/pull/79) — Upstream Mach-O parser fix (Merged)
