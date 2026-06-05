Rendering the Homelab Mermaid diagram

This folder contains `homelab.mmd` (Mermaid source). Use `mmdc` (mermaid-cli) to render an SVG/PNG.

Requirements
- Node.js (LTS)
- npm

Install mermaid-cli

```bash
npm install -g @mermaid-js/mermaid-cli
```

Render commands

```bash
# Render to SVG
mmdc -i assets/homelab.mmd -o assets/homelab.svg

# Render to PNG
mmdc -i assets/homelab.mmd -o assets/homelab.png
```

Notes
- The `click` links may not be active in all renderers; the SVG will preserve them if supported by your viewer.
- If you want, I can run these commands here to produce the SVG (requires Node.js in the environment). Say "Render now" to have me attempt it.