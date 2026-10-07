# AiSCent problem ontology — seed

These are routing identifiers, not claims that every cause can be diagnosed without current App Store Connect state.

| Problem ID | Customer language | Official concept | Public first step |
|---|---|---|---|
| `ASC.SUBSCRIPTION.MISSING_METADATA` | “subscription says Missing Metadata” | In-App Purchase / subscription metadata and related submission state | Check required metadata and related objects; use authenticated diagnosis for live state. |
| `ASC.BUILD.NOT_VISIBLE` | “my build isn't showing up” | App Store Connect build processing/selection | Confirm upload/processing context; live state requires authenticated diagnosis. |
| `ASC.SCREENSHOT.INVALID` | “App Store screenshots won't upload” | App version localization / screenshot requirements | Identify device/locale/version requirements before changing assets. |
| `ASC.LOCALIZATION.INCOMPLETE` | “localization is incomplete” | App metadata/localization completeness | Map locale and required fields; preserve regional terminology. |
| `ASC.IAP.NOT_ATTACHED` | “my IAP/subscription isn't attached to the release” | IAP/subscription submission relationship | Inspect the relevant product/version relationship with authenticated state. |
| `ASC.REVIEW.REJECTED` | “Apple rejected my app” | App Review resolution | Classify the stated review issue before proposing changes. |
