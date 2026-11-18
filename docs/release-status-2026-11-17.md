# AiSCent native release and localization status

_Last checked: November 17, 2026. Review after: November 24, 2026. This page separates source capabilities, real QA findings and Apple-distributed releases._

## Scope

[AiSCent](https://aiscentmcp.com/) helps compatible coding agents inspect App Store Connect, check release readiness, review screenshots and localizations, and prepare supported operations with confirmation and verification. The [free preparation questionnaire](https://aiscentmcp.com/) is **not** a live inspection of your private App Store Connect records. Never submit Apple credentials to a public GitHub issue.

## 39 observed storefronts versus 50 in native source

- The website's **39-storefront / 156-image** example is a **historical verified release-workflow observation**, not a current statement that the product supports only 39 locales.
- [Merged LocalizeShots PR #407](https://github.com/jabbertones-cloud/LocalizeShots/pull/407) added **50 locale definitions** and native app-language/translation-target selectors across iOS, iPadOS and macOS source. It also recorded new-language strings that still required human review.
- **50 compiled locale resources do not mean 50 App Store-approved, fully reviewed localizations.** The newly added language candidates and store metadata need review and release checks before publication.
- [Merged LocalizeShots PR #423](https://github.com/jabbertones-cloud/LocalizeShots/pull/423) stages 50 Fastlane metadata folders per platform (100 version-1.3.3 release notes) and corrects ASC-to-Xcode locale aliases. Eleven new descriptions/keywords/subtitles are **unreviewed English source placeholders**, not customer-ready translations. The Mac validator still holds on 352 `needsReview` entries and no missing-locale alias false positives. No Apple write was made.

## Owner AiSCent MCP locale discovery

On November 17, the separate **owner/fleet AiSCent MCP** was merged and installed at [aiscent-mcp PR #66](https://github.com/jabbertones-cloud/aiscent-mcp/pull/66), source commit [71635d6](https://github.com/jabbertones-cloud/aiscent-mcp/commit/71635d6d96a6b11ddcc17cf13ea8f884a3ae42e6). The installed, connected localizeshots_discover_locales tool was independently read back and returned **50** supported App Store Connect locale identifiers (up from 39), including ur-PK from a filtered lookup.

This is **locale discovery and workflow availability**, not a provider-side App Store Connect inventory, certified translation, released iOS/macOS binary, or public plugin update. The owner fleet installation and the customer MCP installation are distinct; the customer installation was preserved. The current local catalog remains paired to a different application, and AiSCent's needsReview translations must not be treated as approved merely because its locale identifiers are discoverable.

## Hosted plugin release candidate

A new hosted MCP package candidate was merged to source on November 17, 2026. It includes a read-only release-inspection skill and continues to carry 38 localized plugin listing entries. This is separate from the native app's 50 locale definitions. Neither source packaging nor native locale resources establish a newly published ChatGPT plugin, an App Store release, complete human-reviewed translations, or authenticated customer tool access.

## Release readiness is a separate gate

- **macOS 1.3.3:** The exact-version screenshot-only upload added **154 new Marketing Studio Mac remakes** across the **39 existing Apple locales**. Apple now reports **390/390 processed screenshots complete**, exactly ten per locale, with all 154 new asset checksums and byte sizes independently matching local source-verified RGB PNGs; the 236 pre-existing images were retained. Version remains PREPARE_FOR_SUBMISSION. The 11 newly supported native locales are still absent from Apple, all 39 existing version-specific What’s New fields were previously empty, and editorial/human language review remains unapproved. No Duo screenshots, metadata, binaries or App Review submission were uploaded. Source receipt SHA-256 439d26a21f8af47a73a39a4dd82d07d9b5b34cf3efb8feaf61b14b9d6613957e is retained on the M2 developer machine; this is not final public release certification.
- **iPhone Duo:** [PR #427](https://github.com/jabbertones-cloud/LocalizeShots/pull/427) merged as ba656e85 and its exact-main simulator boot guard passed native regression tests on both M2 and M3 plus a real M3 iOS 27.1 readback retaining the app PID. A separate source-bound **AiSCent 1.3.3 M3 iOS 27.1** test verified seven actual consecutive same-process closed / partially open / open / landscape / portrait / reclosed / reopened transitions, native full-size RGB images and real Today UI without the earlier visible gray band. The seven-image receipt SHA is a22d54e3f41ca6cac87c37399c3c00988f2fc48963994dd5a13e1c878260dd78 (internal M3 QA evidence, not public screenshots). The original [issue #406](https://github.com/jabbertones-cloud/LocalizeShots/issues/406) concerns **AiSCent 1.3.1 on iOS 27.2**, so it remains open until that environment is specifically retested. This QA success **does not** approve 50-language screenshots, a signed App Store release or public use of Duo images.
- **iOS/iPadOS:** Apple's November 17 readback reported 1.3.2 `PENDING_DEVELOPER_RELEASE`; this approved version remains untouched. There is no independently confirmed editable iOS 1.3.3 App Store record, attached signed build or 50-locale publication. Do not change the approved 1.3.2 to force the next version.

## Common support situations

For missing store metadata, screenshot rejection or incomplete localizations, start with the [AiSCent troubleshooting index](troubleshooting.md). Confirm the exact platform, app version, intended Store locale, Xcode locale alias, required screenshots, and App Store Connect state. If an upload or release-plan step says `needsReview`, `unknown`, `no build attached` or `blocked`, do not report it as completed.

Search [public issues](https://github.com/jabbertones-cloud/aiscent-support/issues) or [file a sanitized report](https://github.com/jabbertones-cloud/aiscent-support/issues/new/choose). Send private Apple account matters through [AiSCent private support](https://aiscentmcp.com/support).

**Evidence:** [50-locale source implementation](https://github.com/jabbertones-cloud/LocalizeShots/pull/407); [Mac archive blocker](https://github.com/jabbertones-cloud/LocalizeShots/pull/422); [Duo smoke evidence boundary](https://github.com/jabbertones-cloud/LocalizeShots/pull/409).
