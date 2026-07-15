# arunmathewofficial.github.io

Academic site for Arun Mathew, published at <https://arunmathewofficial.github.io>.

Built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io)
template, itself a fork of [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/).

Every push to `master` rebuilds and redeploys the site automatically. There is
nothing to run by hand to publish — commit and push, and GitHub Pages does the rest.

---

## Contents

- [Local preview](#local-preview)
- [Where everything lives](#where-everything-lives)
- [Site-wide settings](#site-wide-settings)
- [Navigation tabs](#navigation-tabs)
- [Editing the pages](#editing-the-pages-home-research)
- [Publications](#publications)
- [Talks](#talks)
- [Teaching](#teaching)
- [Blog posts](#blog-posts)
- [Images](#images)
- [Videos](#videos)
- [Maths](#maths)
- [The CV](#the-cv)
- [Tooling](#tooling)

---

## Local preview

Optional — you can edit files and push without ever running this. But it lets you
see changes before they go live:

```sh
bundle install          # once
bundle exec jekyll serve
```

Then open <http://localhost:4000>. Pages rebuild as you save, **except**
`_config.yml`, which needs the server restarted.

---

## Where everything lives

| Path | What it controls |
| --- | --- |
| `_config.yml` | Your name, sidebar, profile links, publication categories |
| `_data/navigation.yml` | The tabs across the top |
| `_pages/about.md` | The home page |
| `_pages/research.md` | Research page |
| `_pages/cv.md` | CV page — embeds `files/cv.pdf`, no text of its own |
| `_publications/` | One file per paper |
| `_talks/` | One file per talk |
| `_teaching/` | One file per teaching role |
| `_posts/` | Blog posts |
| `images/` | Images and your profile photo |
| `files/cv.pdf` | Your CV — the CV page shows this file |

Every content file starts with a **front matter** block — the bit fenced by `---`
lines at the top. That is metadata (title, date, venue), not page text. The page
text goes below the closing `---`.

---

## Site-wide settings

All in `_config.yml`.

**Sidebar** — under `author:`. Leave a field blank and it disappears from the
sidebar; no icon, no empty row:

```yaml
author:
  avatar           : "profile.jpeg"    # a file in images/
  name             : "Arun Mathew"
  bio              : # a short line under your name
  location         : "Melbourne, Australia"
  employer         : "DIAS, Ireland"
  email            : "tonykochumalil@gmail.com"
  googlescholar    : "https://scholar.google.com/citations?user=i8F73fwAAAAJ&hl=en"
  orcid            : "https://orcid.org/0000-0001-9896-4243"
  github           : "arunmathewofficial"    # username only, not a URL
```

Note the mix: `github` takes a bare **username**, while `googlescholar` and
`orcid` take **full URLs**. There are many more supported (`arxiv`,
`researchgate`, `linkedin`, `bluesky`, `mastodon`…) — they are all listed,
commented out, in the `author:` block.

Setting `googlescholar` also adds a "You can also find my articles on my Google
Scholar profile" line to the Publications page.

**Colour theme** — `site_theme` accepts `default`, `air`, `sunrise`, `mint`,
`dirt`, or `contrast`.

**Other switches worth knowing:**

```yaml
talkmap_link : false   # true adds a link to the talk map from the Talks page
breadcrumbs  : false   # true shows a breadcrumb trail on pages
read_more    : "disabled"
```

---

## Navigation tabs

`_data/navigation.yml`. The order here is the order on screen:

```yaml
main:
  - title: "Research"
    url: /research/
  - title: "Publications"
    url: /publications/
```

Delete an entry to hide a tab — the page itself still exists and stays
reachable by URL. To remove a page entirely, delete its file in `_pages/`.

---

## Editing the pages (Home, Research)

These are ordinary Markdown files in `_pages/`. Edit the text below the front
matter and push.

Headings use the underline style, where `======` under a line makes it a heading:

```markdown
Research interests
======

Some text. **Bold**, *italic*, and [a link](https://example.com).

* a bullet
* another bullet
```

The home page is `_pages/about.md`. It has `permalink: /`, which is what makes
it the front page rather than a separate "About" tab.

---

## Publications

One file per paper in `_publications/`. **The filename must start with a date**:
`YYYY-MM-DD-short-slug.md`.

### Add a publication

Create `_publications/2025-03-01-multi-ion-solver.md`:

```markdown
---
title: "A multi-ion non-equilibrium solver for ionised astrophysical plasmas"
collection: publications
category: manuscripts
permalink: /publication/2025-03-01-multi-ion-solver
excerpt: 'One or two sentences, shown under the title in the list.'
date: 2025-03-01
venue: 'Astronomy &amp; Astrophysics'
paperurl: 'https://doi.org/10.1051/0004-6361/202452373'
citation: 'Mathew, A., &amp; Mackey, J. (2025). &quot;Full title here.&quot; <i>Astronomy &amp; Astrophysics</i>, 695, A73.'
---

Any extra text here appears only on the paper's own page, not in the list.
```

**`category:` must be one of these three** — it decides which heading the paper
appears under:

| Category | Heading on the page |
| --- | --- |
| `manuscripts` | Journal Articles |
| `conferences` | Conference Proceedings |
| `forthcoming` | Forthcoming, Under Review, and In Preparation |

These are defined under `publication_category:` in `_config.yml`. Add a fourth
(say `books: title: 'Books'`) if you ever need one.

**Optional fields:** `slidesurl` and `bibtexurl` work exactly like `paperurl`
and add their own download links.

### Notes on the fields

- **Only the year of `date` is ever displayed** — entries render as
  "Published in *Venue*, 2025". The month and day just control the ordering, so
  a paper with only a known year is fine.
- `&amp;` for `&` and `&quot;` for quote marks inside `citation:`, because that
  field is inserted as raw HTML. `<i>...</i>` italicises the journal name.
- Newest appears first; the list is sorted by `date` descending.

### Edit or remove

Editing is just editing the file. To remove a paper, delete its file — nothing
else references it.

**These collections do not feed the CV page** — that page is only the PDF (see
[The CV](#the-cv)). A new paper shows up on `/publications/` straight away, but
your CV PDF is a separate document: to have it listed there too, update your
CV and [replace the PDF](#replacing-it-with-a-newer-cv).

---

## Talks

One file per talk in `_talks/`, named `YYYY-MM-DD-slug.md`:

```markdown
---
title: "Multi-ion Chemical Kinetics Modelling of Interstellar Shockwaves"
collection: talks
type: "Invited talk"
permalink: /talks/2023-12-12-multi-ion-chemical-kinetics-unam
venue: "Instituto de Astronomía, UNAM"
date: 2023-12-12
location: "Mexico City, Mexico"
---

Free text about the talk. Optional.
```

`type:` is free text and shows on the page — currently in use: `Invited talk`,
`Seminar`, `Public lecture`, `Outreach talk`.

**`location:` matters more than it looks.** A workflow geocodes it into a world
map at `/talkmap.html` on every push that touches `_talks/`. Keep it in
`City, Country` form so it can be found. The map is not linked from anywhere
until you set `talkmap_link: true` in `_config.yml`.

---

## Teaching

One file per role in `_teaching/`, named `YYYY-MM-DD-slug.md`:

```markdown
---
title: "Undergraduate Teaching Assistantship"
collection: teaching
type: "Undergraduate courses and laboratories"
permalink: /teaching/2015-08-01-iitg-undergraduate-teaching-assistantship
venue: "Indian Institute of Technology Guwahati, Department of Physics"
date: 2015-08-01
location: "Guwahati, India"
---

Describe the role. List individual courses here rather than making a
separate file per course.

Courses
======
* **PH307** *Statistical Mechanics* — Aug–Nov 2015
```

Use the start date for a multi-year role. Like publications, only the year shows.

---

## Blog posts

One file per post in `_posts/`, named `YYYY-MM-DD-title.md`. **The date in the
filename is required** — Jekyll ignores files in `_posts/` that lack one.

```markdown
---
title: 'Simulating bow shocks with NEMO'
date: 2026-03-14
permalink: /posts/2026/03/simulating-bow-shocks/
tags:
  - simulations
  - NEMO
---

Your post. Markdown, images, maths — all of it works here.
```

Posts appear under the **Blogs** tab, which is the `/year-archive/` page,
grouped by year, newest first. `tags:` are optional and generate tag pages.

Two things worth knowing: `future: true` is set, so a post dated in the future
appears immediately rather than waiting. And comments are configured but have no
provider set, so none are shown — to enable them, set `comments: provider:` in
`_config.yml`.

---

## Images

Put the file in `images/`, then reference it with a path starting `/images/`:

```markdown
![Simulated bow shock](/images/bow-shock.png)
```

The alt text in the square brackets is what a screen reader announces and what
shows if the image fails to load. Worth writing properly.

### Alignment and size

Append `{: .class}` directly after the image:

```markdown
![Centred](/images/plot.png){: .align-center}
![Left, text wraps around](/images/plot.png){: .align-left}
![Right, text wraps around](/images/plot.png){: .align-right}
![Full content width](/images/plot.png){: .full}
```

For a specific width, use HTML instead — Markdown has no syntax for it:

```html
<img src="/images/plot.png" alt="Simulated emission map" width="400">
```

### Caption

```html
<figure>
  <img src="/images/plot.png" alt="Simulated emission map">
  <figcaption>Synthetic X-ray emission from a wind-driven bow shock.</figcaption>
</figure>
```

### Several images side by side

Declare them in the front matter, then place the gallery in the body:

```markdown
---
title: "My page"
gallery:
  - url: /images/one.png
    image_path: /images/one.png
    alt: "First"
  - url: /images/two.png
    image_path: /images/two.png
    alt: "Second"
---

{% include gallery caption="Two views of the same simulation." %}
```

Two images lay out as halves, three or more as thirds.

**Keep files small.** A few hundred KB per image is plenty; multi-MB photos make
the page slow. Prefer PNG for plots and diagrams, JPEG for photographs.

---

## Videos

There is no video helper in this theme, so embed with plain HTML.

**YouTube or Vimeo** — take the ID from the URL (`youtube.com/watch?v=ABC123`
gives `ABC123`) and use the `/embed/` form:

```html
<iframe width="560" height="315"
        src="https://www.youtube.com/embed/ABC123"
        title="Simulation flythrough"
        frameborder="0" allowfullscreen></iframe>
```

To make it scale on phones instead of being fixed at 560px, wrap it:

```html
<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe src="https://www.youtube.com/embed/ABC123"
          title="Simulation flythrough"
          style="position: absolute; width: 100%; height: 100%;"
          frameborder="0" allowfullscreen></iframe>
</div>
```

The `56.25%` is 9÷16 — it reserves the right height for a 16:9 video. Use `75%`
for 4:3.

**A video file of your own** — put it in `files/` and serve it directly. No
YouTube involved:

```html
<video controls width="100%">
  <source src="/files/simulation.mp4" type="video/mp4">
</video>
```

Keep these well under ~50 MB. GitHub Pages is not a video host, and there is a
1 GB limit on the whole repository — for anything large, upload to YouTube and
embed it.

---

## Maths

MathJax is loaded on every page (via `_includes/footer/custom.html`), so LaTeX
works anywhere — pages, posts, publication entries.

**Use `$$…$$` for everything.** Whether it comes out inline or centred depends
on where you put it, not on the delimiter:

```markdown
Compact objects in $$f(R,T)$$ gravity behave differently.   <- inline

$$
\frac{dP}{dr} = -\frac{G m(r) \rho(r)}{r^2}
$$
```

Inside a sentence it renders inline; alone in its own paragraph it renders as a
centred display equation.

> **Single `$…$` does not work.** It is left on the page as literal text —
> you would see `$f(R,T)$` rather than the formula. MathJax only treats single
> dollars as maths when configured to, and this site does not configure it.
> Use `$$…$$` even for a single symbol. (`\\(…\\)` also works inline, if you
> prefer the explicit form.)

---

## The CV

The CV page is **just the PDF**. `_pages/cv.md` holds no CV text of its own — it
embeds `files/cv.pdf` in a viewer and offers a download link underneath. The
whole page is these two lines:

```html
<iframe src="/files/cv.pdf" width="100%" height="800" frameborder="no" border="0" marginwidth="0" marginheight="0"></iframe>

You can download a PDF copy of my CV [here](/files/cv.pdf).
```

So the PDF *is* the CV. There is no second copy to keep in sync.

### Replacing it with a newer CV

**Overwrite `files/cv.pdf` and push. That is the whole job** — the page picks up
the new file automatically, and nothing else needs editing:

```sh
cp /path/to/your/new-cv.pdf files/cv.pdf
git add files/cv.pdf
git commit -m "Update CV"
git push
```

The page updates within a minute or two of the push.

**The filename must stay exactly `files/cv.pdf`.** That path is hardcoded in
`_pages/cv.md` in two places, the iframe and the download link. If you want to
keep a dated name like `cv-2026-03.pdf`, you have to edit both lines to match,
so overwriting the same filename is the easier path.

A few practical notes:

- **Hard-refresh to see the change.** Browsers cache PDFs aggressively, so your
  old CV may persist on screen after a successful deploy. Use Ctrl+Shift+R
  (Cmd+Shift+R on a Mac), or open the URL in a private window, before concluding
  something is broken.
- **Every version stays in Git history**, since the PDF is committed. Replacing
  the file removes it from the live site but not from the repository's past.
- **The viewer does not work everywhere.** Embedded PDFs are unreliable on
  phones — iOS Safari and some Android browsers show a blank box or only the
  first page. That is why the download link below the viewer matters; it is the
  fallback for every visitor the iframe fails. Do not remove it.
- **Keep the file reasonably small.** Under a few MB loads promptly in the
  embedded viewer.

### Changing the viewer height

`height="800"` in `_pages/cv.md` is the viewer's height in pixels. Raise it to
show more of a page at once; `height="90vh"` instead makes it 90% of the
browser window's height.

---

## Tooling

**`markdown_generator/`** — converts a BibTeX file, an ORCID profile, or a TSV
export into publication entries in bulk, rather than writing each by hand.
`PubsFromBib.ipynb` is the BibTeX one; `publications.tsv` and `talks.tsv` are
worked examples of the input format. Check the generated files before committing
— the output usually needs a little tidying.

**`talkmap.ipynb`** — reads the `location:` field of every file in `_talks/`,
geocodes it, and writes `talkmap/org-locations.js`, which draws the map at
`/talkmap.html`. `.github/workflows/scrape_talks.yml` runs this automatically on
any push touching `_talks/` and commits the result, so **after adding a talk,
`git pull` before your next change** — the bot will have pushed a commit.

Both are excluded from the built site in `_config.yml`, so they are not
published as public URLs.
