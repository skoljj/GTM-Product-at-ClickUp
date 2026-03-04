# GTM Capability Architecture

Self-contained deployment package for the core visualizations. Includes mobile-optimized variants and Vercel routing configuration.

## Structure

```
src/
├── product_design_concept1.html              ← 3D Three.js capability architecture
├── product_design_concept1_mobile.html       ← Mobile-optimized 3D version
├── product_thesis_and_concept_flyover.html   ← 7-section scrollable framework
└── product_thesis_and_concept_flyover_mobile.html ← Mobile-optimized framework
```

## Deployment

Configured for Vercel with clean URL routes:

| Route | Destination |
|-------|-------------|
| `/` | Framework (mobile) |
| `/framework` | Framework (mobile) |
| `/3d` | 3D Architecture (mobile) |

All HTML files are self-contained. External CDN dependencies: Google Fonts and Three.js r128.
