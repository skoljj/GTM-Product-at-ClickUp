# applied HI ^ applied AI = actual V

Interactive visualizations exploring a thesis about GTM capability architecture — the idea that the quality of human intelligence (base), amplified by the sophistication of AI application (exponent), produces value that neither achieves alone.

These artifacts model what happens when you treat enablement as a product engineering discipline rather than a content delivery function: capabilities designed like features, shipped through an architecture, measured by behavioral change, and iterated on with data.

## The Visualizations

### Thesis & Framework (`chapters/`)

A multi-chapter scrollable experience laying out the full framework:

- **Framework** — The core formula (`HI^AI = V`), operating principles, and the argument for exponentiation over addition
- **Knowledge Vault** — Per-person capability records tracking Human Quotient and AI Quotient
- **Product Architecture** — How capabilities are engineered: API integrations, orchestration layer, MCP tool connections
- **Bowtie Funnel** — Full revenue lifecycle mapping with conversion rates, motion types (PLG / Commercial / Enterprise), and action layer connections
- **Opportunity Seeker** — Interactive firmographic filtering with animated funnel visualizations
- **Action Layer** — The frontline manager's operating surface as an SVG dashboard

Navigation: `chapters/index.html`

### 3D Capability Architecture (`diagram/`)

An interactive Three.js visualization of the three-layer stack:

- **Contributor Layer** — 38 buildings across 6 GTM districts (Commercial, Enterprise, Partnerships, Post Sales, XDR, Operations) on a dark platform with cyan grid
- **Product Layer** — Transparent disc housing API integrations, codebase core, and MCP tool connections
- **Agent Layer** — AI agent characters with capability cabinets, lab and studio environments

Orbit with pointer drag, scroll to navigate layers, ctrl+scroll to zoom. Nav dots on the right edge jump between views.

Navigation: `diagram/index.html`

### Old Game / New Game (`old-game-new-game.html`)

A contrast visualization showing the paradigm shift from traditional enablement (content warehouse) to capabilities-as-product (factory with feedback loops).

### Thesis Overview (`product thesis and concept flyover.html`)

The full seven-section framework as a single scrollable page with scroll-reveal animations and interactive data visualizations.

## Running Locally

Every HTML file is fully self-contained — all CSS and JavaScript inline. Just open any `.html` file in a browser.

External dependencies loaded via CDN (no install required):

- **Google Fonts** — DM Sans, Instrument Serif, IBM Plex Mono, Playfair Display, Outfit
- **Three.js r128** — Required for the 3D visualizations; loaded from cdnjs.cloudflare.com

## Design Language

Dark backgrounds, sci-fi aesthetic, data-forward. Cyan, purple, pink, and orange accents against near-black surfaces. Metallic materials, glowing edges, fog effects, minimal HUD patterns. Every artifact rewards exploration — the 3D file rewards orbiting, the framework rewards scrolling.

## License

All rights reserved.
