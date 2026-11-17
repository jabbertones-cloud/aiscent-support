# AiSCent 1.3.3: localization and submission status

Last checked: November 17, 2026.

This is a public support/status document, **not** an Apple App Store release receipt. Read [AiSCent](https://aiscentmcp.com/) for customer information and use authenticated AiSCent diagnosis for account-specific release data.

## What changed after 1.3.2

The [exact Git comparison](https://github.com/jabbertones-cloud/LocalizeShots/compare/v1.3.2...c132029d8dcb1d97b042d17d9d08bc040496c13a) includes 23 merged commits:

- Shared macOS/iPhone/iPad language and translation-target controls, covering 50 locale identifiers in native source. The 11 added languages still require linguistic and RTL/layout review ([PR #407](https://github.com/jabbertones-cloud/LocalizeShots/pull/407)).
- Clearer iPhone first-run instructions and agent connection, with better contrast and readable guidance ([PR #405](https://github.com/jabbertones-cloud/LocalizeShots/pull/405)).
- Native read-only Apple Analytics refresh and explicit distinction between unavailable/missing metrics and measured zero ([PR #413](https://github.com/jabbertones-cloud/LocalizeShots/pull/413), [PR #415](https://github.com/jabbertones-cloud/LocalizeShots/pull/415)).
- Source-verifiable app build, signing, screenshot QA and release-preparation safeguards. Internal QA tools are **not** end-user features.

## Eleven new App Store locale identifiers

`bn-BD` Bengali, `gu-IN` Gujarati, `kn-IN` Kannada, `ml-IN` Malayalam, `mr-IN` Marathi, `or-IN` Odia, `pa-IN` Punjabi, `sl-SI` Slovenian, `ta-IN` Tamil, `te-IN` Telugu, and `ur-PK` Urdu.

These identifiers are present in the native app's 50-locale registry, string catalog, and bundle declarations. They are **not** 11 human-reviewed translations. The app's localization source explicitly marks all 657 translatable strings in each new locale `needsReview`; the catalog's structural checks are not language-quality certification. Check [source QA notes](https://github.com/jabbertones-cloud/LocalizeShots/blob/main/docs/localization/aiscent-50-locale-20261113.md).

## Platform-specific Apple state

| Platform | App Store version | Last observed Apple status | What it means |
| --- | --- | --- | --- |
| iPhone / iPad | 1.3.2 | PENDING_DEVELOPER_RELEASE | Already approved; a new 1.3.3 Apple version cannot be treated as editable while this state remains |
| macOS | 1.3.3 | PREPARE_FOR_SUBMISSION | Editable submission record, but still requires independently checked metadata, review, and signed-build evidence |
| macOS | 1.3.2 | READY_FOR_SALE | Prior approved version; does not demonstrate the 1.3.3 features |

Statuses were read through the authorized AiSCent credential broker on November 17, 2026. They are not continuously refreshed here.

## What is not ready

- New language candidates must be reviewed by regional/native speakers and visually inspected on representative real screens, particularly Urdu right-to-left text and complex Indic scripts.
- Each platform needs its own App Store metadata localization and exact-version Apple readback; the checked-in Fastlane metadata historically had 39 locale directories.
- Screenshots must be current, genuine, version-bound, and checked per target device and language. **No iPhone Duo screenshots** will be used on the store, website, support or marketing pages.
- The iPhone Duo experimental four-pose capture pipeline ([PR #404](https://github.com/jabbertones-cloud/LocalizeShots/pull/404)) is developer QA tooling. The continuous fold/rotate rendering defect is not demonstrated fixed. It must not appear as a customer-facing launch claim.
- No one should infer from merged code or a published support page that an Apple binary was uploaded, approved or released.

## Platform capability boundary

The **Mac App Store edition** manages App Store Connect records and existing static screenshots; it does not install, execute, launch, emulate or preview other developers' apps. The **iOS/iPadOS edition** is a secure client for an authorized MCP host. Do not attribute Mac-only capture or build automation to the mobile edition.

## Release acceptance

Use exact merged main source SHA, native build and signing tests, review-gated metadata and screenshots, App Store Connect version-scoped update, Apple readback, and independently observed App Store/TestFlight status. Keep iOS and macOS version records separate. Do not turn off release guards or re-enable GitHub Actions. For account-specific evidence, use [private support](https://aiscentmcp.com/support); never send secrets through public GitHub issues.
