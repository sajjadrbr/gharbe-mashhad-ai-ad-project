# MASTER SDXL Workflows — v2

**Date:** 2026-10-21
**Status:** Three reusable ComfyUI workflow JSON files created, linked, structurally validated and committed. Actual execution on the user's Windows ComfyUI is **not yet tested**.

## Workflows
- [MASTER_Text2Image_SDXL_v2.json](MASTER_Text2Image_SDXL_v2.json): generate a new scene or character from a positive and negative prompt.
- [MASTER_Img2Img_SDXL_v2.json](MASTER_Img2Img_SDXL_v2.json): upload an image, describe a change, adjust KSampler denoise (default 0.35).
- [MASTER_Inpaint_SDXL_v2.json](MASTER_Inpaint_SDXL_v2.json): upload image, open MaskEditor, paint the area to change, describe replacement, adjust denoise (default 0.80).

## Main interface
All three use two large, separately titled editable **PrimitiveStringMultiline** nodes:
- **POSITIVE PROMPT — WRITE HERE** (green)
- **NEGATIVE PROMPT — WRITE HERE** (red)

Each prompt node feeds BOTH `text_g` and `text_l` on the corresponding `CLIPTextEncodeSDXL`, avoiding duplicate edits. The workflow is not specific to any character, burger shop, or future client.

## Current model defaults, user-adjustable
- SDXL checkpoint `DreamShaperXL1.0Alpha2_fixedVae_half_00001_.safetensors`.
- Style LoRA `3D_Animation_Style-000009.safetensors` at 0.8 model / 0.8 CLIP; set both to **0** to disable.
- KSampler 30 steps, CFG 5.5, DPM++ 2M / Karras.
- Text2Image latent 832×1472 (near 9:16). For square character assets use 1024×1024.
- Img2Img / Inpaint SDXL conditioning defaults 1024×1024; **change the SDXL width/height/target_width/target_height on both encoders** for other input sizes.

## Import and first run
1. Drag the JSON onto the ComfyUI canvas.
2. Select the locally installed checkpoint and LoRA if their actual dropdown paths differ (a checkpoint under an `SDXL/` subfolder may need adjustment).
3. Write prompts inside green and red prompt nodes. Do not edit the text widgets inside the SDXL encoders directly.
4. For Img2Img and Inpaint, the preset LoadImage filename is **a placeholder**. Upload the image first.
5. For Inpaint, open the input LoadImage MaskEditor, paint the desired edit zone, save mask; then run.
6. After validation in the user's installation, save a separate version for each client/shot, preserving the MASTER templates unchanged.

## Why v2 Inpaint is different
The former `VAEEncodeForInpainting` + low-denoise approach produced gray artifacts in the SDXL sausage test. The v2 template uses **regular VAEEncode → SetLatentNoiseMask**, followed by **ImageCompositeMasked** to keep the original pixels outside the edited mask. This avoids the known gray prefill step and protects untouched regions, but **does not guarantee** clean edits at the mask edge or character preservation.

## Important limits
- Image-to-image and masked edits can change undesired features. Prompt alone cannot guarantee visual identity or anatomy.
- The LoRA/checkpoint choices are defaults, not guaranteed best for all projects.
- These are SDXL workflows; changing to Flux, Wan or SD1.5 requires architecture-specific nodes and models.
- Only the graph structure was checked offline. No models were downloaded or ComfyUI inference executed in this update.
