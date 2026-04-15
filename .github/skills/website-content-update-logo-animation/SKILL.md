---
name: website-content-update-logo-animation
description: 'Update marketing website content and branding for Nex-X Pix Select. Use when renaming Zerolink references, adding logo animation, setting a workflow video placeholder, using a single software download landing link, and updating license-key download page content across static HTML pages.'
argument-hint: 'Brand name, logo animation style, download landing URL, license page behavior, and optional future video URL'
---

# Website Content Update and Logo Animation

## What This Skill Produces
- A consistent rebrand from "Zerolink" to "Nex-X Pix Select" across meta tags, headings, copy, structured data, and footer text.
- Updated pages for software download and license-key download flow.
- A workflow explainer video section with a placeholder now and an easy upgrade path to embed later.
- Animated logo behavior that keeps layout stable and respects reduced-motion preferences.
- Verification checklist with link/content consistency checks.

## When to Use
- You need a full website copy and branding refresh.
- You need to update download/license experience and related CTAs.
- You need to add or tune logo animation without breaking performance or accessibility.

## Inputs To Collect First
1. Final brand text:
   - Primary name: `Nex-X Pix Select`
   - Any uppercase lockup variant (example: `NEX-X PIX SELECT`)
2. Asset locations:
   - Logo file path
   - Optional future explainer video URL (YouTube/Vimeo/file)
3. Download destinations:
   - Single software download landing URL
   - License-key download or retrieval URL/page path
4. Content rules:
   - Claim statements to keep/remove
   - Pricing/legal text changes needed

## Procedure

1. Audit all current branding mentions.
   - Search HTML/CSS/JS/MD for `Zerolink`, `ZEROLINK`, and old org labels.
   - Create a replacement map for headings, meta tags, social tags, and JSON-LD.

2. Apply global rebrand changes.
   - Update page titles, meta description/author, Open Graph, Twitter tags, schema `name`, and visible headings.
   - Update logo alt text and footer copyright strings.

3. Update download and license journey.
   - In download page sections, point all software CTAs to the single landing URL.
   - Ensure license-key page clearly states both paths: email delivery and direct key download fallback.
   - Keep CTA labels action-based (`Download Software`, `Download License Key`, `Get Help`).

4. Add workflow explainer video module.
   - Place a section near onboarding/download steps with a clear heading.
   - Use a `Coming soon` placeholder block now with optional future video slot.
   - Add caption text explaining the workflow in 1-2 lines.

5. Implement logo animation safely.
   - Add subtle animation (pulse/shine/tilt or hover scale) to logo container.
   - Respect reduced motion via `@media (prefers-reduced-motion: reduce)` to disable animation.
   - Avoid layout shift: animate transform/opacity only, not width/height/top/left.

6. Validate consistency and navigation.
   - Verify nav/footer link targets for `download.html`, `license.html`, `faqs.html`, `privacy.html`, `refund.html`.
   - Confirm no old brand token remains in production content.

7. Final QA pass.
   - Desktop and mobile visual check.
   - Link check for all download and license actions.
   - Accessibility spot-check: alt text, heading order, focus visibility, motion fallback.

## Decision Points

- If video URL is missing:
   - Keep placeholder block with `Coming soon` text and reserve an embed container.
- If license-key flow supports both email and direct download:
   - Show both actions and add one-line guidance that email is primary and direct download is fallback.
- If any legal copy is uncertain:
  - Keep existing legal terms, only rebrand names, and flag for legal review.

## Completion Criteria

- Zero instances of old brand terms in user-facing content unless intentionally retained in history/changelog.
- Download CTAs point to the single landing destination, and license-key CTAs support email + direct fallback.
- Explainer video section exists with placeholder content and upgrade-ready structure.
- Logo animation works and disables cleanly for reduced-motion users.
- Core pages render correctly without console errors after edits.

## Example Prompts

- `/website-content-update-logo-animation Rebrand all pages to Nex-X Pix Select and add a hover glow logo animation`
- `/website-content-update-logo-animation Add a workflow video placeholder to the download page and route software CTA to one landing URL`
- `/website-content-update-logo-animation Refresh license page copy and add Download License Key CTA`