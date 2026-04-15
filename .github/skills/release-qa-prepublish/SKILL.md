---
name: release-qa-prepublish
description: 'Run final pre-publish QA for static marketing websites. Use for broken-link checks, mobile layout validation, branding consistency, metadata verification, and accessibility spot checks before release.'
argument-hint: 'Target pages, deployment/local URL, and strict pass criteria'
---

# Release QA Prepublish

## What This Skill Produces
- A release readiness report with PASS/FAIL results.
- A page-by-page issue list prioritized by severity.
- A short go/no-go recommendation for publishing.

## When to Use
- Before publishing website content updates.
- After branding, download flow, or CTA changes.
- Before handing off to client/demo/release stakeholders.

## Inputs To Collect First
1. Environment to validate:
   - Local file preview or deployed preview URL
2. In-scope pages:
   - Default set: `index.html`, `download.html`, `license.html`, `faqs.html`, `privacy.html`, `refund.html`
3. Business-critical links:
   - Software download destination (single landing link)
   - License key delivery and fallback download destination

## Procedure

1. Build the QA page inventory.
   - Confirm which pages are release-facing and which are test-only.
   - Exclude technical test pages from release checklist unless requested.

2. Run link integrity checks.
   - Validate all internal navigation links and footer links.
   - Validate critical CTAs (download, license key, contact/help).
   - Flag missing files, malformed URLs, and dead anchors.

3. Verify branding consistency.
   - Confirm no unintended legacy brand strings remain.
   - Confirm brand appears consistently in title, hero, nav, CTA, and footer.

4. Validate metadata and sharing tags.
   - Check `<title>` and meta description quality on each page.
   - Verify Open Graph/Twitter fields are present and on-brand.
   - Confirm schema/JSON-LD name consistency where present.

5. Validate core journeys.
   - Download journey: all software CTAs route to the single landing link.
   - License journey: page clearly supports email-first delivery plus direct download fallback.
   - Workflow video area: placeholder text exists and layout remains clean.

6. Perform responsive UI checks.
   - Check layout at 320, 375, 768, 1024, and 1440 widths.
   - Verify nav readability, CTA visibility, section spacing, and overflow behavior.

7. Perform accessibility spot checks.
   - Verify image alt text and heading order sanity.
   - Verify visible keyboard focus indicators.
   - Verify reduced-motion behavior for animated logo and transitions.

8. Perform final smoke checks.
   - Open all release pages and navigate main links.
   - Confirm no obvious console errors and no broken media.

9. Publish readiness output.
   - Summarize issues in `Critical`, `Major`, and `Minor` groups.
   - Provide final recommendation: `Go`, `Go with caveats`, or `No-go`.

## Decision Points

- If a critical CTA is broken:
  - Mark release as `No-go` until fixed.
- If only cosmetic/mobile minor issues exist:
  - Allow `Go with caveats` when business approves.
- If branding is inconsistent on legal-only historical pages:
  - Keep legacy references only when clearly labeled as historical context.

## Completion Criteria

- Zero critical defects on release-facing pages.
- All business-critical links are valid and reachable.
- Branding and metadata are consistent with Nex-X Pix Select.
- Mobile and desktop checks show no blocking layout defects.

## Example Prompts

- `/release-qa-prepublish Run full prepublish QA for all release pages and return pass/fail with severity`
- `/release-qa-prepublish Check only download and license flows with strict go/no-go criteria`
- `/release-qa-prepublish Validate branding and metadata consistency before release`
