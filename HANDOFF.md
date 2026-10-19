# Ryan Hardwood Floor LLC — handoff at ~60%

**Live:** https://10elizabethbell.github.io/ryanHardwoodFloor/ · **Repo:** https://github.com/10elizabethbell/ryanHardwoodFloor · **Built:** 2026-10-18 from Muse brief (run 2026-10-18, Facebook group ads)

## What's built
- One page, single `index.html`, phone first. Order: header (logo, (973) 493-2410 top right) → hero → What we do → How it works → Get a free estimate form → closing section → footer.
- **World:** inside a New Jersey home. Slate-navy painted walls, a white baseboard, oak plank floors. Gold trim comes from the roof mark on their flyer. Light sections are the same room in daylight (pale slate).
- **Signature element:** a canvas hardwood floor you sand. It starts as a worn, grey, scuffed finish. Each pass of a finger or mouse leaves pale bare wood that warms into finished oak within about 1.5s, with sawdust thrown off. A sander runs along the grain by itself until you touch it, then picks up again after about 3s idle. The worn finish creeps back over about 25s. The hero floor takes drags in every direction without scrolling (pull-to-refresh is off). Two more floor strips sit at the base of the "How it works" and closing walls; those sand on hover or a sideways drag, and a vertical drag scrolls as normal.
- **Contact:** everything goes by text or call to (973) 493-2410. The hero has two buttons: Text for a free estimate (pre-filled text) and Get a free quote (jumps to the form). Each service row opens a text with that service named. The form (name, town, services, optional size/when/notes) validates inline and composes one text message. Its fallback shows the message with a Copy button and a call link.
- The closing section ("Love your floors again.") carries only the Facebook button ("Click to see more of our work"); its Text button was removed so two Text buttons are never in view at once. Facebook is also in the footer.
- og image (`og.jpg`, 1200x630) and favicon/home-screen icon drawn from the flyer's roof-and-window mark.
- Tunables sit at the top of the floor script (`T`): REGROW, CURE, BITE, BRUSH, SANDER_SPEED, IDLE_RESUME, plank widths.

## Assumptions I made
- **"We" voice.** It's an LLC and crew size is unknown. Switch to "I" if it's one person.
- **Hero promise** ("We treat your home like our own, and we don't call a floor finished until you love walking on it.") is my wording about how they treat customers, not their quote. It needs the owner's OK. The How it works steps use only brief facts (call or text, free estimate).
- **Headline** is their own flyer slogan: "Beautiful floors. Built to last."
- **Colors:** the flyer is black and gold. Black isn't allowed as a page ground, so I chose slate-navy (#1c2a37) with their gold (#d6a94e).
- **Logo:** redrawn as SVG from the flyer (gold roof, chimney, four-pane window, "RYAN / HARDWOOD FLOOR LLC"). No original logo file exists.
- **Services:** split into six short items from the caption's wording: hardwood installation, sanding & refinishing, staining, vinyl (LVP) & laminate, floor repairs, stair refinishing.
- **Audience:** treated as general NJ homeowners, so the page has motion. If Ellie thinks they skew 40+, switch to the still version (`older-audience.md`).

## Placeholders and gaps
- **No photos of their work at all.** The flyer is an AI-made ad (stock-style couple, not Paulo, not a real job), so I left it out. Proof is the top need: 3–6 real floors, ideally before/after pairs, which would slot into a proof section above the closing wall.
- **Facebook link goes to Paulo Lopes's personal profile** (brief fallback, id 100004622314386). Its avatar is a family photo with a child. Ellie should decide whether to keep it or wait for a business page.
- No email (footer has none), hours, towns, reviews, prices, years in business, or license/insurance info, so the page says nothing about them. "Serving New Jersey" is the only area line.
- Owner identity unconfirmed: the page names no person.

## Questions for the owner
- Can you send photos of recent floors, especially before and after?
- Which towns or counties do you cover?
- Is it "I" or "we"? Who answers the phone (Paulo? Ryan?)
- Do you have a business Facebook page, Instagram or Google listing to link instead of the personal profile?
- Licensed/insured in NJ? Years in business? Any reviews we can quote?
- Hours, and is there an email for the footer?
- Which services bring the most work, so they can go first?

## Ideas not built (yours to pick)
- **Runner-up world: stain wiped on with a rag.** Drag to deepen raw oak into a chosen stain color, with a swatch picker (natural, golden oak, walnut, ebony) that doubles as a "what color do you want?" field in the form.
- Other worlds considered: wet poly being rolled on (gloss line following the roller), planks clicking into place (install), sawdust in a window sunbeam, stair treads.
- Before/after sliders once real pairs exist (round frame, plain gold divider).
- A stain-color question in the form.
- A small "drag to sand" hint near the floor if testers don't discover it (autoplay currently teaches it).
- A visible drum sander riding the autoplay path, and a slight floor perspective / raking window light (finish reviewer's ceiling notes).
- After the form is sent, run one sander pass on the closing floor strip as a "done" moment.
- On desktop the right side of the hero wall and the form column is empty. Fill it with real work photos once they arrive.

## Impeccable sweep (done)
- Ran every mode except live, plus the finish reviewer and the detector; onboard and extract don't apply. Applied:
  - one left edge on desktop
  - frame-rate-independent sanding
  - a darker focus ring on the light sections
  - more of the floor pre-sanded, with ragged ends
  - matte bare wood and settling tan dust
  - softer wear stains
  - truthful How it works copy
  - one Text button per screen
  - polite error announcements
  - the form fallback shown before the text app opens
  - lazy-built floor strips and a debounced resize
  - a larger tagline on small phones
- **Skipped:**
  - Renaming "Get a free quote": Ellie's text + free-quote button pair.
  - Removing the optional size field.
  - A drawn sander and floor perspective: listed in ideas.
  - The concept-roll seed: the build ran unattended, so no roll happened.
- Detector: only Roboto left, as the system-stack Android fallback. It's suppressed in `.impeccable/config.json` with the reason recorded.

## Not verified
- Real-device touch on iPhone Safari and inside Facebook's in-app browser (tested with Playwright WebKit plus Chromium CDP touch events).
- Real SMS handoff on iOS/Android (body encoding verified by decoding the links).
- Frame rate on older phones (canvas is capped at 1.5x DPR, one shared loop that pauses off screen).
