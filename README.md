# Introduction to ArcGIS Pro — Video Course

A free ArcGIS video course from first install to Python automation, web apps and field data collection: **115 lessons in 33 modules across four tracks**, about 12 hours of video. Every lesson has a full narration script with on-screen recording cues, and every module ends with a quiz.

**Live site:** https://rgiq2024.github.io/arcgis-pro-course/

| Level | Modules | Topics |
|---|---|---|
| **Basics** (39 lessons) | M1–M7 | Install and sign in, projects, the interface, navigating maps and scenes, shapefiles, adding data, the Contents pane, symbology |
| **Intermediate** (26 lessons) | M8–M15 | Geodatabases, domains and subtypes, editing, Select By Attributes/Location, charts, Calculate Field, joins, coordinate systems, georeferencing, labeling and annotation, layouts and map series, geoprocessing and overlay tools |
| **Advanced** (24 lessons) | M16–M23 | Spatial Analyst terrain and suitability, imagery and classification, hot spots and spatial statistics, geocoding and network analysis, 3D, lidar and animation, ModelBuilder, ArcPy and notebooks, Arcade, topology, publishing and a capstone project |
| **ArcGIS Online & Apps** (26 lessons) | M24–M33 | ArcGIS Online organizations and content, Map Viewer, Scene Viewer, Living Atlas, StoryMaps, Dashboards, Experience Builder, Instant Apps, Field Maps (including Tasks), QuickCapture, Survey123, Hub, web analysis, Notebooks, Data Pipelines, ArcGIS Enterprise, Earth, Urban, Business Analyst, Velocity, Maps SDKs, and a field-to-dashboard capstone |

## Features

- **Learning path home** with overall and per-level progress
- **Progress tracking**: mark lessons complete (button or `C`); progress, quiz scores and notes are saved in the learner's browser
- **Module quizzes**: 99 questions with instant feedback and explanations
- **Search** across every lesson and script (`Ctrl K` or `/`)
- **Teleprompter** for recording: auto-scroll, speed and size controls, mirror mode, cue toggle (`T`, `Space` to play/pause)
- **YouTube / LinkedIn script versions**: switches each lesson's intro and outro
- **Upload details**: ready YouTube title, description, tags and LinkedIn description per lesson
- **Personal notes** on every lesson
- **Light, dark and system themes**; works on phones
- **Keyboard shortcuts**: `←` `→` lessons, `C` complete, `T` teleprompter, `H` home, `?` help

## Files

| File | What it does |
|---|---|
| `index.html` | The website. No build step, no frameworks. |
| `course.js` | All lesson scripts and quiz questions. Edit text here. |
| `videos.js` | Each lesson's video: YouTube link, LinkedIn link or local file. |
| `videos/` | Optional folder for video files you host directly. |
| `scripts.md` | Every script and quiz in one readable document. |

## Add your videos

Open `videos.js` (on GitHub, click the pencil icon) and fill in a lesson:

```js
"1.1": { youtube: "https://youtu.be/XXXXXXXXXXX", file: "", linkedin: "", status: "published" },
```

- **YouTube (recommended):** any watch, youtu.be, shorts or live link. The site embeds the player.
- **Your own file:** put it in `videos/` and set `file: "videos/1-1.mp4"`. GitHub rejects files over 100 MB, so use YouTube for full-length lessons.
- **LinkedIn Learning:** paste the lesson link to show a "Watch on LinkedIn Learning" button.
- **status:** `todo`, `recording`, `editing` or `published`.

Commit the change; GitHub Pages updates in a minute or two. Lessons with a video get a dot in the lesson list.

## Edit lessons or quizzes

Each module in `course.js` looks like this:

```js
{ "id": "M8", "title": "Geodatabases and Data Management", "level": "intermediate",
  "quiz": [ { "q": "Question?", "a": "Right answer", "w": ["Wrong 1","Wrong 2","Wrong 3"], "x": "Why it's right" } ],
  "lessons": [ { "id": "8.1", "title": "…", "dur": "6 min", "obj": "…", "tip": "…",
                 "body": ["[ON SCREEN: what to show]", "Narration paragraph…"] } ] }
```

To add a lesson, add an entry to `lessons` and a matching line in `videos.js`.

## Publish on GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)` → Save.

## Preview locally

Double-click `index.html`. Everything works offline except Google Fonts and YouTube embeds.

---

ArcGIS and ArcGIS Pro are trademarks of Esri. This course is independent and not affiliated with Esri.
