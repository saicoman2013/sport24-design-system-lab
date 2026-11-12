# Sport24 Phase 2 — Foundations

Scope: existing Figma file `j3xgA2ZDMBbmbJnsGCxdhf`, page `2011:17965`. Source: the five completed reports under `/workspace/audit/`, their JSON/CSS evidence and screenshots, plus focused source verification in this phase. The canonical Button radius is **4px**, confirmed by the user; historical 3px Button measurements do not override it.

## Completion status

Supported foundations and core components are built and validated. Phase 2 is **partially complete**: system-font and Cera Pro patterns are blocked by font availability. No replacement fonts, flattened UI, HTML imports, React components, or dependencies were introduced.

77 new Variables; 11 existing Variables reused (88 total). 8 new Text Styles; 1 existing Button Text Style reused. 1 new Effect Style. 8 new native COMPONENT nodes (6 standalone plus 2 Heading variants), 1 new COMPONENT_SET. Existing Button set and its 2 variants preserved. Total on page: 10 COMPONENT nodes and 2 COMPONENT_SET nodes. Four variant members across Button and Section Heading; no duplicate family names.

## Collections and values

- Existing `Sport24 / Button Test`, Website mode: retained unchanged; original IDs preserved.
- `Sport24 / Primitives`: source color values, including alpha. Existing black, yellow and yellow-hover primitives reused rather than duplicated.
- `Sport24 / Semantic`: aliases for verified text/background/border/action/status roles. Semantic names are library organization proposals, not a claim that the source website exposes those exact names.
- `Sport24 / Metrics`: measured spacing, independent radii, borders and layout reference widths. One Website mode; no invented light/dark modes.

Every variable has targeted scopes or empty primitive scopes. CSS expressions are preserved where there is an actual CSS variable; literal source values are used in code syntax when no equivalent website custom property exists. No fabricated CSS custom property names are implied. Alpha values read as CSS 0.5 retain exactly 0.5; hexadecimal suffixes ending 80 are display labels rounded to 8 bits.

## Typography

Stag Sans LC Medium and Bold are available. The website maps CSS weight 400 to `StagSansLC-Medium.woff2` and 700 to Bold. Text Styles implement only verified Stag patterns; no arbitrary typographic scale was added. Existing Button Medium16/19.2 style reused.

Cera Pro, Arial and Helvetica Neue failed exact Figma font loading. The website system stack is `-apple-system, "Helvetica Neue", Arial, sans-serif`; neither HelveticaNeueCyr nor Inter was substituted. Body, news-link, metadata, tab and select styles requiring that stack remain unbuilt. A CSS family declaration alone does not establish a font's actual use on every sports-data node.

## Spacing and radius

Normalized measured spacing: 0, 2, 3.5, 4, 5, 7, 8, 10, 11, 12, 12.5, 16, 19, 24px. Existing zero/10px variables reused. These are contextual source metrics, not an invented 4px/8px scale or assertion that margins and gaps are interchangeable.

Independent source radii: 0, 2, 3, 3.5, 4, 8, 14px; do not infer interchangeability. For example, 3px is observed on sports-status marks; 3.5px on form-result marks; 4px on image links/selects; 8px is also declared on Group values; 14px belongs to a separate comment/reaction control. All **Sport24 Button** assets created here use `radius/button = 4`. Radius0 remains on non-button icon primitives, text links, labels and headings.

The new Icon Button reuses the earlier header icon-container component ID, rather than duplicating it. It serves the icon-container role too. Its 40×44 source geometry is retained, and the canonical Button4px rule is applied to its transparent control bounds; the source menu trigger had square bounds. This is explicitly a user-specification override, not a claim that the source CSS radius is 4px.

## Borders and effects

Border widths 0/1px and verified source colors are stored as variables. Native Effect Style `Sport24 / Popup / Declared shadow` implements declared `--Popup-box-shadow: 0 0 10px #0003`; it is marked declared-only and is not an invented elevation ladder.

## Layout references

| Viewport | Measured main width | Columns | Gap | Outer margins |
|---|---:|---:|---:|---|
| 390 | 358 | 4 | 8 | 16px |
| 768 | 688 | 9 | 24 | 40px |
| 1440 | 1032 | 12 | 24 | auto, centered |
| 1920 | 1032 | 12 | 24 | auto, centered |

Source: home viewport JSONs, `responsive-behavior.md`, saved HTML `._465xgJ` inline `--grid-columns-mobile:4`, `--grid-columns-tablet:9`, `--grid-columns-desktop:12`, and main CSS media queries. Desktop source column width is64px; tablet/mobile use fractional columns. These grids describe the sampled main-content layout, not every grid on every page.

Main breakpoints: max767px; 768–1279px; min1280px. Native reference frames and column grids were created. Figma Variables do not automatically switch with viewport width; Heading variants are selected manually.

## Canvas organization

- 00 — Foundations: [ 2020:92 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2020-92)
- 01 — Primitives: [ 2020:243 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2020-243)
- 02 — Components: [ 2020:244 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2020-244)
- 03 — Composite Components: [ 2020:245 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2020-245)
- 04 — Patterns: [ 2020:248 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2020-248)

The original test section `2014:15` and Button masters were not moved or renamed. `02 — Components` contains connected Button examples referencing the original family. Sections03/04 are reserved documentation areas, not empty component sets.
