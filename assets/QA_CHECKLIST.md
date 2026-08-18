# Production Artwork QA Checklist

Project:
Artwork:
Batch:
Revision:
Date:
Mode: AUDIT_ONLY / PREPARE_AND_PACKAGE
Route: VECTOR / EMBEDDED_RASTER / HYBRID

Use PASS, FAIL, UNKNOWN, or N/A.

## Source and version

- [ ] Exact current source identified
- [ ] Approval state recorded
- [ ] Original source unchanged
- [ ] Working and delivery directories separated
- [ ] Date and R## revision present in generated filenames
- [ ] Obsolete and unrelated files excluded

## File integrity

- [ ] Working source opens without repair warnings
- [ ] Prepared source saved, closed, and reopened
- [ ] Fonts and linked assets accounted for
- [ ] Application and compatibility version recorded
- [ ] Artboard or page count verified
- [ ] Hidden, locked, guide, and non-printing layers inspected

## Production route

- [ ] Route recorded accurately
- [ ] Vector objects remain editable where required
- [ ] No unintended raster objects or missing external links
- [ ] Intentional raster assets are embedded where required
- [ ] Raster pixel size, physical size, effective PPI, color mode, profile, and origin recorded
- [ ] Hybrid objects checked under both vector and raster rules

## Geometry and repeat

- [ ] Units, scale, orientation, and dimensions verified
- [ ] Trim, bleed, safety area, dieline, fold, seam, and cut guides verified or marked unknown
- [ ] Repeat dimensions recorded or marked N/A
- [ ] Left/right, top/bottom, and four-corner repeat checks pass
- [ ] Exact candidate tile passes a 3 × 3 visual check
- [ ] Approved pattern scale and placement recorded

## Color

- [ ] Color mode and ICC profile recorded
- [ ] Process and spot-color settings verified
- [ ] Named colors are consistent across files
- [ ] Overprint, knockout, transparency, and separations checked when relevant
- [ ] Substrate, ink, RIP, and proofing requirements recorded or marked unknown
- [ ] Screen or Pantone simulations are not presented as physical proof

## Exports

- [ ] Every output was created from the exact prepared source
- [ ] Every output was reopened in an appropriate application
- [ ] Dimensions, orientation, scale, crop, and visible content match
- [ ] Editability or rasterization matches the stated purpose
- [ ] Fonts, links, clipping, transparency, and color behavior match expectations
- [ ] Compatibility tradeoffs are documented
- [ ] No nonexistent or unvalidated format is claimed

## Package and status

- [ ] Manifest matches exact filenames and checksums
- [ ] QA record matches actual evidence
- [ ] Package contains only current delivery candidates
- [ ] Package opens after copying or archiving
- [ ] “Generated,” “sent,” “received,” “opened,” “confirmed,” and “sample approved” remain separate
- [ ] Reported status does not exceed the evidence
- [ ] Supplier sending remains unperformed unless explicitly authorized

## Blockers and next approval

- Failed checks:
- Unknown specifications:
- Required owner or supplier decision:
- Safest current status:
- Next single approval:

