<h1 align="center">Awesome Seedance 2.5 Prompts</h1>

<p align="center"><i>30 秒单镜直出 · 50 个全模态参考 · 局部级可控编辑。</i></p>

<p align="center">
  <a href="LICENSE"><img alt="License: CC BY 4.0" src="https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg"></a>
  <a href="https://tosea.ai/blog/seedance-2-5-bytedance-ai-video-model-guide"><img alt="Seedance 2.5 guide on Tosea.ai" src="https://img.shields.io/badge/Guide-Tosea.ai-000000?style=flat"></a>
  <img alt="Status: preview" src="https://img.shields.io/badge/Seedance%202.5-preview%20%C2%B7%20public%20launch%20July%202026-orange">
  <a href="https://github.com/ToseaAI/awesome-seedance-2.5-prompts/stargazers"><img alt="GitHub stars" src="https://img.shields.io/github/stars/ToseaAI/awesome-seedance-2.5-prompts?style=flat&color=yellow"></a>
</p>

<p align="center"><b>中文</b> · <a href="README.md">English</a></p>

为 **字节跳动 Seedance 2.5** 整理的开源 prompt 合集 —— 这款豆包视频生成模型于 **2026 年 6 月 23 日**火山引擎 FORCE 原动力大会上亮相,预计 **7 月初**正式上线。Prompt 按使用场景分类:文生视频、图生视频、多参考一致性、局部编辑与运镜。

> **状态** — Seedance 2.5 当前处于预览(企业内测),**尚未公开上线**。本仓库提前开张,为的是模型上线当天社区就有一个 Seedance 2.5 prompt 的归处。下列条目是作者撰写的**起手模板**,用于演示有效的 prompt 结构 —— 均已明确标注、不含任何虚构产出;待公开版上线后,会陆续加入社区贡献、带真实产出验证的 prompt。想一起共建?见[贡献指南](#贡献指南)。

## 什么是 Seedance 2.5?

Seedance 2.5 是字节跳动新一代视频模型。据 FORCE 主题演讲,三项核心升级:

- **30 秒单镜直出** —— 一段连续镜头直接生成(2.0 为 15 秒),叙事无需拼接。
- **最多 50 个全模态参考** —— 图像、视频、文字在一次联合生成中组合(2.0 为 12 个),用于跨镜头的角色与品牌一致性。
- **更可控的编辑** —— 局部级编辑(替换主体而不改动动作、机位与灯光),外加 3D 白模预演。

完整解析与横向对比,见我们的 [Seedance 2.5 指南](https://tosea.ai/blog/seedance-2-5-bytedance-ai-video-model-guide)。

## 目录

- [文生视频](#文生视频) · *2 条*
- [图生视频](#图生视频) · *1 条*
- [多参考一致性](#多参考一致性) · *2 条*
- [局部编辑](#局部编辑) · *1 条*
- [运镜与电影感](#运镜与电影感) · *2 条*

> 共 8 条起手 prompt,覆盖 5 个分类. [→ 阅读 Seedance 2.5 指南](https://tosea.ai/blog/seedance-2-5-bytedance-ai-video-model-guide)

## 文生视频

### 01. 城市黎明长镜头 · 30 秒一镜到底

*作者 **Tosea Team*** · `起手模板`

<a id="1-cinematic-city-dawn-oner"></a>

文生视频起手模板,用一段连续运镜验证 30 秒单镜直出能力。

<details>
<summary><b>Prompt</b> — 展开完整 prompt</summary>

<blockquote>A single continuous 30-second shot of a quiet metropolis at dawn. Open on wet asphalt reflecting the first warm light, then a slow forward dolly down an empty avenue as the city wakes: shop shutters lifting, steam rising from a vendor cart, a lone cyclist crossing frame. Soft golden-hour key light, long shadows, gentle volumetric haze. Anamorphic look, shallow depth of field, subtle film grain. Camera: steady ground-level dolly, no cuts. Duration: 30s. Aspect ratio 16:9.</blockquote>

</details>

**参数:** duration: 30s · aspect: 16:9 · refs: 0

---

### 02. 无缝棚拍产品揭示

*作者 **Tosea Team*** · `起手模板`

<a id="2-product-reveal-seamless"></a>

干净的商业文生视频模板 —— 描述产品、运镜与布光,背景保持无缝便于后期合成。

<details>
<summary><b>Prompt</b> — 展开完整 prompt</summary>

<blockquote>Studio product film of {PRODUCT}. The object floats and rotates slowly on a seamless gradient sweep (deep charcoal to soft graphite). A single large softbox key from upper left, subtle rim light tracing the silhouette, gentle specular highlights rolling across the surface as it turns. Macro detail on texture and edges. Camera: slow 180-degree orbit, locked focus on the product. Photoreal, commercial-grade, no text overlays. Duration: 12s. Aspect ratio 16:9.</blockquote>

</details>

**参数:** duration: 12s · aspect: 16:9 · refs: 0

---

## 图生视频

### 01. 让静态人像动起来

*作者 **Tosea Team*** · `起手模板`

<a id="3-still-portrait-to-life"></a>

图生视频模板:用一张人像作为首帧,只描述你想添加的动作。

<details>
<summary><b>Prompt</b> — 展开完整 prompt</summary>

<blockquote>Use the supplied portrait as the first frame. Add natural, subtle life: slow breathing, a soft blink, a faint smile forming, a few strands of hair drifting in a light breeze. Keep the identity, lighting, and framing exactly as in the reference image — no change to facial structure, wardrobe, or background. Gentle handheld micro-movement on the camera. Duration: 8s. Aspect ratio 9:16.</blockquote>

</details>

**参数:** duration: 8s · aspect: 9:16 · refs: 1

---

## 多参考一致性

### 01. 用参考素材集锁定角色一致性

*作者 **Tosea Team*** · `起手模板`

<a id="4-character-consistency-refset"></a>

多参考模板,用于验证 50 素材上限:输入角色转面图 + 服装 + 风格帧,让同一角色全程不走形。

<details>
<summary><b>Prompt</b> — 展开完整 prompt</summary>

<blockquote>References: [character turnaround images], [wardrobe close-ups], [one lighting/style frame]. Generate a 20-second scene in which this exact character walks through a sunlit warehouse toward a single shaft of window light, stops, and looks up. The character&#x27;s face, hairstyle, and outfit must match the references across every frame. Cool ambient fill, one warm hard light source. Camera: slow tracking push-in. Duration: 20s. Aspect ratio 16:9.</blockquote>

</details>

**参数:** duration: 20s · aspect: 16:9 · refs: 6

---

### 02. 用品牌素材包生成一致性广告

*作者 **Tosea Team*** · `起手模板`

<a id="5-brand-ad-reference-kit"></a>

输入产品图、包装、logo 与品牌色,让同一产品与配色在整支广告中保持锁定。

<details>
<summary><b>Prompt</b> — 展开完整 prompt</summary>

<blockquote>References: [product hero shots], [packaging], [logo lockup], [brand color swatches]. Generate a 15-second lifestyle ad: the product sits on a sunlit kitchen counter, a hand enters frame to pick it up, and the camera follows it toward a window. Product geometry, label, and brand colors must match the references exactly — no drift in logo or packaging. Warm naturalistic light, airy color grade. Camera: smooth follow with a rack focus to the label. Duration: 15s. Aspect ratio 16:9.</blockquote>

</details>

**参数:** duration: 15s · aspect: 16:9 · refs: 8

---

## 局部编辑

### 01. 替换主体而不改动镜头

*作者 **Tosea Team*** · `起手模板`

<a id="6-region-swap-subject"></a>

局部编辑模板:仅替换画面中的主体/产品,保留原片的动作、机位与灯光。

<details>
<summary><b>Prompt</b> — 展开完整 prompt</summary>

<blockquote>Take the supplied source clip. Replace only {ORIGINAL_SUBJECT} with {NEW_SUBJECT}. Do not change the camera movement, the timing, the lighting, the shadows, or the background. Match the new subject&#x27;s scale, contact shadows, and motion to the original so the edit is seamless. Output the full edited clip at the source resolution and duration.</blockquote>

</details>

**参数:** duration: match source · aspect: match source · refs: 1

---

## 运镜与电影感

### 01. 变形宽银幕推轨 + 焦点转移

*作者 **Tosea Team*** · `起手模板`

<a id="7-anamorphic-dolly-rack-focus"></a>

运镜语言模板 —— 明确写出镜头、运动与焦点变化,获得有意识的电影感摄影。

<details>
<summary><b>Prompt</b> — 展开完整 prompt</summary>

<blockquote>A 10-second cinematic shot of {SCENE}. Begin wide with the foreground out of focus; execute a slow dolly-in while racking focus from a foreground object to the subject in the midground. 2.39:1 anamorphic framing with horizontal lens flares, shallow depth of field, soft halation on highlights. Moody low-key lighting with one practical light motivating the key. Camera: motorized dolly, smooth ease-in. Duration: 10s. Aspect ratio 16:9 (letterboxed to 2.39:1).</blockquote>

</details>

**参数:** duration: 10s · aspect: 16:9 · refs: 0

---

### 02. 卡点动画解说片段

*作者 **Tosea Team*** · `起手模板`

<a id="8-animated-explainer-beat"></a>

短解说的动态图形模板:描述概念、节奏点与一套干净的视觉系统。

<details>
<summary><b>Prompt</b> — 展开完整 prompt</summary>

<blockquote>A 12-second animated explainer segment about {CONCEPT}. Clean flat-design motion graphics: simple geometric icons assembling and transforming on each beat, a restrained two-color palette plus one accent, generous negative space, smooth ease-in-out transitions. Numbers and labels animate in crisply and legibly. Light, optimistic pacing. No live action. Duration: 12s. Aspect ratio 16:9.</blockquote>

</details>

**参数:** duration: 12s · aspect: 16:9 · refs: 0

---

## 贡献指南

欢迎贡献 prompt。**请只修改 `prompts.json`** —— README 由 `scripts/build_readmes.py` 自动生成,手动改会在合并时被覆盖。公开版上线后,请附上产出视频/GIF 并署名 prompt 作者。数据结构见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## 许可协议

本合集采用 [CC BY 4.0](LICENSE) 协议。每条 prompt 的著作权归原作者所有,本仓库仅负责整理、翻译与分类。**Seedance**、**豆包(Doubao)** 为字节跳动商标;本项目为独立的社区资源,与字节跳动无隶属或背书关系。

<p align="center"><sub>Seedance 2.5 · announced 2026-06-23 at the Volcano Engine FORCE conference · public launch early July 2026 · Curated by <a href="https://tosea.ai">Tosea.ai</a> · Auto-generated from <code>prompts.json</code>.</sub></p>
