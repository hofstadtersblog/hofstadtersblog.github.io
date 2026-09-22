# site template

A minimalist, colorful personal site built for GitHub Pages, using
Jekyll (which GitHub builds for you automatically — no separate build
step needed once it's pushed).

## Putting it on GitHub Pages

1. Create a new GitHub repository.
   - If you want it at `https://yourname.github.io`, name the repo
     exactly `yourname.github.io`.
   - Otherwise, name it anything, and your site will live at
     `https://yourname.github.io/repo-name/`.
2. Push everything in this folder to that repo (root of the repo, not
   inside a subfolder).
3. In the repo, go to **Settings → Pages**, and under "Build and
   deployment," set **Source** to "Deploy from a branch," branch
   `main`, folder `/ (root)`.
4. If your repo is **not** named `yourname.github.io`, open
   `_config.yml` and set `baseurl: "/repo-name"` (with the leading
   slash, no trailing slash).
5. Wait a minute or two, then visit the URL GitHub gives you.

That's it — no npm, no build tooling, nothing to install to go live.

## Editing locally (optional, but nice for previewing before you push)

You'll need Ruby installed, then:

```
bundle install
bundle exec jekyll serve
```

and open `http://localhost:4000`.

## Adding an entry to any section

Each section is a folder starting with an underscore:

```
_reading/       _mathphysics/     _simulations/
_projects/      _music/           _rambling/
```

To add a post, add a new Markdown file to the relevant folder. Name it
`YYYY-MM-DD-a-short-title.md` (the date in the filename is what sets
the post's date if you don't set one in the front matter, but it's
clearer to set it explicitly). At the top of the file, include front
matter like this:

```
---
title: "Your title here"
date: 2026-02-14
---

Your content, in Markdown, goes here.
```

That's genuinely all you need to do — the listing pages
(`/reading/`, `/math-physics/`, etc.) update themselves automatically,
newest first.

## Writing math

LaTeX works anywhere, via MathJax:

- inline: `$e^{i\pi}+1=0$`
- block:
  ```
  $$
  \int_0^\infty e^{-x^2}\,dx = \frac{\sqrt{\pi}}{2}
  $$
  ```

## Changing your name / pseudonym

Edit `title:` and `author:` at the top of `_config.yml`. That single
change propagates through the header, page titles, and RSS feed.

## Changing the colors

Each section has its own accent color, defined in two places that need
to agree:

- `_config.yml` — under `sections: <name>: accent:` (used for the
  homepage cards)
- `assets/css/style.scss` — under `body.section-<name> { --accent: ...; }`

Everything else (backgrounds, text, layout) is intentionally left
alone — the idea is one accent color doing the work per section, not a
rainbow all at once.

## Structure at a glance

```
_config.yml          site settings, section labels/colors/blurbs
index.md             homepage / about page
reading.md           listing page for the reading section
math-physics.md      listing page for math & physics
simulations.md       listing page for simulations
projects.md          listing page for projects
music.md             listing page for music
rambling.md          listing page for rambling
_reading/ etc.        one Markdown file per entry, per section
_layouts/             default.html (plain pages), post.html (entries)
_includes/            head, header, footer partials
assets/css/style.scss all styling
assets/js/typing.js   homepage typewriter effect (edit PHRASES here)
assets/img/           images for simulations, etc.
```
