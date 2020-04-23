# doaj-templates

A static Jekyll site for doaj.org


## Install Jekyll

Ruby is required.

1. `gem install jekyll`

## Running the site locally

1. `git clone https://github.com/DOAJ/doaj-static.git`
2. `cd doaj-static`
3. `jekyll s`
4. Navigate to `http://127.0.0.1:4000` in your browser
5. You must make changes locally (and not via Github) to see them.

## Building the site

1. `git clone https://github.com/DOAJ/doaj-static.git`
2. `cd doaj-static`
3. `jekyll build`
4. Compiled static HTML, CSS, & JS will be found in `_site/`

## Updating static content & data

Each static page is represented by a single `.md` file.

Most of the content of doaj.org’s static pages can be written in Markdown (`.md`) and modified in the following directories (representing a section of the site):
- `about/`
  - `index.md`: the main About section page (_Mission_, _History_)
  - `advisory-board-council.md`
  - `faq.md`
  - `team-ambassadors.md`
  - `volunteers.md`
- `apply/`
  - `guide.md`
  - `seal.md`
  - `transparency.md`
  - `why-index.md`
- `data/`
  - `openurl.md`
  - `public-data-dump.md`
  - `widgets.md`
  - `xml.md`
- `support/`
  - `index.md`: the main Support section page (_Support DOAJ_)
  - `publisher-supporters.md`
  - `sponsors.md`
  - `supporters.md`

### Static page contents

Static content is usually long-form, unstructured texts (Data documentation, About...).

Each static page includes YAML front matter at the top of the document which indicates:
- `layout`:
  - the layout to be used for that page
  - for now, we only have `sidenav`
- `title`:
  - the page title displayed in `<h1>` and `<title>` tags
- `toc` (`true` or `false`):
  - whether or not we want a table of contents on the side
- `highlight` (`true` or `false`):
  - whether or not the page should start with a highlight section (slightly darker background, as seen in the homepage’s search box)

### Data files

Whenever we have structured content that could be stored in a database (e.g. records of people or organisations with metadata), we use Jekyll’s _data files_. 

Data files can be in `CSV`, `YAML`, or `JSON` and are uploaded in the **`_data/`** directory (not to be confused with the `data/` section).

We are currently using the `YAML` (`.yml`) format, but are not restricted to it.

The following information is represented in data files:
- _About_ section
  - Advisory Board: `advisory-board.yml`
  - Council: `council.yml`
  - Team: `team.yml`
  - Ambassadors: `ambassadors.yml`
  - Volunteers: `volunteers.yml`
- _Support_ section
  - Publisher supporters: `publisher-supporters.yml`
  - Sponsors: `sponsors.yml`
  - Supporters: `supporters.yml`
- Other
  - Promotional snippet (in page sidebar): `promo.yml`

**Make sure** to follow the indentation and line breaks of already-existing records when adding a new line or entry.
