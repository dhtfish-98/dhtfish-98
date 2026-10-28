# Security Researcher Profile & Handle Verification

- **Contact / Anthropic CVP Application Email:** `dhtfish988@gmail.com`
- **GitHub Handles:**
  - **`@Ch111p` (`Ch1p`)** — Upstream vulnerability research, fuzzing, and CVE disclosures ([https://github.com/Ch111p](https://github.com/Ch111p))
  - **`@dhtfish-98`** — Defensive security review tooling, static analysis, and local verification labs ([https://github.com/dhtfish-98](https://github.com/dhtfish-98))
- **Research Scope:** Offline source-code auditing, C/C++ memory-safety bug triage, multimedia/binary format parser verification (ISOBMFF/MP4, GIF, Mach-O, DWARF), and coordinated vulnerability disclosure.

---

## Published CVEs & Upstream Vulnerability Disclosures

### 1. CVE-2020-19751 (CVSS v3.1: 9.1 Critical — CWE-125 / CWE-126)
- **Target Software:** GPAC Multimedia Framework v0.8.0
- **Vulnerable Component:** `src/odf/odf_code.c` (line 3295, `gf_odf_del_ipmp_tool`)
- **Technical Summary:** Improper size validation during ODF IPMP tool descriptor parsing causes a heap-based buffer over-read / heap-buffer-overflow, leading to an invalid memory address dereference and free in `gf_odf_del_ipmp_tool`.
- **Upstream Issue Report:** [https://github.com/gpac/gpac/issues/1272](https://github.com/gpac/gpac/issues/1272)
- **Upstream Maintainer Fix Commit:** [https://github.com/gpac/gpac/commit/c26b0aa605aaea1f0ebe8d21fe1398d94680adf7](https://github.com/gpac/gpac/commit/c26b0aa605aaea1f0ebe8d21fe1398d94680adf7)
- **Official NVD Record:** [https://nvd.nist.gov/vuln/detail/CVE-2020-19751](https://nvd.nist.gov/vuln/detail/CVE-2020-19751)

### 2. CVE-2020-19750 (CVSS v3.1: 7.5 High — CWE-125 / CWE-126)
- **Target Software:** GPAC Multimedia Framework v0.8.0
- **Vulnerable Component:** `src/isomedia/box_code_base.c` (line 8637, `txtc_Read`)
- **Technical Summary:** In `txtc_Read(GF_Box *s, GF_BitStream *bs)`, a heap buffer `str` of size `ptr->size` is populated byte-by-byte from the bitstream. When the stream fills `str` without encountering a null byte (`\x00`), the subsequent call to `gf_strdup(str)` reads past the allocated heap buffer boundary.
- **Upstream Issue Report:** [https://github.com/gpac/gpac/issues/1262](https://github.com/gpac/gpac/issues/1262)
- **Upstream Maintainer Fix Commit:** [https://github.com/gpac/gpac/commit/3fcf66c6031da966cf33ee89bcbefa2f8bec4b02](https://github.com/gpac/gpac/commit/3fcf66c6031da966cf33ee89bcbefa2f8bec4b02)
- **Official NVD Record:** [https://nvd.nist.gov/vuln/detail/CVE-2020-19750](https://nvd.nist.gov/vuln/detail/CVE-2020-19750)

### 3. CVE-2020-19752 (CVSS v3.1: 7.5 High — CWE-476)
- **Target Software:** Gifsicle v1.92
- **Vulnerable Component:** `src/support.c` (line 1110, `find_color_or_error`)
- **Technical Summary:** A NULL pointer dereference on the `gfcm` colormap pointer in `find_color_or_error` when processing malformed GIF streams via CLI options (e.g., `gifsicle -t`).
- **Upstream Issue Report:** [https://github.com/kohler/gifsicle/issues/140](https://github.com/kohler/gifsicle/issues/140)
- **Upstream Maintainer Fix Commit:** [https://github.com/kohler/gifsicle/commit/eb9e083dcc0050996d79de2076ddc76011ad2f10](https://github.com/kohler/gifsicle/commit/eb9e083dcc0050996d79de2076ddc76011ad2f10)
- **Official NVD Record:** [https://nvd.nist.gov/vuln/detail/CVE-2020-19752](https://nvd.nist.gov/vuln/detail/CVE-2020-19752)

---

## Upstream Binary Analysis & Toolchain Security Contributions

- **LLVM (`llvm/llvm-project`):**
  - [`PR #168925`](https://github.com/llvm/llvm-project/pull/168925) — `[dsymutil] Add missing validation for zero alignment section`
  - [`PR #173503`](https://github.com/llvm/llvm-project/pull/173503) — `[dsymutil] Add new argument allow_invalid_macho`
- **Radare2 (`radareorg/radare2`):**
  - [`PR #26748`](https://github.com/radareorg/radare2/pull/26748) — `Detect dsc subcache entry format the way dyld does ##io`
- **go-macho (`blacktop/go-macho`):**
  - [`PR #79`](https://github.com/blacktop/go-macho/pull/79) — `[Fix] Fix incorrect category method dump`

---

## Defensive Security Review Repositories (`@dhtfish-98`)

- **[SecurityResearchIndex](https://github.com/dhtfish-98/SecurityResearchIndex)** — Public index of defensive security review tools, local testbeds, and verification boundaries.
- **[DeserializeCallReview](https://github.com/dhtfish-98/DeserializeCallReview)** — Offline AST review tool for Python deserialization call sites and import aliases without target code execution.
- **[DOMSinkReview](https://github.com/dhtfish-98/DOMSinkReview)** — Offline static review of declared HTML sinks and local sanitizer bindings in JavaScript source.
- **[WheelNamespaceReview](https://github.com/dhtfish-98/WheelNamespaceReview)** — Pre-installation archive, `RECORD`, and namespace boundary inspector for Python wheels.
