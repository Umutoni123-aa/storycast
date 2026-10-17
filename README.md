# StoryCast

StoryCast is a three-page accessible microsite for audio and human stories. It uses semantic HTML, Sass, vanilla CSS, CSS Grid/Flexbox, container queries, and cascade layers. It does not use a framework.

## Pages

- [`index.html`](./index.html): home and story list
- [`story/story-one.html`](./story/story-one.html): audio story with a visible transcript
- [`about.html`](./about.html): project and accessibility information

## Project structure

```text
storycast/
├── index.html
├── about.html
├── story/story-one.html
├── sass/        Sass entry point and partials
├── css/         Compiled CSS
├── assets/      PNG images and WAV audio
├── docs/        Research and sitemap PDFs (not included yet)
└── design/      Figma link placeholders
```

## Design

- Paper: `#F8F5EF`
- Ink: `#242321`
- Oxblood: `#963D48`
- Stone: `#DDD5C9`
- Headings: Newsreader
- UI text: Inter

Figma wireframes: `[add Figma wireframe URL]`

Figma high-fidelity mockups: `[add Figma mockup URL]`

## Run locally

1. Install Node.js and Sass: `npm install --global sass`
2. From the project root, compile Sass:

   ```text
   sass sass/main.scss css/main.css
   ```

3. Open `index.html` with a local server such as VS Code Live Server. A local server is recommended so all relative assets behave consistently.

## Accessibility checklist

- [x] Semantic `header`, `nav`, `main`, `article`, `section`, `figure`, `figcaption`, and `footer`
- [x] Logical heading order with one `h1` per page
- [x] Skip link that appears on keyboard focus and jumps to `#main`
- [x] Visible focus outlines for links and native audio controls
- [x] Color choices meet the intended WCAG AA text contrast target
- [x] Audio has native controls and a full visible transcript
- [x] Images have useful alt text, width, and height attributes
- [x] Keyboard-friendly navigation and current-page indicators
- [x] Responsive layout at mobile, tablet, and desktop widths
- [x] Container query on `.story-list` stacks `.story-entry` at narrow widths
- [x] `prefers-reduced-motion` disables animation and transitions

## Known limitations

- The listed follow-up stories are editorial placeholders marked “Coming soon”; they are not videos and do not claim captions.
- The available WAV is a two-second audio preview, not a narrated recording of the transcript.
- The image files are designed placeholder title cards, not documentary photography.
- Figma URLs and the research/sitemap PDFs still need to be supplied by the project author. The `docs/` directory does not currently contain `research.pdf` or `sitemap.pdf`.
- The site has not had a formal automated WCAG audit or usability study.

## Tools

HTML5, Sass, CSS (Grid, Flexbox, container queries, cascade layers), and Figma.
