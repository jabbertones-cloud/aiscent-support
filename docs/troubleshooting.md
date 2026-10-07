# AiSCent troubleshooting index

Start from what the developer sees, not from internal tool names.

| Symptom / search phrase | Problem ID | Next step |
|---|---|---|
| Subscription says “Missing Metadata” | `ASC.SUBSCRIPTION.MISSING_METADATA` | Check subscription + related group/localization/submission state; use authenticated diagnosis for live ASC state. |
| Build is not showing in App Store Connect | `ASC.BUILD.NOT_VISIBLE` | Confirm upload/processing/version context, then inspect live ASC state. |
| App Store screenshots will not upload | `ASC.SCREENSHOT.INVALID` | Identify device/locale/version requirement and validate assets before retrying. |
| Localization is incomplete | `ASC.LOCALIZATION.INCOMPLETE` | Identify missing locale-specific fields and preserve regional terminology. |
| IAP/subscription is not part of the submission | `ASC.IAP.NOT_ATTACHED` | Inspect product/version/submission relationship in authenticated state. |
| Apple rejected the app | `ASC.REVIEW.REJECTED` | Classify the review reason first; do not make broad changes before identifying the stated blocker. |

## Escalation rule
Search public knowledge first. Diagnose authenticated state second. Open a support case only when the problem remains unresolved.
