# Edgar Allan Poe — Author Website Portfolio Concept

A complete five-page static author website created as a Northrealm Digital portfolio demonstration. The site uses plain HTML5, CSS3, and vanilla JavaScript, with no build tools or runtime dependencies.

This is an independent portfolio concept. It is not an official Edgar Allan Poe estate website and is not affiliated with any estate, museum, archive, or publisher.

## Project structure

```text
poe-author-website/
├── index.html          Homepage
├── about.html          Biography and timeline
├── books.html          Filterable selected works
├── journal.html        Historical editorial journal
├── contact.html        Demonstration contact and newsletter forms
├── css/
│   └── styles.css      Shared responsive design system
├── js/
│   └── main.js         Navigation, reveals, filters, and demo forms
└── img/
    ├── edgar-allan-poe.jpg
    └── raven-dore.jpg
```

## Local preview

The site can be opened directly by double-clicking `index.html`. For the best test environment, serve the folder over HTTP:

```powershell
cd path\to\poe-author-website
python -m http.server 8080
```

Then visit `http://localhost:8080`.

No package installation or build command is required.

## Deploy to Cloudflare Pages

### Direct Upload

1. Sign in to the Cloudflare dashboard.
2. Open **Workers & Pages** and choose **Create application** → **Pages** → **Upload assets**.
3. Name the project and upload this entire `poe-author-website` folder (or a ZIP of its contents).
4. Deploy. The root `index.html` is detected automatically.

### Git integration

1. Push this folder to a GitHub or GitLab repository.
2. In Cloudflare Pages, choose **Connect to Git** and select the repository.
3. Use these settings:
   - Framework preset: `None`
   - Build command: leave blank
   - Build output directory: `/` (or the repository subfolder containing `index.html`)
4. Save and deploy.

Because all asset paths are relative, the site works both at a custom domain and in a Pages preview deployment.

## Image licensing and sources

Both included historical images were selected only after their licensing status was verified on Wikimedia Commons.

- `img/edgar-allan-poe.jpg` — W. S. Hartshorn, *Edgar Allan Poe*, 1848. Public domain. Source and license record: <https://commons.wikimedia.org/wiki/File:Edgar_Allan_Poe_1848.jpg>
- `img/raven-dore.jpg` — Gustave Doré, illustration for *The Raven*, 1884. Public domain. Source and license record: <https://commons.wikimedia.org/wiki/File:Paul_Gustave_Dore_Raven15.jpg>

## Historical reference set

Biographical dates and publication context were checked against:

- U.S. National Park Service, “The Life and Times of Edgar Allan Poe”: <https://www.nps.gov/edal/learn/historyculture/timelines-lifeandtimespoe.htm>
- Academy of American Poets, “About Edgar Allan Poe”: <https://poets.org/poet/edgar-allan-poe>
- Edgar Allan Poe Society of Baltimore, chronology: <https://www.eapoe.org/geninfo/poechron.htm>

The journal entries are original editorial summaries written for this demonstration. The site contains no invented testimonials, reviews, historical publications, or purchase links.

## Functional notes

- The mobile navigation supports keyboard use and closes with `Escape`.
- Current-page navigation is set automatically from the file name.
- Reduced-motion preferences disable reveal animation.
- The works page filter operates entirely in the browser.
- Both forms are intentionally non-functional demonstrations. They prevent submission, store nothing, and display an explicit confirmation message.
- Structured data appears on the home, biography, works, and journal pages.

## Five-page test checklist

### Global

- [ ] Open all five pages and confirm there are no missing assets or console errors.
- [ ] Test at approximately 1440 px, 1024 px, 768 px, 390 px, and 320 px wide.
- [ ] Confirm the shared header and footer appear consistently on every page.
- [ ] Confirm the active navigation link matches the current page.
- [ ] Navigate using only `Tab`, `Shift+Tab`, `Enter`, and `Escape`.
- [ ] Verify the skip link becomes visible on keyboard focus.
- [ ] Check text contrast, focus outlines, heading order, and image alternative text.
- [ ] Enable reduced motion at OS/browser level and confirm content remains visible without animation.

### `index.html`

- [ ] Confirm the hero image, primary calls to action, featured works, quotation, and journal callout display correctly.
- [ ] Confirm all internal links reach the intended page or work.

### `about.html`

- [ ] Confirm the portrait and public-domain attribution display.
- [ ] Check the biography and every timeline entry at desktop and mobile widths.

### `books.html`

- [ ] Test All Works, Poetry, Tales, and Mystery filters.
- [ ] Confirm every required work is present: *The Raven*, *The Tell-Tale Heart*, *The Fall of the House of Usher*, and *The Black Cat*.
- [ ] Confirm browser Back/Forward behavior remains normal after filtering.

### `journal.html`

- [ ] Confirm the featured essay, all three editorial notes, and external source links render correctly.
- [ ] Verify external sources open and remain valid before a production launch.

### `contact.html`

- [ ] Confirm demo labeling is visible before interacting with either form.
- [ ] Test required-field and email-format validation.
- [ ] Submit valid sample data and confirm the “nothing was sent or stored” status appears.
- [ ] Confirm no network request, email, or subscription is created.

## Production handoff notes

Before adapting this concept for a real client, replace portfolio language and historical branding, configure the client’s domain and canonical URLs, add a real privacy policy, connect approved form/newsletter services, and update Open Graph image URLs to absolute production URLs.
