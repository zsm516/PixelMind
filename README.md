# 🎨 PixelMind — AI Image Studio

> A free, unlimited, single-file AI image generator supporting 10+ AI models — no backend, no signup, no limits.

![PixelMind](https://img.shields.io/badge/PixelMind-AI%20Image%20Studio-7c5cfc?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIGZpbGw9Im5vbmUiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNMTIgMkwyIDdsIDEwIDUgMTAgNSAxMC01WiIvPjwvc3ZnPg==)
![HTML](https://img.shields.io/badge/Pure-HTML%20%2F%20CSS%20%2F%20JS-f97316?style=for-the-badge)
![No Backend](https://img.shields.io/badge/No%20Backend-Required-22c55e?style=for-the-badge)
![Free](https://img.shields.io/badge/100%25-Free-a78bfa?style=for-the-badge)

---

## ✨ What is PixelMind?

**PixelMind** is a fully client-side AI image generation studio built into a single `index.html` file. It connects directly from your browser to the APIs of 10+ leading AI image models — no server, no database, no build tools, no monthly subscription. You bring your own API keys (all providers offer free tiers), and PixelMind does the rest.

Whether you're a developer, designer, artist, or just curious about AI-generated imagery, PixelMind gives you a professional-grade interface to explore, experiment, and create — all for free.

---

## 🚀 Live Demo

> Deploy your own in 60 seconds:
> 1. Download `index.html`
> 2. Drag it to [netlify.com/drop](https://netlify.com/drop)
> 3. Done — live URL instantly, no account needed

---

## 🤖 Supported AI Models

| Model | Provider | Free Tier |
|-------|----------|-----------|
| **DALL·E 3** | OpenAI | ✅ $5 free credit |
| **DALL·E 2** | OpenAI | ✅ $5 free credit |
| **Stable Diffusion XL** | Stability AI | ✅ 25 free/day |
| **Stable Diffusion 3** | Stability AI | ✅ Free credits |
| **FLUX Pro** | Black Forest Labs (Replicate) | ✅ Free credits |
| **SD Lightning** | ByteDance (Replicate) | ✅ Free credits |
| **Playground v2.5** | Playground AI (Replicate) | ✅ Free credits |
| **Kandinsky 2.2** | Sber AI (Replicate) | ✅ Free credits |
| **Imagen 3** | Google AI | ✅ Completely free |
| **Ideogram V2** | Ideogram AI | ✅ 10 free/day |

---

## 🎛️ Features

### Core Generation
- **10+ AI models** — switch between providers in one click
- **12 style presets** — Photorealistic, Anime, Oil Painting, Watercolor, Cyberpunk, Dark Fantasy, 3D Render, Pixel Art, Pencil Sketch, Cinematic, Minimalist, and more
- **4 canvas sizes** — Square (1024×1024), Portrait (1024×1792), Landscape (1792×1024), Auto
- **3 quality levels** — Standard (fast), HD (balanced), Ultra (max detail)
- **Negative prompt** — tell the AI exactly what to exclude

### Prompt Tools
- **✨ Enhance** — automatically appends quality-boosting keywords to your prompt
- **🎲 Random** — generates a random creative prompt to spark inspiration
- **🎨 Variation** — tweaks your last prompt and regenerates for a fresh take

### Fine-Tune Controls
- **Creativity (CFG Scale)** — control how closely the AI follows your prompt
- **Sampling Steps** — more steps = more detail (slower)
- **Seed** — lock in a specific seed for reproducible results
- **Image Count** — generate up to 4 images at once

### UX & Output
- **Live generation status** with animated progress bar
- **Error messages with hints** — invalid key, rate limit, billing issues explained clearly
- **Session history** — last 9 generations saved and accessible in one click
- **Download as PNG** — save any generated image instantly
- **Copy prompt** — copy the exact prompt used for any generation
- **API status panel** — see which providers are connected at a glance
- **Dark theme** — easy on the eyes, beautiful ambient glow design

---

## 🔑 Getting API Keys (All Free)

| Provider | Where to get it | Notes |
|----------|----------------|-------|
| **OpenAI** | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) | New accounts get $5 free credit |
| **Stability AI** | [platform.stability.ai/account/keys](https://platform.stability.ai/account/keys) | 25 free images/day |
| **Replicate** | [replicate.com/account/api-tokens](https://replicate.com/account/api-tokens) | Free tier + pay-per-use |
| **Google AI** | [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey) | Completely free |
| **Ideogram** | [ideogram.ai/manage-api](https://ideogram.ai/manage-api) | 10 free generations/day |

> **🔒 Privacy:** Your API keys are stored only in your browser's `localStorage`. They are never sent to any server other than the AI provider you're actively using.

---

## 🛠️ Setup & Usage

### Option 1 — Open Locally (Simplest)
```bash
# Just open the file in any browser
open index.html
```
No installation. No npm. No server. It works.

### Option 2 — GitHub Pages
```bash
# 1. Fork or upload index.html to a repo
# 2. Go to Settings → Pages → Deploy from branch main
# 3. Your site is live at https://yourusername.github.io/pixelmind
```

### Option 3 — Netlify Drop
1. Go to [netlify.com/drop](https://netlify.com/drop)
2. Drag `index.html` onto the page
3. Instant live URL — no account required

### Option 4 — Vercel CLI
```bash
npm i -g vercel
vercel
# Follow the prompts — done in ~30 seconds
```

---

## 🧠 How It Works

PixelMind is a zero-dependency, single-file web app. When you click **Generate**:

1. Your browser reads the API key from `localStorage`
2. It sends a direct HTTPS request to the selected AI provider's API
3. The provider returns either an image URL or a base64-encoded image
4. PixelMind displays it in the output panel

No middleman. No proxy. No data collection. Your prompts go directly from your browser to the AI provider.

```
Your Browser  →  OpenAI / Stability / Replicate / Google / Ideogram
              ←  Image URL or Base64
```

---

## 📁 Project Structure

```
pixelmind/
└── index.html    # The entire app — HTML + CSS + JS in one file (52KB)
```

That's it. One file. Fully self-contained.

---

## 🎨 Customization

All source code is in `index.html`. Key areas to customize:

```javascript
// Add or edit style presets
const STYLE_MODS = {
  'My Style': ', my custom style keywords here',
  ...
};

// Add or edit random prompt suggestions
const SAMPLE_PROMPTS = [
  'Your custom prompt here',
  ...
];
```

```css
/* Change the color theme */
:root {
  --accent: #7c5cfc;      /* Primary purple */
  --accent2: #a78bfa;     /* Secondary purple */
  --bg: #08080f;          /* Background */
}
```

---

## ⚠️ Important Notes

- **API costs:** While all providers offer free tiers, heavy usage may incur charges on your API account. Monitor your usage at each provider's dashboard.
- **Content policies:** Each AI provider has its own content policies. Prompts that violate these policies will be rejected by the provider, not by PixelMind.
- **CORS:** Some providers (like Replicate) may require CORS-enabled requests. The app handles this automatically.
- **Key security:** Never share your API keys publicly. If a key is exposed, revoke it immediately at the provider's dashboard.

---

## 🤝 Contributing

Contributions are welcome! Ideas for improvement:

- [ ] Add more AI models (Midjourney API, Adobe Firefly, Amazon Titan)
- [ ] Image-to-image generation support
- [ ] Inpainting / outpainting tools
- [ ] Export generation history as JSON
- [ ] Prompt library / favorites system
- [ ] Multi-language UI support

Feel free to open an issue or submit a pull request.

---

## 📄 License

MIT License — free to use, modify, and distribute for any purpose.

---

## 🙏 Acknowledgements

Built on top of the amazing APIs from:
[OpenAI](https://openai.com) · [Stability AI](https://stability.ai) · [Replicate](https://replicate.com) · [Google AI](https://ai.google.dev) · [Ideogram](https://ideogram.ai) · [Black Forest Labs](https://blackforestlabs.ai)

---

<p align="center">zsm516 Made with ❤️ · Zero backend · Zero tracking · 100% free</p>
