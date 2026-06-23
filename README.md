# your site

A small, warm, minimal personal website. No build step, no frameworks, no npm —
just HTML and one stylesheet. Double-click `index.html` to see it.

## the files

| file | what it is |
|------|------------|
| `index.html` | the homepage — your name, a typed line, and the section links |
| `alt-home.html` | an alternate cover (scattered links) — linked from the homepage; swap names with `index.html` to use it instead |
| `resume.html` | experience + education timeline, and the PDF download |
| `projects.html` | your projects — a `technical / not nerd stuff` toggle |
| `snapshots.html` | a travel journal of photos grouped by place, with a click-to-enlarge lightbox (the only colour on the site) |
| `musings.html` | blogs, musings, and half-baked ideas |
| `now.html` | what you're currently listening to / reading |
| `interests.html` | the miscellaneous rest of you |
| `styles.css` | **the one place that controls how everything looks** |

## how to edit

Open any `.html` file in a text editor. Look for `EDIT:` comments — they mark the
spots meant for your words. Things to know:

- **Your name + email** appear in every page (the nav, and the footer line). Find &
  replace `your name` and `you@example.com` across all files when you're ready.
- **Add another project / job / photo:** copy a block and paste it below itself.
  Each repeatable block has a comment like `duplicate to add another`.
- **Add a real photo:** make a `photos/` folder next to these files, drop an image
  in, then in `snapshots.html` find a `<button class="shot">`, replace its
  `<div class="placeholder">photo</div>` with
  `<img src="photos/your-photo.jpg" alt="a short description">`, and add
  `data-full="photos/your-photo.jpg"` to that button (that's the big version the
  click-to-enlarge lightbox shows). Duplicate a whole `<section class="trip">` to add
  a new place.
- **Add your resume PDF:** save it as `resume.pdf` right next to `resume.html`.
  The download button already points at it.

## how to change the look

You almost never edit styling inside the HTML. Open `styles.css` and edit the
**`:root`** block at the top — every colour, font, and spacing value lives there,
each with a comment. Examples:

- Want a pure-white background? Change `--paper: #f8f5ef;` to `--paper: #ffffff;`.
- Want bigger text? Bump `--size-body`.
- Want more air? Raise `--gap-section`.

Change one value, the whole site updates.

## how to add a new page

1. Copy `interests.html` to `newpage.html`.
2. Change the `<title>` and the `<h1 class="page-title">`.
3. Add a link to it: a `<li>` in the `nav-links` of every page, and an `<a>` in the
   `.menu` nav in `index.html`.

## fonts

The pages load **Hanken Grotesque** (headings) and **Inter** (body) from Google Fonts via
the `<link>` in each `<head>`. That needs an internet connection. If you'd rather
not depend on Google, delete that `<link>` — the site falls back to clean system
fonts automatically (defined in `styles.css`).

## putting it online

It's plain static files, so anything works: GitHub Pages, Netlify, Cloudflare
Pages — drag the folder in. No server needed.
