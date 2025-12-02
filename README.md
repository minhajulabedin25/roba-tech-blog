# ROBA Technical Blog – Reproducible Static Site

This repository contains a small MkDocs-based project that explains ROBA's mission, Creator Hub, challenge funnel, and marketplace from a developer‑centric perspective.

The site is authored in Markdown and rendered to a static HTML file (`index.html`) using a static‑site workflow. The project is intentionally minimal so that reviewers can easily rebuild and verify the output.

---

## Project Structure

```text
.
├── index.html          # Executable static output (entry point for ROBA)
├── mkdocs.yml          # MkDocs configuration
├── docs/
│   └── index.md        # Markdown source for the article
└── assets/
    └── README.md       # Placeholder for future diagrams or images
```

---

## Build & Reproduction Steps

These steps assume Python and `pip` are available.

1. **Install MkDocs**

```bash
pip install mkdocs
```

2. **Serve the site locally**

From the repository root:

```bash
mkdocs serve
```

Then open:

```text
http://127.0.0.1:8000
```

3. **Build the static site**

```bash
mkdocs build
```

By default MkDocs writes its output to the `site/` directory.  
The `index.html` at the repository root is a copy of the main built page so that ROBA can treat it as the executable file.

---

## Notes for Reviewers

- The Markdown article in `docs/index.md` is the single source of truth.
- `mkdocs.yml` configures a minimal documentation site with a single navigation entry.
- The repository is intentionally lightweight, with no extra dependencies beyond MkDocs itself.