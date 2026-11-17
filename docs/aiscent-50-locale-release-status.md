# AiSCent 50-locale release readiness (2026-11-17)

AiSCent 1.3.3 source includes a selectable set of 50 locales for iOS/iPadOS and macOS. Source evidence: native locale expansion [PR #407](https://github.com/jabbertones-cloud/LocalizeShots/pull/407), and current merged 1.3.3 metadata candidate source [PR #423](https://github.com/jabbertones-cloud/LocalizeShots/pull/423), commit [`6c76ea2`](https://github.com/jabbertones-cloud/LocalizeShots/commit/6c76ea2ec9b08668a27cef941cfb69ef91c16015).

## Do the additional languages work?

Eleven new locale IDs are registered in native source: `bn-BD`, `gu-IN`, `kn-IN`, `ml-IN`, `mr-IN`, `or-IN`, `pa-IN`, `sl-SI`, `ta-IN`, `te-IN`, `ur-PK`. There are 657 translatable native UI strings per language with generated nonempty candidates, but all 11 catalogs are still in Xcode's `needsReview` state. Some strings may fall back to English. This is **not** a certified translation or a claim of localization quality. Native-speaker review, protected terms, placeholders, RTL layout and real-device visual acceptance are required.

## Is every storefront already on App Store Connect?

No. The native selectable-locale set, App Store Connect listing metadata, screenshot sets and signed App Store binaries are separate deliverables. The merged Fastlane iOS and macOS metadata trees now each contain 50 **draft** storefront locale folders and 1.3.3 release-note candidates. The 11 new locale descriptions and other storefront fields still include English-source placeholders, and all new notes require linguistic review; no claim of 50 Apple-created records or approved translations is made. The source remains intentionally blocked from App Store Connect reconciliation until version-scoped app-info, metadata, media, and human-review gates are satisfied. Do not infer Apple's current locale inventory from Xcode's `CFBundleLocalizations` count.

At the November 17 readback, iOS version 1.3.2 is `PENDING_DEVELOPER_RELEASE` (already approved; not an editable 1.3.3 record). macOS version 1.3.3 is `PREPARE_FOR_SUBMISSION`. Never overwrite the iOS 1.3.2 approved version to push the new strings. Before any Apple write, re-read the exact version, platform, app ID, locale, approval and live metadata baseline.

## Which screenshots belong in the release?

Use approved, genuine screenshots from the current signed ordinary iPhone, iPad and macOS targets, with the correct locale and device dimensions. **Do not use iPhone Duo screenshots** in App Store Connect, marketing, the product website or support gallery. PRs [#404](https://github.com/jabbertones-cloud/LocalizeShots/pull/404) and [#409](https://github.com/jabbertones-cloud/LocalizeShots/pull/409) concern internal Duo simulator screenshot capture/testing and an unresolved live fold/rotation verification, not a shipped customer feature.

The earlier 39-locale, 156-image, four-duplicate-group screenshot audit is historical evidence only. It does not establish that 50 storefronts have unique or approved images.

## Release verification procedure

1. Verify 50 native language selectors and the signed binary on the exact release commit; check independent iOS and Mac App Store targets.
2. Confirm linguistic and visual approval for each new locale; do not turn `needsReview` into `translated` automatically.
3. Validate locale-specific App Store descriptions, subtitles, keywords, What's New and approved screenshot sets for the actual platform version.
4. Perform version-scoped Apple reconciliation with a digest-bound approval and reread all changed Apple records, never unrelated app information or an approved version.
5. Upload/test/review only when signing, StoreKit, account and App Store Connect prerequisites pass; verify final live state.

For customer support, share no credentials or private application data in public issues. Use [private support](https://aiscentmcp.com/support) for account-specific App Store Connect state.
