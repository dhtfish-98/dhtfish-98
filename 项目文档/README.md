### dhtfish-98

Native tools for inspecting Mach-O signing declarations, analyzing AArch64
control flow, and running local browser workflows. Each project publishes its
reproducible examples and the scope of its verification.

---

#### [MachOInspect](https://github.com/dhtfish-98/MachOInspect)

A C++20 library and CLI for Mach-O signing metadata, declared entitlements,
hardening settings and resource seals. The [owned-binary example](https://github.com/dhtfish-98/MachOInspect/blob/main/%E9%A1%B9%E7%9B%AE%E6%96%87%E6%A1%A3/docs/OWNED_BINARY_EXAMPLE.md)
builds two fixtures and compares their declarations with Apple's `codesign`.

The inspector does not authenticate CMS, verify executable code pages or establish
OS-granted permissions. `codesign` checks the signature; runtime permission grants
remain a separate question. See the [verification record](https://github.com/dhtfish-98/MachOInspect/blob/main/%E9%A1%B9%E7%9B%AE%E6%96%87%E6%A1%A3/validation/README.md).

#### [A64Dispatch](https://github.com/dhtfish-98/A64Dispatch)

A C++20 library and CLI for AArch64 dispatch analysis and same-size branch
rewriting, with a thin IDA adapter. The CLI produces separate snapshots; the
adapter submits changes to an IDA database.

Known-vector and coverage checks bound what is accepted; they are not a proof for
every input. The [IDA guide](https://github.com/dhtfish-98/A64Dispatch/blob/main/%E9%A1%B9%E7%9B%AE%E6%96%87%E6%A1%A3/integrations/ida/README.md)
and [verification record](https://github.com/dhtfish-98/A64Dispatch/blob/main/%E9%A1%B9%E7%9B%AE%E6%96%87%E6%A1%A3/validation/README.md)
show the owned fixture and distinguish native tests from actual host checks.

#### [ChromeRelay](https://github.com/dhtfish-98/ChromeRelay)

A C++20 MCP bridge to an existing loopback Chrome DevTools endpoint. It provides
54 canonical actions and 75 legacy names. The [local-page workflow](https://github.com/dhtfish-98/ChromeRelay/blob/main/%E9%A1%B9%E7%9B%AE%E6%96%87%E6%A1%A3/docs/LOCAL_WORKFLOW.md)
fills a form, clicks once and reads the result.

The [verification record](https://github.com/dhtfish-98/ChromeRelay/blob/main/%E9%A1%B9%E7%9B%AE%E6%96%87%E6%A1%A3/validation/README.md)
covers temporary profiles and owned pages on macOS. It does not establish
compatibility with arbitrary websites or existing personal browser profiles.

#### [CDTranslator](https://github.com/dhtfish-98/CDTranslator)

A small macOS desktop app: translation as you type, and local OCR on a pasted
screenshot through Apple's Vision framework. Text, including OCR results, is sent
to Google for translation. SwiftUI, no API key. The privacy
policy is published at
[dhtfish-98.github.io/CDTranslator](https://dhtfish-98.github.io/CDTranslator/).

---

Ordinary bug reports go through each repository's issues. For sensitive reports,
follow that repository's security policy and private reporting instructions.
Upstream authors and licenses are credited in the repositories.
