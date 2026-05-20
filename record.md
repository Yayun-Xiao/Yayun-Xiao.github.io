# Project Record: Personal Homepage & Blog

## 1. Overview
Created a static personal homepage and technical blog for Yayun Xiao (肖雅芸) located in `/home/xyy/xyy_homepage`. The website was built purely using semantic HTML and custom CSS, adhering to a strict green & white design system without reliance on external frameworks or libraries.

## 2. Files Created
- **`styles.css`**: Developed a responsive design system utilizing CSS variables. Configured a professional green/white color palette (`--color-primary: #1e5631`, `--color-bg: #ffffff`) and established a clean, rigorous editorial typographic scale.
- **`index.html`**: The main personal homepage. Synthesized factual personal data from `CV_xyy.tex`.
  - Included personal introduction, education, technical skills, and honors.
  - Highlighted selected research experience (Multimodal Emotion-aware Video Compression and Digital Avatar Driving, Interactive Dialogue System).
  - Ensured sensitive information (phone number) from the CV was excluded while retaining email and GitHub links.
  - Set up navigation linking to the blog page.
- **`blog.html`**: The first technical blog entry.
  - **Topic**: *Rethinking Video Compression Through the Lens of Digital Avatars*.
  - **Content**: An original reflection integrating themes from the work survey (SumTalk, TalkSummary, CineTalk) and discussing the semantic vs. pixel-level challenges in multimodal emotion-aware video compression and digital human synthesis.

## 3. Validations Performed
- Checked the contents of `/home/xyy/xyy_homepage` using standard shell tools.
- Ensured `index.html`, `blog.html`, and `styles.css` were properly structured and existing in the directory.
- Confirmed that there are no external network calls or dependencies (no Node.js, no `package.json`, no external font CDNs). All styling and structural definitions are strictly self-contained.
- Verified that no CV files or PDFs were altered during the process.
- Checked that cross-linking between `index.html` and `blog.html` uses valid relative paths.

## 4. Follow-up Refinement
- Added an explicit blog entrance card on the homepage to satisfy the assignment requirement that the blog can be reached directly from the homepage, beyond the top navigation link.
- Removed inline homepage styles and moved them into reusable `.name-native` and `.research-focus` CSS classes.
- Ran a local Python static validation script confirming HTML parsing, existing relative links, no private phone-number leak, no inline styles, and responsive CSS presence.
- Attempted LSP diagnostics on `/home/xyy/xyy_homepage`; unavailable because the configured `biome` language server is not installed in the environment.

## 5. GitHub Pages Publishing Preparation
- Added `.nojekyll` so GitHub Pages serves the static HTML/CSS files directly without Jekyll processing.
- Added `.gitignore` to exclude `CV_xyy.tex` and the assignment PDF from the public repository because the CV source contains a private phone number and the PDF is not required for page access.
