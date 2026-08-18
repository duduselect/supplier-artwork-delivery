# Supplier Artwork Delivery

A Codex Skill for preparing and packaging approved production artwork for supplier or manufacturing handoff. It creates a traceable delivery candidate with source inspection, route checks, export verification, a manifest, and evidence-based QA.

## What it covers

- Source and revision identification without overwriting originals
- VECTOR, EMBEDDED_RASTER, and HYBRID production routes
- Dimensions, bleed, safety, dieline, repeat, color, and export checks
- Requested AI/PDF/EPS/SVG/PNG/TIFF outputs only
- Delivery manifests, QA checklists, and explicit evidence statuses
- Clear stop conditions when specifications or approvals are missing

The Skill does not redesign artwork, invent production specifications, send files to suppliers, or claim production approval without evidence.

## Install

Clone this repository, then place the Skill folder in your Codex skills directory:

~~~sh
git clone https://github.com/duduselect/supplier-artwork-delivery.git
mkdir -p ~/.codex/skills
cp -R supplier-artwork-delivery ~/.codex/skills/
~~~

## Use

Example prompts:

- “Use $supplier-artwork-delivery to audit this Illustrator file for supplier handoff. Do not change it.”
- “Prepare a dated AI and PDF delivery candidate from the approved source.”
- “Build a supplier package, but leave color and production approval pending.”

The Skill definition is in [SKILL.md](SKILL.md). Templates and QA guidance are in [assets](assets/) and [references](references/).

## License

MIT. See [LICENSE](LICENSE).

