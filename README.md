# Introduction to ArcGIS Pro — Video Course Site

A free, step-by-step video course for ArcGIS Pro beginners: 39 lessons in 7 modules, each with a full narration script, on-screen recording cues, YouTube upload details and a video player.

**Modules:** Getting Started · The Interface · Navigating Maps and Scenes · Shapefiles · Adding Data · The Contents Pane · Symbology

## What's in this repo

| File | What it does |
|---|---|
| `index.html` | The website. No build step, no frameworks. |
| `course.js` | All 39 lesson scripts (titles, objectives, narration, tips). Edit text here. |
| `videos.js` | Where you add each lesson's video (YouTube link, LinkedIn link or a local file). |
| `videos/` | Optional folder for video files you host directly. |
| `scripts.md` | All scripts in one readable document. |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are. |

## Publish on GitHub Pages

1. Create a new repository on GitHub, for example `arcgis-pro-course`.
2. Upload these files (drag them into the repo page, or use the commands below).
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, and click **Save**.
5. After a minute your site is live at `https://<your-username>.github.io/arcgis-pro-course/`.

```bash
cd arcgis-pro-course
git init
git add .
git commit -m "Introduction to ArcGIS Pro course site"
git branch -M main
git remote add origin https://github.com/<your-username>/arcgis-pro-course.git
git push -u origin main
```

## Add your videos

Open `videos.js` and fill in the lesson you've recorded:

```js
"1.1": { youtube: "https://youtu.be/XXXXXXXXXXX", file: "", linkedin: "", status: "published" },
```

- **YouTube (recommended):** paste any YouTube link — watch, youtu.be, shorts or live. The site embeds the player.
- **Your own file:** put the video in `videos/` (for example `videos/1-1.mp4`) and set `file: "videos/1-1.mp4"`. GitHub rejects files over 100 MB and warns above 50 MB, so export at 1080p H.264 and keep lessons short, or use [Git LFS](https://git-lfs.com) for larger files.
- **LinkedIn Learning:** paste the lesson link; the site shows a "Watch on LinkedIn Learning" button.
- **status:** `todo`, `recording`, `editing` or `published` — shown on the lesson page.

Commit and push; the site updates within a minute or two.

The progress bar and the green dots in the lesson list fill in automatically as you add videos.

## Using the scripts

- The **YouTube / LinkedIn** switch changes each lesson's intro and outro. YouTube gets a hook and a subscribe call-to-action; LinkedIn Learning gets a neutral intro and an "Up next" close.
- **Copy script** copies the full lesson script for your teleprompter.
- **Upload details** gives a ready YouTube title, description, tags and a LinkedIn description.
- **Download all scripts** saves every script as one Markdown file.
- Link to a lesson directly with `#lesson-4-1` at the end of the URL.

## Preview locally

Double-click `index.html`. Everything works offline except the Google Fonts and YouTube embeds.

---

ArcGIS and ArcGIS Pro are trademarks of Esri. This course is independent and not affiliated with Esri.
