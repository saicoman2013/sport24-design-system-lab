# Sport24 validation report

## Result

Supported batches passed native structure, variable binding, editable-property, connection and visual checks. Phase2 remains partial due to unavailable fonts and unverified patterns; see known-limitations.md.

77 new Variables; 11 existing Variables reused (88 total). 8 new Text Styles; 1 existing Button Text Style reused. 1 new Effect Style. 8 new native COMPONENT nodes (6 standalone plus 2 Heading variants), 1 new COMPONENT_SET. Existing Button set and its 2 variants preserved. Total on page: 10 COMPONENT nodes and 2 COMPONENT_SET nodes. Four variant members across Button and Section Heading; no duplicate family names.

## Batch acceptance

| Batch | Result | Evidence |
|---|---|---|
| 1 Foundations | PASS for available fonts |77 new variables, aliases resolve; no ALL_SCOPES;8 Stag styles; visual specimen reviewed; Button snapshot unchanged |
| 2 Basic primitives | PASS for supported patterns |6 native components initially; Label overrides and Icon swap tested; source vector descendants; light specimen contrast corrected and reviewed |
| 3 Interactive | PASS for Button/Icon Button; font-blocked patterns deferred |Button exact IDs/properties retained; default/hover switching and390/768/1440/1920 tests pass; header icon-container reused as Icon Button |
| 4 Structural | PASS for Section Heading |Native Component Set with2 responsive variants; editable Label; viewport switching; four measured content-width tests pass |

## Native structure and bindings

| Node | Type | Auto Layout | Dimensions | Radius | Text style references |
|---|---|---|---|---|---|
| [ 2014:16 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2014-16) | COMPONENT | HORIZONTAL | 170 × 48 | 4 | S:0dc6b053b9aa097ab4c9afa7c53361f9d85c9f5f, |
| [ 2014:18 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2014-18) | COMPONENT | HORIZONTAL | 170 × 48 | 4 | S:0dc6b053b9aa097ab4c9afa7c53361f9d85c9f5f, |
| [ 2021:3 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-3) | COMPONENT | HORIZONTAL | 25 × 18 | 0 |  |
| [ 2021:6 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-6) | COMPONENT | HORIZONTAL | 18 × 18 | 0 |  |
| [ 2021:9 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-9) | COMPONENT | HORIZONTAL | 29 × 20 | 0 |  |
| [ 2021:12 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-12) | COMPONENT | HORIZONTAL | 29 × 32 | 0 | S:7fe3568444aa1f465dd548ad3beef7eb1060ef80, |
| [ 2021:14 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-14) | COMPONENT | HORIZONTAL | 246 × 59 | 0 | S:4cdb0d29887a3040baf34c0181b9268a20531e7f, |
| [ 2021:19 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-19) | COMPONENT | HORIZONTAL | 40 × 44 | 4 |  |
| [ 2024:24 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2024-24) | COMPONENT | HORIZONTAL | 171 × 40 | 0 | S:703f784cb27b356868b09811c538c8fa4977e14f, |
| [ 2024:26 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2024-26) | COMPONENT | HORIZONTAL | 358 × 24 | 0 | S:6c4f4197401cf6c44b09e6dd16f383f09c6ff191, |

Broken bound-variable references:0. Duplicate component family names:0. Variables with ALL_SCOPES:0. All created component nodes use native Auto Layout. Native Label text layers remain editable; vector icons remain vector paths.

## Responsive checks

Button: minimum170×48 and radius4 retained at390/768/1440/1920. Variant switch Default→Hover→Default passed.

Section Heading uses actual content widths:

| Viewport | Content width | Height | Font size | Passed |
|---|---|---|---|---|
| 390 | 358 | 24 | 20 | True |
| 768 | 688 | 40 | 32 | True |
| 1440 | 1032 | 40 | 32 | True |
| 1920 | 1032 | 40 | 32 | True |

Text Link: fill-container stress tests passed at content358/688/1032/1032; nested icon stays29×20. These stress tests establish Figma resizing only, not website visibility or layout equivalence at all widths. The source control was specifically measured at the768px context.

Heading variant switching, Label text override, natural-width label growth, Icon INSTANCE_SWAP and connected nested instances passed. Icons remain fixed-size.

## Existing-design preservation

Original Button set2015:2; Default2014:16; Hover2014:18; original instance2015:3 still connected to2014:16. All four corners remain bound to VariableID:2014:11, radius/button4. Dimensions, fills, text styles, Label and State definitions preserved. Original test section2014:15 retains bounds x120/y120/520×240. All new sections are outside its bounds. No existing unrelated layer was deleted, moved, renamed, detached or edited.

## Visual review

Figma screenshots were reviewed for Foundations, primitives and interactive/heading specimens. Documentation contrast was corrected, and the resulting render rechecked. No screenshots are used as UI components. Historical audit screenshots and DOM/CSS properties were used for source comparison. Text shaping differs by small subpixel amounts between browser and Figma; see component-registry.md.
