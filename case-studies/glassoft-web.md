# GlasSoft Web

**A production-oriented studio portfolio built as a real web product, not a static brochure.**

GlasSoft Web is the public studio surface for GlassBox, GlassPort, NodeMedic, GAR and related engineering work.

The implementation is private while the product and publication model continue to evolve. This case study focuses on the engineering constraints, design implementation, bilingual content architecture, accessibility, CI and release discipline behind the site.

## Current product shape

The current application is built with:

- Next.js 16 App Router;
- React 19;
- TypeScript;
- Node.js;
- Zod-backed public content contracts;
- Vitest-based regression coverage;
- Vercel preview/release workflows;
- GitHub Actions on a self-hosted Linux runner.

The site is intentionally more structured than a generic portfolio CMS. Public entries are projected from explicit publication-safe contracts so internal product names, operational details, unqualified claims or private evidence do not accidentally become public UI.

## Figma-authored Home baseline

The Home composition is derived from an accepted Figma-authored design baseline.

The implementation treats that accepted composition as product evidence rather than loose inspiration:

- desktop and mobile visual anchors are preserved;
- authored assets and composition geometry are reused;
- later product evolution is separated from baseline fidelity work;
- new surfaces can evolve without silently rewriting the accepted Home;
- visual changes remain subject to explicit Product review.

This has required a distinction between **pixel/composition fidelity** and ordinary reusable component architecture.

## Bilingual HU / EN product work

The current vNext line is expanding the site from an English-first baseline toward genuine Hungarian and English product surfaces.

Implemented work includes:

- Hungarian Projects and Engineering listing routes;
- Hungarian Studio navigation/surfaces;
- a dedicated Hungarian Home using the same accepted Figma media/composition;
- HU/EN locale switching on localized route pairs;
- localized public-safe project copy;
- canonical/alternate-language metadata work;
- explicit indication when a linked detail page is still English-only.

Localization is treated as a product and accessibility concern, not string replacement.

The active vNext line has since expanded beyond listing pages: paired HU/EN detail routing now covers public project details and GAR Engineering presentation, with tests that fail closed when an approved Hungarian claim is missing. The work still does **not** claim complete production language parity until the full release/QA gates are accepted.

## Publication-safe content architecture

Public portfolio content is projected through explicit contracts rather than rendered directly from private product state.

The system distinguishes:

- Projects from Engineering surfaces;
- public-safe product claims from internal evidence;
- lifecycle/qualification state from marketing copy;
- blocked internal identities from publishable entries;
- product actions from engineering-only material.

Examples include keeping GAR on Engineering surfaces, withholding the internal learning-product codename, and avoiding download/release claims that have not been validated.

## Accessibility and interaction

The site is designed around WCAG-oriented product constraints rather than visual-only acceptance.

Current work includes:

- keyboard-visible focus states;
- touch-safe interaction sizes;
- reduced-motion behavior;
- forced-colors considerations;
- responsive navigation;
- mobile/desktop composition review;
- semantic locale/navigation behavior;
- visible fallback contact paths instead of relying only on `mailto:`;
- copy-to-clipboard status exposed through an ARIA live region.

The target QA matrix includes Safari, Chrome, Firefox, mobile layouts, zoom/reflow and assistive-technology review.

The current draft line also has browser-level accessibility automation using Playwright + axe, explicit keyboard navigation checks, forced-colors/reduced-motion coverage and route-specific diagnostic evidence. A Firefox run has exercised nine WCAG-tagged scenarios with zero detected automatic violations while preserving unresolved/inconclusive contrast findings for manual review rather than converting them into false passes.

## Testing and CI

The project uses deterministic CI to prevent visual/product evolution from bypassing engineering constraints.

Checks include combinations of:

- formatting;
- linting;
- TypeScript;
- Vitest;
- Next.js production build;
- performance-baseline checks;
- public-content/publication-safety regression tests;
- route/locale/metadata contracts;
- secret hygiene.

A self-hosted Linux GitHub Actions runner handles repository CI.

The browser/release QA system now also covers:

- responsive capture matrices at 320 / 390 / 768 / 1440 CSS px;
- touch, mouse and keyboard activation of portfolio cards;
- Chromium and Firefox browser suites;
- route/reflow/text-spacing coverage across HU and EN;
- Lighthouse tooling;
- RSC/navigation-timing diagnostics that separate destination, origin and alternate-locale resources;
- manual-only macOS/WebKit lanes where hosted/runtime cost or platform requirements matter.

Successful CI is not treated as visual acceptance. Browser/device review remains a separate gate for user-facing design changes.

## Preview and release boundaries

Feature work is validated through preview deployments before production promotion.

The current vNext line remains explicitly separated from Production while design, localization and interaction work is still being reviewed.

Important distinctions are kept visible:

- READY preview is not Production;
- successful build is not visual acceptance;
- preview metadata behavior is not assumed to equal production metadata;
- merge to the production branch is a deployment decision, not a routine code-review side effect.

## Current October 2026 vNext work

The active vNext line includes:

- evolution of Projects, Engineering and Studio surfaces from the accepted visual baseline;
- responsive editorial project cards;
- bilingual Hungarian/English portfolio surfaces;
- localized Hungarian Home while preserving the accepted English Home;
- stronger project presentation and media use;
- safer contact behavior with copy-email fallback;
- localization/SEO/accessibility cleanup;
- paired HU/EN project and GAR detail experiences;
- broader responsive and accessibility regression automation;
- navigation/resource diagnostics for the observed Safari-specific latency investigation;
- continued Product review before production release.

The branch remains a work-in-progress release line; this case study does not claim that all vNext work is currently live in Production.

## What this project demonstrates

GlasSoft Web demonstrates:

- modern Next.js / React product engineering;
- Figma-to-implementation fidelity work;
- reusable design-system thinking without erasing authored design intent;
- bilingual product architecture;
- publication-safe content modeling;
- accessibility-first interaction decisions;
- responsive frontend implementation;
- deterministic CI and regression testing;
- preview/production release discipline;
- engineering communication around explicit product gates.

## Public boundary

This case study intentionally omits:

- private repository source;
- deployment credentials;
- private product evidence;
- unpublished internal identities;
- reusable production-access configuration;
- claims that have not passed their own release/acceptance gates.

The goal is to show engineering decisions and verified product scope without turning internal implementation or infrastructure into public operational material.
