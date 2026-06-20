# DSBMS — Hugo site

A static site for the **Data Science & Bioinformatics for Mass Spectrometry of
Small Molecules (DSBMS)** group, IBG-5, Forschungszentrum Jülich. Synthesized
from the frozen `v1` design (see `../versions/v1/`).

## Layout

```
hugo/
├── hugo.toml                # config, params, main menu
├── content/                 # one folder per section
│   ├── _index.md            # home
│   ├── research/_index.md
│   ├── tools/_index.md
│   ├── standards/_index.md
│   ├── team/_index.md
│   └── publications/        # one Markdown file per paper (front-matter only)
├── data/                    # the editable content for data-driven pages
│   ├── research.yaml        # four research areas + applications
│   ├── tools.yaml           # tool cards (delivery type, OS, links, registries)
│   ├── standards.yaml       # standards cards
│   └── team.yaml            # lead, members, former members
├── layouts/                 # templates
│   ├── _default/baseof.html
│   ├── partials/{header,footer}.html
│   ├── index.html           # landing
│   ├── research/list.html
│   ├── tools/list.html
│   ├── standards/list.html
│   ├── team/list.html
│   └── publications/{list,single}.html
└── static/
    ├── css/main.css         # the whole design system
    └── img/emblem.png
```

## Editing content

- **Tools** — edit `data/tools.yaml`. Each tool: set `web` / `desktop` /
  `library` / `rest` booleans, an `os` list (shown for desktop tools), and paste
  URLs into `github`, `docker`, `biotools`, `conda`, `bioconductor`, `denbi`.
  An empty string renders a dashed "to be added" chip. `external: true` marks a
  third-party tool (e.g. Skyline).
- **Team** — edit `data/team.yaml` (lead, `members`, `former`). Replace the
  placeholder names, focus lines and `linkedin` URLs.
- **Research / Standards** — edit the YAML in `data/`.
- **Publications** — add a Markdown file in `content/publications/`. Copy an
  existing one; all content lives in the front matter (`area`, `areanum`,
  `weight`, `tag`, `year`, `venue`, `authors`, `doi`, `toolurl`, `idea`, `lead`,
  `concepts`, `findings`). `areanum` groups papers; `weight` orders them.
- **Portraits** — drop images in `static/img/` and swap the `.portrait`
  placeholders in `layouts/team/list.html` for `<img>` tags.

## Run locally

```bash
hugo server -D      # needs Hugo extended ≥ 0.128
```

Open http://localhost:1313.

## Deploy to GitHub Pages

1. Push the **contents of this `hugo/` folder** to the root of the `DSBMS`
   repository (so `hugo.toml` sits at the repo root). The included
   `.github/workflows/hugo.yml` builds and deploys on every push to `main`.
2. In the repo: **Settings → Pages → Build and deployment → Source: GitHub
   Actions**.

The workflow sets `--baseURL` automatically from the Pages URL, so project-site
sub-paths work without editing `hugo.toml`.
