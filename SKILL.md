---
name: supplier-artwork-delivery
description: Prepare and package approved production artwork for supplier or manufacturing handoff through source-file inspection, version control, vector/raster route verification, dimensions, repeat and color checks, requested AI/PDF/EPS/SVG/PNG/TIFF exports, manifest creation, and evidence-based prepress QA. Use for supplier artwork delivery, production artwork packaging, prepress checks, or factory handoff. Do not invent missing production specifications, overwrite originals, send files, or declare production approval without evidence.
---

# Supplier Artwork Delivery

Turn an approved artwork source into a traceable delivery candidate without changing the creative direction or overstating production readiness.

## Operating boundary

Start from an exact source file and preserve the approved visual result. Treat mockups, screenshots, concepts, and previews as references rather than production masters.

Do not:

- redesign the artwork unless the user separately requests design changes;
- guess dimensions, bleed, substrate, print method, color profile, spot colors, repeat size, or supplier compatibility;
- convert raster artwork to vector and call it editable without inspecting the result;
- flatten, outline, expand, relink, recolor, or remove objects unless required and authorized;
- overwrite the source file;
- include references, obsolete versions, hidden drafts, or temporary files in a delivery package;
- send a package or message a supplier without explicit authorization;
- use “final,” “print-ready,” or “production-approved” when the available evidence supports only a delivery candidate.

## Select the mode

Choose the narrowest mode supported by the request.

### AUDIT_ONLY

Inspect the artwork and report issues. Do not modify, export, rename, move, or package files.

### PREPARE_AND_PACKAGE

Create a new dated working copy, apply only authorized production-preparation changes, export requested formats, run QA, and build a delivery candidate.

A request to “check,” “review,” or “audit” does not authorize edits. A request to “prepare,” “export,” “package,” or “make the supplier files” authorizes the corresponding scoped changes, but not supplier transmission.

## Establish the evidence baseline

Before changing artwork, record:

1. the exact source path or asset identifier;
2. the project, artwork name, current revision, and approval state;
3. intended product, physical print area, orientation, and units;
4. print or manufacturing method and substrate, when known;
5. required master and interchange formats;
6. color requirements: RGB, CMYK, ICC profile, named spot colors, or supplier standard;
7. bleed, trim, safety area, dieline, repeat, trapping, overprint, and transparency requirements;
8. required application and compatibility version;
9. supplier specifications and the source of each requirement.

Use “UNKNOWN” for missing facts. Continue only with work that does not depend on those facts, and identify the resulting limitation.

## Preserve protected content

Do not change the following without explicit approval or an authoritative specification:

- dimensions, scale, orientation, dielines, cut lines, fold lines, seams, bleed, and safe areas;
- brand marks, legal text, barcodes, QR codes, certification marks, product codes, and regulatory content;
- approved colors, named inks, Pantone references, ICC profiles, and color-separation logic;
- approved pattern density, repeat tile, placement, cropping, and artwork-to-product registration;
- live text, fonts, linked assets, layer structure, spot-color names, and overprint settings.

Report a suspected defect without guessing the intended replacement.

## Use evidence-based statuses

Use one status per artifact:

| Status | Meaning |
| --- | --- |
| WORKING_SOURCE | Editable internal source; not a supplier file. |
| ART_APPROVED | Visual direction is approved; production checks may remain. |
| PREPRESS_CANDIDATE | Local preparation and documented QA are complete; supplier confirmation remains. |
| SUPPLIER_OPEN_CHECKED | The supplier confirmed that the exact delivered version opens correctly. |
| SAMPLE_APPROVED | A physical sample or proof for the exact version was approved. |

Keep these events separate: generated, sent, received, opened, technically confirmed, sampled, and sample approved.

## Workflow

### 1. Resolve the current source

- Inspect repository or project guidance before handling files.
- Identify the exact current source and all linked or embedded dependencies.
- Detect similarly named drafts and old revisions; do not choose by filename alone.
- Record file size, modification time, checksum when practical, application format, artboard or page count, and visible revision labels.
- Stop if the current source cannot be distinguished safely.

### 2. Create a dated working copy

In PREPARE_AND_PACKAGE mode:

- keep the original untouched;
- create a new batch using local date and revision;
- place editable work outside the supplier delivery directory;
- record every intentional change;
- avoid destructive cleanup until the new copy has been saved, reopened, and verified.

Use:

~~~text
YYYY-MM-DD_HHmm_<project>_<stage>_R##/
<project>_<purpose>_<YYYY-MM-DD>_R##_<STATUS>.<ext>
~~~

Do not use names such as “final2,” “latest,” or “send-this-one.”

### 3. Classify the production route

Choose and record one route.

#### VECTOR

Use when all production artwork must remain editable paths, shapes, groups, symbols, patterns, gradients, or live text allowed by the specification.

Verify:

- no unintended embedded or linked raster artwork;
- no missing fonts, links, plugins, or unsupported live effects;
- paths and clipping structures remain editable;
- automatic tracing has not introduced excessive anchors, holes, noise, or open paths.

#### EMBEDDED_RASTER

Use when a raster master is intentional.

Record:

- pixel dimensions;
- physical output dimensions;
- effective PPI at final size;
- color mode and ICC profile;
- bit depth and transparency requirements;
- whether the image is native, resampled, or AI-upscaled;
- confirmation that the raster is embedded rather than missing or externally linked when placed in a container file.

Changing only PPI metadata does not create additional image detail.

#### HYBRID

Use when intentional vector and raster elements coexist. Apply both sets of checks and identify which objects belong to each route.

Never describe a placed or embedded image as true vector artwork.

### 4. Verify geometry and production layers

- Confirm units, artboard or page dimensions, orientation, scale, and origin.
- Verify trim, bleed, safety area, dieline, fold, seam, cut, and non-printing guide layers against supplied specifications.
- Keep production guides visually distinct and named.
- Confirm that hidden or locked objects are intentional.
- Check clipping masks, compound paths, strokes, transparency, blend modes, overprint, knockout, and trapping only to the extent required by the process.
- Do not expand strokes, outline text, flatten transparency, or remove guides by default; make a compatible copy when required.

### 5. Verify repeats when applicable

For repeating surface artwork:

- identify the true tile width and height;
- verify exact left/right and top/bottom correspondence;
- verify all four corners;
- inspect at least a 3 × 3 repeat preview for seams, gaps, overlaps, doubled strokes, banding, unintended clusters, and directional discontinuity;
- confirm that the preview uses the exact candidate tile and spacing;
- record the approved physical repeat size and pattern scale.

Mark repeat checks “N/A” for non-repeating artwork. Do not infer a repeat from a visual mockup.

### 6. Verify color

- Record the document color mode, profile, named inks, and intended output process.
- Check that spot-color names and process/spot settings are consistent across files.
- Compare exported color values with the source; do not rely on appearance alone.
- Treat on-screen CMYK and Pantone simulations as references, not physical proof.
- Never select or substitute a Pantone color automatically.
- Record missing ICC, RIP, substrate, ink, or proofing requirements as unresolved.
- Keep color approval distinct from file-structure approval.

### 7. Export only requested formats

Create only formats required by the user or supplier. Common outputs may include:

- editable master: AI or the documented native format;
- interchange: PDF, EPS, or SVG when compatible with the artwork and process;
- raster production or preview: TIFF or PNG at documented physical size and effective PPI;
- palette or color reference;
- proof or placement preview clearly marked as non-production.

For every export:

- derive it from the exact approved working source;
- preserve dimensions, scale, color intent, transparency, and repeat behavior;
- reopen the exported file in an appropriate application;
- confirm visible content, page or artboard size, links, fonts, rasterization, clipping, and editability expectations;
- record any deliberate compatibility tradeoff.

Do not create placeholder files or claim a format exists when the available tools cannot produce or validate it.

### 8. Run QA and package

Read [references/qa.md](references/qa.md) and apply every relevant check.

Copy and complete:

- [assets/DELIVERY_MANIFEST.md](assets/DELIVERY_MANIFEST.md)
- [assets/QA_CHECKLIST.md](assets/QA_CHECKLIST.md)

Use this default package structure, removing empty categories:

~~~text
<project>_DELIVERY_<YYYY-MM-DD>_R##/
├── 01_MASTER/
├── 02_INTERCHANGE/
├── 03_RASTER/
├── 04_COLOR/
├── 05_QA/
└── DELIVERY_MANIFEST_<YYYY-MM-DD>_R##.md
~~~

Include only the current delivery candidate and its supporting manifest or QA records. Keep working files, references, mockups, temporary previews, and history outside the package unless the specification explicitly requires one.

## Report the result

Lead with the highest supported status and list:

- mode and scope;
- exact source used;
- production route;
- files created or inspected;
- checks passed;
- unresolved specifications or failed checks;
- status of each deliverable;
- the single next approval or supplier confirmation needed.

Do not bury blockers behind a general “ready” statement.

## Completion criteria

Complete AUDIT_ONLY when the exact source has been inspected, applicable checks are reported, and unknowns are explicit.

Complete PREPARE_AND_PACKAGE only when:

- the original remains unchanged;
- the current revision and requested formats are unambiguous;
- dimensions, route, repeat, color, and export checks are recorded as passed, failed, unknown, or not applicable;
- each generated file has been reopened and inspected;
- manifest and QA checklist match the actual package;
- the delivery directory contains no obsolete, temporary, or unrelated files;
- the reported status does not exceed the available evidence.

## Example requests

- “Audit this Illustrator file for supplier handoff. Do not change it.”
- “Prepare a dated AI and PDF delivery candidate from the approved source.”
- “Check whether this pattern is truly seamless and package the approved repeat.”
- “Build a supplier package, but leave color and production approval pending.”

