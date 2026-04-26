# Agent-Oman — Final Locked Brand Specification

**Status:** FINAL LOCKED · 2026-04-26
**Owner:** Acuterium Technologies Inc.
**Classification:** TS//SOVEREIGN — Acuterium brand asset

---

## 1. Identity

| Field | Value |
|---|---|
| Brand name (English) | **Agent-Oman** |
| Brand name (Arabic)  | **وكيل عُمان** |
| Tagline              | **POWERED BY ACUTERIUM OCF** |
| Parent platform      | Acuterium OCF (Orchestrated Cognition Fabric) |
| Doctrine             | COSM (Consciousness-Orchestrated Sovereign Management) |
| Symbol               | 8-pointed Islamic star (نجمة ثُمانية) |

The 8-pointed star (the *Khatim Sulaymani* / Seal of Solomon) carries 1,400 years of Islamic geometric heritage and is the canonical motif of GCC sovereign design. It is reframed here as a *consciousness gate*: outer crystalline rays (perception), inner circuit core (cognition), white luminous center (sovereign intelligence).

---

## 2. Asset Inventory

| ID  | Filename | Variant | Background | Use Case |
|-----|----------|---------|------------|----------|
| 041 | `agent_oman_logo_full_dark.jpg`             | Full lockup | Dark (#000000) | Splash, hero, social cards, presentations |
| 042 | `agent_oman_logo_full_dark-transparent.jpg` | Full lockup | Transparent    | Embed on dark backdrops, dashboards |
| 043 | `agent_oman_logo_icon.jpg`                  | Icon only   | Dark (#000000) | App icon (iOS/Android), favicons fallback |
| 044 | `agent_oman_logo_icon-transparent.jpg`      | Icon only   | Transparent    | Overlay, favicon, watermark, header |

**Canonical paths:**
- `MAJD-AI78/acuterium-logo-registry` → `agent-oman/brand/`
- `MAJD-AI78/Agent-Oman`              → `brand/`
- `Acuterium-Technologies/Agent-Oman` → `brand/`

---

## 3. Color Tokens — `--ao-*` (Agent-Oman)

```css
:root {
  /* Primary — emerald sovereignty (outer rays) */
  --ao-emerald:        #10B981;
  --ao-emerald-glow:   #34D399;
  --ao-emerald-deep:   #059669;

  /* Accent — Oman-flag red (inner core, sovereignty signal) */
  --ao-oman-red:       #DC1F26;   /* matches Sultanate of Oman flag */
  --ao-oman-red-deep:  #9B0E13;
  --ao-oman-red-glow:  #FF4548;

  /* Sovereign white — central intelligence luminance */
  --ao-sovereign:      #FFFFFF;
  --ao-sovereign-soft: #F0F0F0;

  /* Gold — circuit traces, framing, premium rails */
  --ao-gold:           #C9A84C;
  --ao-gold-soft:      #E5C87A;

  /* Backdrop — dark sovereign canvas */
  --ao-bg-deep:        #000000;
  --ao-bg-panel:       #0A0F0E;
}
```

### Usage Map

| Token | Where it appears |
|---|---|
| `--ao-emerald`       | Primary actions, ConsciousnessOrb outer ring, success states, links |
| `--ao-oman-red`      | Sovereign-tier UI (Royal Decree refs, sovereign queries), critical states, PATHOS stress > 70 |
| `--ao-sovereign`     | Central glyphs, headline accent, intelligence-active pulse |
| `--ao-gold`          | Trace lines, decorative borders, PATHOS focus axis, mashrabiya overlays |
| `--ao-bg-deep`       | Default canvas (Commercial Edition / Defense) |
| RUZN-light backdrop  | Government Edition pages keep RUZN.AI's `#B8D4E8` palette (Agent-Oman icon overlays in emerald) |

---

## 4. ACAI V2 Theme Slot

Agent-Oman registers a **6th edition theme** in ACAI V2:

```ts
// acai-v2/theme/editions.ts
export type ACAIEdition =
  | 'commercial'       // dark — majd.chat, finarah, bizelev
  | 'government'       // light blue — ruzn.ai
  | 'defense'          // dark + scanlines — erebus dashboards
  | 'agent-oman';      // dark + emerald-red sovereign — agent-oman.acuterium.ai

export const AGENT_OMAN_EDITION = {
  edition:    'agent-oman',
  parentMode: 'AUI Glass',           // uses glassmorphic AUI base
  particles:  45,                     // emerald + occasional red sparks
  aurora:     'emerald-red-radial',   // radial gradient from red core to emerald rim
  defaultLanguage: 'mixed',           // Arabic-first, English co-equal
  rtl:        true,                   // RTL when Arabic active
  prayerTimes: true,                  // CHRONOS prayer-time adaptation
};
```

---

## 5. Typography Lock-in

| Role | Latin | Arabic |
|---|---|---|
| Wordmark    | Custom geometric (rendered in raster — do not retype) | Custom Kufi (rendered in raster — do not retype) |
| Headlines   | Cinzel (serif, sovereign feel)            | Noto Kufi Arabic 700 |
| Body        | Inter 400/500                              | Noto Kufi Arabic 400 |
| Tagline     | Inter 500, tracking +200, UPPERCASE        | n/a |
| Telemetry   | JetBrains Mono                             | n/a |

---

## 6. Clear-space, Sizing, Don'ts

- **Clear space:** ≥ 1× icon-height padding on all sides
- **Minimum size:** Icon at 32 px (favicon), full lockup at 200 px wide
- **Never:** recolor the star, separate the Arabic from English, place on busy photo backgrounds without scrim, rotate, skew, or apply drop shadows beyond the existing inner glow
- **Always:** preserve the red-emerald-white-gold ratio. The red core is non-negotiable — it is the sovereign signal.

---

## 7. Provenance

These four assets are the **single source of truth** as locked by Dr. Jalal Saleh AlHadhrami, Founder & Chairman, on **2026-04-26**. Any future variant (light backgrounds, monochrome, vector SVG, motion lottie) must be derived from these masters and registered with new IDs in `acuterium-master-logo-index.{csv,json}`.

— *Acuterium Technologies Inc. — Every interface is a sovereign statement.*
