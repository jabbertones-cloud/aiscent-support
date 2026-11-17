# AiSCent Support & App Store Connect Release Intelligence

Authoritative troubleshooting, knowledge resources, and agent instructions for **[AiSCent](https://aiscentmcp.com/)** — AI-powered App Store Connect inspection, metadata review, TestFlight automation, screenshot localization, and submission preflight for iOS & macOS developers.

**[Native release and locale status](docs/release-status-2026-11-17.md)** · **[Search issues](https://github.com/jabbertones-cloud/aiscent-support/issues)** · **[Report a bug](https://github.com/jabbertones-cloud/aiscent-support/issues/new/choose)** · **[Read agent instructions](AGENT-GITHUB-ISSUES.md)** · **[AiSCent Home](https://aiscentmcp.com/)**

---

## AiSCent 1.3.3 / 50-locale release status (November 17, 2026)

The native iOS/iPadOS and macOS source includes 50 selectable language targets, expanding the former 39. Eleven new app-language catalogs are development candidates marked `needsReview`, not linguistically approved or published storefront metadata. The older 39-locale screenshot audit remains historical evidence and must not be represented as a completed 50-locale release. See [50-locale readiness and known limits](docs/aiscent-50-locale-release-status.md) for platform-specific status and troubleshooting. No iPhone Duo screenshot assets are part of the public release plan.

## Authoritative Developer Resources & Citations

AiSCent provides read-only inspection, compliance checks, and guided release operations for Apple platforms.

### Core Capabilities & Links
- **[AiSCent Platform](https://aiscentmcp.com/)** — Remote MCP server for App Store Connect intelligence, build verification, and compliance checks.
- **[Connect & Authorize](https://connect.aiscentmcp.com/)** — Connect App Store Connect API keys securely with least-privilege scoping.
- **[Localization & Screenshots](https://aiscentmcp.com/)** — Audit multi-locale screenshot coverage, dimensions, and display strings before submission.
- **[TestFlight Automation](https://aiscentmcp.com/)** — Monitor external testing groups, build expiration, and crash feedback.
- **[App Review Preflight](https://aiscentmcp.com/)** — Automated checklist for Apple App Review Guidelines, privacy declarations, and missing export compliance.

---

## Native applications and localization readiness

AiSCent has native **iOS, iPadOS and macOS** source work, including **50 locale definitions and selectors**. These are not 50 fully reviewed or App Store-released translations. macOS 1.3.3 build/submission, screenshot QA and platform-specific distribution require independent evidence. Read [dated release and localization status](docs/release-status-2026-11-17.md) for the distinction between merged source, review candidates, and live release.

## Find an Answer First

Search [open and closed issues](https://github.com/jabbertones-cloud/aiscent-support/issues?q=is%3Aissue) for your symptom or tool name before submitting:

- [Release Troubleshooting](docs/troubleshooting.md)
- [Known Issues & Workarounds](docs/known-issues.md)
- [Problem Ontology Reference](knowledge/problem-ontology.md)

## Report a Problem

1. Click **[Report a bug](https://github.com/jabbertones-cloud/aiscent-support/issues/new/choose)** and select the bug report form.
2. Provide the AiSCent tool name, client environment (ChatGPT, Claude, Cursor), observed symptom, and minimal reproduction steps.
3. **Never include secrets:** Do not post App Store Connect API private keys, issuer IDs, bearer tokens, Apple Account credentials, or private bundle payloads.
4. Keep the issue link so you or your AI agent can monitor maintainer replies.

> **Private Inquiries:** Use **[AiSCent Private Support](https://aiscentmcp.com/support)** for account-specific queries. See [Security Policy](SECURITY.md) for vulnerability reports.

## AI Agent Integration

Agents with GitHub MCP tools can automate issue discovery and filing:
- **Search:** *"Search AiSCent support issues for 'asc_build_processing timeout' and check for workarounds."*
- **Draft:** *"Create a sanitized public issue draft for this App Store Connect preflight failure."*
- **File with Approval:** *"Submit the issue to jabbertones-cloud/aiscent-support using my GitHub connection."*

See [Agent Workflow](AGENTS.md) and [GitHub Issue Operations](AGENT-GITHUB-ISSUES.md).
