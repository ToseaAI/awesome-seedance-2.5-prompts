<h1 align="center">Awesome Seedance 2.5 Prompts</h1>

<p align="center"><i>Direct 30-second clips. 50 multimodal references. Region-level control.</i></p>

<p align="center">
  <a href="LICENSE"><img alt="License: CC BY 4.0" src="https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg"></a>
  <a href="https://tosea.ai/prompts/seedance-2-5"><img alt="Gallery on Tosea.ai" src="https://img.shields.io/badge/Gallery-Tosea.ai-000000?style=flat"></a>
  <img alt="Status: preview" src="https://img.shields.io/badge/Seedance%202.5-preview%20%C2%B7%20public%20launch%20July%202026-orange">
  <a href="https://github.com/ToseaAI/awesome-seedance-2.5-prompts/stargazers"><img alt="GitHub stars" src="https://img.shields.io/github/stars/ToseaAI/awesome-seedance-2.5-prompts?style=flat&color=yellow"></a>
</p>

<p align="center"><b>English</b> · <a href="README.zh-CN.md">中文</a></p>

A curated, open-source collection of prompts for **ByteDance's Seedance 2.5** — the Doubao video generation model previewed at the Volcano Engine FORCE conference on **June 23, 2026**, with a public launch set for **early July 2026**. Prompts are organized by use case: text-to-video, image-to-video, multi-reference consistency, region editing, and camera work.

> **Status** — Seedance 2.5 is in preview (enterprise beta) and is **not yet publicly available**. This repository is opening early so the community has a home for Seedance 2.5 prompts the day the model ships. The entries below are author-built **starter templates** that demonstrate effective prompt structure — they are clearly labelled, carry no fabricated outputs, and will be joined by community-contributed, output-verified prompts as the public model rolls out. Want to help seed it? See [Contributing](#contributing).

## What Is Seedance 2.5?

Seedance 2.5 is ByteDance's next-generation video model. Per the FORCE keynote, its three headline upgrades are:

- **30-second single clips** — one continuous take, generated directly (up from 15s in Seedance 2.0), so narratives hold without stitching.
- **Up to 50 multimodal references** — images, video, and text combined in one joint generation (up from 12), for cross-shot character and brand consistency.
- **More controllable editing** — region-level edits (swap a subject without changing the motion, camera, or lighting) plus a 3D white-model previsualization step.

For the full breakdown and how it compares, read our [Seedance 2.5 guide](https://tosea.ai/blog/seedance-2-5-bytedance-ai-video-model-guide).

## Contents

- [Text-to-Video](#text-to-video) · *2 prompts*
- [Image-to-Video](#image-to-video) · *1 prompts*
- [Multi-Reference Consistency](#multi-reference-consistency) · *2 prompts*
- [Region Editing](#region-editing) · *1 prompts*
- [Camera & Cinematic](#camera--cinematic) · *2 prompts*

> 8 starter prompts across 5 categories. [→ View on Tosea](https://tosea.ai/prompts/seedance-2-5)

## Text-to-Video

### 01. Cinematic city dawn — a single 30-second oner

*by **Tosea Team*** · `starter template`

<a id="1-cinematic-city-dawn-oner"></a>

A starter text-to-video template that exercises the 30-second single-clip capability with one continuous camera move.

<details>
<summary><b>Prompt</b> — Show full prompt</summary>

<blockquote>A single continuous 30-second shot of a quiet metropolis at dawn. Open on wet asphalt reflecting the first warm light, then a slow forward dolly down an empty avenue as the city wakes: shop shutters lifting, steam rising from a vendor cart, a lone cyclist crossing frame. Soft golden-hour key light, long shadows, gentle volumetric haze. Anamorphic look, shallow depth of field, subtle film grain. Camera: steady ground-level dolly, no cuts. Duration: 30s. Aspect ratio 16:9.</blockquote>

</details>

**Parameters:** duration: 30s · aspect: 16:9 · refs: 0

**[→ View on Tosea](https://tosea.ai/prompts/seedance-2-5#1-cinematic-city-dawn-oner)**

---

### 02. Product reveal on a seamless studio sweep

*by **Tosea Team*** · `starter template`

<a id="2-product-reveal-seamless"></a>

A clean commercial T2V template — describe the product, the move, and the light; keep the background seamless for compositing.

<details>
<summary><b>Prompt</b> — Show full prompt</summary>

<blockquote>Studio product film of {PRODUCT}. The object floats and rotates slowly on a seamless gradient sweep (deep charcoal to soft graphite). A single large softbox key from upper left, subtle rim light tracing the silhouette, gentle specular highlights rolling across the surface as it turns. Macro detail on texture and edges. Camera: slow 180-degree orbit, locked focus on the product. Photoreal, commercial-grade, no text overlays. Duration: 12s. Aspect ratio 16:9.</blockquote>

</details>

**Parameters:** duration: 12s · aspect: 16:9 · refs: 0

**[→ View on Tosea](https://tosea.ai/prompts/seedance-2-5#2-product-reveal-seamless)**

---

## Image-to-Video

### 01. Bring a still portrait to life

*by **Tosea Team*** · `starter template`

<a id="3-still-portrait-to-life"></a>

Image-to-video template: supply one portrait as the first frame and describe only the motion you want added.

<details>
<summary><b>Prompt</b> — Show full prompt</summary>

<blockquote>Use the supplied portrait as the first frame. Add natural, subtle life: slow breathing, a soft blink, a faint smile forming, a few strands of hair drifting in a light breeze. Keep the identity, lighting, and framing exactly as in the reference image — no change to facial structure, wardrobe, or background. Gentle handheld micro-movement on the camera. Duration: 8s. Aspect ratio 9:16.</blockquote>

</details>

**Parameters:** duration: 8s · aspect: 9:16 · refs: 1

**[→ View on Tosea](https://tosea.ai/prompts/seedance-2-5#3-still-portrait-to-life)**

---

## Multi-Reference Consistency

### 01. Hold a character across a scene with a reference set

*by **Tosea Team*** · `starter template`

<a id="4-character-consistency-refset"></a>

Multi-reference template exercising the 50-reference ceiling: feed character turnarounds + wardrobe + a style frame to keep one character on-model.

<details>
<summary><b>Prompt</b> — Show full prompt</summary>

<blockquote>References: [character turnaround images], [wardrobe close-ups], [one lighting/style frame]. Generate a 20-second scene in which this exact character walks through a sunlit warehouse toward a single shaft of window light, stops, and looks up. The character&#x27;s face, hairstyle, and outfit must match the references across every frame. Cool ambient fill, one warm hard light source. Camera: slow tracking push-in. Duration: 20s. Aspect ratio 16:9.</blockquote>

</details>

**Parameters:** duration: 20s · aspect: 16:9 · refs: 6

**[→ View on Tosea](https://tosea.ai/prompts/seedance-2-5#4-character-consistency-refset)**

---

### 02. Brand-consistent ad from a reference kit

*by **Tosea Team*** · `starter template`

<a id="5-brand-ad-reference-kit"></a>

Feed product shots, packaging, logo, and brand colors so the same product and palette stay locked across the spot.

<details>
<summary><b>Prompt</b> — Show full prompt</summary>

<blockquote>References: [product hero shots], [packaging], [logo lockup], [brand color swatches]. Generate a 15-second lifestyle ad: the product sits on a sunlit kitchen counter, a hand enters frame to pick it up, and the camera follows it toward a window. Product geometry, label, and brand colors must match the references exactly — no drift in logo or packaging. Warm naturalistic light, airy color grade. Camera: smooth follow with a rack focus to the label. Duration: 15s. Aspect ratio 16:9.</blockquote>

</details>

**Parameters:** duration: 15s · aspect: 16:9 · refs: 8

**[→ View on Tosea](https://tosea.ai/prompts/seedance-2-5#5-brand-ad-reference-kit)**

---

## Region Editing

### 01. Swap a subject without touching the shot

*by **Tosea Team*** · `starter template`

<a id="6-region-swap-subject"></a>

Region-editing template: replace only the on-screen subject/product while preserving the original motion, camera, and lighting.

<details>
<summary><b>Prompt</b> — Show full prompt</summary>

<blockquote>Take the supplied source clip. Replace only {ORIGINAL_SUBJECT} with {NEW_SUBJECT}. Do not change the camera movement, the timing, the lighting, the shadows, or the background. Match the new subject&#x27;s scale, contact shadows, and motion to the original so the edit is seamless. Output the full edited clip at the source resolution and duration.</blockquote>

</details>

**Parameters:** duration: match source · aspect: match source · refs: 1

**[→ View on Tosea](https://tosea.ai/prompts/seedance-2-5#6-region-swap-subject)**

---

## Camera & Cinematic

### 01. Anamorphic dolly-in with a rack focus

*by **Tosea Team*** · `starter template`

<a id="7-anamorphic-dolly-rack-focus"></a>

A camera-language template — name the lens, the move, and the focus change explicitly to get deliberate cinematography.

<details>
<summary><b>Prompt</b> — Show full prompt</summary>

<blockquote>A 10-second cinematic shot of {SCENE}. Begin wide with the foreground out of focus; execute a slow dolly-in while racking focus from a foreground object to the subject in the midground. 2.39:1 anamorphic framing with horizontal lens flares, shallow depth of field, soft halation on highlights. Moody low-key lighting with one practical light motivating the key. Camera: motorized dolly, smooth ease-in. Duration: 10s. Aspect ratio 16:9 (letterboxed to 2.39:1).</blockquote>

</details>

**Parameters:** duration: 10s · aspect: 16:9 · refs: 0

**[→ View on Tosea](https://tosea.ai/prompts/seedance-2-5#7-anamorphic-dolly-rack-focus)**

---

### 02. Beat-synced animated explainer segment

*by **Tosea Team*** · `starter template`

<a id="8-animated-explainer-beat"></a>

A motion-graphics template for short explainers: describe the concept, the beats, and a clean visual system.

<details>
<summary><b>Prompt</b> — Show full prompt</summary>

<blockquote>A 12-second animated explainer segment about {CONCEPT}. Clean flat-design motion graphics: simple geometric icons assembling and transforming on each beat, a restrained two-color palette plus one accent, generous negative space, smooth ease-in-out transitions. Numbers and labels animate in crisply and legibly. Light, optimistic pacing. No live action. Duration: 12s. Aspect ratio 16:9.</blockquote>

</details>

**Parameters:** duration: 12s · aspect: 16:9 · refs: 0

**[→ View on Tosea](https://tosea.ai/prompts/seedance-2-5#8-animated-explainer-beat)**

---

## Contributing

We welcome prompt contributions. **Only edit `prompts.json`** — the READMEs are auto-generated by `scripts/build_readmes.py` and will be overwritten on merge. Once the public model ships, attach the output video/GIF and credit the prompt's author. See [CONTRIBUTING.md](CONTRIBUTING.md) for the schema.

## License

This collection is released under [CC BY 4.0](LICENSE). Individual prompts remain the intellectual property of their authors; we curate, translate, and categorize. **Seedance** and **Doubao** are trademarks of ByteDance; this is an independent, community resource and is not affiliated with or endorsed by ByteDance.

<p align="center"><sub>Seedance 2.5 · announced 2026-06-23 at the Volcano Engine FORCE conference · public launch early July 2026 · Curated by <a href="https://tosea.ai">Tosea.ai</a> · Auto-generated from <code>prompts.json</code>.</sub></p>
