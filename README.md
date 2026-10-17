# StoryCast

StoryCast is an accessible microsite for audio and human stories. It uses semantic HTML, Sass, vanilla CSS, CSS Grid/Flexbox, container queries, and cascade layers. It does not use a framework.

## Pages

- [`index.html`](./index.html): home and story list
- [`story/story-one.html`](./story/story-one.html): audio story with a visible transcript
- [`story/story-two.html`](./story/story-two.html): YouTube video story with a transcript link
- [`about.html`](./about.html): project and accessibility information

## Project structure

```text
storycast/
├── index.html
├── about.html
├── story/       Story pages
├── sass/        Sass entry point and partials
├── css/         Compiled CSS
├── assets/      PNG images and WAV audio
├── docs/        Research and sitemap PDFs
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
- [x] Skip link and visible focus outlines checked in a browser with the keyboard
- [x] Audio has native controls and a full visible transcript
- [x] Images have useful alt text, width, and height attributes
- [x] Keyboard-friendly navigation and current-page indicators
- [x] Responsive layout checked at 360px, 768px, and 1440px
- [x] Container query on `.story-list` stacks `.story-entry` at narrow widths
- [x] `prefers-reduced-motion` disables animation and transitions
- [ ] Formal WCAG 2.1 AA audit

## Known limitations

- The available WAV is a two-second audio preview, not a narrated recording of the transcript.
- The video uses a YouTube embed; captions are controlled by YouTube and there is no local `<track>` file.
- The image files are designed placeholder title cards, not documentary photography.
- The Figma URLs are placeholders and must be replaced by the project author.
- The site has not had a formal automated WCAG audit or usability study.

## Tools

HTML5, Sass, CSS (Grid, Flexbox, container queries, cascade layers), and Figma.
