# Prompt Recipes

Read this file when composing an edit prompt. Use only the modules required by the request, and repeat the preservation block every time.

## Base identity-preserve block

```text
Use case: identity-preserve
Asset type: polished high-resolution social-media portrait
Input images: Image 1 is the edit target and must remain the visual base.
Constraints: Preserve the exact identity, age, facial proportions, expression, head angle, hairstyle unless specified, body size and proportions, pose, hands and fingers, phone and case, crop, camera viewpoint, background objects, and scene geometry. Preserve natural pores and real skin texture.
Avoid: identity drift, invented hidden facial features, plastic skin, waxy smoothing, excessive whitening, blue-gray skin, anatomy distortion, object changes, extra fingers, added text, logos, or watermarks.
```

## HD cool-white module

```text
Primary request: Increase fine detail and perceived resolution; reduce noise, compression artifacts, muddiness, and color contamination. Correct the strong yellow/orange cast toward a neutral-to-cool white balance. Render skin as naturally luminous cool ivory with controlled highlights, gentle shadow detail, and believable indoor light direction. Preserve pores and fine hair. Avoid crunchy oversharpening, broad blur, blown highlights, and dead-white skin.
```

## Subtle lean-muscle module

```text
Primary request: Based strictly on the existing physique, reveal only very subtle lean-muscle definition using delicate directional light and tonal separation. Keep exact body size, weight, shoulder width, waist width, posture, and body-fat impression. Add a faint pectoral lower edge, a soft central abdominal line, extremely subtle upper-ab and oblique contours, and mild shoulder/upper-arm separation. The result must read as slim and lightly trained. Avoid added mass, a narrower waist, wider shoulders, deep six-pack grooves, vascularity, carved lines, or a bodybuilding look.
```

## Invisible face-refinement module

```text
Primary request: Apply extremely subtle, invisible-looking facial refinement. Reduce only distracting forehead shine, brighten the visible under-eye by about 10%, add delicate natural tonal depth along the visible temple and cheek edge, and marginally clarify the visible jaw edge through light and shadow. Slightly neaten excessive hairstyle width while preserving the haircut and hairline. Do not slim the face, reduce cheekbones, point the chin, enlarge the eyes, alter eyebrows, move the hairline, enforce symmetry, or reconstruct obscured features.
```

## Frosted sticker module

```text
Use case: precise-object-edit
Primary request: Add one small semi-transparent silver-gray frosted smear over the visible eye/upper-face area, positioned as an intentional editorial social-media graphic. Let it overlap the phone edge slightly if natural. Keep the hair silhouette visible and preserve the cool-white premium mood. Change only the sticker area; preserve the person, body, phone, pose, lighting, crop, and background exactly.
Avoid: cartoon styling, large stickers, crude mosaic pixels, black censor bars, bright saturated colors, text, logos, or watermarks.
```

## Targeted retry phrases

Use one correction at a time:

- `Reduce the muscle definition by half; restore the original body volume and waist width.`
- `Restore the source identity and eye shape; keep only the lighting cleanup.`
- `Restore natural pores and reduce skin smoothing.`
- `Make the skin less white and more naturally cool ivory.`
- `Shrink the sticker by 25% and keep the hair silhouette unobstructed.`
- `Restore the original crop, phone, hand anatomy, and background geometry.`
