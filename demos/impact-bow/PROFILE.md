# IMPACTBOW: store profile

- URL: https://www.impactbow.com
- Profiled: 2026-10-27
- Slug: `impact-bow`
- Screenshots: `_profile/home-1440.png` (fold), `_profile/home-1440-full.png`, `_profile/collection-1440.png`, `_profile/product-1440.png`
- Demo: `/demos/impact-bow/`

## Platform
- **Shopify: confirmed.** `/products.json?limit=250` returns 200 with JSON. CDN asset paths point at shop `0989/3419/4560`.
- Theme: **Badge**, `schema_name: Next`, version 3.4.0, theme-store id 2240. Assets are on `/cdn/shop/t/3/`.
- Markets: NL (default), EN (`/en/`), DE (`/de/`). 20+ European countries with local currencies in the country switcher.
- Apps seen in the HTML:
  - **Essential Post-Purchase Upsell** (`essential-post-purchase-upsell`) renders the product-page **"Bundel deal"** block.
  - **SyncX Preorder** (`syncx-preorder`) adds pre-order popups.
  - **Bundler** from `cdn-bundler.nice-team.net` is also loaded on the homepage.
  - Shopify Shop app, hCaptcha on forms.
  - **No reviews app** (no Judge.me, Loox, Yotpo or Okendo on the page) and **no loyalty app**.
- Pages that exist: `/pages/contact`, `/pages/veelgestelde-vragen`. There is **no configurator, bundle landing page or gift finder** in the sitemap.

## Identity
- **What they sell:** crossbows and everything around them (arrows, magazines, sights, strings, limbs, targets, carry bags, maintenance), plus a **self-defence** range (alarms, pepper spray, handcuffs, batons, tactical pens, an "extreme storm" umbrella, flashlights).
- **Brands in the catalogue:** Steambow (PD-5, M10, B08), EK Archery (REVO 7, VLAD, Cobra), X-BOW FMA (Supersonic REV / REV XL), Barnett (Demun Tri Strike, HyperBolt), Hawke, NC Star, Nitecore, Ballistol, Real Avid, Energizer.
- **Who buys:** Dutch and Belgian outdoor/prepper buyers and recreational archers. The footer says **"In samenwerking met: DUTCHPREPPER.COM"**, and the self-defence range is aimed at the same audience. The FAQ is written for first-time buyers ("Mag ik een kruisboog bezitten?").
- **The owner is not named anywhere.** The legal notice, the contact page, the FAQ, Article 2 of the terms, Instagram @impactbow (45 followers, 84 following, no personal name) and the Chamber of Commerce entry (85304808 → **DIVALO Trading**, De Taling 59 Almelo, 1 employee, "Myself Only" on LinkedIn) all name the company, never a person. The entity behind IMPACTBOW, DUTCHPREPPER.COM, DIVALO Trading and TomorrowNow is a one-person e-commerce operation. **Do not invent a name** — address the shop and let them fill in their own name if they reply.
  - Ruled out: "R. S. Bruinzeel" (Roland Bruinzeel, KvK 76459667, Heiloo / Broek op Langedijk) resells DIVALO's TomorrowNow products on bol.com, but is a **separate** company with its own KvK, address and brand (BROËL). Not the same owner.
- **They already build product builders.** This is the single strongest reason the demo should exist:
  - The sister shop **DUTCHPREPPER.COM** ships a **"Stel uw eigen noodpakket samen"** builder (`/apps/box-builder/…`): *"Assemble your emergency kit in 13 steps"* — 1 Safe Drinking Water, 2 Food, 3 Cooking, 4 Communication, 5 Lighting, 6 Power Supply, 7 First Aid, 8 Hygiene, 9 Safe Storage, 10 Fire, 11 Heat, 12 Tools, **13 Hunting-Defense**, with "Add to box" per product and a running box total. The same steps → pick → live total pattern.
  - Both shops load the **Bundler** app (nice-team) on product pages and the homepage.
  - **16 crossbow products carry the internal tag `blueprint-596-crossbow-configurator`** and **three "DEMO - " test products are live in the catalogue and visible in /collections/kruisbogen**: DEMO EK Archery VLAD (€ 349,99), DEMO EK Archery REVO 7 120 lb (€ 549,99), DEMO Steambow PD-5 135 lb (€ 999,99).
  - The same three DEMO crossbows also sit in DUTCHPREPPER.COM's collections.
  - So a configurator is clearly already being planned — the demo is the accessories layer, not a competing concept.
- **Price range:** € 4.99-ish for small parts to **€ 1.029,99** for the Steambow PD-5 135 lb. The crossbow ladder is € 42,99 (Cobra) → € 129,99 (Tri Strike) → € 329,99 (VLAD / M10) → € 399,99 (B08) → € 499,99 (REVO 7) → € 539,99 (REV Tactical) → € 679,99 (REVO 7 Tactical) → € 739,99 (REVO 7 Range) → € 929,99 / € 1.029,99 (PD-5 90 / 135).
  - Accessories sit between € 5,99 (wax) and € 239,99 (Hawke XB1 scope).
- **Language and tone:** Dutch (Netherlands), **"je"** in product copy and **"u"** in the service/footer copy. Short, factual, no emoji. Headings are **UPPERCASE** with heavy letter-spacing, often as a question or a statement ("HOE KIES JE EEN KRUISBOOG VOOR JOUW DOEL?", "ALS ELKE SECONDE TELT EN HULPDIENSTEN NOG MINUTEN ONDERWEG ZIJN").
- **Country / currency:** Netherlands, EUR. Address **De Taling 59, 7609 VA Almelo**. KvK **85304808**, BTW **NL004076840B24**. Phone **+31 85 124 9577**, email **customerservice@impactbow.com**, Instagram **@impactbow**.
- **Compliance:** the FAQ is explicit. 18+ to own, no carrying in public, use only on private land or at a club/range, hunting with crossbows forbidden, lamps and lasers banned in some countries. Every product is "uitsluitend bedoeld voor legaal sportief en recreatief gebruik".
- **Shipping:** the shipping policy only says terms are shown at checkout ("Op basis van de aangegeven condities zoals zichtbaar is op het afrekenscherm"). **No free-shipping threshold and no delivery promise on the site**, so the demo must not invent one.
- **Returns:** `/policies/refund-policy` (14/30-day statutory handling, not quoted on the product page).

## Visual system (from live HTML/CSS)
- **Font:** `Anek Tamil` everywhere (`--main_ff`, `--main_ff_h`, `--theme_btn_ff`), self-hosted from `fonts.shopifycdn.com`. Headings weight **500**, letter-spacing **.1em**, line-height **1**. Body **18px / 1.45 / 400**.
- **Colours:**
  - Navy `#1a2350` / `#172048`: header, hero overlay, footer, scheme-1 background
  - Orange `#f2673a`: logo, nav, headings, prices, sale labels, primary buttons (`#f04d19` on hover)
  - White `#ffffff`: page background and product cards
  - Light grey `#ececec` / `#f2f2f2`: product circles, inputs, dividers
  - Gold `#efae45`: secondary accent, used sparingly
  - Sale label `#f2673a`, positive green `#35b058`
- **Buttons:** solid orange, white 700 label, **2px border**, **32px radius**, **55px height**, 16px text. Secondary buttons are black.
- **Cards:** no border or shadow on collection cards. Product photos are transparent/white cut-outs on white, with **orange product titles** and the price inside a **solid orange pill with white bold text**. Old price is orange strikethrough. Sale badge is an orange rectangle top-left ("Sale -21%").
- **Header (desktop):** solid navy bar, ~62px tall. Logo image 26px tall on the left (orange wordmark PNG, `ImpactBow.png`), centred nav in orange uppercase with `.1em` tracking: KRUISBOGEN, ZELFVERDEDIGING, FAQ, CONTACT. Right: NL flag, search, account, cart with a badge. On mobile the nav collapses and the logo stays left.
- **Homepage:** full-bleed dark hero slideshow with a big uppercase orange headline and a slide counter ("02"). Below it, category rows of **circular product thumbnails** on white with orange labels: KRUISBOGEN (PD-5, REVO 7, REV, M10, VLAD, Tri Strike, Cobra), TOEBEHOREN KRUISBOGEN, ZELFVERDEDIGING. Navy footer with orange column headings.
- **Product page:** orange title, big gallery, "Productkenmerken" spec box on the right, orange price, quantity stepper and a full-width orange pill "In winkelwagen". Below the description sits the **"Bundel deal"** block.
- **Logo:** `https://www.impactbow.com/cdn/shop/files/ImpactBow.png?v=1775896468` (orange on transparent, 600×75).

## Catalogue
137 products in `products.json`, of which 3 are `DEMO - …` or untitled placeholders. 25 collections:

| Collection | Products |
|---|---|
| KRUISBOGEN | 20 |
| TOEBEHOREN | 85 |
| ZELFVERDEDIGING | 32 |
| PIJLEN MAGAZIJNEN | 17 |
| RICHTEN | 27 |
| BOOGLATTEN PEZEN | 23 |
| TASSEN | 7 |
| ONDERHOUD | 6 |
| SCHIETDOELEN | 3 |
| VERLICHTING | 11 |
| AFWEER | 9 · ALARMEN | 9 · SPRAYS | 5 · HANDBOEIEN | 2 |
| VOORDEELSETS | 1 |

**Crossbow families and what fits them** (this is the data the demo is built on):

| Family | Models | Arrows | Magazine | Bag | Sight |
|---|---|---|---|---|---|
| Cobra | EK Archery Cobra 80 lb (€ 42,99) | VLAD/Cobra 6.5" (plastic € 8,99, steel € 17,99, carbon bodkin € 37,99) | — | Draagtas Cobra € 27,99 | Red Dot 1x40 |
| VLAD | EK Archery VLAD 60/90 lb (€ 329,99) | VLAD/Cobra 6.5" | 8-shot built in | Draagtas VLAD € 42,99 | Red Dot 1x40 |
| REVO 7 | REVO 7 90 lb (€ 499,99), Tactical Edition (€ 679,99), Range Edition (€ 739,99) | REVO 7 6.5" (standard € 36,99, bodkin € 54,99) | REVO 7 magazijn € 49,99 | Rugtas REVO 7 € 39,99 | Red Dot 1x40, Richtkijker 4x32 |
| REV | X-BOW FMA Supersonic REV Tactical (€ 539,99), REV XL (€ 559,99) | REV Tactical High Impact 10 st. € 42,90 | 6-shot built in | — | Red Dot, riser, Picatinny rail |
| M10 | Steambow M10 Tactical 75 lb (€ 329,99) | Steambow pijlen | Steambow M10 magazijn € 49,99 | Magazijntas REVO 7/M10 € 19,99 | Red Dot |
| B08 | Steambow B08 Tactical 35 lb (€ 399,99, less lethal) | Steambow B08 projectielen .68 | B08 magazijn € 49,99 | — | — |
| PD-5 | Steambow PD-5 90 lb (€ 929,99), 135 lb (€ 1.029,99) | Steambow PD-5 pijlen € 39,99 | 5-shot built in | — | Red Dot / scope |
| Tri Strike | Barnett Demun Tri Strike 50 lb (€ 129,99) | Barnett HyperBolt 2F 12 st. € 26,99 | 3-shot built in | — | Red Dot |

Shared accessories: wax € 5,99, Ballistol 100 ml € 11,99, trekkerslot € 19,99, schietdoel 450 FPS € 79,99 / 500 FPS € 129,99, richtkijkers € 52,99–€ 239,99, red dots € 39,99–€ 139,99.

**Stock on 2026-10-27:** Cobra and M10 Tactical are out of stock; every model used in the demo is in stock.

## Existing offers
- **"Bundel deal"** on the product page: a frequently-bought-together block from Essential Post-Purchase Upsell. It sits **below the gallery and spec box** (starts at ~1160 px on a 900 px viewport, so below the fold) and **above** the product description.
- **Four funnels are configured, but only three render** on a live product page. Checked live on 2026-10-28 across all ten crossbow product pages:

  | Page | Bundel deal | Rows (discounted → list) |
  |---|---|---|
  | EK Archery VLAD (€ 329,99) | **yes** | 5,99 → 3,90 · 17,99 → 16,92 · 37,99 → 36,10 · 39,99 → 34,00 |
  | EK Archery REVO 7 90 lb (€ 499,99) | **yes** | 5,99 → 3,90 · 36,99 → 31,45 · 49,99 → 42,50 · 39,99 → 34,00 · 52,99 → 45,05 |
  | X-BOW FMA REV Tactical (€ 539,99) | **yes** | 5,99 → 3,90 · 42,90 → 36,47 · 39,99 → 34,00 · 19,99 → 19,00 |
  | PD-5 90 / 135, REVO 7 Tactical / Range, REV XL, M10, B08, Tri Strike, Cobra | **no** | — |

  The Essential Post-Purchase Upsell **embed is present on every page**, but only these three have a bundle configured, so the rest render nothing.
- **The discount is per product, not a flat rate.** 35% on the wax, 15% on the red dot, scope and magazine, but only ~5–6% on the VLAD arrows and bolts. The demo applies a flat 15% to every accessory; a real build must mirror their exact per-product rules or it costs them margin.
- **Voordeelpakket Zelfverdediging** (€ 35,99): a static bundle of spray + training spray + holster. The only "voordeelset" product in the store.
- Sale badges on selected products (e.g. PD-5 135 −21%, M10 −13%, Tri Strike −13%, Cobra −14%).
- No cross-sell on the cart page beyond the post-purchase app, no gift finder, no quiz.

## Gaps the demo is built on
1. **The bundle only exists on 3 product pages.** The PD-5 (€ 929,99 / € 1.029,99), the REVO 7 Tactical and Range, the REV XL, the M10, the B08, the Tri Strike and the Cobra buyers get no accessory offer at all.
2. **It sits below the fold.** The block starts around 1160 px down on a 900 px viewport, so the customer has to scroll past the whole gallery and spec box before seeing it.
3. **It is a checkbox list, not a set.** Five accessories are stacked as rows; nothing explains *why* they belong together, and nothing shows the finished set.
4. **No goal guidance.** The homepage asks "HOE KIES JE EEN KRUISBOOG VOOR JOUW DOEL?" and then drops the visitor into a flat 20-product grid.
5. **No bundle landing page.** There is no page that can rank for "kruisboog set" or be linked from ads.
6. **16 crossbows already carry the tag `blueprint-596-crossbow-configurator`** in Shopify, so a configurator is clearly being planned. Nothing public exists yet.

## Demo concept: "Stel je set samen"
- **Goal first.** Three chips (Recreatief / Tactisch / Precisie op afstand) reorder the crossbow grid and label the matching models "Aanbevolen". This answers the store's own homepage question.
- **One bow.** Six in-stock models, real prices, real sale badges, real product photography.
- **Compatible parts only.** Picking a bow rebuilds step 3 from that family: only the arrows, magazines, bags and sights that fit are shown. Switching bows removes what no longer fits and says so.
- **Setvoordeel 15%.** The exact discount the shop already gives, applied to every accessory, shown as struck-through prices and a saved amount.
- **A sticky "Jouw set" panel** on the right of the builder (desktop): thumbnails of every chosen part, the crossbow with its price, the parts list with their set prices, a four-part completeness meter, the set discount and the live total.
- **Each step is a folding wrapper.** The header keeps the choice visible (thumbnail, name, spec, price), so a finished step folds itself away and the next one opens. Picking a crossbow folds step 01 and moves to step 02; picking a sight folds step 02 and moves to step 03. Any header can be reopened by clicking it.
- **Step 03 is tabbed** per product group (pijlen & magazijn / tas / doel & onderhoud) with a count badge per group. Only the groups that fit the chosen crossbow appear. Selecting a part never folds the step, because these groups accept multiple selections.
- **One-click recommendation.** "Neem deze set over" adds a sight, arrows and one extra that match the chosen goal.
- **The bundle is one cart line.** Adding the set creates a single product in the cart with every included product image inside that line, one price and one remove action — not a row per accessory. The cart badge counts 1.

**Why it should raise order value:** the average crossbow is € 330–€ 1.030 and the accessories are € 6–€ 240 with high margin. The current bundle only reaches 4 of 8 families; a configurator reaches all of them, moves the 15% from a footnote to the main event, and turns "which scope fits?" into a guided step instead of a support ticket.

## Mobile layout (rework, 2026-10-28)
The first version was a desktop layout squeezed into 390 px. The rework gives phones their own layout instead of a scaled-down one.
- **Header.** Sticky navy bar with a hamburger that opens a full-screen menu (Kruisbogen / Zelfverdediging / FAQ / Contact + phone, e-mail and address). The logo drops to 20px so the cart button stays reachable.
- **Hero.** One column, smaller type (h1 29–38px) and a 152px product disc instead of 280px, with the price tag pinned to the disc. The hero now ends around 520px instead of 1.000px.
- **Product lists are rows, not a grid.** Two columns at 390px left the price pill and the struck-through price wrapping onto two lines and every card a different height. Each crossbow and sight is now one row: 84px product photo, name, spec, price, discount and a check mark.
- **The set panel is a bottom sheet.** It used to be hidden completely below 1180px, so a phone could never see which parts were in the set or what the total was. Tapping the bottom bar now opens the panel as a sheet with the same breakdown, and the bar itself carries the thumbnail, total, saving and the CTA.
- **Bottom bar rebuilt.** It used to wrap the total onto two lines ("€ / 129,99") and cover the footer. It is now one line with a safe-area inset, the page gets matching bottom padding, and the toast sits above it.
- **Set step.** Underline tabs became scrollable pills, "Alles toevoegen" became a full-width button and the accessory rows were tightened.
- **Footer.** Two columns instead of five stacked lists.
- **Bug fixes that were not mobile-only:** `img` had no `height: auto`, so product photos were stretched and overflowed their cards; the step header used a grid whose tracks shifted when the thumbnail was hidden, pushing the chevron into the middle of the row; and a `min-content` leak from the truncated step summary gave the whole page a horizontal scrollbar.

## Flags / risks
1. **Legal sensitivity.** Crossbows are 18+, no public carry, no hunting. The demo makes no performance or safety claims and repeats the 18+ rule in the trust band.
2. **Prices and stock move.** Every price and image in the demo comes from `products.json` on 2026-10-27. Re-check before sending.
3. **Two bundle apps are installed.** Essential Post-Purchase Upsell already owns the "Bundel deal" slot, and Bundler is loaded too. A configurator would replace (not duplicate) the product-page block, otherwise they discount twice.
4. **A real build needs variant-level data.** Arrows and magazines are family-specific today only by name; the build would need a metafield (or the existing `blueprint-596-crossbow-configurator` tag logic) to guarantee fit.
5. **Photography is inconsistent.** Most bows have clean cut-outs, but the REVO 7 Tactical Edition and Range Edition use flat-lay kit photos. In the demo they look busier than the rest.
6. **No reviews and no social proof on site.** Don't invent any.
7. **Dutch, not English.** The store's default language is Dutch; the email and demo are in Dutch.

## Contact and timing
- **Email: `customerservice@impactbow.com`** (footer, contact page and FAQ). Phone +31 85 124 9577, WhatsApp link in the footer, Instagram @impactbow.
- Small team in Almelo (KvK 85304808, 1 employee), so the inbox is likely read by the owner. The contact page pushes **WhatsApp** and the **contact form** hard — a short WhatsApp message after 3 days of silence will usually beat a second email.
- **Best send time:** Tuesday–Thursday, **09:00–10:30 Europe/Amsterdam** (CET from 25 Oct 2026, UTC+1 — the same clock time as Morocco in October).
- The store answers through a contact form and WhatsApp, so a short email with one clear question fits better than a long pitch.
