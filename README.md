<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=IM+Fell+English&weight=400&size=32&duration=1&pause=999999&color=AAAAAA&center=true&vCenter=true&width=600&lines=Medium+Card+Widget" />

**A serverless widget that fetches your Medium post's cover image, title, and subtitle — and renders a beautiful card for your GitHub README.**

<a href="https://medium-card-widget.vercel.app/api/card?url=https://medium.com/@ojasvissar/ai-in-the-fight-against-climate-change-predicting-environmental-trends-before-its-too-late-0ca6fadce36f">
  <img src="https://medium-card-widget.vercel.app/api/card?url=https://medium.com/@ojasvissar/ai-in-the-fight-against-climate-change-predicting-environmental-trends-before-its-too-late-0ca6fadce36f&v=5" width="500" alt="Example Card"/>
</a>

<br/>

[![Stars](https://img.shields.io/github/stars/ojasvissar/medium-card-widget?style=flat-square&color=7aa2f7&labelColor=1a1b2e)](https://github.com/ojasvissar/medium-card-widget/stargazers)
[![Deploy with Vercel](https://img.shields.io/badge/deploy%20with-vercel-1a1b2e?style=flat-square&logo=vercel&labelColor=1a1b2e)](https://vercel.com/new/clone?repository-url=https://github.com/ojasvissar/medium-card-widget)
[![License: MIT](https://img.shields.io/badge/license-MIT-9ece6a?style=flat-square&labelColor=1a1b2e)](LICENSE)

</div>

---

## ✨ Features

- **Zero config** — just pass your Medium URL, get a card back
- **Live data** — fetches real title, subtitle, and cover image from your post
- **Tokyonight dark theme** — looks great on GitHub's dark mode
- **Base64 image embedding** — cover image renders correctly inside GitHub's SVG sandbox
- **1-hour CDN cache** — fast loads without hammering Medium

---

## 🚀 Usage

### Hosted (instant, no setup)

Just use this URL pattern:

```
https://medium-card-widget.vercel.app/api/card?url=YOUR_MEDIUM_POST_URL
```

#### In your README (centered + sized)

```markdown
<div align="center">
  <a href="YOUR_MEDIUM_POST_URL">
    <img src="https://medium-card-widget.vercel.app/api/card?url=YOUR_MEDIUM_POST_URL" width="450"/>
  </a>
</div>
```

#### With a title above it

```markdown
<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=IM+Fell+English&size=22&duration=1&pause=999999&color=AAAAAA&center=true&width=500&lines=📖+read+my+latest+blog+here"/>
  <br/>
  <a href="YOUR_MEDIUM_POST_URL">
    <img src="https://medium-card-widget.vercel.app/api/card?url=YOUR_MEDIUM_POST_URL" width="450"/>
  </a>
</div>
```

#### Example

```markdown
<div align="center">
  <a href="https://medium.com/@ojasvissar/ai-in-the-fight-against-climate-change-predicting-environmental-trends-before-its-too-late-0ca6fadce36f">
    <img src="https://medium-card-widget.vercel.app/api/card?url=https://medium.com/@ojasvissar/ai-in-the-fight-against-climate-change-predicting-environmental-trends-before-its-too-late-0ca6fadce36f" width="450"/>
  </a>
</div>
```

> **Tip:** If your card looks stale, add `&v=2` (increment each time) to bust GitHub's image cache.

---

## 🛠 Self-Host on Vercel

Want your own instance? Deploy in one click:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/ojasvissar/medium-card-widget)

That's it — no environment variables, no API keys needed.

---

## ⚙️ How It Works

1. Vercel receives a request with your Medium post URL
2. The serverless function fetches the page using a crawler user agent
3. Extracts `og:title`, `og:description`, and `og:image` meta tags
4. Downloads the cover image and encodes it as a base64 data URI (required for GitHub SVG rendering)
5. Returns a styled SVG card with the real data embedded

---

## 🎨 Customisation

To customise colors or layout, fork the repo and edit `api/card.js`.

| Token | Default | Description |
|---|---|---|
| Title color | `#c0caf5` | Post title text |
| Subtitle color | `#565f89` | Description text |
| Accent blue | `#7aa2f7` | Tags, CTA, borders |
| Accent green | `#9ece6a` | Climate tag |
| Card background | `#1a1b2e` | Dark base |

---

## ⭐ Support

If this saved you time, a star goes a long way!

[![Star this repo](https://img.shields.io/badge/⭐%20star%20this%20repo-7aa2f7?style=for-the-badge&labelColor=1a1b2e)](https://github.com/ojasvissar/medium-card-widget/stargazers)

---

## 📄 License

MIT — use it, fork it, build on it.

---

<div align="center">
  <sub>Built by <a href="https://github.com/ojasvissar">@ojasvissar</a></sub>
</div>
