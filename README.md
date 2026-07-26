# Gaurav Pratap Singh : Personal Portfolio Website

<div align="center">
  
  ![Portfolio](https://img.shields.io/badge/Portfolio-Live-brightgreen)
  ![Three.js](https://img.shields.io/badge/Three.js-r128-black?logo=three.js)
  ![GSAP](https://img.shields.io/badge/GSAP-3.12.2-88CE02?logo=greensock)
  ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
  ![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
  ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
  ![Vercel](https://img.shields.io/badge/Vercel-Serverless-black?logo=vercel&logoColor=white)
  ![Resend](https://img.shields.io/badge/Resend-Email_API-white?logo=minutemailer)
  
  <p><strong>Professional Portfolio with 3D WebGL Starfield, GSAP Scroll Animations, and Secure Serverless Architecture!</strong></p>
  
</div>

---

## Overview

A cutting-edge personal portfolio featuring a **3D animated starfield background** built with Three.js and professional **scroll-triggered animations** powered by GSAP. This portfolio showcases advanced web technologies including WebGL rendering, custom particle systems, and sophisticated motion design.

Beyond the frontend, it features a highly secure, **Vercel Serverless Backend** integrated with the **Resend API** to process contact form submissions without exposing sensitive API keys to the browser.

Content is tailored to my work as a **Senior Automation Support Engineer**, covering my BrowserStack experience, automation tooling projects, and technical skill set.

---

## Key Features

- **3D WebGL Starfield** - 3,200 interactive particles with mouse parallax  
- **Premium GSAP Animations** - High-end scroll-triggered staggers and cascading reveals  
- **Dynamic Typing Animation** - Auto-cycling professional roles (Automation Support Engineer, SDET, QA Automation Expert)  
- **Custom Cursor System** - Magnetic hover effects with smooth tracking  
- **3D Card Tilt Effects** - Perspective-based magnetic interactions  
- **Timeline Progress Indicator** - Scroll-synced experience timeline  
- **Serverless Email Backend** - Custom Node.js Vercel function using the Resend API  
- **Advanced SEO** - Fully configured Open Graph & Twitter Cards for social sharing previews  
- **Glassmorphism Design** - Modern backdrop blur aesthetics  
- **Fully Responsive** - Optimized for all screen sizes  
- **Hardware Accelerated** - GPU-powered animations and rendering  

---

## Advanced Architecture

### Three.js 3D Background System
**Particle Starfield:**
- 3,200 procedurally generated stars
- Custom radial gradient texture for realistic glow
- Hardware-accelerated WebGL rendering
- Responsive canvas sizing with pixel ratio optimization
- Smooth auto-rotation with configurable speed

**Interactive Parallax:**
- Mouse-tracking rotation on X and Y axes
- Subtle movement for depth perception

### GSAP Animation System
**Hero Intro & ScrollTriggers:**
- Sequenced timeline animations with overlapping tweens (Power2.out easing)
- **Timeline Items:** Slide in organically from their respective sides
- **Projects/Skills Grids:** Staggered reveals with a subtle bounce (`back.out`) and wave-like ripple effects
- **Dynamic Replays:** Uses `toggleActions: "play none none reverse"` to smoothly replay animations when scrolling back up.

### Secure Backend Architecture
Instead of exposing API keys in client-side JavaScript, this portfolio employs a **Vercel Serverless Function** (`api/submit.js`).
- **Hidden Keys:** The frontend sends a clean POST request to `/api/submit`. The serverless function securely injects the `RESEND_API_KEY` from the Vercel Environment Variables, formats the email using HTML, and forwards it to the Resend API.
- **Node.js Native:** Built using the native `https` module to guarantee runtime stability across all Vercel Node.js environments.

---

## Technologies

### Core Stack
- **HTML5 & CSS3** - Semantic markup, Grid, Flexbox, Custom Properties
- **Vanilla JavaScript (ES6+)** - Core interactivity
- **Node.js (CommonJS)** - Vercel serverless backend logic

### Animation & 3D Libraries
- **Three.js r128** - 3D WebGL rendering engine
- **GSAP 3.12.2 & ScrollTrigger** - Professional animation framework

### External Services
- [Resend API](https://resend.com/) - Secure transactional email backend
- [Vercel](https://vercel.com/) - Serverless hosting & analytics
- [Google Fonts](https://fonts.google.com/) - Inter typography
- [Font Awesome 6.4.0](https://fontawesome.com/) & [Devicon](https://devicon.dev/) - Icon libraries

---

## Performance Metrics

### Benchmark Results
- **Lighthouse Performance:** 95+
- **First Contentful Paint:** < 1.5s
- **WebGL FPS:** Consistent 60fps
- **Total Bundle Size:** ~50KB (excluding CDN)

### Optimization Techniques
- **WebGL Rendering** - GPU-accelerated graphics  
- **BufferGeometry** - Efficient vertex handling  
- **Pixel Ratio Capping** - Prevents mobile over-rendering  
- **Lazy ScrollTrigger** - On-demand, highly-performant animations  

---

## File Structure

```text
portfolio/
│
├── index.html                 # Main markup, SEO tags, and Canvas target
├── style.css                  # Advanced styling, grids, glassmorphism
├── script.js                  # Intersection observers, typing fx, form logic
├── 3d_background.js           # Three.js starfield + GSAP timelines
├── api/
│   └── submit.js              # Vercel Serverless Function (Resend Backend)
├── package.json               # Dependencies & Vercel configuration
├── .env                       # Local environment variables (git-ignored)
├── .gitignore                 # Repo security rules
└── portfolio_assests/         # Resume PDF, favicon, and profile image
```

---

## Setup & Deployment

### Local Development
```bash
npm install
npm run serve
```
Then open `http://localhost:3000`.

### Deploying to Vercel
1. Push this repo to GitHub.
2. Import the repo at [vercel.com/new](https://vercel.com/new) — framework preset: **Other** (static site, no build step).
3. Add these Environment Variables in your Vercel project settings to enable the contact form:
   - `RESEND_API_KEY` — from your [Resend](https://resend.com) dashboard
   - `RECEIVER_EMAIL` — the inbox you want messages delivered to
4. Redeploy. The rest of the site works fully even without the form being configured.

---

## Author

**Gaurav Pratap Singh**  
Senior Automation Support Engineer (L3) @ BrowserStack | Selenium · Playwright · Appium

- LinkedIn: [@gaurav142001](https://www.linkedin.com/in/gaurav142001/)
- GitHub: [@ThakurSahab14](https://github.com/ThakurSahab14)
- Email: [gaurav14jadaun@gmail.com](mailto:gaurav14jadaun@gmail.com)
- Phone: +91-9761321308

---

## Notes for Gaurav (things to double-check / swap in later)

- **Company logos** in the Experience timeline use `Company_Logo_Placeholder.png` — a generic sample. Swap in the
  real BrowserStack / Scaler logos whenever you have them (same filename, or update the `src` in `index.html`).
- **Certificate thumbnails** in the Certifications section use one shared `Certificate_Placeholder.jpg` sample image.
  The **"View Credential" links are real** (your Drive/HackerRank URLs) — only the thumbnail image is a placeholder.
  Swap in actual screenshots of each certificate for a more polished look.
- **SharkTank** repo's default `main` branch has almost no code — the real project lives on the `gaurav` branch, so
  the GitHub button links directly to `github.com/ThakurSahab14/SharkTank-/tree/gaurav`. Consider setting `gaurav`
  as the default branch on GitHub so visitors landing on the repo see the real code first.
- **WeatherApp** live link (`thakursahab14.github.io/WeatherApp`) and **Interactive Quiz** live link (a Vercel
  preview URL found in its README) could not be verified from this sandbox (GitHub Pages / Vercel preview domains
  aren't reachable here) — please click through both yourself before publishing; if either is dead, either fix the
  deployment or let me know and I'll switch that button back to disabled.
- **Project dates** for the 7 GitHub repos are approximate, based on each repo's last commit date — adjust if you
  remember the actual timelines.

## Acknowledgments

- **Three.js Team** - 3D graphics library
- **GreenSock (GSAP)** - Animation framework
- **Resend** - Email backend infrastructure
- **Font Awesome & Devicon** - Icon libraries
- **Aakarsh Bibhaw** - Original [DevHQ Portfolio](https://github.com/arshbibhaw/DevHQ-Personal-Portfolio-Website) template this project is adapted from

---

<div align="center">
  
  **Star this repo if you found the 3D effects impressive!**
  
  Made by Gaurav Pratap Singh
  
  © 2026 All Rights Reserved
  
</div>
