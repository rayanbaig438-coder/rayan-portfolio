# 🕹️ 8-Bit Developer Portfolio: Complete Workshop Guide

Welcome to the **15-Step Portfolio Creation Workshop**! This guide walks you through building a modern, high-performance, pixel-art styled portfolio website from scratch.

---

## 📋 Table of Contents
1. [Prompt 1: Base Structure & HTML Skeleton](#prompt-1-base-structure--html-skeleton)
2. [Prompt 2: Hero Section with Pixel Art & Night Mode Toggle](#prompt-2-hero-section-with-pixel-art--night-mode-toggle)
3. [Prompt 3: Vertical Navigation Bar](#prompt-3-vertical-navigation-bar)
4. [Prompt 4: About Me Section with Profile & Bio](#prompt-4-about-me-section-with-profile--bio)
5. [Prompt 5: Skills Section with Pixel Meters](#prompt-5-skills-section-with-pixel-meters)
6. [Prompt 6: Interactive Career Milestones Timeline](#prompt-6-interactive-career-milestones-timeline)
7. [Prompt 7: Projects Section with Clickable Modals](#prompt-7-projects-section-with-clickable-modals)
8. [Prompt 8: Embedded YouTube Video Showcase](#prompt-8-embedded-youtube-video-showcase)
9. [Prompt 9: Testimonials Section](#prompt-9-testimonials-section)
10. [Prompt 10: AI Chat Interface Simulation & API Hooks](#prompt-10-ai-chat-interface-simulation--api-hooks)
11. [Prompt 11: Contact Form with Email API Integration](#prompt-11-contact-form-with-email-api-integration)
12. [Prompt 12: Pixel Art Social Links in Footer](#prompt-12-pixel-art-social-links-in-footer)
13. [Prompt 13: Responsive Design & Mobile HUD](#prompt-13-responsive-design--mobile-hud)
14. [Prompt 14: Visual Enhancements & Finishing Touches](#prompt-14-visual-enhancements--finishing-touches)
15. [Prompt 15: Testing, Debugging, and Publishing](#prompt-15-testing-debugging-and-publishing)

---

## Prompt 1: Base Structure & HTML Skeleton
**Goal:** Create a clean, semantic HTML5 structure with placeholders for each section.
- **Key Concepts:** Use `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`.
- **Placeholder comments:** Ensure every section has a comment tag so future modules can be inserted sequentially without layout breakage.

---

## Prompt 2: Hero Section with Pixel Art & Night Mode Toggle
**Goal:** Create an attention-grabbing hero section with pixel art character, headline, and night mode detection.
- **CSS Theming:** Use CSS variables with both `@media (prefers-color-scheme: dark)` and manual `[data-theme="dark"]` attribute overrides.
- **Pixel Styling:** Crisp 3px borders, `4px 4px 0px #000` drop-shadow offsets, and custom SVG pixel avatar.
- **JavaScript Hook:** Listen for clicks on `.theme-toggle-btn` and persist choices to `localStorage`.

---

## Prompt 3: Vertical Navigation Bar
**Goal:** Fixed vertical navigation on the left of the screen for desktop viewports.
- **Accessibility:** Semantic `<nav>`, `role="menubar"`, `aria-label`, visible keyboard focus states.
- **Micro-interactions:** Hover arrow indicator `▶` and smooth transition translation.
- **Scroll Spy:** Active class automatically applies to the current section as the user scrolls.

---

## Prompt 4: About Me Section with Profile & Bio
**Goal:** Introduce the engineer with an RPG-inspired character sheet and personal highlights.
- **Layout:** 2-column grid featuring a biography card on the left and a retro "Character Sheet" on the right (Class: Full-Stack Sorcerer, Level: 99).
- **Personal Touch:** Include side quest chips (game jams, mechanical keyboards, synthesizers).

---

## Prompt 5: Skills Section with Pixel Meters
**Goal:** Display technical proficiencies using stepped pixel progress meters.
- **Progress Meter Technique:** Use `repeating-linear-gradient` in CSS to generate discrete 8-bit health-bar segments rather than a plain bar.
- **Categories:** Group into Languages, Frontend & UI, Backend & Cloud.
- **Code Comments:** Document each competency level clearly in the HTML and CSS.

---

## Prompt 6: Interactive Career Milestones Timeline
**Goal:** Highlight education, major roles, and open-source contributions chronologically.
- **Timeline Connector:** A dashed glowing vertical trail connecting milestone nodes.
- **Card Hover Animation:** Elevation translation (`translateY(-4px)`) and pixel shadow expansion on hover.

---

## Prompt 7: Projects Section with Clickable Modals
**Goal:** Showcase portfolio projects with clickable cards that launch an in-depth modal dialog.
- **Data Binding:** Use `data-project-id` on cards and a shared JS dictionary to populate architecture notes, metrics, and live demo links.
- **Accessibility:** Full keyboard `ESC` key support, focus trap, and background backdrop blur.

---

## Prompt 8: Embedded YouTube Video Showcase
**Goal:** Responsive video embed housed within a nostalgic CRT television / arcade monitor bezel.
- **Aspect Ratio:** `aspect-ratio: 16 / 9` with `width: 100%` ensures zero distortion on all screen sizes.
- **Bezel Details:** Realistic retro details including power LED, channel selector (`CH: 08-BIT`), and speaker grills.

---

## Prompt 9: Testimonials Section
**Goal:** Peer and client recommendations presented in card-like containers.
- **Aesthetic:** Pixel quotation marks (`“`), avatar badges, author credentials, and retro drop shadows.

---

## Prompt 10: AI Chat Interface Simulation & API Hooks
**Goal:** Allow visitors to query an AI clone of the portfolio owner.
- **Features:** Message log, interactive prompt suggestion chips, realistic typing dot animation.
- **Production API Hook:** The codebase in `scripts/chat.js` includes a clean drop-in template for OpenAI (`gpt-4o-mini`), Claude, or Gemini APIs.

---

## Prompt 11: Contact Form with Email API Integration
**Goal:** Production-ready contact form with validation, high-contrast submit button, and status messages.
- **Email Service Hook:** The code in `scripts/contact.js` includes the exact snippet to wire up the **Resend API** (`https://resend.com`) or serverless webhook.

---

## Prompt 12: Pixel Art Social Links in Footer
**Goal:** Clean, accessible footer with retro icon links.
- **Aesthetic:** Uniform 44x44px square pixel tiles with hover lift and high contrast.
- **Accessibility:** `aria-label` and `rel="noopener noreferrer"` attributes on all external links.

---

## Prompt 13: Responsive Design & Mobile HUD
**Goal:** Flawless experience across desktop, tablet, and mobile phones.
- **Mobile Drawer:** On screens `< 768px`, the vertical navbar tucks neatly into a sliding drawer triggered by a top-bar hamburger button `[MENU ☰]`.

---

## Prompt 14: Visual Enhancements & Finishing Touches
**Goal:** Polish the user interface with retro atmosphere.
- **CRT Scanlines:** Toggleable overlay scanlines giving authentic arcade monitor flavor.
- **Micro-interactions:** Pixel button press effect using `transform: translate(2px, 2px)`.

---

## Prompt 15: Testing, Debugging, and Publishing

### 1. Local Testing
Start a local server to test in modern browsers:
```bash
# Using Python
python -m http.server 8080

# Using Node.js
npx serve .
```
Visit `http://localhost:8080` in Chrome, Firefox, Safari, or Edge.

### 2. Testing Checklist
- [x] Night/Day mode toggle persists in `localStorage`
- [x] Vertical navigation highlights the active section on scroll
- [x] Mobile menu opens and closes smoothly on small screens
- [x] Clicking project cards opens the modal; pressing `ESC` closes it
- [x] AI Chat responds to questions and chips with typing animation
- [x] Contact form validates inputs and displays success notification
- [x] YouTube video scales responsively without letterboxing

### 3. Deploying to GitHub Pages (Free & Instant)
1. Initialize git in your folder:
   ```bash
   git init
   git add .
   git commit -m "feat: complete pixel art portfolio"
   ```
2. Create a repository on GitHub named `portfolio` or `<your-username>.github.io`.
3. Push your repository:
   ```bash
   git remote add origin https://github.com/<your-username>/portfolio.git
   git branch -M main
   git push -u origin main
   ```
4. In GitHub: Go to **Settings** > **Pages** > Under **Branch**, select `main` and `/ (root)`.
5. Click **Save**. Your site will be live at `https://<your-username>.github.io/portfolio/`!
