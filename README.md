# 🌌 Awesome FLUX 3 — API, Prompts & Complete Guide

> The ultimate resource for FLUX 3 — Black Forest Labs' new unified multimodal frontier model for image, video, and audio generation. Covers API integration, prompt engineering, multimodal workflows, and 20+ curated production-ready prompt examples.

[![FLUX 3](https://img.shields.io/badge/FLUX-3-8b5cf6)](https://bfl.ai/models/flux-3)
[![Powered by MuAPI](https://img.shields.io/badge/Powered%20by-MuAPI-6366f1?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMiAyQzYuNDggMiAyIDYuNDggMiAxMnM0LjQ4IDEwIDEwIDEwIDEwLTQuNDggMTAtMTBTMTcuNTIgMiAxMiAyem0tMSAxNHYtNGgtMnYtMmg0djZoLTJ6bTAtOFY2aDJ2MmgtMnoiLz48L3N2Zz4=)](https://muapi.ai?utm_source=github&utm_medium=badge&utm_campaign=awesome-flux-3)
[![Stars](https://img.shields.io/github/stars/Anil-matcha/awesome-flux-3-api-prompts?style=social)](https://github.com/Anil-matcha/awesome-flux-3-api-prompts)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 🚀 Get Early Access

FLUX 3 was announced by Black Forest Labs on **July 23, 2026** as a unified multimodal frontier model — the same architecture jointly generates image, video, and native synchronized audio, and extends to action-prediction for robotics. **[MuAPI](https://muapi.ai/flux-3?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3)** is preparing 5 FLUX 3 endpoints and will activate each one automatically for existing API keys as Black Forest Labs opens general availability — no separate waitlist required.

**[→ Get an API key now for FLUX 3 early access](https://muapi.ai/flux-3?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3)**

---

## Related Projects

- [awesome-seedance-2.5-api-prompts](https://github.com/Anil-matcha/awesome-seedance-2.5-api-prompts) — ByteDance Seedance 2.5 API guide and prompt library
- [awesome-ai-image-models](https://github.com/Anil-matcha/awesome-ai-image-models) — the most complete, up-to-date comparison of AI image generation models
- [awesome-ai-video-models](https://github.com/Anil-matcha/awesome-ai-video-models) — the most complete, up-to-date comparison of AI video generation models
- [Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI) — open-source, self-hosted AI image & video generation studio (200+ models, no content filters)
- [ai-creator-academy](https://github.com/Anil-matcha/ai-creator-academy) — free curriculum teaching creators how to monetize FLUX and other generative AI models

---

## Table of Contents

- [What is FLUX 3?](#what-is-flux-3)
- [FLUX 3 vs FLUX.2 — What's New](#flux-3-vs-flux2--whats-new)
- [FLUX 3 Variants](#flux-3-variants)
- [API Reference (MuAPI)](#api-reference-muapi)
  - [Text-to-Image](#1-flux-3-text-to-image)
  - [Image-to-Image (Edit)](#2-flux-3-image-to-image-edit)
  - [FLUX 3 Dev](#3-flux-3-dev)
  - [Text-to-Video](#4-flux-3-text-to-video)
  - [Image-to-Video](#5-flux-3-image-to-video)
  - [Polling for Results](#polling-for-results)
  - [Parameters](#muapi-parameters)
- [Prompt Engineering Guide](#prompt-engineering-guide)
  - [The 5-Part Formula](#the-5-part-formula)
  - [Lighting & Camera Vocabulary](#lighting--camera-vocabulary)
  - [Multi-Reference Editing Syntax](#multi-reference-editing-syntax)
- [Prompt Library](#prompt-library)
  - [🌟 Featured Photorealistic Prompts](#-featured-photorealistic-prompts)
  - [🎨 Editing & Restyling](#-editing--restyling)
  - [📦 Product & E-commerce](#-product--e-commerce)
  - [🎬 Video with Native Audio](#-video-with-native-audio)
  - [🚀 Concept & Sci-Fi](#-concept--sci-fi)
- [Tips & Best Practices](#tips--best-practices)
- [API Providers Comparison](#api-providers-comparison)
- [Resources & Links](#resources--links)

---

## What is FLUX 3?

**FLUX 3** is Black Forest Labs' newest frontier model, announced July 23, 2026, as a unified multimodal system trained jointly across **image, video, and audio** within a single architecture — and extendable to **action prediction** for robotics. It is the successor to the FLUX.2 family (FLUX.2 Pro, FLUX.2 Dev, FLUX.2 Klein) and to [FLUX Kontext](https://muapi.ai/flux-kontext?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3) for editing.

Key points from the announcement:

- **Unified architecture** — the same "Self-Flow" approach powers FLUX 3 Image, FLUX 3 Video, and FLUX 3 Action, so video motion and physical plausibility benefit from the same training signal that also drives robotics action-prediction
- **Native synchronized audio** — FLUX 3 Video can generate scene-appropriate ambient audio directly alongside the clip, no separate TTS/audio-sync step
- **Phased rollout** — FLUX 3 Video and FLUX 3 Action entered early access on announcement day; FLUX 3 Image is rolling out in the following weeks
- **Open-weight plans** — Black Forest Labs has confirmed faster, open-weight versions of FLUX 3 will ship later in 2026, continuing the open-access approach from FLUX.1 and FLUX.2
- **Launch partners** — early testers include Canva, Burda, Magnific, Krea, and Picsart; FLUX-mimic (the video-action model) is being tested with Audi and other manufacturers

FLUX 3 accepts **text and reference images** as input for image generation/editing, and **text plus an optional start-frame image** for video, outputting stills or MP4 clips with optional native audio.

---

## FLUX 3 vs FLUX.2 — What's New

| Feature | FLUX.2 | FLUX 3 |
|---|---|---|
| Modalities | Image only | Image, video, audio (unified) |
| Architecture | Diffusion image model | Self-Flow unified multimodal model |
| Video generation | Not supported | Native, with optional synchronized audio |
| Physical plausibility | Image-level only | Reinforced by shared video/action training |
| Open-weight variant | FLUX.2 Klein / Dev | FLUX 3 Dev (planned later in 2026) |
| Editing | FLUX Kontext / FLUX.2 edit | FLUX 3 Image-to-Image (successor) |
| Action prediction | Not applicable | FLUX 3 Action (robotics) |

---

## FLUX 3 Variants

| Variant | Modality | Status |
|---|---|---|
| FLUX 3 Text-to-Image | Image | Rolling out in the coming weeks |
| FLUX 3 Image-to-Image | Image edit | Rolling out in the coming weeks |
| FLUX 3 Dev | Image (fast/low-cost) | Planned, open-weight later in 2026 |
| FLUX 3 Text-to-Video | Video + audio | Early access |
| FLUX 3 Image-to-Video | Video + audio | Early access |

> **[See live status & get API access on MuAPI →](https://muapi.ai/flux-3?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3)**

---

## API Reference (MuAPI)

The fastest way to access FLUX 3 via API — the moment each variant goes live — is through **[MuAPI](https://muapi.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3)**, a unified generative-media API gateway. One API key activates every FLUX 3 endpoint automatically as Black Forest Labs opens general availability — no separate signup.

**Get your API key:** [muapi.ai/flux-3](https://muapi.ai/flux-3?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3)

```bash
x-api-key: YOUR_MUAPI_KEY
Base URL: https://api.muapi.ai/api/v1
```

---

### 1. FLUX 3 Text-to-Image

**Endpoint:** `POST https://api.muapi.ai/api/v1/flux-3-text-to-image`

```bash
curl -X POST "https://api.muapi.ai/api/v1/flux-3-text-to-image" \
  -H "Content-Type: application/json" \
  -H "x-api-key: YOUR_API_KEY" \
  -d '{
      "prompt": "A hyperrealistic portrait of an astronaut standing on red Martian dunes at golden hour, dust particles catching the light, ultra-detailed suit reflections, cinematic depth of field",
      "aspect_ratio": "16:9",
      "resolution": "2k"
  }'
```

**Python:**
```python
import requests

response = requests.post(
    "https://api.muapi.ai/api/v1/flux-3-text-to-image",
    headers={"x-api-key": "YOUR_API_KEY", "Content-Type": "application/json"},
    json={
        "prompt": "A hyperrealistic portrait of an astronaut standing on red Martian dunes at golden hour",
        "aspect_ratio": "16:9",
        "resolution": "2k"
    }
)
request_id = response.json()["request_id"]
```

---

### 2. FLUX 3 Image-to-Image (Edit)

**Endpoint:** `POST https://api.muapi.ai/api/v1/flux-3-image-to-image`

```bash
curl -X POST "https://api.muapi.ai/api/v1/flux-3-image-to-image" \
  -H "Content-Type: application/json" \
  -H "x-api-key: YOUR_API_KEY" \
  -d '{
      "prompt": "Replace the background with a neon-lit city street at night, keep the subject unchanged",
      "images_list": ["https://example.com/input.jpg"],
      "aspect_ratio": "1:1"
  }'
```

---

### 3. FLUX 3 Dev

**Endpoint:** `POST https://api.muapi.ai/api/v1/flux-3-dev`

```bash
curl -X POST "https://api.muapi.ai/api/v1/flux-3-dev" \
  -H "Content-Type: application/json" \
  -H "x-api-key: YOUR_API_KEY" \
  -d '{
      "prompt": "A minimalist product shot of a ceramic mug on a wooden table, soft natural light",
      "aspect_ratio": "1:1",
      "resolution": "1k"
  }'
```

---

### 4. FLUX 3 Text-to-Video

**Endpoint:** `POST https://api.muapi.ai/api/v1/flux-3-text-to-video`

```bash
curl -X POST "https://api.muapi.ai/api/v1/flux-3-text-to-video" \
  -H "Content-Type: application/json" \
  -H "x-api-key: YOUR_API_KEY" \
  -d '{
      "prompt": "A drone shot glides over a bioluminescent forest at night, fireflies drifting between glowing trees, gentle mist rolling across the forest floor",
      "aspect_ratio": "16:9",
      "resolution": "1080p",
      "duration": 6,
      "generate_audio": true
  }'
```

---

### 5. FLUX 3 Image-to-Video

**Endpoint:** `POST https://api.muapi.ai/api/v1/flux-3-image-to-video`

```bash
curl -X POST "https://api.muapi.ai/api/v1/flux-3-image-to-video" \
  -H "Content-Type: application/json" \
  -H "x-api-key: YOUR_API_KEY" \
  -d '{
      "prompt": "The camera slowly pushes in as steam rises from the coffee cup",
      "images_list": ["https://example.com/product.jpg"],
      "duration": 5,
      "generate_audio": true
  }'
```

---

### Polling for Results

All MuAPI endpoints return a `request_id`. Poll until `status` is `completed`:

```python
import time, requests

def wait_for_result(request_id, api_key, poll_interval=5, timeout=300):
    start = time.time()
    while time.time() - start < timeout:
        res = requests.get(
            f"https://api.muapi.ai/api/v1/predictions/{request_id}/result",
            headers={"x-api-key": api_key}
        ).json()
        if res["status"] == "completed":
            return res["outputs"][0]
        elif res["status"] == "failed":
            raise Exception(res.get("error", "Generation failed"))
        time.sleep(poll_interval)
    raise TimeoutError("Generation timed out")

output_url = wait_for_result(request_id, "YOUR_API_KEY")
print(f"Output: {output_url}")
```

---

### MuAPI Parameters

| Parameter | Type | Options | Default | Applies To |
|---|---|---|---|---|
| `prompt` | string | — | required | All |
| `images_list` | array | URLs | — | Image-to-Image, Image-to-Video |
| `aspect_ratio` | string | `16:9` `9:16` `1:1` `4:3` `3:4` `2:3` `3:2` `21:9` | `1:1` | Image variants |
| `resolution` | string | `1k` `2k` `4k` (image) / `480p` `720p` `1080p` (video) | `2k` / `720p` | All |
| `duration` | int | `4`–`10` | `5` | Video variants |
| `generate_audio` | bool | `true` `false` | `true` | Video variants |

> **Playground:** [muapi.ai/flux-3](https://muapi.ai/flux-3?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3)

> **Note:** Parameter names and ranges above reflect MuAPI's planned schema based on Black Forest Labs' announcement. Confirm exact values against the live playground once each endpoint activates, as Black Forest Labs has not published final API specs for general availability.

---

## Prompt Engineering Guide

### The 5-Part Formula

```
[SUBJECT] + [ACTION/POSE] + [ENVIRONMENT] + [LIGHTING] + [STYLE]
```

**Example:**
```
A hyperrealistic astronaut (subject) walking slowly across red dunes (action)
on a windswept Martian desert at golden hour (environment),
warm rim lighting with dust particles catching the light (lighting),
cinematic depth of field, ultra-detailed suit reflections (style).
```

For **video** prompts, add motion and camera direction:
```
[SUBJECT] + [ACTION] + [ENVIRONMENT] + [CAMERA MOVEMENT] + [AUDIO CUE] + [STYLE]
```

```
A drone (subject) glides forward (action) over a bioluminescent forest at night (environment),
slow forward push with gentle altitude drop (camera),
ambient forest sounds and distant owl calls (audio cue),
cinematic color grading, volumetric mist (style).
```

---

### Lighting & Camera Vocabulary

| Look | Keyword |
|---|---|
| Film-quality warmth | `golden hour cinematography` |
| Studio product shot | `soft box three-point lighting` |
| Drama / mystery | `chiaroscuro lighting` |
| Neon / cyberpunk | `neon-drenched night scene` |
| Documentary | `natural available light` |
| Underwater | `volumetric light beams through water` |
| Push in | `slow dolly in` / `camera push` |
| Orbit | `orbit shot` / `360 arc around subject` |
| Static | `locked-off camera` / `static shot` |
| Overhead | `bird's eye view` / `top-down` |

---

### Multi-Reference Editing Syntax

For `flux-3-image-to-image`, list reference images in `images_list` and refer to them in order in your prompt:

```
Take the product from the first reference image and place it on the
marble surface shown in the second reference image, matching its
lighting and shadow direction. Keep the product's shape and color
unchanged.
```

---

## Prompt Library

### 🌟 Featured Photorealistic Prompts

#### 1. Studio Portrait
```
A hyperrealistic close-up portrait of an elderly craftsman with weathered
hands, deep wrinkles, and kind eyes, shot in a wood workshop with warm
tungsten backlight, shallow depth of field, 85mm lens look, skin texture
and pore-level detail, no retouching artifacts.
```
- **Best for:** `flux-3-text-to-image`
- **Aspect Ratio:** `4:3`

#### 2. Epic Landscape
```
A colossal floating city drifts above luminous clouds at dusk, golden
energy streams flowing between its towers, cinematic wide shot,
dramatic atmospheric lighting, hyper-detailed architecture, 8k resolution.
```
- **Best for:** `flux-3-text-to-image`
- **Aspect Ratio:** `21:9`

#### 3. Macro Detail
```
Extreme macro shot of dew drops on a spider web at sunrise, each droplet
refracting the orange sky, shallow depth of field, natural bokeh,
ultra-sharp focus on the central droplet.
```
- **Best for:** `flux-3-dev` (fast iteration)
- **Aspect Ratio:** `1:1`

---

### 🎨 Editing & Restyling

#### 4. Background Swap
```
Replace the background with a sun-drenched Tuscan vineyard at golden hour,
keep the subject's pose, lighting direction, and shadow consistent with
the new environment.
```
- **Best for:** `flux-3-image-to-image`

#### 5. Style Transfer
```
Restyle this photograph as a warm, painterly oil portrait in the style of
a Dutch Golden Age master — preserve the subject's likeness and
composition, add visible brushwork texture and a dark, moody background.
```
- **Best for:** `flux-3-image-to-image`

#### 6. Character Consistency
```
Using the reference image as the character's identity, place them in a
neon-lit Tokyo alley at night, rain-soaked streets, cinematic depth of
field — keep face, hairstyle, and outfit identical to the reference.
```
- **Best for:** `flux-3-image-to-image`

---

### 📦 Product & E-commerce

#### 7. Product Hero Shot
```
A minimalist product shot of a matte-black ceramic mug on a raw wooden
table, soft natural window light from the left, subtle steam rising,
shallow depth of field, clean negative space for text overlay.
```
- **Best for:** `flux-3-text-to-image` / `flux-3-dev`
- **Aspect Ratio:** `1:1`

#### 8. Lifestyle Product Animation
```
The camera slowly pushes in as steam rises gently from the coffee cup on
the table, soft morning light shifting subtly across the ceramic surface,
ambient cafe sounds in the background.
```
- **Best for:** `flux-3-image-to-video`
- **Duration:** 5s

---

### 🎬 Video with Native Audio

#### 9. Nature Documentary Clip
```
A drone shot glides over a bioluminescent forest at night, fireflies
drifting between glowing trees, gentle mist rolling across the forest
floor, cinematic color grading, ambient forest audio with distant owl
calls synchronized to the visuals.
```
- **Best for:** `flux-3-text-to-video`
- **Duration:** 8s · **Aspect Ratio:** `16:9`

#### 10. Urban Night Scene
```
A tracking shot follows a lone figure walking through a rain-soaked
neon-lit city street at night, reflections rippling in puddles, distant
traffic hum and rain ambience synchronized with the visual, cinematic
depth of field.
```
- **Best for:** `flux-3-text-to-video`
- **Duration:** 6s · **Aspect Ratio:** `16:9`

#### 11. Portrait Bring-to-Life
```
The subject in the reference photo turns their head slowly toward the
camera and offers a subtle smile, hair gently moving in a light breeze,
soft ambient room tone synchronized with the motion.
```
- **Best for:** `flux-3-image-to-video`
- **Duration:** 4s

---

### 🚀 Concept & Sci-Fi

#### 12. Floating Architecture
```
A minimalist white museum building floats above golden desert dunes at
dawn, sunlight passing through windblown sand to form volumetric rays,
ultra-detailed stone texture, distant dunes with clear atmospheric layers.
```
- **Best for:** `flux-3-text-to-image`
- **Aspect Ratio:** `1:1`

#### 13. Sci-Fi Ruins Reveal
```
The camera slowly descends through storm clouds toward alien temple
ruins half-submerged in a glowing ocean, volumetric light piercing the
water, deep rumbling ambient tone building as the ruins come into view.
```
- **Best for:** `flux-3-text-to-video`
- **Duration:** 8s · **Aspect Ratio:** `16:9`

#### 14. Mechanical Bloom
```
Macro push-in on a metal flower bud in darkness, gradually revealing the
precision mechanical structure inside the petals, ending with the
mechanical flower fully blooming as light spreads outward, soft
mechanical whirring synchronized with the bloom.
```
- **Best for:** `flux-3-text-to-video`
- **Duration:** 6s · **Aspect Ratio:** `1:1`

---

## Tips & Best Practices

- **Front-load the subject and action** — the opening words of a FLUX 3 prompt carry the most weight
- **One lighting keyword beats ten adjectives** — `golden hour cinematography` outperforms `warm, beautiful, glowing, soft, vibrant...`
- **Be explicit about what to preserve during edits** — for `flux-3-image-to-image`, state exactly what should stay unchanged (subject, pose, lighting) alongside what should change
- **For video, describe camera movement AND audio** — FLUX 3 Video generates native audio, so an explicit audio cue (`ambient forest sounds`, `distant traffic hum`) improves sync quality
- **Use `flux-3-dev` for iteration** — validate composition and lighting cheaply before running the flagship model
- **Reference images in order of importance** — for multi-image edits, list the most important reference first
- **Check live status before building** — FLUX 3 is rolling out in phases; confirm endpoint availability at [muapi.ai/flux-3](https://muapi.ai/flux-3?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3) before shipping production code

---

## API Providers Comparison

| Provider | FLUX 3 | API Key Required | Playground | Pricing |
|---|---|---|---|---|
| **[MuAPI](https://muapi.ai/flux-3?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3)** | ✅ Early access tracking, 5 planned endpoints | Single key | ✅ Yes | TBD at launch |
| Black Forest Labs (direct) | ✅ Early access (Video/Action), Image rolling out | Application required | Limited | Not published |
| Fal.ai | Not yet available | — | — | — |
| Replicate | Not yet available | — | — | — |

> MuAPI provides the simplest path to production once FLUX 3 opens up — one API key, one base URL, unified billing across all 5 variants alongside every other model already on the platform (FLUX Kontext, Seedance 2, Veo 3, and 250+ more).

---

## Resources & Links

- [FLUX 3 Official (Black Forest Labs)](https://bfl.ai/models/flux-3)
- [Black Forest Labs Blog](https://bfl.ai/blog)
- [MuAPI — FLUX 3 API Access & Early Access Tracking](https://muapi.ai/flux-3?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3)
- [FLUX Kontext (available today on MuAPI)](https://muapi.ai/flux-kontext?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3)
- [FLUX.2 Pro Playground](https://muapi.ai/playground/flux-2-pro?utm_source=github&utm_medium=readme&utm_campaign=awesome-flux-3)

---

## Contributing

PRs welcome! Add prompts, correct parameters once FLUX 3 goes live, share API code examples, or link to new FLUX 3 resources. Open an issue to suggest a new category.

---

## License

MIT
