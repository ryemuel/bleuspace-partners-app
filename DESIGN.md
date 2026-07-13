# Bleuspace — DESIGN.md (canonical brand contract)

> **What this is:** the machine-readable brand contract for building any Bleuspace
> digital surface. Drop it (or copy it) into a build root as `DESIGN.md`; the build
> agent conforms every token, component, and motion to it. Format per
> `templates/design-md.md`. Reasoning layer behind it: `context/brand-craft/` +
> `context/bespoke-standard.md`. Asset truth: the brand kit
> ([[bleuspace-brand-identity]] memory) + the approved build.
>
> **Source of truth:** asset library `/Users/ryemuel/Desktop/Bleuspace Branding/
> 01 Brand Assets/Digital Assets`; approved build
> `outputs/drafts/brand-evolution/index.html` (v6 warm-restraint, owner-approved
> 2026-06-13). Live site facts: [[reference_bleuspace_operating_stack]].
>
> **Direction lock:** warm professional · refined RESTRAINT (Aman / Janu / Flora-
> feel) · warmth + palette as WHISPERS, never colour-blocks · photography-led ·
> the keyhole as the through-line. This is the canon; deviations need an owner
> ruling, not a builder's preference.

**Brand:** Bleuspace Properties · **Date:** 2026-06-14 · **Author:** Eve concept → Stu/Lum tokens (from approved build) · **Revision:** v6-derived (1 of N)

---

## 1. Concept Trace — the un-liftable idea

- **The one concept:** **"the keyhole is the grid."** A precise, disciplined
  *container* (Aman/Aesop restraint = the reliability signal) housing warm,
  imperfect, hospitable *soul*. Reliability = what repeats identically;
  hospitality = what varies with care.
- **The signature element:** the **keyhole-B** — a keyhole (circle + tapered
  trapezoid) cut into the "B" = access / "your space" / the key to a home — used
  as an **aperture with a real interior framed inside it**; echoed structurally
  as circular apertures. A fluid double-"S" ligature is the one warm non-geometric
  stroke. Only Bleuspace can use this.
- **Swap test:** drop Sonder/Airbnb/a generic STR brand in → it **breaks** (the
  keyhole motif, the Filipino voice "Mabuhay…Salamat po", and the warm-restraint
  earth palette are all un-liftable). ✅ bespoke.
- **Governs everything:** every load-bearing choice serves *standard of a hotel,
  soul of a residence* — precise container, warm soul.

## 2. Visual Theme & Atmosphere

**Warm restraint** — *competence you can feel cared for by* ("professional
warmth": warm like a host, reliable like an institution). Big beautiful
photography, tiny elegant type, calm, generous whitespace that is **framed and
intentional** (premium ≠ empty). Deliberately NOT: cold-corporate minimal, NOT
loud/cheap colour-blocks, NOT generic-luxury cliché.

## 3. Colour Palette & Roles

> Graded to ONE muted warm register (v6 colour-theory regrade). Palette colours
> appear only as **gentle accents — never blocks.** CSS var names match the build.

```
{colors.canvas}        "#F4E9D7"   (--paper)     # warm ivory ground — THE differentiator; linen-textured
{colors.surface}       "#FBF4E8"   (--cream)     # cards / raised panels
{colors.surface-dark}  "#3A291E"   (--choco)     # grounded bands (Bleu concierge); --choco-dk "#2A1D14"
{colors.ink}           "#2E2218"   (--ink)       # primary text (warm near-black)
{colors.ink-soft}      "#6F6150"   (--soft)      # secondary text
{colors.line}          "rgba(43,36,30,.15)" (--line)  # hairlines
{colors.primary}       "#BC6A47"   (--clay)      # terracotta clay — THE accent: CTAs + signature; hover --clay-dk "#9E5436"
{colors.secondary}     "#1E4E63"   (--navy)      # petrol/teal-navy — the "Bleu" thread (search btn, footer, numbers); hover --navy-dk "#163C4D"
{colors.support-honey} "#CC9A52"   (--mustard)   # accent only
{colors.support-sage}  "#99A286"   (--sage)      # bridge / image placeholder
{colors.support-dusty} "#6E97A3"   (--dusty)     # accent only
{colors.brand-mist}    "#B2C3D6"   (--mist)      # Harbor Mist — logo on navy/choco grounds
```

- **Role intent:** ivory canvas = the warm differentiator (pure white reads
  "any other PMS/STR site"). Clay is the **single warm accent** — reserved for
  primary CTAs, the italic emphasis word, thin rules, kickers. Navy is the
  restrained **"Bleu" nod** (the brand's name equity), warm-dominant. Honey/sage/
  dusty are whispers only. Earth tones live in illustration, not UI blocks.
- **Contrast:** ink `#2E2218` on canvas `#F4E9D7` and clay/navy on white pass
  WCAG 2.1 AA. Verify any new pairing (`digital-accessibility-standard.md`).

## 4. Typography

```
{type.display}  "Cormorant", Georgia, serif        (--serif)  # headlines ONLY; weight 300; italic for emphasis; tracking -.01em
{type.body}     "JUST Sans", Helvetica Neue, Arial  (--sans)   # body + UI; weights 300 / 500 / 600
{type.mono}     "Inconsolata", ui-monospace         (--mono)   # signature micro-labels: section kickers, numbered steps, Bleu terminal
```

**Scale (real, fluid):**

| Token | Size | Weight | LH | Use |
|---|---|---|---|---|
| `display-hero` | `clamp(3rem,7.2vw,6.4rem)` | 300 | 1.0 | hero h1 (max 15ch, tracking -.01em) |
| `h2` | three real sizes: collection `clamp(2.1rem,4.4vw,3.4rem)` · how/model `clamp(2.2rem,4.6vw,3.6rem)` · difference `clamp(2.3rem,5vw,4rem)` | 300 | 1.05–1.08 | section heads — pick by section weight, don't pin one |
| `h3` | `1.45–1.55rem` | 400 | 1.12–1.14 | pillar / card name |
| `body` | `clamp(15px,1.02vw,16.5px)` | 300 | 1.75 | paragraph |
| `lead` | `clamp(1.4rem,2.6vw,2rem)` | 300 *italic* | 1.2 | pull-quote (serif italic) |
| `label-mono` | `.58–.72rem` | 500 | — | kicker / number; tracking .1–.16em; UPPERCASE |

- **Rules:** measure 45–80ch (subs ≤48ch). Cormorant is **display-only** — never
  body, never bold-display. "30%-less-editorial" pass: high-traffic UI (nav,
  buttons, search, card meta, filters, footer) is **sentence-case JUST Sans**;
  mono is kept as the *signature* on kickers, the Bleu terminal, and numbered
  steps only — do not spread mono back across general UI.

## 5. Spacing, Layout & Grid

```
{space.section}  "clamp(5.5rem,12vw,9rem)"   (--section)
{space.pad}      "clamp(1.5rem,5vw,4.5rem)"  (--pad)
{layout.max}     "1260px"                    (.container)
{radius.sm}       "3px"   (--r-sm · buttons, focus outline, burger bars)
{radius.md}       "8px"   (--r-md · business-model / Bleu engine / CLI panels)
{radius.btn-icon} "6px"   (--r-icon · CLI send / icon button / engine chips)
{radius.pill}     "100px" (--r-pill · chips / segmented)
{radius.disc}     "50%"   (--r-disc · dots, avatars, step circles, button spinner)
{radius.card}     "0"     (property cards are squared — editorial, not rounded-SaaS)
```

> Radius **and** shadow are now real CSS vars in the build's `:root` (`--r-*`,
> `--sh-card/lift/deep/deepest/nav`) — not loose literals. Use the token, never a
> raw value (a 2026-06-14 audit found `2px`/`5px`/an extra shadow had drifted in;
> tokenising them closed the gap).

Whitespace is framed and intentional; generous section rhythm; centred max-62ch
intro blocks for "difference"-type sections.

## 6. Depth & Elevation

Philosophy: **flat-warm first, shadow rare and soft.** Depth from the cream-on-
ivory surface contrast + texture, not heavy shadow.

```
{shadow.card}    "0 24px 60px rgba(42,36,32,.14)"   # search card / floating panels
{shadow.lift}    "0 14px 26px rgba(43,36,30,.12)"   # hover lift (steps)
{shadow.deep}    "0 30px 60px–0 34px 80px rgba(0,0,0,.22–.35)"  # dark inverted panels (Bleu engine / CLI)
{nav.scrolled}   "background rgba(247,239,227,.92); backdrop-filter blur(12px); box-shadow 0 1px 0 {colors.line}"
```

## 7. Shape & Texture

Squared cards (aspect-ratio 3/4 for property imagery), 3px buttons, pill chips.
**Signature texture:** real **linen fabric** (`assets/texture/fabric.jpg`, ~110KB)
under an `rgba(244,233,215,.83)` ivory overlay, 420px repeat, on body + cream
sections — colour reads as *textured paper/textile*, the residence truth. Search
card carries a 2px navy top-border (the one "Bleu" structural tell).

## 8. Components & States

| Component | Default | hover | focus-visible | active | disabled | empty | loading | error |
|---|---|---|---|---|---|---|---|---|
| button-primary | bg `{colors.primary}`, #fff, sans 600 .86rem, pad 1.05/1.9rem, `{radius.sm}` | bg `--clay-dk` | 2px solid `{colors.secondary}`, offset 3px | press | .5 opacity, no-pointer | — | spinner/skeleton | inline msg |
| button-navy | bg `{colors.secondary}` | bg `--navy-dk` | same | — | same | — | — | — |
| card (property) | cream, squared, img aspect 3/4 | `translateY(-5px)`, img `scale(1.05)` over 1.3s | outline | — | — | sage placeholder block | skeleton | "no results" empty-state copy |
| filter-chip | pill, 1px `{colors.line}`, `{colors.ink-soft}` | fill/active state | outline | active=filled | — | graceful "nothing in this filter" | — | — |
| nav | fixed, transparent over hero | — | link outline | — | — | — | — | mobile hamburger (working) |
| search-card | cream + 2px navy top, `{shadow.card}`, tabbed | field hover | outline | tab active = navy underline | — | — | — | — |
| input/field | label = sans .72rem `{colors.primary}` | border | outline | — | dimmed | placeholder | — | inline |

Named specs reference tokens only — never hard-code an off-system value.

## 9. Motion

- **Engine:** `context/motion-library.md` primitives (authored-on, never a lifted
  recipe).
- **Signature easing:** `cubic-bezier(.33,0,.16,1)` (`--ease`) — the one owned curve.
- **Signature behaviour:** quiet "breathing" — breathing keyhole marks, gentle
  nav-logo float, hover-lifts, slow (1.3s) card-image zoom. Motion is a *whisper*,
  matching the brand's calm (`feedback_brand_aligned_restraint`: living ≠ drama).
- **Reduced-motion (required):** `@media (prefers-reduced-motion: reduce){ * { animation:none!important } .reveal{opacity:1;transform:none;transition:none} }`.

## 10. Voice & UX Copy

**Tone:** warm, precise, hospitable, Filipino. *Professional warmth.* Real phrases:
- "Mabuhay." / "Salamat po."
- **"The standard of a hotel. The soul of a residence."**
- "Where every stay is an experience."
- "We don't aggregate. We don't host. We curate, we operate, and we obsess over every detail."
- "The warmth of a host. The precision of a profession."
- **Pillars:** AI Concierge 24/7 · Curated, never crowdsourced · Made for the Philippines · One brand, every duration.
- **The concierge has a name: Bleu** (animated keyhole avatar; For guests / For owners toggle).

CTAs = verbs of value. Real stats only: **4.95★ · 25 curated residences · 5,000+
Filipino guests · DOT-accredited · BIR-registered.** No fabricated yields/prices —
digital revenue model is owner-ruling-pending (`business-principles.md`); owner
economics stay conceptual ("share of revenue, terms set with your account manager").

## 11. Responsive Behaviour

| Breakpoint | Width | Changes |
|---|---|---|
| Desktop | > 900px | full nav; 3–4-up collection; multi-col sections |
| Tablet | 760–900px | tightened grid (2-up); nav condenses |
| Mobile | < 760px | **hamburger** nav; type steps down; 1-up stack |
| Small | < 600px | tighter pad; single-column everything |

Touch targets ≥ 44px. Mobile-first. Reduced-motion respected.

## 12. Do's & Don'ts

**Do**
- Anchor every page on the **ivory linen canvas** `{colors.canvas}` — the differentiator.
- Reserve **clay** `{colors.primary}` for primary CTAs, the italic emphasis word, kickers, thin rules.
- Lead with **real photography** (Guesty CDN, hotlinkable, `w_,q_auto,f_auto`).
- Keep the keyhole present — as logo, aperture, and the circular-disc echo.
- Treat warmth + palette as **whispers**; restraint is the brand (Aman/Janu).

**Don't**
- Don't use pure white as canvas, or cool grays — it reads generic-SaaS.
- Don't colour-block the palette (the v4 failure — "too loud / cheap").
- Don't go cold-minimal single-accent either (the v3 failure — "too cold").
- Don't set Cormorant as body or bold it; don't spread mono across general UI.
- Don't fabricate stats/prices/yields; don't reuse the old file illustrations.
- Don't pass the swap test; don't lift a packaged DESIGN.md or a motion recipe.

## 13. Agent Prompt Guide (paste-ready)

**Tokens at a glance:** canvas `#F4E9D7` · surface `#FBF4E8` · ink `#2E2218` ·
clay `#BC6A47` · navy `#1E4E63` · choco `#3A291E` · serif **Cormorant** · sans
**JUST Sans** · mono **Inconsolata** · easing `cubic-bezier(.33,0,.16,1)`.

**Ready prompt:**
> "Build [section] for Bleuspace. Ground on ivory linen `#F4E9D7`; one accent —
> clay `#BC6A47` — for the CTA / kicker / italic word only; navy `#1E4E63` as the
> restrained 'Bleu' thread. Headlines Cormorant 300 (display only); body + UI
> JUST Sans; mono Inconsolata for kickers/numbers only. Lead with real Guesty
> property photography. Section rhythm `clamp(5.5rem,12vw,9rem)`, container max
> 1260px. Motion is a quiet breathing whisper on `cubic-bezier(.33,0,.16,1)`,
> reduced-motion-safe. Conform to this DESIGN.md — no off-system colours/fonts,
> no stock heroes, no colour-blocks. The concept it serves: *the keyhole is the
> grid — precise container, warm soul; the standard of a hotel, the soul of a
> residence.*"

## 14. Iteration Guide

- New components inherit existing tokens; add a token only when a real new role
  appears (justify it here).
- Dials the owner may turn: exact photo→unit mapping; how far earth tones are
  demoted; texture intensity; the navy/"Bleu" dosage.
- Refine via the loop: rate → diagnose the failing *layer* (concept / palette /
  type / motion / structure) → rebuild only that layer → re-rate, target ≥ 9
  (`feedback_creative_conviction`). Never show unrendered work
  (`feedback_no_blind_visuals`).

## 15. Known Gaps

- Only the home page exists in the approved build; inner pages (listing detail,
  owner, booking flow) not yet designed against this contract.
- Photo→unit pairing is approximate (real interiors, pairing not guaranteed).
- Asset paths in the build are local; production hosting paths to be set.
- The Bleu concierge is a client-side intent engine, not yet wired to a real LLM.
- The official 10-colour kit and this v6 warm-graded register are reconciled here
  as **canon = v6** (the kit, warmed/graded + the "Bleu" thread retained); if the
  owner re-opens the palette, update §3 and re-verify contrast.

---

*Canonical as of 2026-06-14, derived from the owner-approved v6 build. "Bespoke"
is earned on `bespoke-standard.md` §IV, not asserted. Concept-first, real-asset,
verified-in-runtime — or it does not ship.*
