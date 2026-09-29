# SampleHTML1

> A two-page static site about Kerala travel, built as an HTML/CSS exercise.

A small multi-page site with a splash/landing page and an inner content page,
sharing one stylesheet. The landing page uses a "go" form to navigate to the
second page — a common beginner pattern for page-to-page navigation without
JavaScript.

## Features

- **Two pages** — `index.html` (splash) and `body.html` (content).
- **Navigation without JavaScript** — `index.html` contains a
  `<form action="body.html">` with a submit button, which acts as a
  "continue" link.
- **Travel content** — a list of places to visit in Kerala with descriptions
  laid out as table rows.
- **Local images** — five photographs and two logo variants in `images/`.
- **Shared stylesheet** — `style.css` styles both pages.
- **Zero dependencies** — no JavaScript, no framework, no build step, no CDN.

## Tech Stack

- **HTML5** — `index.html`, `body.html`.
- **CSS3** — one stylesheet, `style.css`.
- **Static images** — `images/` (JPEG + WebP), `images/logo.ico`.
- **Favicon** — `images/logo.ico`.

No JavaScript is used anywhere on this site.

## Installation

There is nothing to install:

```bash
git clone https://github.com/Hashim-Zj/SampleHTML1.git
cd SampleHTML1
```

## Usage

Open `index.html` in any browser, or serve it locally:

```bash
python3 -m http.server 8000
# -> http://localhost:8000
```

The site is also published at <https://hashim-zj.github.io/SampleHTML1/>.

## Project Structure

```text
SampleHTML1/
├── index.html      Splash page, navigates to body.html
├── body.html       Places to visit in Kerala
├── style.css       Styles for both pages
├── images/
│   ├── kerala-turisom.jpeg
│   ├── plot-land-karala.jpg
│   ├── logo.ico
│   ├── logo.webp
│   └── my-kerala.webp
└── favicon.ico
```

## Configuration

None. The site takes no configuration, environment variables, or build input.

## Development

There is no build step and no test suite. Edit either `.html` file or
`style.css` and reload the browser.

All cross-page navigation uses relative paths (`body.html`, `./style.css`,
`./images/logo.ico`), so the site works when served from a subdirectory such
as a GitHub Pages project path.

Both pages share `body { ... }` rules and differ by a `body id` — `#index_body`
on the splash page — so the two layouts are separated by ID rather than by a
separate stylesheet.

## License

No license file is present. Add one before redistributing this code. The
photographs in `images/` carry their own usage terms.
