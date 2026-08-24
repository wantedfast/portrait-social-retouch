---
name: portrait-social-retouch
description: "Retouch user-supplied portrait and mirror-selfie photos for social media with identity-preserving enhancement: HD cleanup, natural cool-white skin, subtle lean-muscle definition based on the original physique, invisible facial refinement, and tasteful face-cover sticker or privacy variants. Use when the user asks to 高清化人像、调冷白皮、勾勒薄肌、轻修脸型、评价脸部上镜问题、遮脸、加贴纸，或制作适合社交媒体发布的人像版本。"
---

# Portrait Social Retouch

Create a polished social-media portrait while keeping the person recognizably themselves. Favor believable photography over beauty-filter aesthetics.

## Execution substrate

Use the built-in image generation/editing tool. Before editing, read the installed `imagegen` skill completely and follow its save, inspection, prompting, and validation rules. Load every local edit target with `view_image` before the first edit.

Treat the supplied portrait as an **edit target**, not merely a style reference. Save each accepted stage non-destructively with a descriptive sibling filename.

## Decide the operation

Interpret the request before editing:

- If the user asks for critique, advice, or whether something should be changed, inspect and answer first. Do not edit until asked.
- If the user asks to improve the image generally, run the Core Retouch.
- If the user asks for thin muscle, add the Lean-Muscle module after or within the Core Retouch.
- If the user asks to refine the face, use the Face Refinement module.
- If the user dislikes the photographed face and asks whether to retouch or cover it, use the Social Posting Decision.
- If several modules are requested together, prefer one consolidated edit to reduce identity drift. Use staged edits only when the user is reviewing each stage interactively.

Proceed without clarification when the request is clear. Ask only when the desired strength, identity source, or target image is genuinely ambiguous.

## Non-negotiable invariants

Repeat these constraints in every edit prompt:

- Preserve exact identity, age, ethnicity, expression, head angle, pose, anatomy, camera viewpoint, crop, and scene geometry.
- Preserve visible objects, hands and fingers, phone and case, clothing, background, and mirror structure unless explicitly changed.
- Preserve real pores, fine hair, and natural tonal variation.
- Never invent facial features hidden by a phone, hand, hair, or crop.
- Avoid plastic skin, waxy smoothing, excessive whitening, blue-gray skin, halos, fake shadows, anatomy errors, body reshaping, added text, logos, and watermarks.
- Do not overwrite the source or a prior accepted version.

## Core Retouch

Apply only the amount needed:

1. Increase perceived resolution and fine-detail clarity.
2. Reduce digital noise, compression artifacts, muddiness, and color contamination.
3. Correct strong yellow/orange casts toward a neutral-to-cool white balance.
4. Render skin as naturally luminous cool ivory, not pure white or gray.
5. Preserve highlight detail, pores, hair strands, and realistic indoor light direction.
6. Avoid crunchy sharpening and broad skin blur.

Validate that the face, body proportions, hands, phone, and background remain consistent with the source.

## Lean-Muscle module

Base all definition on the original physique. Use gentle light-and-shadow modeling rather than changing anatomy.

- Keep the exact body size, weight, shoulder width, waist width, posture, and body-fat impression.
- Add only faint pectoral lower-edge definition, a soft central abdominal line, extremely subtle upper-ab and oblique contours, and mild shoulder/upper-arm separation.
- Aim for slim, lightly trained, understated thin muscle.
- Avoid added mass, narrowed waist, widened shoulders, deep six-pack grooves, vascularity, carved lines, bodybuilding aesthetics, or dramatic fat loss.

If the result reads as a transformation rather than lighting revealing existing structure, reject it and retry with lower intensity.

## Face Refinement module

Prefer optical cleanup over structural reshaping:

- Reduce distracting forehead shine while keeping texture.
- Brighten a tired visible under-eye area only slightly, usually around 10%.
- Add delicate tonal modeling at the visible temple and cheek edge.
- Clarify the visible jaw/face edge through light and shadow only.
- Slightly neaten excessive hairstyle width while preserving the haircut, hairline, strand direction, and natural volume.

Do not slim the face, reduce cheekbones, sharpen the chin, enlarge eyes, change eyebrows, move the hairline, enforce symmetry, or reconstruct phone-obscured features unless the user explicitly asks and accepts identity-drift risk.

When only part of the face is visible, explain that heavy retouching has limited value and higher uncanny risk.

## Social Posting Decision

Choose the least intrusive solution that supports the user's goal:

1. **Keep visible** when the face already reads naturally and the post is friends-only.
2. **Light refinement** when the issue is shine, fatigue, weak contour, or untidy hair.
3. **Tasteful cover** when the face is substantially obscured, the capture angle is unflattering, or heavy reconstruction would be required.
4. **Recommend a reshoot** when the face is intended to be a focal point but the source lacks usable facial information.

For a tasteful cover, prefer a small semi-transparent silver-gray frosted smear, minimalist cool-white or black graphic, metallic star, or restrained blur. Let it overlap the phone edge slightly when compositionally natural. Preserve hair silhouette and overall mood. Avoid large cartoon stickers, crude mosaics, black censor bars, and elements that dominate the portrait unless requested.

Remember that covering the eyes is an aesthetic choice, not guaranteed anonymity: hair, body, phone case, background, and metadata can still identify a person.

## Editing sequence

1. Inspect the source at original detail.
2. State the planned edit and preservation constraints briefly.
3. Select the minimum required modules.
4. Build a structured identity-preserve prompt using `references/prompt-recipes.md`.
5. Generate one final candidate per requested variant.
6. Inspect the result for identity, anatomy, skin, face, body, hands, objects, crop, and background.
7. Retry once with one targeted correction if a material invariant drifted.
8. Save the accepted output in the task output directory with a descriptive filename such as:
   - `portrait-hd-cool-white.png`
   - `portrait-hd-cool-white-lean-muscle.png`
   - `portrait-hd-cool-white-face-refined.png`
   - `portrait-social-sticker.png`
9. Show or link the final image and summarize the actual changes. Report the built-in tool path and the prompt's core intent.

## Strength defaults

Use conservative defaults unless the user asks otherwise:

- Skin whitening: natural cool-ivory correction, not categorical complexion change.
- Muscle: barely visible at first glance, evident on closer inspection.
- Face: invisible retouching, no geometry change.
- Sticker: smallest size that solves the aesthetic or privacy concern.
