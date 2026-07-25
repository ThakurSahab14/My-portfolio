# Gaurav Pratap Singh — Personal Portfolio

Personal portfolio website of **Gaurav Pratap Singh**, Senior Solutions Engineer & Automation Support
Specialist at BrowserStack. Built with vanilla HTML/CSS/JS, Three.js for the animated background, and
GSAP ScrollTrigger for scroll-based motion.

## Sections

- **Home** — animated typing intro
- **About** — short bio
- **Experience** — BrowserStack timeline (Senior Solutions Engineer L3 → Solutions Engineer L2)
- **Projects** — Gemini ticket automation, Freshdesk notifier, SmashKart Tournament app, VCP trading pipeline
- **Skills** — filterable grid (Languages, Automation, Web & APIs, Databases, Tools)
- **Achievements** — Smart India Hackathon, GFG Jobathon, Hashcode, 800+ DSA problems, etc.
- **Profiles** — LinkedIn, GitHub, Email, Phone
- **Contact** — working contact form (see setup below)
- **Resume modal** — opens `portfolio_assests/Gaurav_Resume.pdf` in an in-page viewer

## Local development

```bash
npm install
npm run serve
```

Then open `http://localhost:3000`.

You can also just open `index.html` directly in a browser for a quick look — only the contact form
needs a server to work (see below).

## Deploying to GitHub + Vercel

1. **Push to GitHub**
   ```bash
   cd gaurav-portfolio
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```

2. **Import into Vercel**
   - Go to [vercel.com/new](https://vercel.com/new) and import the GitHub repo.
   - Framework preset: **Other** (it's a static site, no build step needed).
   - Click **Deploy**.

3. **Enable the contact form (optional but recommended)**
   The contact form (`api/submit.js`) sends messages via [Resend](https://resend.com) (free tier is
   fine). In your Vercel project settings → **Environment Variables**, add:
   - `RESEND_API_KEY` — from your Resend dashboard
   - `RECEIVER_EMAIL` — the email address you want messages delivered to (e.g.
     `gaurav14jadaun@gmail.com`)

   Redeploy after adding the variables. Without them, the form will show a config error — the rest
   of the site works fine regardless.

## Updating content later

- **Resume**: replace `portfolio_assests/Gaurav_Resume.pdf` with an updated file (keep the same
  filename, or update the `src` in the resume modal `<iframe>` in `index.html`).
- **Projects / experience / skills**: all plain HTML in `index.html` — search for the relevant
  section (`id="projects"`, `id="experience"`, `id="skills"`) and edit the cards directly.
- **Colors/theme**: CSS variables are defined near the top of `style.css` (`--accent-purple`,
  `--bg-dark`, etc.).

## Credits

Layout and interaction design adapted from the open-source
[DevHQ Personal Portfolio Website](https://github.com/arshbibhaw/DevHQ-Personal-Portfolio-Website)
by Aakarsh Bibhaw, customized with Gaurav Pratap Singh's experience, projects, and skills.

---

**Gaurav Pratap Singh**
Senior Solutions Engineer @ BrowserStack

- Email: gaurav14jadaun@gmail.com
- Phone: +91-9761321308
- LinkedIn: [gaurav142001](https://www.linkedin.com/in/gaurav142001/)
- GitHub: [ThakurSahab14](https://github.com/ThakurSahab14)
