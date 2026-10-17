# StoryCast

StoryCast is an accessible 3-page microsite for audio and video stories, built for the Advanced Front-End Web Development course. It is a calm, typography-led "online magazine" where the story is the main character.

Built with semantic HTML5, Sass, and vanilla CSS. No frameworks.

## Pages

| Page | File | What it does |
|---|---|---|
| Home | [`index.html`](./index.html) | Introduces StoryCast and lists the featured stories |
| Story (audio) | [`story/story-one.html`](./story/story-one.html) | Audio player, full transcript, related stories |
| Story (video) | [`story/story-two.html`](./story/story-two.html) | Embedded video, transcript link, related stories |
| About / Access | [`about.html`](./about.html) | Mission and accessibility features |

## Design and research

- Sitemap (Figma): https://words-sling-36885228.figma.site/
- Wireframes (3 pages): [add Figma link]
- High-fidelity mockups (3 pages): [add Figma link]
- Research document: [`docs/research.pdf`](./docs/research.pdf)
- Sitemap (PDF): [`docs/sitemap.pdf`](./docs/sitemap.pdf)

### Design tokens

| Token | Value | Use |
|---|---|---|
| Paper | `#F8F5EF` | Background |
| Ink | `#242321` | Text |
| Oxblood | `#963D48` | Links, labels, story numbers |
| Stone | `#DDD5C9` | Thin dividers |

Fonts: Newsreader (headings) and Inter (interface text).

## Project structure

```text
storycast/
├── index.html
├── about.html
├── story/            Story pages
├── sass/             main.scss + partials
│   ├── _colors.scss
│   ├── _typography.scss
│   ├── _spacing.scss
│   ├── _reset.scss
│   ├── _base.scss
│   ├── _layout.scss
│   ├── _components.scss
│   └── _accessibility.scss
├── css/              Compiled CSS
├── assets/           Images, audio, captions, transcripts
├── docs/             Research PDF and sitemap PDF
├── design/           Design notes
└── README.md
```

## Technical approach

- **Sass:** partials and tokens (colors, typography, spacing), compiled to `css/main.css`.
- **BEM naming:** for example `.story-entry`, `.story-entry__title`, `.story-entry__meta`.
- **Cascade layers:** `reset, base, layout, components, utilities`.
- **Layout:** CSS Grid for story entries, the footer, and the access list. Flexbox for the header and menus.
- **Container query:** `.story-list` is the container. Each `.story-entry` changes from three columns to one column when the list is narrow, even on a wide screen.

## Run locally

1. Install Node.js, then install Sass:
```text
   npm install --global sass
```
2. Compile Sass from the project root:
```text
   sass sass/main.scss css/main.css
```
   Or watch for changes:
```text
   sass --watch sass/main.scss:css/main.css
```
3. Open `index.html` with a local server, such as the VS Code Live Server extension.

## Accessibility checklist

Target: WCAG 2.1 Level AA.

- [x] Semantic `header`, `nav`, `main`, `article`, `section`, `figure`, `figcaption`, and `footer`
- [x] Logical heading order, one `h1` per page
- [x] Skip link that appears on keyboard focus and jumps to the main content
- [x] Visible focus outlines on links and controls
- [x] Text contrast of at least 4.5:1 (ink on paper 14.4:1, oxblood on paper 6.3:1)
- [x] Audio has native controls, an accessible label, and a full visible transcript
- [x] Video has a descriptive title, and a link to the YouTube transcript
- [x] Images have useful alt text, width, and height
- [x] Each `nav` has its own label, and the current page is marked with `aria-current`
- [x] Story numbers are hidden from screen readers (decorative only)
- [x] Responsive at 360px, 768px, and 1440px
- [x] `prefers-reduced-motion` is respected
- [x] Nothing plays automatically
- [ ] Formal WCAG 2.1 AA audit (not done)

## Known limitations

- The video is a YouTube embed. Captions are controlled by YouTube, so there is no local `<track>` caption file.
- The video transcript is linked on YouTube, not copied onto the page.
- The images are designed placeholders, not documentary photography.
- The site was tested by hand (keyboard, contrast checker, browser resizing). It has not had a screen reader test, a formal audit, or a usability study.
- Story content is fictional or illustrative, and is marked as such on the site.

## Credits

- Video: "Where is home? Where do you belong?" by Vamba Sherif, TEDxGroningen (2016), via TEDx Talks on YouTube.
- Fonts: Newsreader and Inter, via Google Fonts.

## Tools

HTML5, Sass, CSS (Grid, Flexbox, container queries, cascade layers), Figma, VS Code, Git and GitHub.