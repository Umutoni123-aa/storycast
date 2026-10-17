# StoryCast

An accessible 3-page microsite for audio and video stories. Built with semantic HTML, Sass, and vanilla CSS. No frameworks.

## Pages
- `index.html`: Home
- `story/story-one.html`: Story page
- `about.html`: About / Access

## Project structure
```
storycast/
├── index.html
├── about.html
├── story/
├── sass/        (main.scss + partials)
├── css/         (compiled CSS)
├── assets/      (images, audio, video, captions, transcripts)
├── docs/        (research PDF, sitemap)
└── design/      (Figma links)
```

## Design
- Sitemap: `docs/sitemap.pdf`
- Wireframes (Figma): []
- High-fidelity mockups (Figma): []

## Run locally
1. Install Node.js and Sass: `npm install -g sass`
2. Compile Sass: `sass --watch sass/main.scss:css/main.css`
3. Open `index.html` with the Live Server extension in VS Code.

## Accessibility checklist
- [ ] Semantic HTML (header, nav, main, article, section, figure, footer)
- [ ] Logical heading order, one h1 per page
- [ ] Skip link
- [ ] Visible focus outlines
- [ ] Color contrast meets WCAG AA
- [ ] Audio has a full transcript on the page
- [ ] Images have alt text
- [ ] Keyboard navigation tested
- [ ] Responsive at mobile, tablet, and desktop widths
- [ ] Container query on the story list

## Known limitations
- The site aims for WCAG 2.1 AA but has not had a formal audit.

## Tools
HTML5, Sass, CSS (Grid, Flexbox, container queries, cascade layers), Figma.