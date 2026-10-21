# Next Asset Brief — Tomato Mascot (Shot B)

**Stage:** prompt ready · first render not yet run
**Workflow:** [MASTER_Text2Image_SDXL_v2.json](workflows/MASTER_Text2Image_SDXL_v2.json)
**Checkpoint:** DreamShaperXL1.0Alpha2_fixedVae_half_00001_.safetensors
**LoRA:** 3D_Animation_Style-000009.safetensors (model 0.8, clip 0.8)
**Starting render settings:** 1024×1024 **on EmptyLatentImage AND both CLIPTextEncodeSDXL nodes**; steps 30; CFG 5.5; dpmpp_2m/karras; one image; save seed.

## Positive (copy into green prompt node)
A single original mischievous ripe red tomato character for a premium stylized 3D animated feature film, full-body character design centered in a clean neutral gray studio background. Clear perfectly round plump tomato silhouette, subtle natural lobes, tiny recognizable green leafy calyx on the top. Deep appetizing glossy-red tomato skin with smooth sculpted form, not human skin. Exactly two short thin cartoon arms with small expressive hands and exactly two tiny legs and feet. Wide expressive eyes, one raised eyebrow, playful confident sideways smirk, energetic cheeky troublemaker personality, poised as if about to spring into action. Elegant dimensional sculpting, refined 3D materials, soft subsurface scattering, cinematic softbox lighting with subtle rim light, coherent premium animated-movie aesthetics, soft floor shadow, simple uncluttered composition, whole character visible, isolated one subject.

## Negative (copy into red prompt node)
multiple tomatoes, multiple characters, extra arms, extra legs, duplicated limbs, missing hands, creepy human face, human skin, human body, face on another object, sausage shape, apple, strawberry, pepper, red balloon, melted body, floating parts, oversized feet, shoes, clothing, props, kitchen background, tables, plates, text, watermark, logo, photorealistic macro food photograph, flat drawing, ugly plastic material, distorted eyes, clutter.

## Acceptance criteria
- Immediately readable as a **tomato**, distinct from sausage and from an apple.
- Exactly one character and four limbs; friendly mischievous face rather than babyish human face.
- Studio-style lighting and 3D material broadly compatible with approved clean sausage.
- Silhouette and posing useful for Shot B jumping gag.
- No unnecessary objects, writing or a kitchen set.
- No extra download; inspect **one** result before adjusting prompt or seed.

## Continuity notes
After first approval, store actual image locally (suggested: `assets/characters/tomato/TOMATO_MASTER_V1.png`). Filename/approval not yet confirmed. Reference image of sausage should be visually compared side by side; SDXL prompt alone does not guarantee identical character style.

## First result review: MASTER_T2I_00001_ (2026-10-21)
- Actual ComfyUI image received. Good round tomato body, readable expression and cinematic 3D treatment. **Not approved final character** because foliage looks like tall hair, green claw hands/long vine legs and shoes, orange protruding nose and oversized smile mismatch the clean sausage design.
- Do ONE controlled rerender with the same checkpoint/LoRA/size/seed (if available) and revised prompt below. Compare result; don't default to multi-region inpainting.

### Revised positive prompt (v2)

```text
Single mischievous bright red ripe tomato mascot, premium original stylized 3D animated feature-film character. One plump, clearly round tomato body, smooth glossy red skin with gentle natural lobes, a tiny flat five-point green calyx directly on top, not tall leaves. Large expressive green eyes, slightly raised eyebrow, small cheeky asymmetric closed-mouth smirk, playful confident troublemaker attitude. Exactly two short thin flexible reddish-red arms, each ending in one rounded simplified cartoon hand, exactly two short reddish-red legs with small simple rounded feet matching the tomato body. No clothing or footwear. Clear uncluttered silhouette, playful ready-to-jump pose, tasteful sculpted forms, clean studio gray backdrop, soft warm cinematic studio light, subtle rim light, gentle floor shadow, same polished simple shape language and material quality as a premium 3D animated sausage mascot. One full-body character, centered composition.
```

### Revised negative prompt (v2)

```text
big tall leaves, spiky hair, jungle plant, plant monster, vine tentacles, green claw hands, sharp claws, long skinny legs, shoes, boots, orange nose, yellow nose, human nose, large beak, gaping oversized mouth, human body, animal body, extra limbs, duplicate hands, deformed fingers, multiple characters, apple, strawberry, pepper, glossy plastic toy, creepy face, messy background, product label, text, watermark, logo, duplicate eyes
```

## Second result review: MASTER_T2I_00002_ (2026-10-21)
- Second local render received after the revised positive/negative prompts. **Improved** compared to first: recognizable red round tomato, shorter green crown, red simplified hands, red nose, engaging 3D rendering.
- **Not yet a final approved TOMATO_MASTER**: the model added red sneakers despite negative prompt, long thin green legs, oversized hands giving two thumbs-up, and a big friendly open smile instead of the specified sly asymmetrical smirk.
- Candidate name for continued art direction: `TOMATO_CONCEPT_V2`, not a new finalized asset file or verified GitHub image.
- Avoid uncontrolled global resampling. Proposed next action after user approval: keep as provisional reference; continue to pickle mascot. Revisit specific issues (footwear/leg proportions/action pose) during shot-B posing/compositing.

## User-directed third T2I prompt test — 2026-10-21
- User explicitly requested **one more prompt-only Text2Image attempt before trying Inpaint**. The previously suggested immediate Inpaint plan is postponed.
- Target changes from `MASTER_T2I_00002_.png`: remove red sneakers, replace vine-like long green legs with two short rounded red legs/feet, shrink huge thumbs-up hands, use asymmetrical mischievous closed-mouth smirk instead of friendly ad smile.
- **Positive prompt (trial 3; not yet rendered):**
```text
A single adorable mischievous anthropomorphic ripe red tomato character, original premium stylized 3D animated feature film character design.

A large plump perfectly round red tomato body, slightly wider than tall, smooth vibrant red tomato skin, subtle natural tomato shape, tiny flat green five-point leafy calyx on top of the head.

The big round tomato body is the main visual feature.

Exactly two very short stubby reddish-red legs, tiny simple rounded red feet, feet directly connected to the short legs, compact proportions.

Exactly two short thin reddish-red cartoon arms with small soft rounded hands and simple fingers, naturally proportioned, not oversized.

One arm slightly bent in a playful scheming gesture, the other arm relaxed and slightly raised, natural lively pose.

Big expressive green eyes, one eyebrow playfully raised, a clever cheeky asymmetric smirk, small closed smiling mouth, confident mischievous personality, as if planning a funny prank.

Minimal simple appealing character design, clean readable silhouette, rounded sculpted shapes, refined smooth materials, soft subsurface scattering, warm soft cinematic studio lighting.

Full body visible, standing on a simple neutral gray studio floor, gentle contact shadow, centered character, clean background, high-end 3D animated movie quality.
```
- **Negative prompt (trial 3; not yet rendered):**
```text
sneakers, shoes, boots, footwear, socks, laces, clothing, gloves, long legs, skinny legs, green legs, vine legs, plant stems as legs, long arms, giant hands, oversized fists, thumbs up gesture, pointing thumbs, giant smile, wide open mouth, huge teeth, orange nose, big nose, plant monster, claws, tentacles, spiky hair, tall leaves, thick stem, extra limbs, duplicate arms, extra fingers, deformed feet, human body, realistic human skin, apple, pepper, strawberry, multiple tomatoes, multiple characters, plastic toy, flat illustration, messy background, text, logo, watermark
```
- Workflow `MASTER_Text2Image_SDXL_v2.json`; 1024x1024 on latent AND both SDXL encoders, same DreamShaper XL and 3D animation LoRA 0.8/0.8, steps=30, CFG=5.5, dpmpp_2m/karras, denoise=1, fixed seed matching prior if available.
- **Important:** T2I doesn't actually condition on `MASTER_T2I_00002_.png` (no reference image node), so output likeness is not guaranteed. **NEXT STEP:** one render, then compare; Inpaint only if prompt-only fails and user approves.
