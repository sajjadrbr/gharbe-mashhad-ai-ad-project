# Character & Asset Register — پروژه غرب مشهد

**Updated:** 2026-10-21 · **Authority:** [PROJECT_STATUS.md](PROJECT_STATUS.md)
**Legend:** approved visual anchor ≠ animation-ready rig or verified reusable model.

## A-001 — Sausage mascot / سوسیس بازیگوش

**Current state: VISUAL REFERENCE APPROVED for next production stage**, not yet animation-ready.

### Provenance
1. Local SDXL character exploration: `SDXL_00010` (animal-like reject), `SDXL_00011` (hotdog mascot), `SDXL_00012` (extra arm), `SDXL_00013` (gray inpaint artifact), `SDXL_00014` (white residual), `SDXL_00018` (smaller remnant).
2. Local reusable V2 workflows: `MASTER_I2I_00001_.png` (best clean pre-inpaint base, but two torso bumps); `MASTER_I2I_00002_.png` (0.45 caused body texture/bumps: reject); `MASTER_I2I_00003_.png` (mistaken global I2I when nasal localized edit expected: reject).
3. Local `MASTER_INPAINT_00001_.png` (damaged nose), `MASTER_INPAINT_00003_.png` (successful localized nose-only correction; nose still prominent), `MASTER_INPAINT_00004_.png` (more coherent nose, **two torso bumps remain**).
4. A separate assistant-produced image edit of the provided character removed both torso bumps. User responded **«اوکی»** and instructed documentation then progression. Visually clean, full-body reddish-brown sausage on soft gray studio background, one arm on each side, two short legs, expressive eyes and friendly smile. This is the **approved clean visual anchor**.
5. **Critical provenance limit:** the approved final clean image was produced through a separate image generation/editing tool in the chat, **not** by a reproducible local ComfyUI Inpaint run. It may differ subtly in features, pose, lighting and framing from `MASTER_INPAINT_00004_.png`. It is not evidence that local ComfyUI eliminated both bumps. Store the actual approved PNG in the project asset folder before future compositing; binary has **not** been committed to GitHub. GitHub includes description/status only.

### Design guidelines / constraints
- One continuous smooth reddish-brown sausage body, clear capsule silhouette.
- Exactly two arms, two legs, no duplicate limb and no unwanted bumps.
- Large expressive brown eyes, rounded nose, clean smiling mouth.
- Premium original stylized 3D animated-film material and lighting.
- Reference pose is a neutral smiling wave; shot A additionally needs a **mischievous action expression and grill-compatible pose**. These variations **are not yet generated or approved**.
- Avoid clothes, sneakers, text, logos, human skin pores, animal features.
- **Not a 3D model, character rig, transparent PNG or turnaround sheet.** Front image alone cannot guarantee consistent additional camera angles.

### File handling
- Suggested local names: `assets/characters/sausage/SAUSAGE_MASTER_CLEAN_V1.png`; `assets/characters/sausage/REFERENCE_NOTES.md`.
- Filename is a **planned convention**; physical file placement in user's Windows workspace has **not been verified**.
- Preferred next test after other character assets: one short 2–4s Wan video based on an already composed scene, monitor identity drift.

## A-002 — Tomato mascot / گوجه بازیگوش

**State:** NEXT TO DESIGN; no image approved.

- Shot B lead: cheeky energetic tomato, leaps past pickle and onto springy lettuce.
- Distinctly round red tomato silhouette, tiny green leaf crown; expressive eyes, clear limbs, movement-friendly pose.
- Character on clean studio background, full body, separated from props.
- Match the sausage's soft high-end stylized 3D shape language and light direction, not photoreal produce skin.
- First deliverable: one `1024×1024` master portrait from [MASTER_Text2Image_SDXL_v2.json](workflows/MASTER_Text2Image_SDXL_v2.json). Then assess before producing alternatives.
- Prompt/negative/acceptance checklist recorded in [NEXT_ASSET_TOMATO_BRIEF.md](NEXT_ASSET_TOMATO_BRIEF.md).

## A-003 — Pickle / خیارشور
**State:** planned, not started. Supports Shot B; must be visually distinct from tomato and may be simpler/less anthropomorphic.

## A-004 — Grill chef / سرآشپز
**State:** planned. Contributes Shot A spatula gag. Needs deliberate design and clear hands/spatula interaction.

## A-005 — Kitchen environment / آشپزخانه
**State:** no approved style/layout anchor. Previous SDXL environment attempts were cluttered or too realistic.
**Required geography:** grill left with two burger patties; prep station right; central hero burger counter; film crew behind/right for final reveal.
Create clean set plate without living characters first; avoid repeated burgers.

## A-006 — Burger hero product / برگر نهایی
**State:** planned. Hero food product (not a cartoon mascot); appetizing patty, melted cheese, produce and bun are critical.

## A-007 — Film crew / گروه تصویربرداری
**State:** planned, for Shot D surprise reveal.

## A-008 — Realistic presenter / مرد رئال
**State:** planned. Brother's usable face reference **not supplied**; no claim of likeness or identity consistency.

## Production priority
1. Lock cleaned sausage as visual anchor and keep source image outside repo securely.
2. Tomato lead for Shot B, then pickle/supporting ingredients.
3. Character styling alignment / chef and interior plate, then composite shots.
4. Grill patties and hero burger plate, film crew reveal, coherent shot keyframes.
5. Tiny Wan 2.2 tests per shot; assemble and add sound/branding.

**Current bottleneck:** not more nose/torso cleanup; it is achieving character-to-environment style consistency and reliable shot composition.
