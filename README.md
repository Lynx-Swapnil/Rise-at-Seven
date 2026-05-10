<div align="center">

<br/>

### Pixel-Perfect Agency Clone

<br/>

[![Live Demo](https://img.shields.io/badge/◉_LIVE_DEMO-000000?style=for-the-badge)](https://rise-at-seven-pink.vercel.app/)
[![Original Site](https://img.shields.io/badge/ORIGINAL_SITE-111111?style=for-the-badge)](https://riseatseven.com)
[![Vercel](https://img.shields.io/badge/Vercel-Deployed-000?style=for-the-badge&logo=vercel&logoColor=white)](https://rise-at-seven-ivory.vercel.app)

<br/>

![Next.js](https://img.shields.io/badge/Next.js_15-black?style=flat-square&logo=next.js)
![React](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Tailwind](https://img.shields.io/badge/Tailwind_v4-0EA5E9?style=flat-square&logo=tailwindcss&logoColor=white)
![GSAP](https://img.shields.io/badge/GSAP_3.15-88CE02?style=flat-square&logo=greensock&logoColor=black)
![Swiper](https://img.shields.io/badge/Swiper.js-0080FF?style=flat-square&logo=swiper&logoColor=white)

<br/>

</div>

---

## `// Overview`

Rise at Seven is renowned for its **search-first creative approach** and highly interactive, editorial-style web presence. This project is a high-fidelity, performance-grade reconstruction of their homepage — built to replicate every fluid animation, scroll-triggered sequence, and interactive state with surgical precision.

> All internal links seamlessly hand off to the original `riseatseven.com` domain, giving visitors full site depth while keeping this project focused on the technical frontend implementation.

---

## `// Stack`

| Layer | Technology | Notes |
|---|---|---|
| **Framework** | Next.js 15 (App Router) | File-based routing, RSC |
| **UI Library** | React 19 | Concurrent features |
| **Styling** | Tailwind CSS v4 | CSS-first config |
| **Animation** | GSAP + ScrollTrigger | MatchMedia, custom modifiers |
| **Slider** | Swiper.js | Touch-optimized carousels |
| **Icons** | React Icons | — |
| **Deployment** | Vercel | Edge network |

---

## `// Features`

<br/>

**`⬛ Cinematic Entry Sequence`**
Custom SVG mask-based reveal that orchestrates page load with a premium "peeling" effect via `CinematicTransition`.

<br/>

**`⬛ Layout-Aware Mega Menu`**
GSAP calculates scale ratios (`scaleX`/`scaleY`) between menu states — switching from Services (wide) to Industries (narrow) feels organic, never jarring. A sliding pill indicator fluidly follows the cursor. Real-time image previews update on hover with scale/blur transitions.

<br/>

**`⬛ Scroll-Driven Peeling Stack`**
`LegacyAccordion` features a tactile card stack where cards slide upward and rotate at `–5deg` as the user scrolls, revealing content beneath.

<br/>

**`⬛ Sticky Gallery Panel`**
Project titles stay pinned left while a vertical stack of image cards scrolls right — fully synchronized via `ScrollTrigger`.

<br/>

**`⬛ Velocity-Sensing Marquee`**
`ScrollTrigger.getVelocity()` maps user scroll speed to the tween's `timeScale`. Text rushes ahead on fast scroll, settles back on stop. GSAP's modulo unitize modifier ensures a zero-jump seamless loop.

<br/>

**`⬛ Magnetic Custom Cursor`**
A floating cursor that reacts contextually to the Gallery and Marquee sections.

<br/>

**`⬛ Hybrid Mobile UX`**
Complex desktop animations degrade gracefully into touch-optimized Swiper carousels and accordion navigation.

---

## `// Project Structure`

```
RiseAtSeven/
│
├── public/
│   ├── Header/                   # Mega menu preview images
│   ├── InfiniteMarquee/          # Slogan visual assets
│   ├── LegacyAccordion/          # Peeling stack thumbnails
│   ├── asset/                    # Brand icons & social proof
│   ├── banner-*.jpg              # Hero background pool (randomized)
│   └── featuredWorks/            # Case study gallery assets
│
└── src/
    ├── app/
    │   ├── globals.css           # Tailwind v4 CSS-first config & blurs
    │   ├── layout.jsx            # Global architecture & cinematic entry
    │   └── page.jsx              # Narrative-driven homepage sections
    │
    └── components/
        ├── home/
        │   ├── AboutMission.jsx          # Staggered typography reveal
        │   ├── ClientLogos.jsx           # Infinite scrolling brand ticker
        │   ├── FeaturedWork.jsx          # Sticky-panel scroll gallery
        │   ├── HeroSection.jsx           # Randomized cinematic hero
        │   ├── InfiniteMarquee.jsx       # Velocity-aware marquee
        │   ├── LegacyAccordion.jsx       # Peeling card stack (dual-device)
        │   ├── ReadyToRise.jsx           # Conversion anchor
        │   ├── Service.jsx               # Service breakdown cards
        │   └── WhatsNew.jsx              # Dynamic news layer
        │
        └── layout/
            ├── AnnouncementBar.jsx       # Global top ticker
            ├── CinematicTransition.jsx   # SVG mask entry sequence
            ├── Footer.jsx                # Multi-column brand nav
            └── Header.jsx                # Mega-menu engine (GSAP morphing)
```

---

## `// Architecture Notes`

**GSAP Layout-Aware Scaling**
The mega menu stores the previous panel's dimensions on each transition. When switching menus, GSAP derives a scale ratio and transforms the container fluidly — no pop, no jump.

**Scroll Velocity Detection**
`ScrollTrigger.getVelocity()` is normalized and piped to a tween's `timeScale`, making the marquee feel physically connected to the user's scrolling energy.

**The `min-w-0` Flex Fix**
Used strategically on flex/grid items throughout the Mega Menu and Featured Work sections so that `truncate` functions correctly inside deeply nested animated containers.

**Overflow-Hidden Character Reveal**
Words and lines are wrapped in `overflow-hidden` containers. GSAP animates them from `y: 40` with a slight `rotateX` — producing the "reveal from the floor" effect found in high-end agency work.

---

## `// Screenshots`

| Desktop | Mobile |
|:---:|:---:|
| ![Desktop](https://i.ibb.co.com/Vcn1hLp7/image.png) | ![Mobile](https://i.ibb.co.com/F49fNwhC/image.png) |
| Hero & Sticky Gallery | Touch-optimized Swiper & Accordions |

---

## `// Getting Started`

**Prerequisites:** Node.js 20.x or later · npm or pnpm

```bash
# 1. Clone
git clone https://github.com/rakibsbase/RiseAtSeven.git
cd RiseAtSeven

# 2. Install
npm install

# 3. Develop
npm run dev
# → http://localhost:3000

# 4. Build
npm run build
```

---

## `// Roadmap`

- [ ] Headless CMS integration (Sanity / Contentful) for the `WhatsNew` section
- [ ] Dark mode toggle
- [ ] LCP optimizations for hero background randomization

---


<div align="center">

<br/>

**Built by [Didarul Alam Swapnil](https://lynx-swapnil.github.io/Didarul_Alam_Swapnil-Portfolio/)**

[![GitHub](https://img.shields.io/badge/GitHub-Lynx--Swapnil-181717?style=flat-square&logo=github)](https://github.com/Lynx-Swapnil)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/didarul-alam-swapnil/)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-FF4500?style=flat-square)](https://lynx-swapnil.github.io/Didarul_Alam_Swapnil-Portfolio/)

<br/>

*Built with passion for pixel-perfection.*

</div>