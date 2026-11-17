# AiSCent native release and localization status

_Last checked: November 17, 2026. Review after: November 24, 2026. This page separates source capabilities, real QA findings and Apple-distributed releases._

## Scope

[AiSCent](https://aiscentmcp.com/) helps compatible coding agents inspect App Store Connect, check release readiness, review screenshots and localizations, and prepare supported operations with confirmation and verification. The [free preparation questionnaire](https://aiscentmcp.com/) is **not** a live inspection of your private App Store Connect records. Never submit Apple credentials to a public GitHub issue.

## 39 observed storefronts versus 50 in native source

- The website's **39-storefront / 156-image** example is a **historical verified release-workflow observation**, not a current statement that the product supports only 39 locales.
- [Merged LocalizeShots PR #407](https://github.com/jabbertones-cloud/LocalizeShots/pull/407) added **50 locale definitions** and native app-language/translation-target selectors across iOS, iPadOS and macOS source. It also recorded new-language strings that still required human review.
- **50 compiled locale resources do not mean 50 App Store-approved, fully reviewed localizations.** The newly added language candidates and store metadata need review and release checks before publication.
- [Merged LocalizeShots PR #423](https://github.com/jabbertones-cloud/LocalizeShots/pull/423) stages 50 Fastlane metadata folders per platform (100 version-1.3.3 release notes) and corrects ASC-to-Xcode locale aliases. Eleven new descriptions/keywords/subtitles are **unreviewed English source placeholders**, not customer-ready translations. The Mac validator still holds on 352 `needsReview` entries and no missing-locale alias false positives. No Apple write was made.

## Hosted plugin release candidate

A new hosted MCP package candidate was merged to source on November 17, 2026. It includes a read-only release-inspection skill and continues to carry 38 localized plugin listing entries. This is separate from the native app's 50 locale definitions. Neither source packaging nor native locale resources establish a newly published ChatGPT plugin, an App Store release, complete human-reviewed translations, or authenticated customer tool access.

## Release readiness is a separate gate

- **macOS 1.3.3:** Apple's November 17 readback reported `PREPARE_FOR_SUBMISSION`. [PR #422](https://github.com/jabbertones-cloud/LocalizeShots/pull/422) documents a signed exact-PR-head package and Xcode concurrency mitigation, **not an exact-current-main signed upload or App Store submission**. A signed rebuild from the latest main, verified build association, localization review and screenshots remain separate release gates.
- **iPhone Duo:** [merged PR #409](https://github.com/jabbertones-cloud/LocalizeShots/pull/409) adds strict version-bound diagnostics for live fold/rotation continuity. A merged diagnostic script is **not proof of a customer-shipping Duo experience**.
- **iOS/iPadOS:** Apple's November 17 readback reported 1.3.2 `PENDING_DEVELOPER_RELEASE`; this approved version remains untouched. There is no independently confirmed editable iOS 1.3.3 App Store record, attached signed build or 50-locale publication. Do not change the approved 1.3.2 to force the next version.

## Common support situations

For missing store metadata, screenshot rejection or incomplete localizations, start with the [AiSCent troubleshooting index](troubleshooting.md). Confirm the exact platform, app version, intended Store locale, Xcode locale alias, required screenshots, and App Store Connect state. If an upload or release-plan step says `needsReview`, `unknown`, `no build attached` or `blocked`, do not report it as completed.

Search [public issues](https://github.com/jabbertones-cloud/aiscent-support/issues) or [file a sanitized report](https://github.com/jabbertones-cloud/aiscent-support/issues/new/choose). Send private Apple account matters through [AiSCent private support](https://aiscentmcp.com/support).

**Evidence:** [50-locale source implementation](https://github.com/jabbertones-cloud/LocalizeShots/pull/407); [Mac archive blocker](https://github.com/jabbertones-cloud/LocalizeShots/pull/422); [Duo smoke evidence boundary](https://github.com/jabbertones-cloud/LocalizeShots/pull/409).
