# Sport24 known limitations and remaining work

## Font blockers

Exact Figma font-loading checks failed for **Cera Pro**, **Arial** and **Helvetica Neue**. Available HelveticaNeueCyr, Inter and Arimo were not treated as equivalent replacements. Make the required licensed fonts available to Figma and re-run the checks. The website system stack also includes -apple-system; a cross-platform kit needs a confirmed platform font policy rather than a silent substitution.

Blocked components/styles: general news/body Text Links, default body/caption/sports-data styles requiring these fonts, match Tab/Tab Group, Season Select, system-font category/status labels and badges. No placeholder component sets or flattened replacements were created for these patterns.

## Source and interaction gaps

- Season Select: closed-state geometry is verified; open dropdown indicator/menu and OS/native popup behavior need targeted inspection. Do not invent an open menu.
- Match tabs: selected/default are audited, but system font is unavailable. Hover/pressed/disabled behavior is not comprehensively verified.
- Specialized match-center Text Link: default only. Hover was not reliably captured in its visible viewport; no hover variant created. General underline behavior requires further inspection.
- Icon Button: default menu content only, no invented hover/focus/pressed/disabled states. It serves the icon-container role, avoiding a duplicate wrapper family. Canonical Button4px radius overrides the source menu control's0px, explicitly documented in foundations.md.
- League Label is a text primitive; full logo-bearing league tags and additional status/category/exclusive badges are not claimed complete. Original logo assets and child geometry must be inspected before building these families.
- Section Heading optional action is deferred: source uses a small outline Button. The original validated Button family was preserved without adding a speculative style/size matrix.
- Audit selector div.CvNE7C was initially labeled Search but contains gift/promotion artwork. No Search icon was fabricated from it. Correct source identification is required before Search controls are built.
- Grid column counts verified in saved source HTML. Native grids and number variables are references, not functional CSS media queries. Heading viewport variants require manual selection.
- Native browser and Figma text shaping produce minor natural-width differences, documented in component-registry.md. Fonts were not stretched or silently substituted.
- Source CSS rgba0.5 values retain exact alpha0.5. Hex labels ending80 are rounded display identifiers, not a change to opacity0.50196.
- Popup Effect Style is based on a declared CSS variable, not proof of an observed popup state. No invented elevation levels.

## Diagnostic environment

Focused additional website checks used the installed Playwright/Chromium and ignoreHTTPSErrors because of the previously observed proxy certificate trust failure. No dependencies were installed; no website data was edited or submitted. Exported documentation contains no cookies, authentication state, credentials or temporary screenshot URLs.

## Phase 3

1. Enable required fonts, complete blocked primitive and text-style checks, and finish native Tabs and Season Select before dependent composites.
2. Inspect optional small-outline Button action and extend the existing family only with verified variants; preserve IDs and radius/button4.
3. Verify remaining badge/logo, search, focus, hover, pressed and disabled appearances.
4. Build news cards and article previews from verified primitives, then match summaries/scoreboards and tournament tables with nested instances and bindings.
5. Build navigation and page patterns, validate composition against desktop/tablet/mobile screenshots and check table scrolling/sticky behavior.

Reserved canvas sections03 — Composite Components and04 — Patterns contain documentation only. No Phase3 composites or page templates were created.
