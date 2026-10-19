---
name: Ryan Hardwood Floor LLC
description: A phone-first single page set inside a New Jersey room, where a worn floor sands back to oak under your finger.
colors:
  wall: "#1c2a37"
  wall-deep: "#15212c"
  cream: "#e8edf1"
  paper: "#f8fafc"
  ink: "#1c2a37"
  ink-soft: "#46525e"
  on-wall: "#f4ede1"
  on-wall-soft: "#c4ccd3"
  gold: "#d6a94e"
  gold-deep: "#bf9036"
  line: "#c3cdd7"
  focus: "#2d6cdf"
  err: "#b3261e"
  oak-plain: "#a8763f"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(31px, 8.9vw, 96px)"
    fontWeight: 900
    lineHeight: 0.96
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(30px, 8vw, 54px)"
    fontWeight: 900
    lineHeight: 1
    letterSpacing: "-0.01em"
  title:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "21px"
    fontWeight: 900
    lineHeight: 1.25
  row:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(19px, 5vw, 23px)"
    fontWeight: 800
    lineHeight: 1.2
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.55
  lead:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(17px, 4.6vw, 20px)"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 800
    lineHeight: 1.55
rounded:
  field: "10px"
  card: "12px"
  full: "50%"
spacing:
  gutter-phone: "16px"
  gutter-desk: "40px"
  section-phone: "64px"
  section-desk: "96px"
  field-gap: "24px"
  chip-gap: "10px"
components:
  button-fill:
    backgroundColor: "{colors.gold}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.card}"
    padding: "0 26px"
    height: "58px"
  button-fill-hover:
    backgroundColor: "{colors.gold-deep}"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.on-wall}"
    typography: "{typography.label}"
    rounded: "{rounded.card}"
    padding: "0 26px"
    height: "58px"
  button-ink-line:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.card}"
    padding: "0 26px"
    height: "52px"
  input-text:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.field}"
    padding: "12px 14px"
    height: "54px"
  chip:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.field}"
    padding: "0 16px"
    height: "48px"
  chip-checked:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
  service-row:
    textColor: "{colors.ink}"
    typography: "{typography.row}"
    padding: "10px 0"
    height: "68px"
  sent-panel:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.card}"
    padding: "20px"
---

# Design System: Ryan Hardwood Floor LLC

Source of truth is `index.html` (single file): tokens in `:root`, the direction contract in the HTML comment at the top of `<body>`, floor tunables in the `T` object in the "LIVING FLOORS" script. Edit tokens there; this file describes them.

## Overview

**Creative North Star: "The Room Being Refinished"**

The page is the inside of a New Jersey home. Dark sections are a slate-navy painted wall; each wall section stands on a crisp white baseboard and a strip of oak plank floor. Light sections are the same room in daylight, a pale slate. Gold trim comes from the company's own flyer roof mark. The trade is the interaction: the floor starts worn and grey, and sanding (by finger or by an autoplay sander) takes it back to bare pale oak, which warms into finished amber.

Density is phone-first and plain-spoken: one column, big touch targets (44px minimum, 58px primary buttons), heavy uppercase headings in the system face, sentence-case body. No photography until the owner sends real work photos; the floor canvas is the only imagery.

**Key Characteristics:**
- Wall / baseboard / floor stack at the base of every dark section.
- Slate-navy ground, never black; gold as trim and the one fill CTA.
- Blue appears only on form controls (hover/focus), so it never competes with gold.
- System font stack, 900-weight uppercase display, tabular phone numbers.
- Flat UI; the only depth is physical (baseboard shadow, floor lighting).

## Colors

A two-temperature room: cool slate wall and daylight, warm gold and oak.

### Primary
- **Roof-Mark Gold** (`gold`): the flyer's roof mark. Fill CTA background, the gold line of the hero headline, step numerals, header phone icon, brand subline, footer link underlines (at 60% alpha), text selection, global focus ring on dark ground, service-row arrow on hover. **Gold Deep** (`gold-deep`) is the fill button's hover only.

### Secondary
- **Form Blue** (`focus`): outline and 3px halo (`rgba(45,108,223,.18)`) on inputs, textareas and chips on hover/focus, and the outline on the form's submit button on hover/focus. Nowhere else.

### Neutral
- **Slate-Navy Wall** (`wall`): the dark ground of hero, How it works, and close sections; also `theme-color`. Doubles as **Ink** (`ink`), body text on light ground and the checked-chip fill.
- **Deep Wall** (`wall-deep`): footer ground only, one step darker than the wall.
- **Daylight Slate** (`cream`): body background and light sections; also the message box inside the sent panel.
- **Paper** (`paper`): input, chip and sent-panel surfaces on daylight slate.
- **Warm Plaster** (`on-wall`): headings and primary text on the wall.
- **Soft Plaster** (`on-wall-soft`): secondary text on the wall (promise line, step body, close line, footer fine print).
- **Ink Soft** (`ink-soft`): secondary text on light ground (area line, notes, "(optional)").
- **Hairline** (`line`): service-row dividers, input/chip/sent-panel borders at rest.
- **Error Red** (`err`): error messages and invalid field borders.
- **Plain Oak** (`oak-plain`): floor background before the canvas paints.

### Named Rules
**The Never-Black Rule.** The darkest ground is `wall-deep`. The brand's "black and gold" is translated to slate-navy and gold; pure or near-black grounds are out.

**The Two Accents, Two Jobs Rule.** Gold is trim and the action fill. Blue is form-control outline only. Never put blue on a CTA fill or gold on a form-field outline.

## Typography

**Display Font:** system stack (`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif`)
**Body Font:** same stack

**Character:** One family, carried by weight and case. A deliberate house choice: it loads instantly in the Facebook in-app browser and reads as a contractor's sign, not a boutique.

### Hierarchy
- **Display** (900, clamp 31-96px, 0.96, -0.02em, uppercase): hero headline only, two block lines, second line gold.
- **Headline** (900, clamp 30-54px, 1.0, -0.01em, uppercase): section h2. The close h2 runs larger (clamp 34-80px).
- **Title** (900, 21px, 1.25): step titles, sent-panel heading. Sentence case.
- **Row** (800, clamp 19-23px, 1.2): service rows.
- **Lead** (400, clamp 17-20px, 1.5, max 36-38ch): hero promise and close line on the wall.
- **Body** (400, 17px, 1.55): everything else; secondary notes at 16px, footer fine print 15px.
- **Label** (800, 17px): form labels/legends and button text. "(optional)" drops to 600 in ink-soft.
- **Numerals** (900, 48px, 0.9, gold): step numbers.
- **Wordmark**: "RYAN" 900 with 0.05em tracking (24px phone, 30px desk); "HARDWOOD FLOOR LLC" 800, 10-11.5px, 0.14em tracking, gold. This is the logo lockup from the flyer, not a reusable label style.

### Named Rules
**The Shout-Then-Talk Rule.** Uppercase is for h1/h2 and the wordmark only. Everything else is sentence case.

**The Tabular Phone Rule.** Phone numbers in the header use `font-variant-numeric: tabular-nums`.

## Layout

Single column on phones with a 16px gutter (40px at 900px and up), centered max width 1240px. Forms and the sent panel cap at 640px. Section vertical padding is 64px top on phones, 96px at 900px+; the close section opens at 72px / 110px.

Responsive steps: below 400px the wordmark shrinks and the header phone icon hides so the number never wraps; at 640px hero/close buttons sit side by side; at 900px service rows split into two columns (56px gap) and steps go to three columns.

The hero fills `100svh`: header, copy, baseboard, then a floor that flexes to fill the rest (minimum `max(230px, 34svh)`). Floor strips under other wall sections are `clamp(120px, 22vw, 170px)` tall.

Story order (fixed by the contract): wall hero, services (light), how it works (wall + floor), quote form (light), close (wall + floor), footer (deep wall).

## Elevation & Depth

Flat UI. No card or button shadows. Depth is only physical and belongs to the room: the baseboard casts a soft shadow onto the floor, and the floor canvas carries its own lighting (a dark falloff under the baseboard, a warm radial highlight from upper left, a slight right vignette).

### Shadow Vocabulary
- **Baseboard cast** (`box-shadow: 0 7px 12px -3px rgba(24,14,6,.5)`): baseboard onto floor only.
- **Form halo** (`box-shadow: 0 0 0 3px rgba(45,108,223,.18)`): input/chip hover and focus, paired with the blue border.

### Named Rules
**The Only-The-Room-Has-Depth Rule.** Shadows belong to the baseboard and floor. Interface elements stay flat; state is shown by color and outline.

## Shapes

Softly rounded controls: 12px on buttons and the sent panel, 10px on inputs, chips and the message box. The service arrow is a 42px circle. Borders are 2px on buttons, inputs, chips and the sent panel; 1px hairlines divide service rows. The brand mark is the flyer's roof with chimney and four-pane window, drawn in SVG, reused as favicon.

## Components

### Header
- Wordmark left (links to top), phone number top right as a `tel:` link with a gold phone icon, warm plaster text turning gold on hover. 44px minimum hit area. No nav menu, and the header is not sticky.

### Buttons
- **Shape:** gently rounded (12px), 2px gold border, 58px tall, 800 weight, optional 20px leading SVG icon.
- **Fill:** gold ground, ink text. Hover goes to gold-deep. Used for the one primary action per screen ("Text for a free estimate", "Text my request").
- **Line:** transparent with gold border, plaster text, on the wall. Hover adds a 14% gold wash.
- **Ink line:** inside the sent panel, border and text switch to ink on light ground, 52px tall.
- **In the form:** submit gets a 3px blue outline on hover/focus, matching the fields.
- Transitions: background, color, border at 0.2s.

### Service Rows
- Full-width links with a hairline beneath, label left, 42px circular arrow right (ink at 8% alpha at rest). Each opens an SMS with a prefilled body naming the service.
- **Hover / Focus:** only the arrow disc turns gold (0.2s). The row itself gets no background, underline or shadow. Keyboard focus adds a 3px ink outline around the arrow.

### Steps
- Ordered list: gold 48px numeral spanning two rows, title, and a soft-plaster line capped at 40ch. One column on phones, three at 900px+.

### Inputs / Fields
- **Style:** paper ground, 2px hairline border, 10px radius, 54px minimum height (textarea 110px, vertical resize), 17px text. Label above in 800 weight.
- **Hover and focus:** border goes form blue with the 3px blue halo. The same treatment on hover and focus is intentional.
- **Error:** border turns error red; message below in error red, 700, 16px, announced politely. Errors clear on input.

### Chips
- Checkbox/radio labels styled as 48px paper pills (10px radius), 2px hairline border, 700 weight, wrapping with 10px gaps.
- **Hover / focus-visible:** blue border and halo. **Checked:** ink fill, paper text; keeps the blue border when hovered or focused.

### Sent Panel
- Fallback shown after submit in case the messages app does not open: paper card (12px radius, 2px hairline), title, a line with the phone link, the composed message in a daylight-slate box, and an ink-line "Copy message" button with inline success text. Receives focus when shown.

### Footer
- Deep wall ground. Wordmark, a one-line description, phone and Facebook links (plaster text, gold underline at 60%, gold on hover, 44px targets), copyright. Bottom padding respects the safe-area inset.

### The Room (signature)
Every wall section ends in **wall, then baseboard, then floor**.
- **Baseboard:** 24px white trim with a highlight edge and a cast shadow onto the floor.
- **Floor canvas:** procedurally painted oak planks with shared plank layout across three layers: **worn** (desaturated grey, scuffs, scratches) on top, **bare** (pale sanded oak) under it, **finished** (amber oak) at the base. Planks are 52px wide on phones and 64px at 900px+, with grain lines, cathedral figure, seams and lighting.
- **Sanding:** a round brush (0.62 of a plank's width) removes the worn finish and exposes bare wood. Bare wood cures to finished oak in about 3s; the worn finish creeps back over about 25s. Sawdust particles spray from the brush and settle.
- **Autoplay sander:** runs along the grain, one plank row per pass, reversing at each edge, and resumes 3.2s after the last touch. Each floor starts with a stretch already sanded so before and after both show.
- **Touch:** the hero floor uses `touch-action: none` (it is a sanding surface); strips use `touch-action: pan-y` so the page still scrolls through them.
- **Tuning:** change behavior only through the `T` object (plank widths, cell size, brush, bite, regrow, cure, sander speed, idle resume, dust cap, DPR cap).

### Motion
- UI transitions are short color changes only: 0.2s on buttons and arrows, 0.15s on fields and chips. No entrance animations, no scroll effects.
- The floors animate only while on screen (IntersectionObserver, 200px margin) and the tab is visible; strips build when first scrolled near.
- `prefers-reduced-motion`: the floors paint once (pre-sanded still) and never animate; smooth scrolling is turned off.

## Do's and Don'ts

### Do:
- **Do** end every wall section with a baseboard and a floor strip.
- **Do** keep gold for trim and the single fill action per screen; use blue only for form-control outlines.
- **Do** keep the system font stack with 900-weight uppercase h1/h2 and sentence-case everything else.
- **Do** keep touch targets at 44px or more and primary buttons at 58px.
- **Do** keep the hero floor `touch-action: none` and strips `pan-y`.
- **Do** route new contact actions to `sms:` / `tel:` (973) 493-2410, with a prefilled SMS body where it helps.
- **Do** use only facts in PRODUCT.md; put gaps in HANDOFF.md, never on the page.

### Don't:
- **Don't** use black or near-black grounds; the darkest ground is the deep wall.
- **Don't** add a sticky header, sticky call bar or floating button.
- **Don't** show the phone number more than once per screen (header, sent panel and footer are each on their own screen).
- **Don't** add an email address; none exists. If one is ever confirmed, it goes in the footer only.
- **Don't** invent towns, hours, prices, reviews, years, credentials or owner names.
- **Don't** use photos until the owner supplies real work photos; the flyer image is not proof of work.
- **Don't** highlight a whole service row on hover; only its arrow changes.
- **Don't** add shadows to cards, buttons or fields; depth belongs to the room.
