# ns-guide-assets

Static images for the Nice Shoes **Software Guides** (Confluence → All Company Knowledge Base → Tools and Services).
Served by the Vercel project `ns-guide-assets` (NS_WORKFLOW team), which deploys automatically on every push to `main`.

Layout: `/<tool-slug>/<tool-slug>-cover.png`, `-thumb.png`, `-band-NN-<section>.png` (1×), plus `@2x` masters for cover and thumb.
Images are rendered by `tools/make_guide_assets.py` in the NS Software folder from the brand kit (`NiceShoesCode/niceshoes-brand`). Don't hand-edit PNGs here; re-render and push.

Pipeline: render → push here → Vercel deploys → the n8n workflow `ns/confluence-attach` pulls the URLs and attaches them to the Confluence page.
