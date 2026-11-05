# Allegro visual reference

Extracted from [Allegro](https://allegro.pl/) on 2026-11-05 with Playwright CLI and visible Google Chrome at a 1440 x 1000 CSS-pixel viewport, using the light theme. This is an observed homepage reference, not an official brand manual. Token names and suggested usage below are interpretations of rendered components.

## Assets

| Asset | Local file |
| --- | --- |
| Full-page screenshot | [homepage.png](../assets/homepage.png) |
| Structured tokens | [design-tokens.json](../assets/design-tokens.json) |
| Orange wordmark | [logo.svg](../assets/logo.svg) |
| Favicon | [favicon.ico](../assets/favicon.ico) |
| Inter Light 300 | [inter-300_6e675dc7.woff2](../assets/fonts/inter/inter-300_6e675dc7.woff2) |
| Inter Regular 400 | [inter-400_ff6a2a72.woff2](../assets/fonts/inter/inter-400_ff6a2a72.woff2) |
| Inter Medium 500 | [inter-500_16fd771f.woff2](../assets/fonts/inter/inter-500_16fd771f.woff2) |
| Inter Bold 700 | [inter-700_460e5670.woff2](../assets/fonts/inter/inter-700_460e5670.woff2) |
| Open Sans variable | [open-sans_6cc28a8e.woff2](../assets/fonts/open-sans/open-sans_6cc28a8e.woff2) |
| Roboto variable | [roboto_e4451a57.woff2](../assets/fonts/roboto/roboto_e4451a57.woff2) |

Logo and font usage and redistribution rights must be verified before using these files in a product.

## Colors

| Token | Value | Observed usage |
| --- | --- | --- |
| brand.primary | #FF5A00 | Wordmark, search action, loading indicator |
| brand.accent | #422779 | Smart! and campaign accents |
| brand.success | #107B1E | Discount badges, prices, delivery messages |
| background.default | #FFFFFF | Header, cards, footer content |
| background.light | #ECEFF1 | Page canvas |
| background.footer | #3A4E58 | Dark wordmark strip |
| background.promotion | rgba(14, 14, 14, 0.08) | Promotion panel over the page canvas |
| text.primary | rgba(0, 0, 0, 0.87), approximately #212121 on white | Main UI text |
| text.secondary | rgba(0, 0, 0, 0.54), approximately #757575 on white | Supporting labels |
| text.muted | #767676 | Secondary text and icons |
| text.onDark | #FFFFFF | Primary action and dark campaign text |
| text.action | #008673 | Utility actions |

Keep alpha colors as alpha values; their apparent hex depends on the surface. No error-state color was established. Campaign imagery can introduce additional colors without changing the core palette.

## Typography

Use `Inter, sans-serif` for product cards, prices, section titles and promotional tiles. The search input and header controls use `"Open Sans", sans-serif`. Roboto is declared by the site, but was not identified as a principal visible text style in this sample. Do not copy the browser-default Times New Roman found on structural wrappers or the default blue of icon-only anchors.

The source declares normal-style `@font-face` rules with `font-display: swap`. Inter has weights 300, 400, 500 and 700. Open Sans declares 300, 400, 600 and 700 with a shared variable WOFF2 source; Roboto declares 300, 400, 500 and 700 with its shared variable source. The downloaded subset includes Latin, Polish and other selected European/Cyrillic characters; do not assume universal coverage. Fonts were served from Allegro's asset host, `assets.allegrostatic.com`, and fetched in the page context.

| Size / line height | Use |
| --- | --- |
| 12px / 18px | Badges, delivery and supporting information |
| 14px / 20px | Product names and tile labels |
| 14px / 21px | Header supporting controls |
| 16px / 40px | Search action/control alignment |
| 20px / normal | Section supporting title |
| 22px / normal | Product prices |
| 24px / normal | Section titles |

Regular 400 and bold 700 dominate. Medium 500 appears on the outlined secondary action. Campaign typography also uses responsive fractional sizes; do not turn those into global type tokens. All downloaded font paths are listed above; verify their licenses before use.

## Spacing

Use a 4px base unit as a synthesis of observed repeated values: 4, 8, 12, 16 and 24px. Page gutters are 24px at the sampled desktop width. Cards and tiles use compact gaps with generous white interiors. A promotion container uses 40px vertical padding. Icon navigation has an observed 6px gap, an exception to the base unit.

## Border radius

| Value | Context |
| --- | --- |
| 0px | Structural wrappers and icon controls |
| 2px | Search action and small labels |
| 4px | Small isolated control detail |
| 8px | Secondary controls and smaller surfaces |
| 16px | Product cards, promotional tiles and hero frame |
| 100% | Circular controls/decorative shapes |

The search input has `2px 0 0 2px` so it joins adjacent controls. Preserve joined-control corners rather than rounding every field independently.

## Components and layout

- **Header:** white, two rows, approximately 128px combined. The top row is about 76px. Place the orange logo left, a wide joined search group in the middle, and grey outline utility icons on the right.
- **Navigation:** category control followed by compact campaign/service links. Use Open Sans, restrained dark text, and thin dividers.
- **Primary action:** orange background, white uppercase text, 16px/700, 2px letter spacing, 40px height and 2px corners. The sampled search button has zero computed padding; its width is controlled by layout.
- **Search input:** 14px Open Sans, 8px padding and 40px border-box height. It shares a frame with category selection and the search action. Border styling may belong to the surrounding group.
- **Hero:** wide image-led rotating campaign, 16px corners, 24px page gutters and small pagination dots. Its current artwork is temporary campaign content.
- **Promotional tiles:** five white, rounded tiles with an illustrated symbol and short bold text at the sampled width.
- **Product cards:** white rounded surfaces with large product photos, favourite heart, price, discount badge, Smart! label, product name and delivery details. Prices use 22px regular text; supporting information is 12px. Horizontal rows can clip at the right edge.
- **Secondary action:** compact outlined button with 16px medium text and rounded corners, exemplified by "Więcej".
- **Footer:** multiple dense link columns, followed by a dark strip containing a white wordmark.

Only desktop resting styles were sampled. Hover, focus, validation, mobile layout and modal styling require separate observation before implementation.

## Logo usage

The saved SVG is the actual orange header wordmark, with a `0 0 145 50` viewBox and source dimensions 128 x 43. Preserve its proportions and use it on a light background. Keep surrounding space consistent with the screenshot. A white footer variant was visible, but was not downloaded; do not substitute a recolored asset without checking brand guidance and usage rights.

## Visual style summary

Allegro combines a vivid orange identity with a quiet grey shopping canvas. White cards and rounded promotional blocks separate dense product information. Typography prioritizes prices, short labels and scannable supporting details. Thin outline utility icons keep the header light, while colorful campaign illustrations provide emphasis.

## Capture verification and limits

The initial 403 cleared during a brief wait and normal navigation in the same browser session. Cookie consent was dismissed, overlay searches returned no matches, and the final full-page PNG was visually inspected. Scrolling loaded additional product rows and footer content; one lazy-loading indicator remained in the capture. The page logged third-party resource failures and browser AI service warnings, so this capture is a reference for successfully rendered content, not a claim that every external service loaded. No application code was changed and no commit was created.
