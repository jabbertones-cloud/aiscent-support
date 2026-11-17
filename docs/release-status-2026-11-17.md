# AiSCent native release and localization status

_Last checked: November 17, 2026. Review after: November 24, 2026. This page separates source capabilities, real QA findings and Apple-distributed releases._

## Scope

[AiSCent](https://aiscentmcp.com/) helps compatible coding agents inspect App Store Connect, check release readiness, review screenshots and localizations, and prepare supported operations with confirmation and verification. The [free preparation questionnaire](https://aiscentmcp.com/) is **not** a live inspection of your private App Store Connect records. Never submit Apple credentials to a public GitHub issue.

## 39 observed storefronts versus 50 in native source

- The website's **39-storefront / 156-image** example is a **historical verified release-workflow observation**, not a current statement that the product supports only 39 locales.
- [Merged LocalizeShots PR #407](https://github.com/jabbertones-cloud/LocalizeShots/pull/407) added **50 locale definitions** and native app-language/translation-target selectors across iOS, iPadOS and macOS source. It also recorded new-language strings that still required human review.
- **50 compiled locale resources do not mean 50 App Store-approved, fully reviewed localizations.** The newly added language candidates and store metadata need review and release checks before publication.
- [Open translation QA follow-up PR #418](https://github.com/jabbertones-cloud/LocalizeShots/pull/418) addresses Store-locale to Xcode-locale aliases; do not mark pending QA work complete.

## Hosted plugin release candidate

A new hosted MCP package candidate was merged to source on November 17, 2026. It includes a read-only release-inspection skill and continues to carry 38 localized plugin listing entries. This is separate from the native app's 50 locale definitions. Neither source packaging nor native locale resources establish a newly published ChatGPT plugin, an App Store release, complete human-reviewed translations, or authenticated customer tool access.

## Release readiness is a separate gate

- **macOS 1.3.3:** the [last documented App Store Connect release-plan investigation](https://github.com/jabbertones-cloud/aiscent-mcp/pull/58) found no build attached to the intended version. [Merged archive-build mitigation PR #422](https://github.com/jabbertones-cloud/LocalizeShots/pull/422) limited Xcode build concurrency, but the actual archive run was canceled under disk pressure. **No signed and submitted 1.3.3 macOS package was proven by that change.** Recheck live ASC before stating the current status.
- **iPhone Duo:** [merged PR #409](https://github.com/jabbertones-cloud/LocalizeShots/pull/409) adds strict version-bound diagnostics for live fold/rotation continuity. A merged diagnostic script is **not proof of a customer-shipping Duo experience**.
- **iOS/iPadOS:** native code and locale work are distinct from TestFlight approval, final store screenshots and public App Store availability. Check each platform and version independently.

## Common support situations

For missing store metadata, screenshot rejection or incomplete localizations, start with the [AiSCent troubleshooting index](troubleshooting.md). Confirm the exact platform, app version, intended Store locale, Xcode locale alias, required screenshots, and App Store Connect state. If an upload or release-plan step says `needsReview`, `unknown`, `no build attached` or `blocked`, do not report it as completed.

Search [public issues](https://github.com/jabbertones-cloud/aiscent-support/issues) or [file a sanitized report](https://github.com/jabbertones-cloud/aiscent-support/issues/new/choose). Send private Apple account matters through [AiSCent private support](https://aiscentmcp.com/support).

**Evidence:** [50-locale source implementation](https://github.com/jabbertones-cloud/LocalizeShots/pull/407); [Mac archive blocker](https://github.com/jabbertones-cloud/LocalizeShots/pull/422); [Duo smoke evidence boundary](https://github.com/jabbertones-cloud/LocalizeShots/pull/409).
