# Production artwork QA

Use this checklist as a decision framework. Mark every item PASS, FAIL, UNKNOWN, or N/A and attach a file, application readout, screenshot, checksum, or written specification when evidence matters.

## 1. Source and scope

- Confirm the exact source file, revision, approval state, and owner.
- Confirm that the user authorized AUDIT_ONLY or PREPARE_AND_PACKAGE.
- Confirm the requested outputs and supplier specification source.
- Separate reference images, mockups, working files, and delivery candidates.
- Verify that the original source has not been overwritten.

## 2. File integrity

- Open the working source without repair warnings.
- Save, close, and reopen the prepared source.
- Check for missing or changed fonts, links, plugins, profiles, and placed assets.
- Check hidden, locked, non-printing, template, and guide layers.
- Confirm artboard or page count and visible content.
- Record the application and compatibility version used.

## 3. Vector, raster, and hybrid routes

### Vector route

- Confirm that production objects are editable vector objects.
- Detect unintended raster items and external links.
- Inspect clipping paths, compound paths, gradients, patterns, symbols, strokes, and live effects.
- Check for empty paths, isolated points, excessive anchors, accidental open paths, and tracing noise.
- Confirm whether live text, outlined text, expanded strokes, or flattened effects are required.

### Raster route

- Confirm the intentional raster source and embedding state.
- Record pixel dimensions, physical dimensions, effective PPI, color mode, ICC profile, and bit depth.
- Record whether the source is native, resampled, or AI-upscaled.
- Inspect compression, halos, noise, sharpening, transparency edges, and visible artifacts at final size.
- Confirm that placed raster assets are not missing external links.

### Hybrid route

- Identify vector and raster objects separately.
- Apply all relevant vector and raster checks.
- Confirm that export settings preserve the intended relationship between both types.

## 4. Geometry and guides

- Confirm units, orientation, scale, and coordinate origin.
- Confirm artboard, page, trim, bleed, and safe-area dimensions.
- Confirm dieline, fold, seam, cut, drill, registration, or finishing guides against a supplied specification.
- Keep guides on named, non-printing layers when appropriate.
- Verify object placement relative to production guides.
- Record any unresolved manufacturing tolerance.

## 5. Repeat artwork

When applicable:

- Record tile width, tile height, orientation, and physical scale.
- Confirm exact left/right, top/bottom, and four-corner continuity.
- Inspect a 3 × 3 preview created from the exact candidate tile.
- Check for gaps, seams, overlaps, doubled strokes, banding, holes, clusters, and direction changes.
- Confirm that the repeat preview did not rescale or crop the tile.
- Keep the preview outside the supplier package unless requested.

For non-repeat artwork, mark this section N/A.

## 6. Color

- Confirm document color mode and ICC profile.
- Confirm process, spot, and named-color behavior.
- Compare source and export color definitions.
- Check overprint, knockout, transparency, and separation settings when relevant.
- Record substrate, print method, ink system, RIP, and proofing requirements.
- Treat Pantone and screen simulations as references until checked against the required physical standard.
- Keep file approval, color approval, and sample approval as separate events.

## 7. Exports

For each requested format:

- Export from the exact prepared source.
- Reopen the result in an appropriate application.
- Verify page or artboard size, visible content, orientation, scale, and crop.
- Verify expected editability or rasterization.
- Verify fonts, links, clipping, transparency, overprint, and color behavior.
- Verify raster pixel dimensions and effective PPI.
- Record compatibility compromises.
- Do not report a format as validated when it was only generated.

## 8. Package

- Use dated names and an R## revision.
- Include only current delivery candidates.
- Exclude references, obsolete revisions, temporary files, mockups, caches, and application recovery files.
- Make the manifest match the exact filenames and checksums.
- Make the QA checklist match actual evidence.
- Verify that the package opens after copying or archiving.
- Record package size and checksum when practical.

## 9. Evidence status

Track separately:

1. local candidate generated;
2. package sent;
3. supplier received;
4. supplier opened the exact version;
5. supplier confirmed layers, dimensions, color, and repeat;
6. physical proof or sample produced;
7. proof or sample approved.

Never infer a later status from an earlier one.

## Stop conditions

Stop and report the blocker when:

- the current source or approved revision is ambiguous;
- required dimensions, dielines, bleed, repeat, or color specifications are missing;
- the chosen production route contradicts the file contents;
- an export cannot be reopened or differs materially from the source;
- missing fonts, links, plugins, or profiles change the artwork;
- repeat QA fails;
- the delivery package contains mixed revisions;
- a destructive change would be required without authorization;
- the requested status exceeds the available supplier or sample evidence.

