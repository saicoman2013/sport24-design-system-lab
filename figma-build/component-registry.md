# Sport24 component registry

77 new Variables; 11 existing Variables reused (88 total). 8 new Text Styles; 1 existing Button Text Style reused. 1 new Effect Style. 8 new native COMPONENT nodes (6 standalone plus 2 Heading variants), 1 new COMPONENT_SET. Existing Button set and its 2 variants preserved. Total on page: 10 COMPONENT nodes and 2 COMPONENT_SET nodes. Four variant members across Button and Section Heading; no duplicate family names.

All listed assets exist in the target file. Instances and QA frames are not counted as component masters.

| Component family | Native type | Node | Source / scope |
|---|---|---|---|
| Sport24 / Icon / Menu | COMPONENT | [ 2021:3 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-3) | audit/evidence/details.json div.c6eBIW |
| Sport24 / Icon / Close | COMPONENT | [ 2021:6 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-6) | audit/evidence/details.json div.meSwEH |
| Sport24 / Icon / Match Center | COMPONENT | [ 2021:9 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-9) | phase2-source.json news 768 a.xeeGUd svg; CSS29x20 |
| Sport24 / Label / League | COMPONENT | [ 2021:12 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-12) | news-768 .d42p0x; audit CSS .dB25r0 .d42p0x |
| Sport24 / Text Link / Match Center | COMPONENT | [ 2021:14 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-14) | news-768 a.xeeGUd and phase2-source.json |
| Sport24 / Icon Button | COMPONENT | [ 2021:19 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2021-19) | details.json div.c6eBIW, canonical Button radius override |
| Sport24 / Section Heading | COMPONENT_SET | [ 2024:28 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2024-28) | match h2._7FBqFX at four viewports |
| Sport24 / Button | COMPONENT_SET | [ 2015:2 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2015-2) | Existing validated Button; audit home-1440; user-confirmed canonical radius 4px |

## Sport24 / Icon / Menu

ID: 2021:3


## Sport24 / Icon / Close

ID: 2021:6


## Sport24 / Icon / Match Center

ID: 2021:9


## Sport24 / Label / League

ID: 2021:12

Native properties:

```json
{
  "Label#2021:0": {
    "type": "TEXT",
    "defaultValue": "НХЛ"
  }
}
```

## Sport24 / Text Link / Match Center

ID: 2021:14

Native properties:

```json
{
  "Label#2021:1": {
    "type": "TEXT",
    "defaultValue": "Смотреть все матчи"
  },
  "Icon#2021:2": {
    "type": "INSTANCE_SWAP",
    "defaultValue": "2021:9",
    "preferredValues": []
  }
}
```

## Sport24 / Icon Button

ID: 2021:19

Native properties:

```json
{
  "Icon#2021:3": {
    "type": "INSTANCE_SWAP",
    "defaultValue": "2021:3",
    "preferredValues": []
  }
}
```

## Sport24 / Section Heading

ID: 2024:28

Native properties:

```json
{
  "Label#2024:0": {
    "type": "TEXT",
    "defaultValue": "Статистика"
  },
  "Viewport": {
    "type": "VARIANT",
    "defaultValue": "Desktop",
    "variantOptions": [
      "Desktop",
      "Mobile"
    ]
  }
}
```

Variants:

- Viewport=Desktop: [ 2024:24 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2024-24)
- Viewport=Mobile: [ 2024:26 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2024-26)

## Sport24 / Button

ID: 2015:2

Native properties:

```json
{
  "Label#2015:0": {
    "type": "TEXT",
    "defaultValue": "Загрузить еще"
  },
  "State": {
    "type": "VARIANT",
    "defaultValue": "Default",
    "variantOptions": [
      "Default",
      "Hover"
    ]
  }
}
```

Variants:

- State=Default: [ 2014:16 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2014-16)
- State=Hover: [ 2014:18 ](https://www.figma.com/design/j3xgA2ZDMBbmbJnsGCxdhf?node-id=2014-18)

## Implementation notes

- Icon Menu25×18, Close18×18 and Match Center29×20 use source SVG paths as editable vector descendants; proportions are preserved within the audited CSS icon bounds. Match-center source artwork is24×16 and is scaled uniformly to29px width, vertically centered within20px control height.
- Icon Button `2021:19` is the same node initially built as Icon Container/Header. It was renamed/reused within this build, not duplicated. `Icon` is an INSTANCE_SWAP property. Default only; radius/button4px is the documented user-rule override. Transparent; designed for the black header context.
- Label/League is specifically the `.d42p0x` **text primitive**, not a complete logo-bearing league chip: Stag Medium14/16, vertical padding8px, natural width and height32px. Full league/logo tags remain future work.
- Text Link/Match Center is the specialized observed `a.xeeGUd` control, not the unavailable system-font news/body-link family. Master246×59; Stag14/14 label, 29×20 nested icon, 8px gap, centered. Label and Icon properties; no unverified hidden-icon or hover/disabled variant.
- Section Heading: Desktop32/40 applies at768/1440/1920; Mobile20/24 at390. Editable Label. No fabricated accompanying action: the audit shows a small outline Button which was not added to the validated Button family in this phase.
- Native font shaping produces natural label widths of29px vs28.125px browser and link-label132px vs131.03125px browser; Heading natural width171px vs170.53125px. Font family, style, size and line height match. Text was not horizontally distorted to force these subpixel metrics.
- Existing Button remains170×48, padding0/10, radius4, StagMedium16/19.2, original Label and State properties, original Default/Hover IDs and variable bindings.
