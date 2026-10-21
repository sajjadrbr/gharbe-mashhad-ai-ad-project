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
