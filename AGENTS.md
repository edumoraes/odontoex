# Repository Guidelines

## Project Structure & Module Organization

This is a Hugo landing-page site. Core configuration lives in `hugo.toml`. Page content and front matter are in `content/_index.md`; keep campaign-specific copy drafts in the existing root-level Markdown files. Templates are under `layouts/`, with shared HTML in `layouts/partials/`. Styles and scripts live in `assets/css/main.css` and `assets/js/main.js`; Hugo processes these through the asset pipeline. Public files that should be served as-is belong in `static/`, especially `static/images/`.

## Build, Test, and Development Commands

- `hugo server -D`: run the local development server with draft content enabled.
- `hugo`: build the static site into `public/`.
- `hugo --cleanDestinationDir`: rebuild and remove stale files from the destination.

Run commands from the repository root. Do not commit generated `public/` output unless deployment specifically requires it.

## Coding Style & Naming Conventions

Use two-space indentation in HTML templates and TOML, matching the current files. Keep CSS organized by component or section, using descriptive class names such as `.hero-section`, `.condition-grid`, and `.treatment-card`. Prefer lowercase, hyphenated file names for assets and images, for example `hero-paciente-clinica.png`. Existing copy intentionally avoids accents in many places; preserve that style unless the project owner asks for localized typography changes.

## Testing Guidelines

There is no automated test suite in this repository. Validate changes by running `hugo` and checking the generated site for template errors. For visual or copy changes, run `hugo server -D` and review the page at the local URL, including desktop and mobile widths. Confirm images referenced from templates exist under `static/images/`.

## Commit & Pull Request Guidelines

The current branch has no commits, so no repository-specific commit convention exists yet. Use short, imperative commit subjects such as `Add landing page images` or `Update WhatsApp CTA copy`. Pull requests should include a concise summary, screenshots for visual changes, any linked issue or task, and the validation performed (`hugo`, browser review, or both). Note any required content fields left blank in `content/_index.md`, such as `whatsapp_url` or clinic registration details.

## Security & Configuration Tips

Do not commit private contact numbers, credentials, or unapproved clinic registration data. Treat claims about pricing, financing, and clinical outcomes as content that must be validated before publication.
