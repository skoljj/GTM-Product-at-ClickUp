# GTM Capability Architecture — Project Hub

> **Owner:** JJ (VP Marketing)  
> **Purpose:** Interactive visual system articulating a new paradigm for GTM enablement — "Capabilities as a Product" — built to impress executive audiences and reframe how companies think about revenue team performance.  
> **Stack:** Single-file HTML, Three.js (r128 CDN), vanilla CSS/JS. No build tools. Deploy via Vercel + GitHub.

---

## 🧭 Quick Orientation for Claude Code

This repo contains two flagship HTML artifacts and the conceptual scaffolding to build more. Everything here was developed iteratively in Claude.ai chat over dozens of sessions. This README is the **complete context transfer** — read it before touching any code.

---

## 📁 Project Structure

```
gtm-capability-architecture/
├── README.md                          ← YOU ARE HERE (context bible)
├── src/
│   ├── product_design_concept1.html   ← 3D Three.js capability architecture
│   ├── product_thesis_and_concept_flyover.html  ← 7-section scrollable framework
│   ├── product_design_concept1_mobile.html      ← Mobile-optimized 3D version
│   └── product_thesis_and_concept_flyover_mobile.html ← Mobile-optimized framework
├── docs/
│   ├── ARCHITECTURE.md                ← Conceptual architecture explained
│   ├── DESIGN_SYSTEM.md               ← Colors, typography, component patterns
│   └── NARRATIVE.md                   ← The "old game / new game" thesis
├── concepts/
│   └── (future "old game vs new game" visuals go here)
└── vercel.json                        ← Deployment config
```

---

## 🏗️ The Two Flagship Artifacts

### 1. `product_design_concept1.html` — 3D Capability Architecture
- **What it is:** Full-screen interactive Three.js visualization. Three vertical layers (Contributor → Product → Agent) with orbital data centers, particle systems, animated agent characters, and connection beams.
- **Interaction:** Pointer-drag to orbit 360°, scroll to navigate layers, ctrl+scroll to zoom, pinch-to-zoom on mobile. Nav dots on right side jump between views.
- **Key 3D elements:**
  - **Contributor Layer (top):** 38 buildings organized in 6 districts (Commercial, Enterprise, Partnerships, Post Sales, XDR, Operations) on a dark platform with cyan grid. Fountain + apex orb at center. ClickUp chevron glyph floats above.
  - **Product Layer (middle):** Transparent disc with three sub-layers:
    - *API Layer (ceiling):* 5 disc-stack pods representing LLM partners (Claude, GPT-4, Gemini, Llama, Mistral) + outward-radiating beams
    - *Codebase (core):* Central room with cursor animation, particle field, glowing core
    - *MCP Layer (floor):* 4 gear mechanisms (Salesforce, Gong, ClickUp, Figma)
  - **Agent Layer (bottom):** 6 humanoid agent characters with pulse rings lined up along all 4 walls. Activity cubes (capability cabinets) with particle systems. Lab and Studio visual blocks.
  - **Orbital:** 6 data center arrays orbiting the stack. Connection beams linking all layers.
- **Sidebars:** Three collapsible sidebars (API Layer, Codebase, MCP Layer) with partner logos and descriptions. Auto-show/hide based on camera Y position.
- **Stats bar:** Fixed bottom bar showing building count, IC count, product disc, MCP count, API count, agent tiles, super agents, data centers.
- **Mobile:** Responsive CSS added for 768px/480px breakpoints. Pinch-to-zoom via touch events. Sidebar drawers at 70vw.
- **CDN dependency:** Three.js r128 from cdnjs.cloudflare.com (required for render).

### 2. `product_thesis_and_concept_flyover.html` — 7-Section Framework Scroll
- **What it is:** Long-scroll dark-theme document with 7 sections, sticky nav, scroll-reveal animations, and interactive data visualizations.
- **Sections:**
  1. **Framework (HI^AI = V):** Hero with formula, trio cards (Human Intelligence / AI / Value), equation block, operating principles. The conceptual foundation.
  2. **Knowledge Vault:** HQ/AQ dual-column (Human Quotient vs AI Quotient), vault instance example, scale visual, consumer cards, feedback loop. The per-person capability record.
  3. **Product Architecture:** Design system inheritance (Figma → GTM), AI model APIs, core engine (RAG → Orchestrator → MCP → Tools), ClickUp platform, analytics. How capabilities are built and delivered.
  4. **Bowtie Funnel:** Full bowtie with SVG visualization, stage cards, motion tags (PLG/Commercial/Enterprise), conversion rate cards with action layer connections. How capabilities map to revenue stages.
  5. **Opportunity Seeker:** Interactive firmagraphic filters, funnel visualization with animated fill bars, readout grid, insight cards. Dynamic data exploration.
  6. **Action Layer (FLM):** Large SVG dashboard visualization. The frontline manager's operating surface.
  7. **3D Architecture (embedded):** The Three.js visualization from file 1, embedded as a scrollable section with scoped canvas.
- **Typography:** DM Sans (body), Instrument Serif (section titles), IBM Plex Mono (labels/code), Playfair Display (hero/formula), Outfit (secondary).
- **Color system:** ~60 CSS custom properties. Key palette: bg #0c0e13, text #e4e7ee, accent #D0D8EC, action #34d399, vault #f59e0b, selection #60a5fa, awareness #a78bfa, impact #f87171, grow #f472b6.
- **Mobile:** Hamburger menu added for nav. All grids collapse to single column. Bowtie stage cards become horizontally scrollable. SVG panel gets overflow scroll.
- **Scripts:** IntersectionObserver for scroll reveals. Active nav highlighting on scroll. Section 5 has interactive filter state machine (JS). Section 5 has dynamic roster rendering.

---

## 🧠 The Conceptual Architecture

### The Core Formula
```
applied Human Intelligence ^ applied Artificial Intelligence = actual Value
```
Or equivalently:
```
Human Quotient × AI Quotient = Real Outcome
```

This is NOT addition. It's exponentiation. The quality of human input (base) amplified by the sophistication of AI application (exponent) produces value that neither achieves alone.

### The Three-Layer Stack (visualized in 3D)
1. **Contributor Layer** — The humans. Organized by GTM function (Commercial, Enterprise, Partnerships, Post Sales, XDR, Ops). Each "building" = a capability unit. Buildings have floors (team members), districts (functions), and quadrants (Actions, Decisions, Exposure, Authorship).
2. **Product Layer** — The system. APIs on top (LLM partners), codebase in middle (the engine), MCP on bottom (tool connections to Salesforce, Gong, ClickUp, Figma). This is where capabilities are *engineered*, not just written.
3. **Agent Layer** — The AI workforce. Autonomous agents that execute against prescribed capabilities. Capability cabinets store the playbooks. Lab and Studio are where new capabilities are developed and tested.

### The Knowledge Vault (visualized in Section 2)
Every GTM team member gets a personal **vault**:
- **Human Quotient (HQ):** What was *given* to them (training, playbooks, certifications) → What they *did* with it (Gong/SFDC/ClickUp behavioral evidence) → Where the *gaps* are
- **AI Quotient (AQ):** Agentic skills *prescribed* to close those gaps (coaching intelligence agent, deal strategy assist, content generation agent, etc.)

### The Bowtie (visualized in Section 4)
Full revenue lifecycle: Awareness → Education → Selection → Commit → Onboarding → Impact → Growth. Three motion types per stage: PLG (self-serve), Commercial, Enterprise. Conversion rates between stages are the operating metrics. Each stage has an "Action Layer Connection" describing how AI capabilities intervene.

---

## 🎯 THE "OLD GAME / NEW GAME" THESIS

This is the **next artifact to build.** The entire framework above implicitly argues against traditional enablement, but we need an explicit visual that makes the contrast visceral.

### Old Game: Traditional Enablement
- **Model:** Content delivery. Ship training, playbooks, decks. Pray for adoption.
- **Measurement:** Completion rates, satisfaction scores, content consumption.
- **Architecture:** LMS + content library + occasional coaching.
- **Failure mode:** "78% consumed the playbook. 12% applied it." No feedback loop. No gap detection. No prescription. No compounding.
- **Metaphor:** Warehouse — you build shelves of content and hope people come browse.

### New Game: Capabilities as a Product
- **Model:** Product engineering discipline. Ship capabilities (not content) through an architecture (not a library). Measure adoption, application, and impact (not consumption).
- **Measurement:** Behavioral change (Gong patterns), pipeline impact (SFDC), capability adoption rates, gap closure velocity, conversion rate movement by stage.
- **Architecture:** Knowledge Vault (HQ/AQ per person) → Orchestrator → MCP tool connections → AI agents that prescribe and execute → Feedback loop that adjusts the roadmap.
- **Success mode:** "Discovery gap detected via Gong. Coaching intelligence agent prescribes targeted brief. FLM delivers in 1:1. Rep behavior changes within 2 weeks. Deal velocity improves 18%."
- **Metaphor:** Factory + operating system — you *engineer* capabilities, *ship* them through a product stack, *measure* behavioral change, and *iterate* based on data.

### Visual Concepts to Develop (in `concepts/`)
Ideas for the old-vs-new artifact:

1. **Split-screen / before-after:** Left side shows the "warehouse" (static shelves of content, grey/muted, cobwebs). Right side shows the "factory" (the three-layer stack, glowing, alive with particles and agents). Could be a single HTML with a draggable divider.

2. **Timeline evolution:** Horizontal scroll showing the progression from LMS → Content Library → Enablement Platform → Capabilities as a Product. Each stage gets more sophisticated visually. The last stage transitions into the 3D architecture.

3. **Two cities:** Side-by-side cityscapes. Old city: small, flat buildings, no connections, dark/static. New city: the contributor layer with districts, glowing connections, orbital agents, alive. Same metaphor as the 3D file but purpose-built for the comparison.

4. **Equation contrast:** Old game: HI + AI = V (linear addition, small number). New game: HI^AI = V (exponential, massive number). Animated counter showing the value divergence over time.

5. **Capability lifecycle comparison:** Old game flowchart (Create → Deliver → Hope → Measure completion) vs. New game flowchart (Engineer → Ship → Vault records → Gaps detected → AI prescribes → Behavior changes → Measure impact → Iterate). Side by side, showing how many more feedback loops the new model has.

---

## 🎨 Design System Reference

### Colors (CSS Custom Properties)
```css
/* Backgrounds */
--bg: #0c0e13;        /* Primary background */
--bg2: #111520;        /* Card backgrounds */
--bg3: #161B27;        /* Elevated surfaces */
--surface: #13161e;    /* Component surfaces */

/* Text hierarchy */
--text: #e4e7ee;       /* Primary text */
--text-mid: #a0a8be;   /* Secondary text */
--text-muted: #6b7590; /* Tertiary text */
--text-dim: #3e465c;   /* Labels, metadata */
--white: #EEEFF2;      /* Emphasis */
--accent: #D0D8EC;     /* Accent text */

/* Borders */
--border: #252a3a;     /* Default borders */
--border-light: #2f3548; /* Hover borders */

/* Semantic colors */
--action: #34d399;     /* Green — actions, commit, deployed */
--selection: #60a5fa;  /* Blue — selection stage, HQ, APIs */
--awareness: #a78bfa;  /* Purple — awareness, AQ, enterprise */
--impact: #f87171;     /* Red — impact stage, gaps, authorship */
--grow: #f472b6;       /* Pink — growth stage, figma, product */
--vault: #f59e0b;      /* Amber — vault, orchestrator */
--onboard: #fbbf24;    /* Yellow — onboarding, given */
--commercial: #fb923c; /* Orange — commercial motion */

/* 3D visualization (used in product_design_concept1.html) */
/* Cyan: #00e5ff — primary accent, nav dots, layer names */
/* Green: #00e5a0 — Actions quadrant */
/* Indigo: #6366f1 — Decisions quadrant */
/* Orange: #f4a623 — Exposure quadrant */
/* Red: #e63946 — Authorship quadrant */
/* Teal: #10a37f — API layer */
/* Purple: #c77dff — Codebase */
/* MediumSlateBlue: #7B68EE — MCP layer */
```

### Typography
```css
/* Primary body */
font-family: 'DM Sans', sans-serif;

/* Section titles, hero text */
font-family: 'Instrument Serif', serif;

/* Labels, code, metadata */
font-family: 'IBM Plex Mono', monospace;

/* Formula, large display */
font-family: 'Playfair Display', serif;

/* 3D file uses system fonts */
font-family: 'SF Pro Display', system-ui, -apple-system, sans-serif;
```

### Component Patterns
- **Cards:** `background: var(--surface); border: 1px solid var(--border); border-radius: 10-14px; padding: 14-36px`
- **Tags/badges:** `padding: 2-3px 6-8px; border-radius: 3-4px; font-size: 7-8px; font-weight: 600-700; letter-spacing: 0.3px`
- **Section labels:** `font-family: IBM Plex Mono; font-size: 9-10px; letter-spacing: 0.15-0.3em; text-transform: uppercase; color: var(--text-dim)`
- **Accent bars:** `position: absolute; top/left: 0; width/height: 2-3px; border-radius` — used on cards, left or top
- **Scroll reveal:** `.reveal { opacity:0; transform:translateY(24px); transition:0.6-0.7s }` → `.reveal.vis { opacity:1; transform:translateY(0) }`
- **Section transitions:** Centered divider with section number, italic title, gradient line

---

## 🚀 Deployment

### Vercel (recommended)
1. Connect this GitHub repo to Vercel
2. Root directory serves the HTML files directly
3. Custom domain optional but recommended for sharing

### File serving
Both HTML files are fully self-contained (all CSS/JS inline). External dependencies:
- **Google Fonts** (DM Sans, Instrument Serif, IBM Plex Mono, Playfair Display, Outfit) — graceful fallback to system fonts
- **Three.js r128** from cdnjs.cloudflare.com — required for 3D file, will not render without it

### vercel.json
```json
{
  "rewrites": [
    { "source": "/3d", "destination": "/src/product_design_concept1_mobile.html" },
    { "source": "/framework", "destination": "/src/product_thesis_and_concept_flyover_mobile.html" },
    { "source": "/", "destination": "/src/product_thesis_and_concept_flyover_mobile.html" }
  ]
}
```

---

## 📋 Next Steps (for Claude Code sessions)

### Priority 1: "Old Game / New Game" Visual
Build a standalone HTML artifact that makes the paradigm shift explicit. See concepts section above. This is the opening move before showing the full framework — it creates the "aha" moment that makes everything else land harder.

### Priority 2: Polish & Refine
- Test mobile versions on actual devices
- Optimize Three.js performance (reduce particle counts on mobile, add devicePixelRatio capping)
- Consider adding a loading state for the 3D file (it's heavy on first load)

### Priority 3: Presentation Flow
- Build a lightweight landing page that links to both artifacts with context
- Consider a "guided tour" mode for the 3D visualization that auto-orbits through the layers with narrative overlays

---

## 🔑 Key Decisions Already Made
- **Single-file HTML** — No build tools, no frameworks. Each artifact is one file. This is intentional for portability, shareability, and "view source" impressiveness.
- **Dark theme only** — The aesthetic is deliberate. These are meant to feel like looking into a system, not reading a document.
- **Interactive over static** — Every artifact rewards exploration. The 3D file rewards orbiting. The framework rewards scrolling. This is the opposite of a slide deck.
- **The formula is the brand** — `HI^AI = V` appears everywhere. It's the organizing principle, the nav mark, the footer. It's not a tagline — it's the thesis.

---

## 💡 Context That Matters
- JJ is VP Marketing at a B2B SaaS company (Tapcart — mobile apps for Shopify brands)
- This framework was developed in the context of GTM performance & productivity — how to make revenue teams better using AI
- The audience is executive (C-suite, board) and peer (other marketing/revenue leaders)
- The "wow factor" matters — these artifacts are meant to demonstrate that JJ thinks architecturally and can build, not just strategize
- The 3D visualization is the showstopper. The framework scroll is the leave-behind.
- Both files have been through many iterations — the current versions represent the best of dozens of rounds of refinement
