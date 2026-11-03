# Prompt Recipes

Read this file for every image edit. Use the muscle-evidence and relighting modules by default. Add optional modules only when needed.

## Base identity and geometry lock

```text
Use case: identity-preserve
Asset type: evidence-guided muscle-relighting portrait for social media
Input images: Image 1 is the sole edit target and exact visual base.
Constraints: Preserve exact identity, age, ethnicity, facial proportions, expression, head angle, hairstyle, pose, outer body silhouette, shoulder width, chest width and volume, arm width, waist width, torso length, body-fat impression, nipple and navel positions, hands and fingers, phone and case, crop, camera viewpoint, perspective, background objects, and scene geometry. Preserve source-visible pores, fine hair, skin folds, natural tonal variation and photographic softness. Keep uncertain or occluded landmarks exactly as visible; do not newly define or reposition a navel or nipple.
Avoid: added muscle mass, broader shoulders, larger chest or arms, narrower waist, fat removal, extra abdominal segments, invented hidden anatomy, body reshaping, identity drift, plastic skin, halos, anatomy distortion, object changes, text, logos, or watermarks.
```

## Source muscle-evidence statement

Before generating, replace the bracketed content with observations from the actual image:

```text
Visible source evidence: [list only genuinely visible pectoral planes/borders, sternum separation, linea alba, abdominal transitions, oblique or serratus hints, deltoid/arm transitions, and pose-driven tension].
Occluded or unsupported regions: [list areas hidden, blurred, flat-lit, or not visibly defined]. Do not create definition in these regions.
Dominant source light: [direction, softness, highlight region, and existing shadow direction].
```

## Default muscle-relighting module

```text
Primary request: Reveal and beautify only the muscle texture and contours already supported by the source. Follow the existing dominant light direction and simulate a soft directional grazing key light with believable ambient fill. Place subtle highlights on existing raised muscle planes and deepen only existing valleys and boundaries with broad feathered shadows. Increase local micro-contrast along supported pectoral, chest-separation, abdominal, oblique, shoulder, and arm transitions without changing any body geometry or muscle volume. Preserve natural softness between muscle groups, continuous light falloff, pores, fine hair, and skin variation. The physique should look clearly more defined and aesthetically pleasing at first glance, yet remain a believable naturally well-lit photograph on close inspection.
Avoid: drawing dark muscle lines, carving a six-pack, inventing segments, bodybuilding shadows, vascularity, sharp dodge-and-burn edges, conflicting key lights, rim-light cutouts, fat loss, shoulder widening, waist narrowing, chest enlargement, or arm enlargement.
```

## Supporting cleanup module

```text
Supporting cleanup: Clarify source-supported broad contours with restrained cleanup. Retain natural snapshot texture, soft skin, some haze and the source's overall exposure and color. Gently control washed-out highlights while preserving curvature and shadow separation. Do not reconstruct missing fine detail, aggressively dehaze, flatten torso lighting, or apply crunchy sharpening or broad skin smoothing.
```

## Preferred blurry-source clarity module

Use with muscle relighting for blurry sources by default; omit or adjust for an already clear source or an explicit different strength. Treat percentages as perceptual guidance, not a precise numerical guarantee.

```text
Natural soft-snapshot finish: Work from the ORIGINAL photo. Reduce perceived blur by approximately 50%, retaining about half of its original soft-focus character. Recover only existing edges and broad tonal transitions; do not manufacture sharp pores, individual hairs, camera lenses, phone-case details or denim weave lost to blur. Preserve recognizable haze, window glow, pale/warm exposure if present, and ordinary phone-photo softness. Apply only restrained evidence-supported muscle relighting with broad feathered shadows. The chest and side-abdominal planes should be a little easier to read while the photograph still looks like the original casual snapshot. Keep a flat-lit central abdomen soft; do not invent horizontal ab grooves, new anatomy or a more prominent navel. No high-definition reconstruction, studio finish, crispy edges, plastic skin or sharpening halos.
```

## Optional cool-white module

```text
Optional color grade: Correct strong yellow or red casts toward healthy natural cool ivory. Keep muscle shadows neutral and separated; preserve pores and local tonal variation. Avoid dead-white, blue-gray, or over-bright skin that erases muscle texture.
```

## Optional invisible face-refinement module

```text
Optional face refinement: Reduce only distracting facial shine, lift a tired visible under-eye slightly, and neaten excessive hairstyle width while preserving the exact face and hairline. Do not slim the face, alter cheekbones, point the chin, enlarge eyes, change eyebrows, enforce symmetry, or reconstruct obscured features.
```

## Optional frosted-cover module

```text
Use case: precise-object-edit
Optional social cover: Add one small semi-transparent silver-gray frosted smear over the requested eye or upper-face area, positioned as an intentional editorial graphic. Keep the hair silhouette visible and the body/lighting edit dominant. Avoid cartoons, crude mosaic pixels, censor bars, saturated colors, text, logos, or watermarks.
```

## Validation checklist

Reject or retry when any answer is yes:

- Did the outer body silhouette move?
- Did shoulders, chest, arms, or waist change width or volume?
- Did body fat appear removed?
- Did new abdominal segments appear without source evidence?
- Do shadows look drawn, hard-edged, or inconsistent with the room light?
- Did nipples, navel, hands, phone, face, crop, or background move?
- Did skin lose pores or become plastic?
- Did the result invent fine detail absent from the source, remove too much softness/haze, or look like a newly reconstructed high-definition photo?
- Did an uncertain or occluded navel/nipple become newly defined or move relative to the original torso and belt?

## Targeted retry phrases

Use one correction at a time:

- `Restore the exact source silhouette, widths, body volume, and body-fat appearance; keep only evidence-supported relighting.`
- `Remove all newly invented abdominal segments; enhance only the source-visible linea alba and broad abdominal planes.`
- `Reduce the relighting contrast by 30% and soften every muscle shadow edge.`
- `Restore the source light direction; remove conflicting highlights and shadows.`
- `Restore natural pores and skin softness while preserving the existing muscle separation.`
- `Restore the original crop, anatomical landmarks, hands, phone, and background geometry.`
- `Return to the original photo and retain about half its soft-focus character; remove invented fine detail and aggressive dehazing while keeping moderate source-supported clarity.`
- `Restore the exact source nipple/navel positions and visibility; remove any newly invented or relocated landmark while retaining only gentle chest and side-waist relighting.`
