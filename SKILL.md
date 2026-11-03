---
name: portrait-social-retouch
description: "Reveal and beautify a person's real, already-present muscle texture and contour in portrait or mirror-selfie photos through evidence-guided directional relighting, tonal separation, and restrained detail enhancement without inventing muscles or changing body geometry. Use by default when the user invokes this skill, or asks to 显现肌肉纹理、勾勒原有肌肉线条、塑光显肌、增强胸腹肩臂轮廓、改善健身照光影、高清化身材照，或制作自然有美感的社交媒体身材人像；face retouching, cool-white grading, and cover stickers are optional secondary modules only when requested or helpful."
---

# Portrait Social Retouch

Reveal the subject's real muscle structure through believable light. Make the physique read more clearly and aesthetically without adding mass, removing fat, narrowing the waist, widening the shoulders, or drawing invented anatomy.

## Execution substrate

Use the built-in image generation/editing tool. Before editing, read the installed `imagegen` skill completely and follow its inspection, prompting, validation, and non-destructive save rules. Load every local edit target with `view_image` at original detail.

Treat the supplied portrait as the edit target. Read `references/prompt-recipes.md` before composing an edit prompt.

## Default behavior

When the user invokes this skill without further instructions, run the complete **Evidence-Guided Muscle Relighting** workflow. Do not default to a generic beauty retouch.

### Preferred finish: natural soft snapshot

The user's approved finish combines moderate clarity recovery with restrained muscle relighting: the same casual photograph, with chest and side-abdominal contours easier to see, while soft focus, gentle haze, natural exposure, and skin softness remain recognizable. Prefer this finish by default unless the user requests another look.

- For a blurry source, aim perceptually for **about 50% less blur**, retaining roughly half its original softness. This is a visual target, not a measurable restoration guarantee. Do not blur an already clear source to meet it.
- Recover only source-supported edges and broad tonal transitions. Do not reconstruct crisp pores, individual hair strands, camera lenses, phone-case patterns, or fabric weave lost to blur.
- Keep the source's overall color, exposure, window glow, and photographic character close to the original. Avoid aggressive dehazing, high-definition reconstruction, crunchy sharpening, and studio-like polish.
- Enhance existing chest, shoulder/arm, and side-waist planes through broad, softly feathered tonal separation. A flat-lit abdomen should retain soft broad planes rather than acquire new segmented abs.
- Use the original photograph as the base when changing clarity or retouch strength. Use accepted outputs as style references if useful, rather than repeatedly regenerating an edited image and accumulating drift.
- Preserve uncertain anatomical landmarks as they appear. In particular, do not turn a barely visible or occluded navel into a newly defined hole or relocate it; compare nipple and navel positions directly with the original.

The desired impression is “the original photo, moderately clearer and more flattering,” with no obvious AI reconstruction. Later explicit instructions override this default; a clarity-only request does not authorize extra muscle relighting.

Use these secondary modules only when explicitly requested or clearly supportive:

- Apply basic cleanup and neutral color correction when noise or color casts obscure muscle texture.
- Apply cool-white grading only when requested or consistent with the intended mood.
- Apply face refinement only when requested.
- Apply a face-cover sticker only when requested or after giving posting advice.

If the user asks only for critique or advice, inspect and answer without editing.

## Evidence-Guided Muscle Relighting

### 1. Read existing muscle evidence

Inspect the source before prompting. Identify only contours supported by visible surface evidence, such as:

- pectoral upper plane and lower border;
- sternum and central chest separation;
- existing linea alba and abdominal segment transitions;
- external oblique and side-waist transition;
- serratus hints when genuinely visible;
- deltoid, biceps, triceps, and chest-to-shoulder transitions;
- natural highlight ridges, shadow valleys, skin folds, and pose-driven tension.

Do not infer a complete six-pack from a flat abdomen. Do not manufacture anatomy hidden by the phone, arm, clothing, crop, deep shadow, or low resolution.

### 2. Lock body geometry

Keep these features unchanged:

- outer silhouette and subject scale;
- shoulder, chest, arm, and waist widths;
- torso length, posture, pose, and body-fat impression;
- nipple, navel, joint, hand, and phone positions;
- body volume and muscle mass;
- camera viewpoint, crop, perspective, and scene geometry.

Muscle definition must come from relighting and tonal separation, not body reshaping.

### 3. Derive the relighting direction

Follow the source's dominant light direction. Simulate a soft directional or grazing key light that reveals existing surface curvature while retaining plausible ambient fill.

- Place soft highlights on already raised muscle planes.
- Deepen existing valleys and boundaries with broad, feathered shadows.
- Preserve continuous light falloff across the torso.
- Keep cast shadows consistent with the face, phone, hand, and room.
- Avoid multiple conflicting key lights, rim-light cutouts, or painted dark lines.

Treat this as photographic dodge-and-burn plus subtle relighting, not anatomical illustration.

### 4. Enhance texture and separation

Increase local micro-contrast only along supported muscle structure, within the source's level of resolved detail. Preserve visible pores, fine hair, minor skin variation, and natural softness; do not synthesize texture erased by blur. For soft sources, use the preferred finish above and the clarity module in `references/prompt-recipes.md`.

The default aesthetic target is: the physique looks clearly better at first glance, while close inspection still reads as a naturally well-lit photograph.

### 5. Apply supporting cleanup

Reduce noise, compression artifacts, and distracting color contamination only when they obscure real structure; retain the source's natural snapshot texture and some haze. Gently control blown highlights without flattening muscle curvature or substantially changing exposure. Keep skin healthy and realistic.

## Non-negotiable invariants

Repeat these constraints in every edit prompt:

- Preserve exact identity, age, ethnicity, facial proportions, expression, head angle, hairstyle, pose, anatomy, and body geometry.
- Preserve hands and fingers, phone and case, clothing, background, mirror, crop, and scene geometry unless explicitly changed.
- Preserve source-visible pores, hair, skin texture, tonal variation, and an appropriate amount of original softness; never invent missing detail.
- Never add muscle volume, shrink the waist, broaden shoulders, reduce body fat, or generate extra abdominal segments.
- Never draw hard contour lines or apply bodybuilder-style shadows unsupported by the source.
- Avoid plastic skin, waxy smoothing, excessive whitening, halos, fake shadows, anatomy errors, text, logos, and watermarks.
- Do not overwrite the source or a prior accepted version.

## Source-limited cases

When the source lacks usable muscle evidence, enhance only supported broad planes. Explain that stronger definition would require a better pose or more directional capture light. Recommend a reshoot rather than hallucinating muscles when:

- the torso is heavily covered or obscured;
- flat frontal light removes almost all surface relief;
- motion blur or low resolution erases texture;
- the requested definition would require new anatomy or major fat loss.

## Optional modules

### Cool-white mood

Correct strong yellow or red casts toward neutral cool ivory while protecting muscle shadow separation. Do not whiten so strongly that local texture disappears.

### Invisible face refinement

Use optical cleanup rather than structural reshaping. Reduce distracting shine, slightly lift tired under-eyes, and tidy excess hair width. Do not slim the face, point the chin, enlarge eyes, change eyebrows, move the hairline, or reconstruct obscured features.

### Social cover

When requested, prefer a small semi-transparent silver-gray frosted smear, restrained blur, or minimal cool-tone graphic. Keep the hair silhouette and body image dominant. Explain that covering the eyes is not guaranteed anonymity.

## Workflow

1. Inspect the source at original detail.
2. Identify supported muscle contours and the dominant light direction.
3. State which muscle regions can be revealed and what geometry will remain locked.
4. Build one consolidated prompt from `references/prompt-recipes.md`.
5. Generate one candidate per requested variant.
6. Compare with the original for identity, silhouette, widths, body volume, anatomical landmarks, muscle evidence, light direction, hands, phone, crop, and background. Also compare softness, haze, exposure, and whether new fine detail makes the result look reconstructed.
7. Reject the result if it adds mass, narrows the waist, invents segments or landmarks, paints hard lines, or becomes conspicuously sharper than the requested finish. Retry once from the original with a targeted correction; if still unresolved, state the limitation rather than claiming exact preservation.
8. Save non-destructively with a descriptive name such as `portrait-evidence-guided-muscle-relight.png`.
9. Show or link the result and summarize the revealed muscle regions, lighting treatment, and preserved invariants.

## Strength defaults

- Muscle visibility: clearly aesthetically improved at first glance, still natural on inspection.
- Blurry-source clarity: perceptually about 50% less blur, retaining roughly half the source softness; adapt to source quality and explicit user instructions.
- Geometry change: zero.
- Muscle mass change: zero.
- Body-fat change: zero.
- Relighting: soft directional, consistent with the source.
- Skin texture: source-supported and naturally soft, without fabricated high-resolution detail.
- Color grade: close to original by default; supportive, not dominant.
