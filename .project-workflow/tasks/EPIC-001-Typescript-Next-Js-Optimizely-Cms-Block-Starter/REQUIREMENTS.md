# Requirements

## Summary

- Task: EPIC-001
- Title: TypeScript Next.js Optimizely CMS Block Starter
- Last updated: 2026-06-17

## Goal

Create a production-minded starter that demonstrates how a TypeScript Next.js application can compose Optimizely CMS content from reusable page elements and blocks, style the experience with Tailwind CSS, document UI pieces in Storybook, and support localized English and Italian routes from the beginning.

## Non-Goals

- Build a full production website for a specific brand, campaign, or vertical.
- Cover every possible Optimizely CMS integration pattern, deployment topology, or content modeling strategy.
- Create a broad component library unrelated to CMS-driven page composition.
- Implement complete editorial workflows inside Optimizely CMS beyond the starter content model and integration points needed for demonstration.
- Add languages beyond English and Italian in this epic.

## Users & Context

- Frontend developers evaluating or starting an Optimizely CMS-backed website.
- Digital experience teams that need a clear model for composing pages from reusable blocks.
- Product, design, and content stakeholders reviewing how multilingual pages can be structured and extended.

## Requirements (Outcome-Focused)

- The starter exposes a clear Next.js app structure using TypeScript, App Router conventions, and maintainable CMS data boundaries.
- Pages are assembled from reusable, typed page elements and content blocks rather than one-off templates.
- Optimizely CMS integration is represented through realistic content fetching, mapping, preview/error states, and documented extension points.
- Tailwind CSS provides the styling foundation with shared tokens or theme conventions that block components can reuse consistently.
- Storybook documents reusable components and CMS block variants with representative English and Italian content.
- Internationalization supports English and Italian routing, dictionaries, metadata, and localized content examples.
- Developer onboarding explains how to run the app, Storybook, linting, type checks, and how to add a new block.
- The starter remains small enough to understand while showing enough structure for production-minded evaluation.

## Acceptance Criteria (Verifiable)

- AC1: A TypeScript Next.js application scaffold exists with documented scripts for local development, production build, linting, and type checking.
- AC2: The app includes a typed CMS content layer for Optimizely-backed pages and blocks, including mock or fixture-backed data that works without external CMS credentials.
- AC3: At least one composed page renders from reusable block data rather than hardcoded page-only markup.
- AC4: A reusable block registry or equivalent mapping layer resolves CMS block types to React components with typed props and graceful handling for unknown block types.
- AC5: Tailwind CSS is configured and used by shared layout, page, and block components with a coherent starter theme.
- AC6: Storybook is configured for the project and includes stories for core page elements, block components, and notable content states.
- AC7: English and Italian locales are supported through routes, dictionaries, localized metadata, and representative localized content fixtures.
- AC8: The README or project docs explain the architecture, content model, local setup, Storybook usage, localization workflow, and steps for adding a new block.
- AC9: Automated validation covers the expected baseline: linting, type checking, build verification, and focused tests or stories for block rendering behavior.

## Open Questions (Answer Needed)

- Should the starter target a specific Optimizely package/API version, or keep the CMS layer adapter-oriented until implementation begins?
- Should Storybook publish static output as part of the validation baseline, or only be runnable locally?
- Should localized routes use locale prefixes for both languages, or should English be the default unprefixed locale?

## Decisions (Resolved)

- Use TypeScript, Next.js, Tailwind CSS, Storybook, and English/Italian internationalization as core epic scope.
- Keep the starter composition-first: CMS block data should drive page rendering through reusable components.
- Provide fixture-backed content so the starter is inspectable without requiring live CMS access.

## Validation Plan

- Run the project-workflow doctor after epic updates.
- During implementation, verify the baseline with local lint, type check, build, and relevant tests.
- Run or build Storybook to verify documented components and block states.
- Manually inspect English and Italian routes to confirm localized content, metadata, and composed block rendering.
