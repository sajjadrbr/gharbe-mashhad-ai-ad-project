# Local 10 GB RTX 3080 versus free online First/Last-Frame video — research
**Checked:** 2026-10-22. **Status:** literature/platform-feature review, no account login and no local new-model test.

## Why this was researched
User needs free/low-cost **start frame and end frame**, especially for controlled transitions in the 25–30s 9:16 fast-food promotion. User does not want new tens-of-GB downloads without a practical reason. Three existing Wan 2.2 5B 512²/49f local tests failed to follow motion directions consistently, despite largely holding mascot identity.

## Strongest candidate for free cloud testing: Vidu
- **First-party May 25, 2026 article** explicitly says “Features like first-and-last-frame control ... are available free on platforms like Vidu.” https://www.vidu.com/blog/ai-image-animator-free
- First-party Vidu UI workflow says start frame + optional second end frame: https://www.vidu.com/tools/ai-animation-generator
- Vidu API *supports* start-end-video (not proof of free UI eligibility): https://platform.vidu.com/docs/function-list
- Free credits cited in May article as 80/month plus off-peak free generation; **do not quote as Oct 2026 guaranteed quota**. Free output may have watermark and limited commercial rights/resolution. Current model-specific availability in actual user's free account was **not verified**.
- **Next action:** in a free Vidu account, navigate Image-to-Video/Start-End, upload two sample frames and check whether Generate shows free credits instead of an Upgrade demand **before spending**. If enabled, test identical 3–4-second tomato action as local benchmark.
- Other vendors (Kling, Runway, PixVerse) support start/end or keyframes on some models, but **no reliable confirmation** that exact feature is included in their current free plans: do not present as guaranteed free options.

## Local reality: 10GB VRAM does NOT categorically block newer/larger video models
- Quantization (GGUF Q4/Q5), CPU/RAM offload, smaller output dimensions/frame counts, staged VAE decode/upscaling can enable some checkpoints bigger than GPU VRAM, at the expense of speed, RAM/SSD use and potentially fidelity.
- **Wan2.2 I2V A14B + official First–Last Frame workflow**: ComfyUI first-party docs https://docs.comfy.org/tutorials/video/wan/wan2_2 and workflow https://comfy.org/workflows/video_wan2_2_14B_flf2v-7016f027bcf1/ . Standard 14B first/last weights are large, and 10GB execution would require **community quant/offload testing**, not guaranteed.
- **LTX-2.3 22B distilled / FLF2V**: official ComfyUI template https://github.com/Comfy-Org/workflow_templates/blob/main/templates/video_ltx2_3_flf2v.json and docs https://github.com/Comfy-Org/docs/blob/main/tutorials/video/ltx/ltx-2-3.mdx . Reports of limited 8GB workflows exist (https://www.reddit.com/r/StableDiffusion/comments/1t4ef4l/ltx23_8gb_vram_workflow/) but they are community demonstrations, not vendor guarantees; some GGUF checkpoints are >10GB *on disk* plus huge encoders. May take tens of minutes for short clips, depends on settings. This is more novel than user's 5B but its actual suitability is unverified.
- **Wan2.2 Fun InP official FLF2V** is **14B**, NOT evidence that a locally installed file labeled Fun Inpaint 5B can do first/last. Official https://docs.comfy.org/tutorials/video/wan/wan2-2-fun-inp . Need exact user disk filenames and workflow before claiming existing FLF support.

## Recommendation / decision state
1. Don't claim local model research is exhausted or cloud models categorically dominate. No 14B/LTX comparisons performed yet.
2. Verify user's total system RAM (16/32/64GB), available SSD capacity, and exact model filenames before any large local download or attempting 14B first-last.
3. Meanwhile Vidu free First/Last is the **first cloud candidate to verify interactively**; free usage is for tests, not a commercial-use license assumption.
4. Preserve ComfyUI/Wan for controllable pipeline and no-subscription video iterations. Evaluate one A/B sample before reallocating production.
**No model newly downloaded, no external service account tested, no new render generated in this research step.**
