---
description: "Use when editing website HTML or Markdown to enforce Nex-X Pix Select branding and prevent Zerolink naming regressions."
name: "Nex-X Pix Select Branding Guardrail"
applyTo:
  - "**/*.html"
  - "**/*.md"
---

# Nex-X Pix Select Branding Guardrail

## Goal
Keep all customer-facing website copy and metadata consistent with the current brand name: Nex-X Pix Select.

## Must Follow Rules
- Replace old product name variants (`Zerolink`, `ZEROLINK`, `Zero Link`) with approved naming unless explicitly marked as legacy history.
- Use `Nex-X Pix Select` for normal body copy, headings, buttons, and metadata.
- Use all-caps lockup only where design intentionally uses a logo lockup style.
- Update every changed page consistently across visible and hidden metadata content.

## Required Places to Check on Each Edited Page
- `<title>` and description/meta tags
- Open Graph and Twitter tags
- JSON-LD/schema `name` fields
- Logo `alt` text and footer copyright line
- CTA text that references product naming

## Content Safety Notes
- Keep legal terms intact unless legal copy is specifically in scope.
- If historical references to the old brand are required, label them as legacy context.

## Quick Verification Before Finalizing
1. Search for old brand tokens in edited files.
2. Confirm brand text is identical in nav, hero, CTA, footer, and metadata.
3. Ensure there are no mixed-brand strings on the same page.
