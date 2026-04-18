# 🏨 Hotel Booking Platform | Luxury Stay Website

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![GSAP](https://img.shields.io/badge/GSAP-3.x-88CE02?style=flat-square&logo=greensock&logoColor=white)](https://greensock.com/gsap/)

> **A visually rich hotel showcase website** — built with pure HTML, CSS, and JavaScript, featuring smooth GSAP-powered animations and an elegant multi-section layout.

---

## 🖼️ Screenshots

<table>
  <tr>
    <td align="center"><img src="hotel_images/Page1.png" width="340" alt="Homepage"/><br/><sub><b>Homepage</b></sub></td>
    <td align="center"><img src="hotel_images/Page2.png" width="340" alt="Services"/><br/><sub><b>Services</b></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="hotel_images/Page3.png" width="340" alt="Overview"/><br/><sub><b>Overview</b></sub></td>
    <td align="center"><img src="hotel_images/Page4.png" width="340" alt="Explore"/><br/><sub><b>Explore</b></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="hotel_images/Page5.png" width="340" alt="Rooms & Suites"/><br/><sub><b>Rooms & Suites</b></sub></td>
    <td align="center"><img src="hotel_images/Page6.png" width="340" alt="Community"/><br/><sub><b>Community</b></sub></td>
  </tr>
  <tr>
    <td align="center"><img src="hotel_images/Page7.png" width="340" alt="Satisfied Customers"/><br/><sub><b>Satisfied Customers</b></sub></td>
    <td align="center"><img src="hotel_images/Page8.png" width="340" alt="Got A Question"/><br/><sub><b>Got A Question</b></sub></td>
  </tr>
</table>

---

## 📋 Overview

A fully static hotel website built from scratch using only HTML, CSS, and vanilla JavaScript — no frameworks, no back-end. Smooth scroll-triggered animations are powered by **GSAP (GreenSock Animation Platform)**, creating a polished, immersive experience across all sections.

**Built by:** [Your Team Name]

---

## 🎯 Key Features

### 🌐 Pages & Sections
- **Homepage** — Hero section with animated entrance and call-to-action
- **Services** — Hotel amenities and offerings showcase
- **Overview** — About the hotel, vision, and highlights
- **Explore** — Local attractions and experiences
- **Rooms & Suites** — Room catalog with details and imagery
- **Community** — Social proof and guest stories
- **Satisfied Customers** — Testimonials and ratings
- **Got A Question** — Contact form and FAQ section

### ✨ Animations & Interactions
- GSAP-powered scroll-triggered reveal animations
- Smooth entrance effects on hero and section headings
- Interactive hover states on cards and buttons
- Animated navigation and mobile hamburger menu
- Staggered card reveals for rooms and features

### 🎨 Design & UX
- Fully responsive layout (mobile, tablet, desktop)
- Custom CSS variables for consistent theming
- Elegant typography pairing for a luxury feel
- Optimized images for fast load times
- Accessible semantic HTML5 structure

---

## 🛠️ Tech Stack

| Layer | Technology | Link |
|-------|------------|------|
| **Markup** | HTML5 | [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/HTML) |
| **Styling** | CSS3 | [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/CSS) |
| **Logic** | JavaScript ES6+ | [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript) |
| **Animations** | GSAP 3.x | [greensock.com](https://greensock.com/gsap/) |
| **GSAP Plugin** | ScrollTrigger | [greensock.com/scrolltrigger](https://greensock.com/scrolltrigger/) |
| **Dev Tools** | VS Code | [code.visualstudio.com](https://code.visualstudio.com/) |
| | Live Server | [VS Code Extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) |
| | Git | [git-scm.com](https://git-scm.com/downloads) |

---

## 📥 Getting Started

No build tools or package manager required — just open and run.

### Option A: Live Server (Recommended)

1. Install [VS Code](https://code.visualstudio.com/)
2. Install the **Live Server** extension by Ritwick Dey
3. Open the project folder in VS Code
4. Right-click `index.html` → **"Open with Live Server"**
5. Visit `http://127.0.0.1:5500` in your browser

### Option B: Direct File Open

```bash
# Clone the repository
git clone https://github.com/your-username/hotel-platform.git
cd hotel-platform

# Open index.html directly in your browser
# (double-click the file, or drag it into a browser window)
```

> ⚠️ Some browsers restrict local font/image requests. Live Server avoids this entirely.

---

## 📁 Project Structure

```
hotel-platform/
├── index.html                  ← Main entry point
├── css/
│   ├── style.css               ← Global styles & CSS variables
│   ├── animations.css          ← GSAP animation helpers
│   └── responsive.css          ← Media queries & breakpoints
├── js/
│   ├── main.js                 ← Core interactions & logic
│   ├── animations.js           ← GSAP timelines & ScrollTrigger setup
│   └── navbar.js               ← Navigation & mobile menu toggle
├── hotel_images/
│   ├── Page1.png               ← Homepage
│   ├── Page2.png               ← Services
│   ├── Page3.png               ← Overview
│   ├── Page4.png               ← Explore
│   ├── Page5.png               ← Rooms & Suites
│   ├── Page6.png               ← Community
│   ├── Page7.png               ← Satisfied Customers
│   └── Page8.png               ← Got A Question
└── README.md
```

---

## 🎬 GSAP Setup

GSAP is loaded via CDN — no installation needed:

```html
<!-- Add before </body> in your HTML -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>
```

Example animation patterns used in the project:

```javascript
gsap.registerPlugin(ScrollTrigger);

// Hero entrance
gsap.from(".hero-title", {
  opacity: 0,
  y: 60,
  duration: 1.2,
  ease: "power3.out"
});

// Scroll-triggered card stagger
gsap.from(".room-card", {
  scrollTrigger: {
    trigger: ".rooms-section",
    start: "top 80%",
  },
  opacity: 0,
  y: 40,
  stagger: 0.15,
  duration: 0.9,
  ease: "power2.out"
});
```

---

## 🌐 Deployment

Since this is a fully static site, it can be deployed anywhere for free:

| Platform | How to Deploy |
|----------|---------------|
| **GitHub Pages** | Push to `main` → Settings → Pages → Deploy from branch |
| **Netlify** | Drag & drop the project folder at [app.netlify.com/drop](https://app.netlify.com/drop) |
| **Vercel** | Import the repo at [vercel.com](https://vercel.com/) — zero config needed |

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
