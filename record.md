# Project Record: Personal Homepage & Blog

## 1. Overview
Created a static personal homepage and technical blog for Yayun Xiao (肖雅芸) located in `/home/xyy/xyy_homepage`. The website was built purely using semantic HTML and custom CSS, adhering to a strict green & white design system without reliance on external frameworks or libraries.

## 2. Files

### `index.html`
Main personal homepage. Restructured to match the academic dual-column layout of `cat-blizzard.github.io`:
- Fixed masthead navigation bar with anchor links (About, Research, Skills, Education, Awards, Writing)
- Left sidebar: SVG avatar placeholder (green circle with "YX" initials), name, Chinese name, institution, email, GitHub
- Right content area: scrollable sections with CV content (about, research items, skills tags, education, awards, writing/blog link)
- Blog entry links to `emotion-aware-avatar.html` (not `blog.html`)

### `styles.css`
Responsive CSS with green+white color system and dual-column grid layout:
- CSS variables: `--color-primary: #1e5631`, `--color-secondary: #3b734b`, `--color-accent: #4e9c61`
- Grid layout: `grid-template-columns: 190px minmax(0, 650px)`, max-width 980px
- Sticky sidebar, fixed masthead, smooth scrolling with `scroll-margin-top` for anchor offsets
- Responsive breakpoints at 760px and 460px
- Blog card, tag pills, research/education items, article-shell for blog pages

### `emotion-aware-avatar.html`
Technical blog replacing the old `blog.html`:
- Topic: "从'会动'到'有情绪'：我对多模态情感感知数字人的理解"
- 5 sections covering digital avatar emotion awareness, multimodal alignment, video compression connection, practical experience, and future questions
- Same masthead navigation as `index.html`
- Fixed paths (same-directory relative links, no `../` prefix)
- Back-link to `index.html#writing`

### `blog.html`
Legacy blog page, no longer linked from the homepage. Retained in directory but not referenced.

## 3. Design Reference
Layout and structure adapted from `https://cat-blizzard.github.io/`:
- Masthead with site-title + anchor navigation
- Two-column page grid (sidebar + content)
- Sticky sidebar with avatar, name, bio, links
- Responsive single-column on mobile

## 4. Validations Performed
- HTML parsing: both `index.html` and `emotion-aware-avatar.html` parse successfully
- All navigation anchor IDs match their href targets
- All relative file links resolve to existing files
- No phone number (+86-18788838061) present in any published file
- No external CDN, framework, or library references
- No inline styles
- No `blog.html` references in published pages
- No `script.js` reference (file does not exist)
- No `../` path prefix in `emotion-aware-avatar.html`
- Responsive CSS present with `@media` breakpoints
- Smooth scrolling with `scroll-margin-top` offset for fixed header
- No duplicate or unused CSS rules

## 5. Publishing Safeguards
- `.nojekyll`: GitHub Pages serves static files directly
- `.gitignore`: excludes `CV_xyy.tex` (contains phone number) and `2026-课程大作业1.pdf`
