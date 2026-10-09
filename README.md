# GIS Skills Course — ArcGIS · QGIS · gIQ

Free GIS video courses for three platforms, with a full narration script for every lesson, on-screen recording cues, module quizzes and progress tracking: **162 lessons in 51 modules**, about 17 hours of video.

**Live site:** https://rgiq2024.github.io/arcgis-pro-course/ — switch platforms with the **ArcGIS · QGIS · gIQ** tabs at the top.

### ArcGIS (115 lessons)

| Track | Modules | Topics |
|---|---|---|
| **Basics** (39) | M1–M7 | Install and sign in, projects, the interface, navigating maps and scenes, shapefiles, adding data, the Contents pane, symbology |
| **Intermediate** (26) | M8–M15 | Geodatabases, domains and subtypes, editing, Select By Attributes/Location, charts, Calculate Field, joins, coordinate systems, georeferencing, labeling and annotation, layouts and map series, geoprocessing and overlay tools |
| **Advanced** (24) | M16–M23 | Spatial Analyst terrain and suitability, imagery and classification, hot spots and spatial statistics, geocoding and network analysis, 3D, lidar and animation, ModelBuilder, ArcPy and notebooks, Arcade, topology, publishing and a capstone project |
| **Online & Apps** (26) | M24–M33 | ArcGIS Online, Map Viewer, Scene Viewer, Living Atlas, StoryMaps, Dashboards, Experience Builder, Instant Apps, Field Maps (including Tasks), QuickCapture, Survey123, Hub, web analysis, Notebooks, Data Pipelines, Enterprise, Earth, Urban, Business Analyst, Velocity, Maps SDKs, field-to-dashboard capstone |

### QGIS (29 lessons, written for QGIS 4 LTR)

| Track | Modules | Topics |
|---|---|---|
| **Basics** (11) | Q1–Q4 | Installing (LTR vs latest), the interface, projects, adding data, XYZ basemaps, CSV and web services, CRSs, symbology, labels, print layouts and atlases |
| **Intermediate** (9) | Q5–Q8 | Attribute table, expressions and the Field Calculator, joins, digitizing and snapping, attribute forms, the Processing Toolbox, overlay tools, the Georeferencer, GeoPackage, PostGIS and DB Manager |
| **Advanced** (9) | Q9–Q11 | Terrain analysis, Raster Calculator and zonal statistics, SCP land-cover classification, Graphical Modeler, PyQGIS, essential plugins, 3D and elevation profiles, QField, qgis2web and QGIS Server |

### gIQ by Space42 (18 lessons)

| Modules | Topics |
|---|---|
| G1–G7 | Platform overview and data flow, logging in (including UAE Pass) and roles, the Explore globe and layer details, uploads and ingestion jobs, Data Manager and alerts, inference jobs, archive search and satellite tasking (optical, SAR, thermal), orders and continuous collection, workspaces and the Exploration tab, annotation projects, reports and stories, AI models, AMD and the AI Assistant, the Marketplace, Seller Central and Geostream, administration and credits |

gIQ lessons follow the official documentation at [docs.giq.ae](https://docs.giq.ae/). Module names, permissions and providers can change between gIQ releases, so check the docs and release notes before recording.

## Features

- **Learning path home** with overall and per-level progress
- **Progress tracking**: mark lessons complete (button or `C`); progress, quiz scores and notes are saved in the learner's browser
- **Platform tabs**: ArcGIS, QGIS and gIQ, each with its own home, tracks and progress
- **Module quizzes**: 153 questions with instant feedback and explanations
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

ArcGIS is a trademark of Esri. QGIS is a project of the QGIS.org association. gIQ is a product of Space42. This course is independent of all three.
