# Personal web — Peeraya Dumrongpun

Static personal site for job search: professional summary, technical skills, an experience-and-education timeline (years aligned with a vertical rail), contact details, and a downloadable CV (PDF).

[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/9Yu-ry0Z)

## Stack

- **HTML** — single-page layout (`index.html`)
- **CSS** — light professional theme (`css/styles.css`)
- **JavaScript** — footer year only (`js/main.js`)

No build step or package manager required.

## Run locally

From this directory:

```bash
python3 -m http.server 8080
```

Open [http://127.0.0.1:8080/](http://127.0.0.1:8080/). Using a local server ensures the CV download link behaves consistently.

You can also open `index.html` directly in a browser for a quick preview (some browsers restrict `download` behavior on `file://` URLs).

## Project layout

| Path | Purpose |
|------|---------|
| `index.html` | Page structure and content |
| `css/styles.css` | Layout, light theme, timeline styling |
| `js/main.js` | Sets footer copyright year |
| `assets/CV_Peeraya_Dumrongpun_2026.pdf` | Resume PDF linked from hero and contact |

## Deploy

Host as static files (for example **GitHub Pages**): publish the repository root so `index.html` is the site entry point and paths like `css/styles.css` and `assets/…` resolve correctly.

## License

Content is personal to the author; reuse of branding or biography text is not implied.
