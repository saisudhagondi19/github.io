# 🚀 Sai Sudha Gondi — Data Engineer Portfolio

> **Live Site:** [saisudhagondi.vercel.app](https://saisudha-de.vercel.app/)

A fully responsive, single-file portfolio website built for a Data Engineer role. Features a full-screen video hero, animated impact metrics, brand-colored skill tags, a working contact form that opens Gmail, and mobile navigation — all in one self-contained HTML file.

---

## ✨ Features

- **Full-screen video hero** — MP4 background with mute/unmute toggle
- **Animated count-up metrics** — Numbers animate on scroll ($200K, 95%, 10TB+)
- **Brand-colored skill tags** — Kafka, Snowflake, Databricks, AWS, Azure each styled with their real brand colors
- **Working contact form** — Opens Gmail directly with the recruiter's message pre-filled
- **Download Resume button** — One-click PDF download from the hero
- **Mobile hamburger menu** — Full-screen overlay nav for phones
- **Scroll reveal animations** — Sections fade in as you scroll
- **SEO optimized** — Meta tags, Open Graph (LinkedIn preview), Twitter card
- **Favicon** — Custom SSG badge in browser tab
- **Zero dependencies** — No frameworks, no npm, no build step. One HTML file.

---

## 🗂️ Project Structure

```
portfolio/
├── index.html       # Entire portfolio (HTML + CSS + JS in one file)
├── reel.mp4         # Hero background video
├── resume.pdf       # Downloadable resume
└── photo.png        # Profile photo (base64 embedded in HTML)
```

---

## 🏗️ How I Built It

### Tech Stack
| Layer | Technology |
|-------|-----------|
| Structure | HTML5 |
| Styling | CSS3 (custom, no frameworks) |
| Interactivity | Vanilla JavaScript |
| Fonts | Google Fonts — Inter, JetBrains Mono |
| Deployment | Vercel |

### Design Decisions

**Single-file approach** — Everything (HTML, CSS, JS, base64 photo) lives in one `index.html` file. This means zero file path issues, works offline, and deploys by dragging one file.

**Video hero** — The hero uses an HTML5 `<video>` tag with `autoplay muted loop`. A red gradient overlay sits on top so text stays readable regardless of what's in the video. Mute/unmute is controlled via the Web Speech API toggle on the right.

**Count-up animation** — Impact numbers use `IntersectionObserver` to trigger when the section enters the viewport. Each number animates from 0 to its target over 1800ms using `setInterval`.

**Contact form → Gmail** — No backend needed. On submit, the form builds a Gmail compose URL (`https://mail.google.com/mail/?view=cm&...`) with the recruiter's name, email, and message pre-filled, then opens it in a new tab.

**Scroll reveal** — All sections have class `reveal`. A single `IntersectionObserver` watches all `.reveal` elements and adds `.visible` when they enter the viewport, triggering a CSS `opacity + translateY` transition.

**Brand colors on skill tags** — Each `<span class="tag">` gets a `data-brand` attribute via JavaScript regex replacement at build time. CSS attribute selectors (`[data-brand="kafka"]`) apply the correct brand color without any extra markup.

---

## 📐 Sections

| Section | Description |
|---------|-------------|
| **Hero** | Full-screen video, name, title, opening line, 3 CTA buttons |
| **About** | Photo, polished bio, key chips (location, email, experience) |
| **Expertise** | 6 core DE competency cards with hover animations |
| **Impact** | 8 animated metrics from real production work |
| **Skills** | 8 tech categories with brand-colored tags |
| **Experience** | Timeline: Meta → Horizon BCBS → Cognizant |
| **Projects** | 4 GitHub-linked project cards |
| **Learning** | Career growth roadmap — what's next for a DE |
| **Education** | MS Computer Science + B.Tech |
| **Contact** | Form with big G watermark → opens Gmail on submit |

---

## 🚀 How to Deploy

### Vercel (Recommended)
1. Push `index.html`, `reel.mp4`, `resume.pdf` to a GitHub repo
2. Go to [vercel.com](https://vercel.com) → Import that repo
3. Click Deploy — live in 60 seconds
4. Go to Settings → Domains → rename to `saisudhagondi.vercel.app`

### Netlify Drop
1. Go to [netlify.com/drop](https://netlify.com/drop)
2. Drag your `portfolio` folder onto the page
3. Get a live URL instantly — rename in Site Settings

### GitHub Pages
1. Create repo named `saisudhagondi19.github.io`
2. Upload files → Settings → Pages → Deploy from main branch
3. Live at `https://saisudhagondi19.github.io`

---

## 🎨 Color Theme

| Color | Hex | Used For |
|-------|-----|---------|
| Primary Red | `#C0392B` | Buttons, accents, contact bg |
| Orange | `#E05030` | Gradients, hover states |
| Dark BG | `#0a0a0a` | Page background |
| Card BG | `#181818` | Section cards |
| Text | `#EFEFEF` | Body text |

---

## 📬 Contact

**Sai Sudha Gondi**
- 📧 saisudhagondi19@gmail.com
- 💼 [linkedin.com/in/saisudha-gondi](https://linkedin.com/in/saisudha-gondi)
- 🐙 [github.com/saisudhagondi19](https://github.com/saisudhagondi19)
- 📞 (972) 768-0034

---

*Built with HTML, CSS, and JavaScript — no frameworks, no build tools, no dependencies.*
