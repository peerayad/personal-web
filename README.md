# Personal web — Peeraya Dumrongpun

Static personal site for job search: professional summary, technical skills, an experience-and-education timeline, contact details, and a downloadable CV (PDF).

**Course submission:** This repo satisfies the project requirements: it contains **web code** (`index.html`, `css/`, `js/`, `assets/`) and this **README** with **how to run** the site locally (start in [Quick start](#quick-start-copy-and-paste) below).

[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/9Yu-ry0Z)

---

## Prerequisites

- **Git** — to clone the repository  
- **Python 3** — to run a tiny local web server (already installed on most Mac/Linux systems; [python.org](https://www.python.org/) on Windows)

No Node.js, npm, or build tools are required.

---

## Quick start (copy and paste)

Run these commands **in order**. Replace `8080` with another port (e.g. `8081`) if you get “address already in use.”

```bash
git clone https://github.com/GIX-Luyao/personal-web-peerayad.git
cd personal-web-peerayad
python3 -m http.server 8080
```

Then in your browser open:

**http://127.0.0.1:8080/**

(use the **same port number** as in the last command)

**You should see:** the portfolio page (title *Peeraya Dumrongpun*, hero section, navigation).  
**If you see** a white page titled **“Directory listing for /”** with only a folder link, see [Troubleshooting](#troubleshooting) below.

Leave the terminal open while you browse. Press **Ctrl+C** in that terminal to stop the server.

---

## Step-by-step (what each part does)

### 1. Clone the repository

This downloads the project into a folder named `personal-web-peerayad` next to where you run the command.

```bash
git clone https://github.com/GIX-Luyao/personal-web-peerayad.git
```

### 2. Enter the project folder (**important**)

The site files—including **`index.html`**—live **inside** this folder. You must `cd` into it before starting the server.

```bash
cd personal-web-peerayad
```

**Check you are in the right place** (you should see `index.html` in the list):

```bash
ls index.html
```

- If you see `index.html` — good, continue.  
- If you see `No such file` — you are still outside the repo; `cd` again until `ls index.html` works (or open the cloned folder in your terminal app and `cd` there).

### 3. Start the local server

```bash
python3 -m http.server 8080
```

Pick any free port instead of `8080` if needed (e.g. `8081`, `5500`).

### 4. Open the site in a browser

Go to **http://127.0.0.1:8080/** — change the port in the URL if you used a different port in step 3.

A local server is recommended so styles, scripts, and the **Download CV** link work the same way as on a real host.

---

## Troubleshooting

| What you see | What it usually means | What to do |
|--------------|------------------------|------------|
| **“Directory listing for /”** and only a link like `personal-web-peerayad/` | The server was started **outside** the repo (e.g. in `Documents` or `Test`). There is no `index.html` at that location. | Stop the server (**Ctrl+C**). Run `cd personal-web-peerayad` until `ls index.html` works, then start `python3 -m http.server` again. **Or** go to **http://127.0.0.1:PORT/personal-web-peerayad/** (same `PORT` you used) to open the site without changing folders. |
| **`OSError: [Errno 48] Address already in use`** | Another program is using that port (often an old `http.server`). | Use a different port: `python3 -m http.server 8081` and open **http://127.0.0.1:8081/** . On macOS you can free a port: `lsof -i :8080` then `kill <PID>` . |
| **Blank page or broken styling** | Wrong URL or opened `index.html` from disk with wrong relative paths. | Use the server from step 3 and open **http://127.0.0.1:PORT/** . |

### Preview without Python (optional)

You can open **`index.html`** in a browser from Finder or **File → Open**. The layout usually works, but the CV **Download** button may not behave like on a real server; use the steps above when testing downloads.

---

## Stack

- **HTML** — `index.html`
- **CSS** — `css/styles.css` (light professional theme)
- **JavaScript** — `js/main.js` (footer year only)

## Project layout

| Path | Purpose |
|------|---------|
| `index.html` | Page structure and content |
| `css/styles.css` | Layout and styling |
| `js/main.js` | Footer copyright year |
| `assets/CV_Peeraya_Dumrongpun_2026.pdf` | Resume PDF |

## Deploy

Publish as **static files** (for example **GitHub Pages**): use the **repository root** as the site root so `index.html` loads at `/` and paths like `css/styles.css` and `assets/…` still work.

## License

Content is personal to the author; reuse of branding or biography text is not implied.
