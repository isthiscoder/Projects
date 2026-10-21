# Projects

End to end projects deployed & documented. Try them out at [projects.isidd.dev](https://projects.isidd.dev).
How each one is built: [architecture.isidd.dev](https://architecture.isidd.dev) · How the technology works: [playbook.isidd.dev](https://playbook.isidd.dev)

## How it works
- **Home page:** the newest **5 Major** and **5 Minor** projects, each list with an "Open all" link.
- **/major/** and **/minor/** list every project of that kind, newest first, **12 per page**, with page numbers and Newer / Older links (`/minor/page2/`, `/minor/page3/` …).
- **Each project** has its own page at `projects.isidd.dev/<title>/` with the date, reading time, author (Siddharth Singh), and **Try it out / How I built it / Code** buttons.
- **Updates** (`/updates/`, the button next to search): building now with progress bars, live projects, a month-by-month changelog, and what is next. Edit `_data/updates.yml`.
- **Search** in the top bar looks through every project's title, tags, type and date.
- Black on white, EB Garamond only, no italics (monospace is used inside code blocks).

## Add a project
Create `_posts/YYYY-MM-DD-project-name.md`:

```markdown
---
layout: project
title: "Travel Experience Agent"
kind: major                 # major or minor
tags: [AI, agents]
demo: "https://…"           # Try it out (optional)
build: "https://architecture.isidd.dev/travel-experience-agent/"   # How I built it (optional)
code: "https://github.com/isthiscoder/…"                            # Code (optional)
---

What it does and why you built it.
```

The file name decides the address: `2026-12-20-travel-experience-agent.md` → `projects.isidd.dev/travel-experience-agent/`.
Always close the top block with `---` on its own line.

## Settings
`_config.yml`: `home_per_kind: 5` (projects per section on the home page), `per_page: 12` (projects per list page).
List pages live in `lists/` (10 pages each for Major and Minor = 120 projects each). Need more? Copy `lists/minor-10.html` to `lists/minor-11.html` and change `page_num: 11` and `permalink: /minor/page11/`.

Fonts: EB Garamond (SIL OFL, self-hosted). MIT [LICENSE](LICENSE).
