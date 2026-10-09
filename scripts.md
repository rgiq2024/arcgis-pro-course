# GIS Skills Course — Lesson Scripts
Three platforms: ArcGIS (Basics, Intermediate, Advanced, Online & Apps), QGIS (Basics, Intermediate, Advanced) and gIQ by Space42. Each lesson: objective, narration with [ON SCREEN] recording cues, and a tip. Intro/outro templates are at the end.

# ArcGIS · Basics

## M1 — Getting Started with ArcGIS Pro

### Lesson 1.1: How to Install ArcGIS Pro  (6 min)

**Objective:** Download, install and license ArcGIS Pro on a Windows computer.

*[ON SCREEN: Esri system requirements page]*

Before we install anything, let's make sure your computer is ready. ArcGIS Pro runs on 64-bit Windows 10 or 11. Check the official system requirements page for the release you're installing — it lists the minimum RAM, the graphics card requirements, and the version of the Microsoft .NET Desktop Runtime you need.

*[ON SCREEN: My Esri > Downloads]*

Next, sign in to My Esri, or to your organization's ArcGIS Online account, and open the Downloads area. Find ArcGIS Pro, choose your language, and download the installer. If your organization manages software for you, your administrator may give you the installer directly.

*[ON SCREEN: installer running]*

Run the setup file. If the .NET Desktop Runtime is missing, the installer will tell you and give you a link — install it, then run setup again. Accept the license agreement, and choose whether to install for all users or just for you. Installing for just you doesn't need administrator rights, which is handy on a work laptop. Keep the default install folder unless you have a reason to change it.

*[ON SCREEN: progress bar, then Finish]*

The install takes a few minutes. When it finishes, you'll find ArcGIS Pro in the Start menu.

> **Tip:** Download the optional offline Help and language packs from the same page if you often work without internet.

### Lesson 1.2: Opening ArcGIS Pro and Signing In  (4 min)

**Objective:** Launch ArcGIS Pro and sign in with a named user license.

*[ON SCREEN: Start menu > ArcGIS Pro]*

Open the Start menu and click ArcGIS Pro. You can also pin it to your taskbar so it's one click away next time.

*[ON SCREEN: sign-in dialog]*

The first time ArcGIS Pro starts, it asks you to sign in. Most people use a named user license, which is tied to your ArcGIS Online or ArcGIS Enterprise account. Type your username and password, or use your organization's single sign-on button.

Tick "Sign me in automatically" if this is your own computer — it saves you a step every time.

*[ON SCREEN: Settings > Licensing]*

If you use a different license type, like a single use or concurrent license, you can change it later from Settings, then Licensing. That page also shows which extensions are licensed for you, such as Spatial Analyst or 3D Analyst.

> **Tip:** If you see a sign-in error, check you're signing in to the right portal URL — ArcGIS Online versus your company's Enterprise portal.

### Lesson 1.3: The Start Page and How It Differs from ArcMap  (5 min)

**Objective:** Read the ArcGIS Pro start page and understand the project-based workflow.

*[ON SCREEN: ArcGIS Pro start page]*

After signing in, you land on the start page. On the left are your recent projects. In the middle are the templates for creating a new project: Map, Catalog, Global Scene, Local Scene, and Start without a template. You can also open a project from your computer or your portal, and reach Settings at the bottom left.

*[ON SCREEN: split screen, ArcMap vs ArcGIS Pro]*

If you're coming from ArcMap, this is the biggest change. ArcMap opened straight into a single map document, an MXD, with one map and one layout. ArcGIS Pro opens into a project. A project can hold many maps, many layouts, scenes, toolboxes, databases and folder connections — all together in one place.

ArcMap also needed separate apps — ArcCatalog for data, ArcScene and ArcGlobe for 3D. In ArcGIS Pro, all of that lives in one 64-bit application.

> **Tip:** Projects created in a 3.x release won't open in the older 2.x releases, so keep that in mind when sharing with colleagues.

### Lesson 1.4: Creating a Project: File Extension and Folder Structure  (6 min)

**Objective:** Create a new project and understand the files ArcGIS Pro makes on disk.

*[ON SCREEN: start page > Map template]*

Let's create our first project. On the start page, click the Map template. Give the project a name — I'll call it Intro_Pro — and choose a location. By default, projects go in Documents\ArcGIS\Projects.

Notice the checkbox "Create a new folder for this project". Leave it ticked; it keeps everything tidy. Click OK.

*[ON SCREEN: File Explorer showing project folder]*

Now let's look at what ArcGIS Pro created on disk. Inside the project folder you'll find:

The .aprx file — this is the project file itself. It stores your maps, layouts, and settings, but not the data.

A file geodatabase ending in .gdb, with the same name as the project. This is the default place your outputs are saved.

A toolbox ending in .atbx — the default place for your own custom tools.

An Index folder, which ArcGIS Pro uses to make searching your project fast.

You may also see folders like ImportLog or GpMessages once you start working.

Remember: the .aprx points to your data; it doesn't contain it. If you send someone only the .aprx, they'll see broken links. To share everything, use a project package instead.

### Lesson 1.5: Project Types: Map, Global Scene, Local Scene, Catalog, No Template  (7 min)

**Objective:** Choose the right project template for the job.

*[ON SCREEN: start page templates]*

ArcGIS Pro gives you five ways to start. They all create the same kind of project — the template just decides what opens first.

*[ON SCREEN: Map template result]*

Map. Opens a 2D map with a basemap. This is the everyday choice for mapping, editing and analysis.

*[ON SCREEN: Global Scene result]*

Global Scene. Opens a 3D globe. Use it when your data covers a large area — a country, a continent, flight paths — where the curve of the Earth matters.

*[ON SCREEN: Local Scene result]*

Local Scene. Opens a flat 3D view in a projected coordinate system. Use it for smaller areas like a city, a campus or a building site, and when you want to look underground — for example at pipes or boreholes.

*[ON SCREEN: Catalog template result]*

Catalog. Opens the Catalog view instead of a map. Choose this when your job is managing data — browsing folders, creating shapefiles and geodatabases, editing metadata.

*[ON SCREEN: Start without a template]*

Start without a template. Opens ArcGIS Pro instantly with an untitled project and nothing saved to disk. It's perfect for a quick look at some data. If you decide to keep the work, use Save As to give it a name and location.

> **Tip:** You can always add a map, scene or layout to any project later from the Insert tab — the template is just a starting point.

### Lesson 1.6: Saving and Closing a Project  (3 min)

**Objective:** Save your work safely and close a project.

*[ON SCREEN: Quick Access Toolbar save icon]*

Save your project with the save icon at the top left, the Project tab, or Ctrl+S. ArcGIS Pro shows an asterisk in the title bar when there are unsaved changes.

*[ON SCREEN: Project tab > Save As]*

Use Save As when you want a copy of the project under a new name.

*[ON SCREEN: closing the app with unsaved changes prompt]*

To close a project, either open or create a different project from the Project tab, or close ArcGIS Pro with the X at the top right. If there are unsaved changes, ArcGIS Pro asks whether to save.

Note that unsaved edits to data are handled separately from the project. If you've been editing features, save or discard the edits from the Edit tab first.

> **Tip:** ArcGIS Pro can auto-save project backups — turn this on under Settings, Options, General.

#### Module quiz

1. Which file is the ArcGIS Pro project file?  
   **Answer:** .aprx — The .aprx stores maps, layouts and settings; ArcMap used .mxd.

2. Which template opens a flat 3D view for a city-sized area?  
   **Answer:** Local Scene — Local scenes use a projected coordinate system for smaller areas.

3. Does the .aprx contain your data?  
   **Answer:** No, it points to the data — Share a project package to include the data.

## M2 — The ArcGIS Pro Interface

### Lesson 2.1: A Tour of the ArcGIS Pro Interface  (6 min)

**Objective:** Name the main sections of the ArcGIS Pro window.

*[ON SCREEN: full interface with highlights]*

Here's the ArcGIS Pro window with a map open. Let's name each part so you can follow along in every lesson.

At the very top is the Quick Access Toolbar — save, undo, redo.

Below it is the ribbon, with tabs like Map, Insert, Analysis, View, Edit, Imagery and Share.

On the left is the Contents pane, listing the layers in the active map.

In the middle is the view — here a map view. Views can be maps, scenes, layouts, tables or the catalog, and each opens as a tab, so you can have many at once.

On the right is the Catalog pane, showing the items in your project.

At the bottom of the view is the status bar, with scale, coordinates and drawing controls.

*[ON SCREEN: dragging a pane to dock]*

Every pane can be moved, docked, floated or closed. Drag a pane's title bar and drop it on one of the docking targets. If you get lost, View tab, Reset Panes puts everything back.

### Lesson 2.2: The Ribbon, Tabs and the Project Tab  (6 min)

**Objective:** Find tools on the ribbon and use the Project tab.

*[ON SCREEN: ribbon tabs]*

The ribbon organizes tools into tabs, and each tab into groups. The Map tab holds navigation, layers, selection and labeling. Insert adds new maps, layouts and toolboxes. Analysis opens geoprocessing tools. View controls panes and windows. Edit holds editing tools. Share is for publishing and exporting.

*[ON SCREEN: clicking a layer reveals Feature Layer tab]*

Some tabs are contextual — they only appear when relevant. Click a feature layer in Contents and the Feature Layer tab appears, with Appearance, Labeling and Data.

*[ON SCREEN: Project tab backstage]*

The Project tab is different. It opens a full-screen page where you create, open and save projects, manage portal connections and licensing, change Options, and manage Python environments and add-ins. Press Escape or the back arrow to return.

*[ON SCREEN: ArcMap menu bar vs Pro ribbon]*

In ArcMap, tools were in drop-down menus and floating toolbars you had to switch on. In ArcGIS Pro, the ribbon shows the tools for what you're doing right now. If you can't find something, use the Command Search box at the top — type the tool name and run it directly.

### Lesson 2.3: The Contents Pane and the Attribute Table  (5 min)

**Objective:** Use Contents to manage layers and open an attribute table.

*[ON SCREEN: Contents pane]*

The Contents pane lists everything in the active map: the map itself, your layers, and the basemap. Checkboxes switch layers on and off. The order of layers is the drawing order — layers at the top draw on top.

If Contents is closed, reopen it from View tab, Contents.

*[ON SCREEN: right-click > Attribute Table]*

Every feature layer has an attribute table — the information behind each feature. Right-click a layer and choose Attribute Table, or press Ctrl+T with the layer selected.

The table opens as its own view below the map. Each row is a feature, each column is a field. Click a row header to select that feature on the map; double-click it to zoom to it.

We'll explore Contents in much more depth in Module 6.

### Lesson 2.4: The View Tab  (4 min)

**Objective:** Open, close and reset panes from the View tab.

*[ON SCREEN: View tab]*

The View tab is your control centre for windows. Its Windows group opens the Catalog pane, Catalog view, Contents, Geoprocessing, Python window and Tasks. Reset Panes restores a standard layout for mapping, geoprocessing or editing.

*[ON SCREEN: Link Views]*

Link Views keeps two maps in step — great for comparing before-and-after images side by side.

*[ON SCREEN: Convert to scene]*

You'll also find Convert, which turns a 2D map into a global or local scene, and the Accessibility options for appearance and keyboard use.

> **Tip:** Most panes have a keyboard shortcut. Hover over a button to see it.

### Lesson 2.5: The Catalog Pane and Catalog View  (5 min)

**Objective:** Browse project items and data with Catalog.

*[ON SCREEN: Catalog pane]*

The Catalog pane shows everything that belongs to the project. The Project tab inside it lists Maps, Toolboxes, Databases, Styles, Folders and Locators. The Portal tab lists your online content, and Favorites keeps connections you use in every project.

*[ON SCREEN: expanding Databases and Folders]*

Expand Databases to see the project's default geodatabase. Expand Folders to browse folders you've connected — we'll add our own folder connection in Module 4.

*[ON SCREEN: Catalog view]*

For bigger data-management jobs, open the Catalog view from the View tab. It's like a file explorer for GIS data, with a details panel showing previews and metadata.

> **Tip:** Drag a dataset from Catalog straight onto the map to add it.

#### Module quiz

1. Where do you create, open and save projects and change Options?  
   **Answer:** The Project tab — The Project tab opens the backstage view.

2. A tab that appears only when you select a layer is called…  
   **Answer:** A contextual tab — Contextual tabs like Feature Layer show tools for the current selection.

3. How do you restore the default pane layout?  
   **Answer:** View tab > Reset Panes — Reset Panes puts panes back in a standard arrangement.

## M3 — Navigating Maps and Scenes

### Lesson 3.1: The Map View, Explore Tool and Identify  (5 min)

**Objective:** Pan, zoom and identify features with the Explore tool.

*[ON SCREEN: Map tab > Explore]*

The Explore tool is your all-in-one navigation tool. It's on the Map tab, in the Navigate group, and it's active by default.

Drag with the left mouse button to pan. Roll the mouse wheel to zoom in and out. Hold the right button and drag to zoom smoothly.

*[ON SCREEN: clicking a feature, pop-up appears]*

Click a feature and a pop-up appears showing its attributes. This is how you identify features in ArcGIS Pro — in ArcMap this was the separate Identify tool.

If several features overlap, the pop-up lists them all; click each one to see its details.

*[ON SCREEN: Explore drop-down]*

Use the drop-down under Explore to choose which layers it identifies: the topmost layer, visible layers, selectable layers, or selected layers in Contents.

### Lesson 3.2: Zoom Controls, Full Extent, Previous Extent and Scale  (5 min)

**Objective:** Control what part of the map you see.

*[ON SCREEN: Navigate group buttons]*

Next to Explore are more navigation buttons. Full Extent zooms to show all layers in the map. Fixed Zoom In and Fixed Zoom Out step in or out around the centre.

Previous Extent and Next Extent work like back and forward in a web browser — very useful after you've zoomed too far.

*[ON SCREEN: right-click layer > Zoom To Layer]*

To jump to one layer, right-click it in Contents and choose Zoom To Layer.

*[ON SCREEN: scale box at bottom]*

At the bottom left of the map is the scale. Type a value like 1:50,000 and press Enter, or pick one from the list. Small-scale numbers like 1:1,000,000 show a large area; large-scale numbers like 1:1,000 show detail.

> **Tip:** Create bookmarks from the Map tab to save views you return to often.

### Lesson 3.3: Status Bar: Snapping, Grid, Coordinates, Refresh and Pause  (6 min)

**Objective:** Use the controls along the bottom of the map view.

*[ON SCREEN: status bar with highlights]*

The status bar at the bottom of the map holds several small but important controls.

*[ON SCREEN: coordinate display moving]*

The coordinate display shows the location of your pointer. Use the drop-down beside it to change the units — decimal degrees, degrees minutes seconds, or projected units like metres.

*[ON SCREEN: Snapping toggle]*

Snapping helps your pointer jump to vertices, edges and endpoints of existing features while editing, so your new features connect precisely. Toggle it here or on the Edit tab, where you can pick which snapping types are active.

*[ON SCREEN: Grid toggle]*

Grid shows a reference grid you can snap to while editing — handy for drawing regular shapes.

*[ON SCREEN: Refresh and Pause]*

Refresh redraws the view and reloads the data — use it if something hasn't drawn correctly. Pause stops drawing, so you can rearrange layers or change symbology on a heavy map without waiting for every redraw. Click it again to resume.

### Lesson 3.4: Global Scenes and the Navigator Tool  (6 min)

**Objective:** Move around a 3D globe with the mouse and the Navigator.

*[ON SCREEN: Global scene]*

Here's a global scene. The Explore tool still works: left-drag to pan, scroll to zoom. To tilt and rotate, hold the middle mouse button — or the mouse wheel — and drag. Or hold the V key while dragging with the left button.

*[ON SCREEN: Navigator in corner]*

The Navigator is the on-screen control in the lower left. In its small form, it's a compass — click North to reset your heading.

*[ON SCREEN: expanded Navigator]*

Hover over it to expand it. The outer ring rotates the view. The arrows pan. The inner control tilts and orbits around the centre. Drag a control and hold to keep moving.

*[ON SCREEN: tilting to see terrain]*

Smart use: tilt to around 60 degrees to see mountains in profile, then orbit slowly — this makes great footage for presentations.

> **Tip:** If the Navigator is hidden, turn it on from the Map tab, Navigate group, under the Navigator drop-down.

### Lesson 3.5: Local Scenes  (4 min)

**Objective:** Navigate a local scene and understand when to use it.

*[ON SCREEN: Local scene of a city]*

A local scene displays 3D content on a flat plane in a projected coordinate system. Navigation is the same as a global scene: Explore to pan and zoom, middle-drag or V-drag to tilt and rotate, and the Navigator for precise control.

*[ON SCREEN: navigating below ground]*

The big advantage is that you can enable underground navigation and look beneath the surface — perfect for utilities, geology, or basements of buildings. Turn it on in the scene properties, then make the ground semi-transparent.

*[ON SCREEN: View > Convert]*

You can convert any 2D map to a local or global scene from the View tab. ArcGIS Pro asks which type; pick local for city-sized areas.

#### Module quiz

1. Which tool replaces ArcMap's Identify tool?  
   **Answer:** Explore (click a feature for a pop-up) — Clicking with Explore opens a pop-up with attributes.

2. How do you tilt a 3D scene with the mouse?  
   **Answer:** Hold the middle button or V and drag — Middle-drag or V+drag tilts and rotates.

3. What does the Pause button do?  
   **Answer:** Stops the map from redrawing — Pause stops drawing while you change layers or symbology.

## M4 — Shapefiles

### Lesson 4.1: What Is a Shapefile? The Files That Make It Up  (6 min)

**Objective:** Recognise each file in a shapefile and know which ones are required.

*[ON SCREEN: File Explorer showing a shapefile's files]*

A shapefile is not one file — it's a set of files with the same name and different extensions, stored together in one folder. Let's go through them.

Three are mandatory:

.shp — the main file. It stores the geometry: the points, lines or polygons.

.shx — the shape index. It records where each feature's geometry starts in the .shp, so software can jump straight to any feature.

.dbf — the attribute table, in dBASE format. One row per feature, in the same order as the geometry.

The rest are optional but important:

.prj — the coordinate system. Without it, ArcGIS Pro reports an unknown coordinate system and the layer may not line up. Fix it with the Define Projection tool, which writes a new .prj.

.cpg — the code page. It tells software which character encoding the attributes use, so non-English text displays correctly.

.shp.xml — the metadata.

.sbn and .sbx — a spatial index that can speed up drawing and spatial queries on large shapefiles.

*[ON SCREEN: warning graphic]*

The golden rule: never rename, move or copy just one of these files. Always manage shapefiles inside ArcGIS Pro's Catalog, which keeps the whole set together. If you email a shapefile, zip all the files.

> **Tip:** Shapefiles have limits — field names are 10 characters max, and each file under 2 GB. For new work, a file geodatabase is usually a better choice.

### Lesson 4.2: Create a Shapefile in a Catalog Project  (6 min)

**Objective:** Make a folder connection and create a new shapefile with a coordinate system.

*[ON SCREEN: start page > Catalog template]*

Start a project with the Catalog template. In the Catalog pane, right-click Folders and choose Add Folder Connection. Browse to the folder where you keep your data and click OK. A folder connection is a shortcut — ArcGIS Pro won't copy or move anything.

*[ON SCREEN: right-click folder > New > Shapefile]*

Right-click the folder and choose New, then Shapefile. The Create Feature Class tool opens with the location already filled in.

Type a name — let's call it Schools. Set the Geometry Type: Point, Polyline, Polygon, Multipoint or Multipatch. We'll choose Point.

*[ON SCREEN: Coordinate System picker]*

Now the coordinate system. Click the globe icon. Choose a geographic system like WGS 1984, or a projected system for your area, such as a UTM zone. Searching by name or EPSG code is quickest. Click OK.

Click Run. The new, empty shapefile appears in the folder, ready for editing.

### Lesson 4.3: Second Way: the Create Feature Class Tool  (4 min)

**Objective:** Create a shapefile from the Geoprocessing pane.

*[ON SCREEN: Analysis tab > Tools]*

You can also start from the tool itself. On the Analysis tab click Tools, search for Create Feature Class, and open it.

*[ON SCREEN: tool parameters]*

For Feature Class Location, browse to a folder — not a geodatabase. That's what makes the output a shapefile rather than a geodatabase feature class.

Fill in the name, geometry type and coordinate system as before. Use the Template Dataset option if you want to copy the fields of an existing layer.

Click Run. Because you're in a map project, the new layer is added to the map automatically.

### Lesson 4.4: Third Way: the Quick Method  (4 min)

**Objective:** Create a shapefile in seconds from the Catalog pane of a map project.

*[ON SCREEN: map project, Catalog pane]*

The quickest route is from a map project. In the Catalog pane, expand Folders, right-click your folder, choose New, then Shapefile. Give it a name, a geometry type and a coordinate system, and click Run.

*[ON SCREEN: layer appears in Contents]*

The shapefile is created and added straight to your map, so you can start drawing features immediately from the Edit tab, Create.

The strengths of this method: it's fast, it uses the folders you already have connected, and it drops you right into editing. Use it when you need a working layer for a quick task — digitizing a few sites, sketching a study area, or practising editing.

#### Module quiz

1. Which three shapefile files are mandatory?  
   **Answer:** .shp, .shx, .dbf — Geometry, index and attributes are required.

2. What happens if the .prj file is missing?  
   **Answer:** The coordinate system is unknown — Use Define Projection to write a new .prj.

3. To create a shapefile instead of a geodatabase feature class, the output location must be…  
   **Answer:** A folder — Create Feature Class writes a shapefile when the location is a folder.

## M5 — Adding Data

### Lesson 5.1: Adding Data and Shapefiles, and Fixing Invisible Layers  (6 min)

**Objective:** Add vector data to a map and troubleshoot layers that don't appear.

*[ON SCREEN: Map tab > Add Data]*

On the Map tab, in the Layer group, click Add Data. Browse to your shapefile, select it, and click OK. Or simply drag it from the Catalog pane onto the map.

*[ON SCREEN: layer in Contents but nothing visible]*

Sometimes a layer appears in Contents but nothing shows on the map. Work through this checklist:

Is the box ticked? Is the layer greyed out? Grey means it's outside its visible scale range — right-click, Properties, General, and check the range.

Is it hidden under another layer? Drag it to the top.

Right-click and Zoom To Layer — maybe it's just somewhere else.

If it lands in the ocean near zero degrees, the coordinate system is probably missing or wrong. Check the .prj and use Define Projection if needed.

Finally, check Symbology for full transparency, and Properties for a definition query hiding the features.

### Lesson 5.2: Adding Raster Data and Georeferenced Images  (5 min)

**Objective:** Add rasters and understand what makes an image georeferenced.

*[ON SCREEN: Add Data > GeoTIFF]*

Raster data — satellite images, scanned maps, elevation models — is added the same way: Add Data, or drag from Catalog. Common formats are GeoTIFF, JPEG 2000, IMG and rasters inside geodatabases.

ArcGIS Pro may ask to build pyramids and statistics. Say yes for large images; it makes them draw much faster.

*[ON SCREEN: image lines up with basemap]*

A georeferenced image knows where it belongs on Earth. That information is either built in, as in a GeoTIFF, or stored in a small side file called a world file, like .tfw or .jgw, plus an .aux.xml.

*[ON SCREEN: un-georeferenced scan]*

If your image lands in the wrong place or not at all, it isn't georeferenced. Use the Imagery tab, Georeference, to add control points and fix it.

### Lesson 5.3: Adding Layers to Global and Local Scenes  (5 min)

**Objective:** Add data to 3D scenes and control how layers sit on the surface.

*[ON SCREEN: scene Contents with categories]*

In a scene, Contents is split into categories: 3D Layers, 2D Layers, and Elevation Surfaces. Add Data works just as in a map; ArcGIS Pro sorts each layer into the right category.

*[ON SCREEN: dragging a layer from 2D to 3D]*

2D layers are draped flat over the ground. Drag a layer into 3D Layers to give it height.

*[ON SCREEN: Layer Properties > Elevation]*

Then open the layer's Properties, Elevation. Choose On the ground, Relative to the ground — with an offset in metres — or At an absolute height. For buildings, use the Appearance tab to extrude them using a height field.

> **Tip:** Use Elevation Surfaces to add your own DEM for more accurate terrain.

### Lesson 5.4: Adding KML and KMZ Files  (5 min)

**Objective:** View Google Earth data in ArcGIS Pro and convert it for analysis.

*[ON SCREEN: Add Data > .kmz]*

KML and KMZ are the formats used by Google Earth. ArcGIS Pro can add them directly: Add Data and choose the file. You'll see the placemarks, lines and polygons, with their styling.

*[ON SCREEN: KML layer properties]*

A KML layer added this way is read-only. You can view it, identify features with pop-ups, and change some display properties, but you can't edit its features or run most analysis tools on it.

*[ON SCREEN: KML To Layer tool]*

To work with the data fully, convert it with the KML To Layer tool. It creates a file geodatabase with feature classes for points, lines and polygons, plus a layer file that keeps the original look.

To go the other way, Layer To KML exports your ArcGIS layers for Google Earth.

#### Module quiz

1. A layer name is greyed out in Contents. The likely cause is…  
   **Answer:** It's outside its visible scale range — Grey layers are out of their scale range.

2. Which tool converts KML into geodatabase features?  
   **Answer:** KML To Layer — KML To Layer creates feature classes you can edit and analyse.

3. What makes an image georeferenced?  
   **Answer:** Built-in or world-file location information — GeoTIFF tags or a world file place the image on Earth.

## M6 — Mastering the Contents Pane

### Lesson 6.1: Elements of Contents and Comparison with ArcMap  (4 min)

**Objective:** Understand the parts of the Contents pane.

*[ON SCREEN: Contents toolbar]*

At the top of Contents is a search box and a row of buttons. These buttons switch the list mode — how your layers are listed. Below them is the map name, then layers and group layers, then the basemap.

*[ON SCREEN: ArcMap Table of Contents vs Pro Contents]*

In ArcMap the Table of Contents had a few tabs. ArcGIS Pro's Contents does more: it adds views for selection, editing, snapping and labeling, and it changes to match the active view — a map, a scene, a layout or a table each show their own contents.

### Lesson 6.2: List by Drawing Order, Data Source and Selection  (5 min)

**Objective:** Switch Contents views to answer different questions.

*[ON SCREEN: List By Drawing Order]*

List By Drawing Order is the default. The order here is the order things draw. Drag layers to restack them.

*[ON SCREEN: List By Data Source]*

List By Data Source groups layers by where the data lives — which folder or geodatabase. It's the quickest way to spot broken data links, shown with a red exclamation mark.

*[ON SCREEN: List By Selection]*

List By Selection shows how many features are selected in each layer and lets you set which layers are selectable. Untick a layer here, and the selection tools ignore it.

### Lesson 6.3: List by Editing, Snapping and Labeling, and Searching Layers  (5 min)

**Objective:** Control editing, snapping and labels per layer.

*[ON SCREEN: List By Editing]*

List By Editing shows which layers are editable. Untick a layer to protect it while you edit others.

*[ON SCREEN: List By Snapping]*

List By Snapping lets you choose which layers your pointer snaps to — useful when a busy map makes snapping jump to the wrong thing.

*[ON SCREEN: List By Labeling]*

List By Labeling shows which layers have labels switched on and their label classes. Here's the key difference from Drawing Order: Drawing Order controls how layers stack, while Labeling controls which labels show and their priority — the order of layers in Labeling does not change drawing at all.

*[ON SCREEN: typing in search box]*

On a map with dozens of layers, type part of a name into the Search box at the top of Contents to filter the list instantly.

### Lesson 6.4: The Layer Menu: Copy, Remove, Attribute Table, Zoom To  (5 min)

**Objective:** Use the most common layer right-click commands.

*[ON SCREEN: right-click layer menu]*

Right-click any layer to open its menu. Let's use the most common commands.

Copy — then right-click the map or another map and choose Paste. The copy keeps its symbology, so it's a fast way to show the same data two ways.

Remove — takes the layer off the map. The data on disk is not deleted.

Attribute Table — opens the table.

Zoom To Layer — zooms to the layer's full extent.

*[ON SCREEN: Make Default / Data / Sharing submenus]*

Further down you'll find submenus for Data, Sharing, Symbology, Labeling and Properties, which we'll cover next.

### Lesson 6.5: Selection, Labels and Pop-ups from the Layer Menu  (6 min)

**Objective:** Manage selection, labels and pop-ups for a layer.

*[ON SCREEN: Map tab > Select]*

To select features, use the Select tool on the Map tab. To identify them, use Explore. Remember to check which layers are selectable — right-click a layer, Selection, Make This The Only Selectable Layer.

*[ON SCREEN: Selection submenu]*

The Selection submenu also has Zoom To Selection, Clear Selection, and Switch Selection, which flips the selection — selected becomes unselected and the other way round. Great for "select everything except these".

*[ON SCREEN: right-click > Label]*

Click Label in the menu to switch labels on. ArcGIS Pro uses the layer's display field; change it on the Labeling tab.

*[ON SCREEN: Enable/Disable Pop-ups]*

The layer menu also has an option to enable or disable pop-ups. Disable them on reference layers so clicking only shows the data you care about.

### Lesson 6.6: Export Features, Metadata and Layer Properties  (6 min)

**Objective:** Save a layer to new data, view metadata and explore Layer Properties.

*[ON SCREEN: Data > Export Features]*

Right-click, Data, Export Features. If features are selected, only those are exported — a quick way to make a new dataset from a subset. Choose an output in a geodatabase or a folder and click OK.

*[ON SCREEN: View Metadata]*

View Metadata shows who made the data, when, and how. Edit Metadata lets you add a summary, tags and credits — always worth doing before you share.

*[ON SCREEN: Layer Properties dialog]*

Finally, Properties. The pages include General, Metadata, Source, Elevation, Selection, Display, Definition Query, Time, Range, Joins and Relates.

Compared with ArcMap, symbology and labeling have moved out of the properties dialog into their own panes, which stay open while you work, so you see changes immediately.

#### Module quiz

1. Which Contents view shows broken data links?  
   **Answer:** List By Data Source — Data Source groups layers by location and flags broken links.

2. What does Switch Selection do?  
   **Answer:** Selects the unselected features and unselects the selected — It flips the selection.

3. Removing a layer from Contents…  
   **Answer:** Takes it off the map but doesn't delete the data — The data on disk stays intact.

## M7 — Symbology

### Lesson 7.1: Opening the Symbology Pane and the Types of Symbology  (6 min)

**Objective:** Open the Symbology pane and know which methods exist.

*[ON SCREEN: right-click > Symbology]*

Right-click a layer and choose Symbology, or select the layer and click Symbology on the Feature Layer tab, Appearance group. The Symbology pane opens on the right.

*[ON SCREEN: Primary symbology drop-down]*

At the top is Primary symbology. The main choices are Single Symbol, Unique Values, Graduated Colors, Graduated Symbols, Proportional Symbols, Unclassed Colors, Bivariate Colors, Dot Density, Charts, and for points, Heat Map.

The options depend on geometry. Points, lines and polygons all get the core methods, but Dot Density is only for polygons and Heat Map is only for points.

*[ON SCREEN: pane tabs]*

Under the method you'll see tabs: Primary symbology, Vary symbology by attribute, and Advanced symbology options. We'll use all three in the coming lessons.

### Lesson 7.2: Single Symbol and Vary Symbology by Attribute  (7 min)

**Objective:** Style every feature the same way, then vary it by an attribute.

*[ON SCREEN: Single Symbol]*

Single Symbol draws every feature with the same symbol. Click the symbol swatch to open the Format Symbol pane. In Gallery pick a preset; in Properties set the fill colour, outline colour and outline width.

For polygons, a thin dark outline of about 0.5 points with a light fill usually looks clean. Set the fill to no colour if you only want the boundary.

*[ON SCREEN: Vary symbology by attribute tab]*

Now the clever part. Open Vary symbology by attribute. Here a single symbol can change with a numeric field:

Transparency — features with lower values fade out.

Color — shades the symbol along a colour ramp by value.

Size or rotation — for points and lines.

*[ON SCREEN: transparency by population]*

For example, set Transparency to the Population field, and sparsely populated areas fade. It's a subtle way to show a second variable without changing the main style.

Note: these options only work with numeric fields.

### Lesson 7.3: Unique Values  (7 min)

**Objective:** Give each category its own symbol.

*[ON SCREEN: Unique Values on land use]*

Unique Values gives each distinct value in a field its own symbol — ideal for categories like land use, road type or country name.

Choose Unique Values, then pick the Field. That's the specific field the categories come from; you can add up to three fields to combine them. ArcGIS Pro lists every value with a colour from the scheme.

*[ON SCREEN: Add all values / Add values button]*

If new values appear in the data later, click Add all values to refresh the list. Use Add values to pick only some, and everything else falls into "all other values".

*[ON SCREEN: grouping and reordering]*

Drag classes to reorder them, or select several and group them into one class. Edit a label by clicking it.

*[ON SCREEN: transparency for a unique value class]*

Transparency: open a class's symbol and set the fill transparency. A 30 to 50 percent transparent fill lets the basemap show through — very useful for overlays like flood zones on top of streets.

### Lesson 7.4: Graduated Colors  (8 min)

**Objective:** Classify numeric data into coloured classes.

*[ON SCREEN: Graduated Colors on districts]*

Graduated Colors shades features by a numeric value, grouped into classes. It's the classic choropleth map.

Pick the Field. Use Normalization to divide by another field — for example population divided by area for density. Normalizing is important: raw counts on polygons of different sizes can mislead.

*[ON SCREEN: Method and Classes]*

Choose the Method: Natural Breaks, Equal Interval, Quantile, Standard Deviation, Geometric Interval, or Manual. Then set the number of Classes — five to seven is a good range.

Each feature gets the colour of the class its value falls into. The table shows each class's upper value and its label.

*[ON SCREEN: Color scheme]*

Pick a Color scheme. For values going from low to high, use a single-hue or sequential ramp, light for low and dark for high.

*[ON SCREEN: Histogram tab]*

Switch to the Histogram tab to see how your data is distributed. Drag a break line to adjust a class manually; the method switches to Manual.

*[ON SCREEN: layer transparency]*

Set transparency for the whole layer on the Feature Layer tab, Effects group, so labels and basemap stay readable.

### Lesson 7.5: Graduated Symbols  (7 min)

**Objective:** Show quantities with symbols that change size by class.

*[ON SCREEN: Graduated Symbols on districts]*

Graduated Symbols shows quantities with symbol size instead of colour. Values are grouped into classes, and each class gets a bigger symbol.

How is it different from Graduated Colors? Colour is good for rates and densities across areas. Size is better for counts — total population, number of schools — because our eyes read bigger as more.

*[ON SCREEN: Field, Method, Classes]*

Pick a numeric Field; it must be numeric. Choose a classification Method and number of Classes, just like graduated colours.

*[ON SCREEN: Minimum and Maximum size]*

Set the size range — a Minimum size and Maximum size. The smallest class gets the minimum, the largest the maximum. If big symbols cover each other, reduce the maximum.

*[ON SCREEN: Template and Background]*

Use Template to change the symbol shape, and for polygon layers, set the Background symbol — the fill drawn under the circles. A light grey works well.

### Lesson 7.6: Unclassed Colors  (5 min)

**Objective:** Show a continuous colour ramp without classes.

*[ON SCREEN: Unclassed Colors]*

Unclassed Colors shades features along a continuous colour ramp. Instead of five or six steps, every value gets its own exact shade between the lowest and highest colour.

That's why it's called unclassed: there are no class breaks — the colour is calculated straight from the value.

*[ON SCREEN: compare with Graduated Colors]*

The trade-off: graduated colours are easier to read from a legend, because each colour means a range. Unclassed colours show subtle differences more faithfully, but readers can't easily tell exact values apart.

*[ON SCREEN: upper and lower labels]*

You can set the upper and lower values and their labels, so outliers don't stretch the ramp.

### Lesson 7.7: Proportional Symbols  (6 min)

**Objective:** Size symbols in exact proportion to a value.

*[ON SCREEN: Proportional Symbols]*

Proportional Symbols sizes each symbol exactly in proportion to its value. A city with twice the population gets a symbol with twice the area.

That's the difference from graduated symbols: graduated uses classes, so many features share the same size. Proportional uses no classes.

*[ON SCREEN: Field, Unit, sizes]*

Choose the Field. Set the Unit — leave it Unknown units for counts, or pick a distance unit if the value is a real-world size, like a radius in metres. Set the Minimum size, and the Maximum size or turn on appearance compensation.

*[ON SCREEN: Template and legend count]*

Change the symbol shape with Template, and choose how many sample sizes appear in the legend.

*[ON SCREEN: Vary symbology > Rotation]*

For dynamic rotation, use Vary symbology by attribute, Rotation, and pick a field holding an angle — handy for arrows showing wind direction.

### Lesson 7.8: Dot Density  (7 min)

**Objective:** Show counts as scattered dots inside polygons.

*[ON SCREEN: Dot Density on districts]*

Dot Density places dots randomly inside each polygon, where each dot stands for a set number of things. It only works for polygon layers.

*[ON SCREEN: adding fields]*

Add one or more numeric fields. With several fields — say, population by age group — each gets its own colour. Click the colour scheme to pick a random or custom palette so groups stand out.

*[ON SCREEN: Dot Size and Dot Value]*

Two settings matter most. Dot Size is how big each dot is. Dot Value is how many units each dot represents — one dot equals 500 people, for example. Adjust them together until dense areas look full but not solid.

*[ON SCREEN: Background]*

Set a Background symbol for the polygons, usually a pale fill and thin outline.

*[ON SCREEN: population map]*

Dot density is excellent for population research and presentations, because it shows where people are concentrated without the area bias of a choropleth. Remember the dots are random within each polygon — they're not real household locations.

### Lesson 7.9: Choosing the Right Symbology and Basics Wrap-up  (5 min)

**Objective:** Match the symbology method to the data and the message.

*[ON SCREEN: decision chart]*

Let's pull it together.

Categories, like land use: Unique Values.

Rates, percentages or densities across areas: Graduated Colors, or Unclassed Colors for subtle variation.

Counts or totals: Graduated Symbols or Proportional Symbols.

Counts spread across areas where distribution matters: Dot Density.

Everything the same, just a reference layer: Single Symbol.

*[ON SCREEN: recap montage]*

In the Basics level you installed ArcGIS Pro, created projects, learned the interface, navigated maps and scenes, created shapefiles, added data, mastered Contents, and designed maps with every core symbology method.

*[ON SCREEN: next steps]*

Practise by mapping a dataset from your own city with three different symbology methods. Then continue to the Intermediate level, where we start with geodatabases.

#### Module quiz

1. Which method suits land-use categories?  
   **Answer:** Unique Values — Categories get one symbol per value.

2. Which symbology works only for polygons?  
   **Answer:** Dot Density — Dot density places dots inside polygons.

3. How do proportional symbols differ from graduated symbols?  
   **Answer:** They size each symbol by its exact value, without classes — Graduated symbols group values into classes.

# ArcGIS · Intermediate

## M8 — Geodatabases and Data Management

### Lesson 8.1: File Geodatabases vs Shapefiles  (6 min)

**Objective:** Create a file geodatabase and explain why it beats shapefiles for most work.

*[ON SCREEN: Catalog pane > Databases]*

Every project already has a file geodatabase — the .gdb folder we saw in Module 1. You can create more: right-click Databases, or a folder, and choose New File Geodatabase.

*[ON SCREEN: comparison table on screen]*

Why use a geodatabase instead of shapefiles? Field names can be long and readable. There's no 2 GB limit per dataset. Dates store time as well as date. And you get tools shapefiles can't offer: domains, subtypes, attachments, topology, and editor tracking.

*[ON SCREEN: right-click gdb > New > Feature Class]*

Inside a geodatabase you create feature classes, tables, and feature datasets. A feature dataset is a container for feature classes that share one coordinate system — needed for topology and network datasets.

Right-click the geodatabase, New, Feature Class. A wizard walks you through name, alias, geometry type, fields and coordinate system in one place.

> **Tip:** Keep one geodatabase per project for working data, and a separate one for final, clean deliverables.

### Lesson 8.2: Fields, Data Types, Domains and Subtypes  (7 min)

**Objective:** Design a table with the right field types and enforce valid values with domains.

*[ON SCREEN: right-click layer > Data Design > Fields]*

Open the Fields view: right-click a layer, Data Design, Fields. Each row is a field with a name, alias, data type and length.

*[ON SCREEN: data type drop-down]*

Choose types carefully. Text for names and codes. Short or Long Integer for whole numbers. Float or Double for decimals. Date for dates and times. Picking the right type now saves conversion work later.

*[ON SCREEN: Data Design > Domains]*

A domain limits what can go in a field. A coded value domain is a pick list — for example road type: 1 Highway, 2 Arterial, 3 Local. A range domain sets a minimum and maximum, like a speed limit between 10 and 140. Create domains under Data Design, Domains, then assign one to a field in the Fields view.

*[ON SCREEN: Data Design > Subtypes]*

Subtypes split one feature class into categories that can each have their own default values and domains. Editors then pick "Highway" or "Local road" as a template, and the right rules come with it.

Save your changes with the Save button on the Fields tab.

### Lesson 8.3: Importing and Exporting Data  (5 min)

**Objective:** Move data between shapefiles, geodatabases and tables.

*[ON SCREEN: Feature Class To Geodatabase tool]*

To bring many shapefiles into a geodatabase at once, use Feature Class To Geodatabase. Add the inputs, pick the output geodatabase, and run.

*[ON SCREEN: Export Features]*

For one layer, right-click it and choose Data, Export Features. You can rename fields, drop fields, and apply a query in the same step.

*[ON SCREEN: Excel To Table and XY Table To Point]*

Spreadsheets come in with Excel To Table. If the table has coordinates, XY Table To Point turns rows into points — just pick the X and Y fields and the coordinate system the numbers are in.

*[ON SCREEN: Table To Excel]*

To go the other way, Table To Excel exports an attribute table for colleagues who don't use GIS.

> **Tip:** Clean Excel files before importing: one header row, no merged cells, no blank columns.

#### Module quiz

1. Which item can group feature classes that share one coordinate system inside a geodatabase?  
   **Answer:** A feature dataset — Feature datasets hold feature classes with the same coordinate system, which topology and networks need.

2. What does a coded value domain do?  
   **Answer:** Limits a field to a list of valid values — Domains enforce valid attribute values, such as a fixed list of road types.

3. Which tool copies several shapefiles into a geodatabase in one run?  
   **Answer:** Feature Class To Geodatabase — Feature Class To Geodatabase converts many inputs at once and keeps their names.

## M9 — Editing Features

### Lesson 9.1: Creating Features  (7 min)

**Objective:** Draw points, lines and polygons with feature templates and snapping.

*[ON SCREEN: Edit tab > Create]*

Editing starts on the Edit tab. Click Create to open the Create Features pane. Each editable layer has a template; click one and the construction tools appear underneath.

*[ON SCREEN: drawing a polygon]*

For polygons, choose Polygon, then click on the map to add vertices. Double-click or press F2 to finish. For lines it's the same; for points, a single click.

*[ON SCREEN: snapping to an existing edge]*

Turn on snapping so new features meet existing ones exactly. Press Spacebar while drawing to suspend snapping for one click.

*[ON SCREEN: right-click context menu while drawing]*

Right-click during a sketch for precision options — enter a direction and distance, or an absolute X and Y. Use the Trace tool to follow existing edges, for example to draw a parcel that shares a boundary with its neighbour.

> **Tip:** Press Ctrl+Z to undo the last vertex while you're still drawing.

### Lesson 9.2: Modifying Features: Move, Reshape, Split and Merge  (7 min)

**Objective:** Change the shape of existing features with the Modify Features tools.

*[ON SCREEN: Edit tab > Modify]*

Click Modify on the Edit tab to open the Modify Features pane. It groups tools by job: Alignment, Reshape, Divide, Construct and more. Use the search box if you know the tool name.

*[ON SCREEN: Edit Vertices]*

Select a feature and choose Edit Vertices. Drag a vertex to move it. Click a segment to add one. Select a vertex and press Delete to remove it. Press F2 to finish.

*[ON SCREEN: Reshape]*

Reshape lets you draw a line across a feature's edge to push it out or pull it in.

*[ON SCREEN: Split, then Merge]*

Split cuts a line or polygon where you draw. Merge does the opposite: select two or more features in the same layer, run Merge, and choose which feature's attributes to keep.

*[ON SCREEN: Move tool]*

To move or rotate whole features, select them and use Move or Rotate on the Edit tab.

### Lesson 9.3: Editing Attributes and Saving Edits  (5 min)

**Objective:** Update attributes for one or many features and manage your edit session.

*[ON SCREEN: Edit tab > Attributes]*

The Attributes pane shows the fields of the selected feature. Click a value, type a new one, and press Enter. Select many features to change a field for all of them at once.

*[ON SCREEN: editing in the attribute table]*

You can also type straight into the attribute table, or copy values down a column.

*[ON SCREEN: Save and Discard buttons]*

Edits aren't written to the data until you click Save on the Edit tab. Discard throws away everything since the last save. Saving the project does not save edits — they're separate.

*[ON SCREEN: Settings > Options > Editing]*

In Options, Editing, you can turn on "Save edits automatically" every few minutes, and choose whether ArcGIS Pro asks before saving. Turning off editing for layers in List By Editing protects them from accidental changes.

#### Module quiz

1. Where do you pick the template to draw a new feature?  
   **Answer:** The Create Features pane — Create Features lists a template for each editable layer.

2. Which tool divides one polygon into two along a line you draw?  
   **Answer:** Split — Split cuts features along a sketch line.

3. Edits are written to the data when you…  
   **Answer:** Click Save on the Edit tab — Data edits are saved separately from the project.

## M10 — Querying and Exploring Data

### Lesson 10.1: Select By Attributes  (6 min)

**Objective:** Build attribute queries with the clause builder.

*[ON SCREEN: Map tab > Select By Attributes]*

On the Map tab, click Select By Attributes. Choose the input layer and the selection type — new selection, add, remove, or select from the current selection.

*[ON SCREEN: clause builder: Population is greater than 100000]*

Build a clause with three drop-downs: field, operator, value. For example, Population — is greater than — 100000. Click Add Clause to combine more with And or Or.

*[ON SCREEN: switching to SQL mode]*

Switch the toggle to SQL to see and edit the raw expression. This is handy for patterns, like NAME LIKE 'San%'.

*[ON SCREEN: Apply and table showing selection count]*

Click Apply to check the result without closing the tool, then OK. The status bar and the table show how many features are selected.

> **Tip:** Save a query you use often with the save button, and load it next time.

### Lesson 10.2: Select By Location  (6 min)

**Objective:** Select features by their spatial relationship to another layer.

*[ON SCREEN: Map tab > Select By Location]*

Select By Location answers questions like "which schools are within 1 kilometre of a highway?" Open it from the Map tab.

*[ON SCREEN: tool parameters]*

Set the Input Features — the layer you want to select from. Choose the Relationship, such as Intersect, Within a distance, Completely contain, or Have their center in. Set the Selecting Features — the layer you're comparing against. For distance relationships, enter a search distance.

*[ON SCREEN: combining with an attribute selection]*

Use the selection type to refine: first select schools near highways, then use Select By Attributes with "select subset" to keep only primary schools.

*[ON SCREEN: Invert spatial relationship checkbox]*

Tick Invert spatial relationship to get the opposite — schools more than 1 kilometre away.

### Lesson 10.3: Definition Queries and Summary Statistics  (5 min)

**Objective:** Filter a layer permanently and summarise its attributes.

*[ON SCREEN: Layer Properties > Definition Query]*

A definition query hides features that don't match a clause — the data stays intact. Open Layer Properties, Definition Query, click New definition query, and build the clause the same way as Select By Attributes.

Use it to show only one region, one year, or one category, and to make every tool and chart work on just that subset.

*[ON SCREEN: right-click field header > Statistics]*

For quick numbers, right-click a field heading in the attribute table and choose Statistics. You get count, minimum, maximum, sum, mean and standard deviation, with a chart.

*[ON SCREEN: Summary Statistics tool]*

To summarise by category — total population per province, for example — run Summary Statistics with a case field. The output is a new table you can join or chart.

### Lesson 10.4: Creating Charts  (6 min)

**Objective:** Build interactive charts linked to the map.

*[ON SCREEN: right-click layer > Create Chart]*

Right-click a layer, Create Chart, and pick a type: bar, line, histogram, scatter plot, pie and more.

*[ON SCREEN: Chart Properties pane]*

In the Chart Properties pane, set the category and the numeric field. For a bar chart of population by province, set Category to Province and Aggregation to Sum of Population.

*[ON SCREEN: clicking a bar selects features]*

Charts are linked to the map. Click a bar and those features are selected on the map and in the table. Select features on the map and the chart highlights them.

*[ON SCREEN: Format tab, export]*

Change colours, titles and axes on the Format tab. Charts are saved with the layer, and you can export them as images or add them to a layout.

#### Module quiz

1. Which tool selects parcels that fall inside a flood zone polygon?  
   **Answer:** Select By Location — Select By Location uses spatial relationships between layers.

2. A definition query…  
   **Answer:** Hides features that don't match, without deleting them — Definition queries filter what a layer displays and uses.

3. Charts in ArcGIS Pro are linked to…  
   **Answer:** The layer's selection — Selecting bars selects features on the map, and the other way round.

## M11 — Working with Tables

### Lesson 11.1: Adding Fields and Calculating Values  (7 min)

**Objective:** Add a field and fill it with Calculate Field.

*[ON SCREEN: attribute table > Add Field]*

In the attribute table, click Add Field to open the Fields view, or run the Add Field tool. Give it a name, a type and, for text, a length. Save.

*[ON SCREEN: right-click field > Calculate Field]*

Right-click the new field heading and choose Calculate Field. Pick the expression type: Python or Arcade.

*[ON SCREEN: expression Population / Area]*

Double-click fields to build an expression. For density, the Python expression is !POP! / !AREA_KM2!. In Arcade, it's $feature.POP / $feature.AREA_KM2.

*[ON SCREEN: code block with if/else]*

For conditions, use the code block — for example a function that returns "High" when density is over 1000 and "Low" otherwise.

Calculate Field only updates selected rows if there's a selection, so clear the selection first if you want every row.

> **Tip:** Use the Verify button to check your expression before running.

### Lesson 11.2: Calculating Geometry: Area, Length and Coordinates  (5 min)

**Objective:** Store area, length and X/Y values in attribute fields.

*[ON SCREEN: right-click field > Calculate Geometry]*

Right-click a numeric field and choose Calculate Geometry, or run Calculate Geometry Attributes.

*[ON SCREEN: property and units]*

Pick the property: Area or Area (geodesic) for polygons, Length for lines, Point X and Point Y for points. Choose the units — square kilometres, metres, decimal degrees.

*[ON SCREEN: coordinate system parameter]*

Set the coordinate system to calculate in. Geodesic area and length give true values on the ellipsoid, so they're the safe choice when your data is in latitude and longitude.

These values are a snapshot: if you reshape a feature later, recalculate.

### Lesson 11.3: Joins, Relates and Spatial Joins  (7 min)

**Objective:** Combine data from different tables and layers.

*[ON SCREEN: right-click layer > Joins and Relates > Add Join]*

A join appends fields from a table to a layer using a common field, like a district code. Right-click the layer, Joins and Relates, Add Join. Choose the layer field, the join table and the join table field. Click Validate Join to check matches first.

*[ON SCREEN: joined fields in the table]*

Joins are temporary. To make them permanent, export the layer or use the Join Field tool.

*[ON SCREEN: Add Relate]*

Use a relate for one-to-many data — one parcel with many inspection records. Relates don't add fields; instead you select a feature and open its related records.

*[ON SCREEN: Spatial Join tool]*

When there's no common field, Spatial Join matches by location. For example, count the number of crimes inside each district: target features are districts, join features are crimes, and the output gets a Join_Count field.

#### Module quiz

1. Which language can Calculate Field use?  
   **Answer:** Python or Arcade — Calculate Field supports Python and Arcade expressions.

2. What does a join do?  
   **Answer:** Appends fields from a table based on a common field — Joins attach fields from another table using a key field.

3. Which tool attaches attributes based on location rather than a key field?  
   **Answer:** Spatial Join — Spatial Join matches features by their spatial relationship.

## M12 — Coordinate Systems and Georeferencing

### Lesson 12.1: Geographic vs Projected Coordinate Systems  (6 min)

**Objective:** Explain the two kinds of coordinate system and when to use each.

*[ON SCREEN: globe with latitude/longitude lines]*

A geographic coordinate system describes locations on a model of the Earth using latitude and longitude, in degrees. WGS 1984 is the most common.

*[ON SCREEN: flat projection with grid in metres]*

A projected coordinate system flattens the Earth onto a plane and uses linear units like metres. Every projection distorts something — area, shape, distance or direction — so each one is designed for a region or a purpose. UTM zones and national grids are common examples.

*[ON SCREEN: measurement comparison]*

Use a projected system when you measure distance or area, or when you need an accurate map of a local area. Use a geographic system for storing and exchanging global data.

*[ON SCREEN: Layer Properties > Source > Spatial Reference]*

To see a layer's coordinate system, open Layer Properties, Source, and expand Spatial Reference.

### Lesson 12.2: Map Coordinate Systems and Transformations  (6 min)

**Objective:** Set the map's coordinate system and handle datum transformations.

*[ON SCREEN: Map Properties > Coordinate Systems]*

The map has its own coordinate system, set by the first layer you add. ArcGIS Pro projects every other layer to it on the fly, so they line up.

Change it in Map Properties, Coordinate Systems. Search by name or by EPSG code, or pick from Layers to match one of your datasets.

*[ON SCREEN: Transformation tab]*

When layers use different datums — for example WGS 1984 and a local datum — a geographic transformation is needed for them to line up exactly. Set it on the Transformation tab of Map Properties. ArcGIS Pro suggests suitable ones for your area.

> **Tip:** If two layers are offset by tens or hundreds of metres, a missing transformation is the usual cause.

### Lesson 12.3: Define Projection vs Project  (5 min)

**Objective:** Fix missing coordinate systems and convert data to a new one.

*[ON SCREEN: Define Projection tool]*

Define Projection writes the coordinate system information for data that's missing it. It doesn't move anything — it just tells ArcGIS Pro what the numbers already mean. Use it only when you know the correct system.

*[ON SCREEN: Project tool]*

Project actually converts coordinates to a new system and writes a new dataset. Use it when you need your data stored in a projected system for analysis, or to match a client's standard.

*[ON SCREEN: Project Raster]*

For rasters, use Project Raster, and choose a resampling method — Nearest for categories like land cover, Bilinear for continuous data like elevation.

The rule of thumb: Define Projection when it's missing, Project when it's wrong for the job.

### Lesson 12.4: Georeferencing a Scanned Map  (7 min)

**Objective:** Place a scanned map or image in its real-world location.

*[ON SCREEN: add scanned JPG]*

Add the scanned map to a map that has a reference layer, such as a basemap or roads. Select the image in Contents, then on the Imagery tab click Georeference.

*[ON SCREEN: Fit to Display]*

Click Fit To Display to bring the image into view.

*[ON SCREEN: Add Control Points]*

Click Add Control Points. Click a recognisable spot on the scan — a road junction — then the same spot on the reference layer. Add at least four, spread across the whole image.

*[ON SCREEN: Control Point Table with RMS]*

Open the Control Point Table to see residuals and the total RMS error. Remove points with large residuals. Choose a transformation: 1st Order Polynomial for most scans, Spline for very distorted ones.

*[ON SCREEN: Save / Save as New]*

Click Save to store the georeferencing with the image, or Save as New to create a new, rectified raster.

#### Module quiz

1. Which kind of coordinate system uses latitude and longitude?  
   **Answer:** Geographic — Geographic coordinate systems use angular units on the spheroid.

2. You know a shapefile's coordinates are UTM zone 40N, but it has no .prj. Which tool do you use?  
   **Answer:** Define Projection — Define Projection records the existing coordinate system without changing coordinates.

3. What does a low RMS error in georeferencing indicate?  
   **Answer:** Control points fit the transformation closely — RMS measures how far control points are from where the transformation puts them.

## M13 — Labeling and Annotation

### Lesson 13.1: Label Classes and Expressions  (6 min)

**Objective:** Label features with fields, expressions and label classes.

*[ON SCREEN: Feature Layer > Labeling tab]*

Select a layer and open the Labeling tab. Click Label to turn labels on, then pick the Field.

*[ON SCREEN: Expression button, Arcade]*

For more control, click Expression. In Arcade you can combine fields — $feature.NAME + TextFormatting.NewLine + $feature.POP — to show the name with population underneath.

*[ON SCREEN: Class drop-down > Create label class]*

Label classes let one layer use different label styles. Create a class called Large cities with an SQL query of POP greater than 1000000, give it a bigger, bold font, and keep the default class smaller.

*[ON SCREEN: Visibility Range]*

Set a visibility range so small towns only label when you zoom in.

### Lesson 13.2: Label Placement and Conflicts  (6 min)

**Objective:** Control where labels go and which ones win when space is tight.

*[ON SCREEN: Label Class pane > Position]*

Open the Label Class pane with the small arrow in the Label Placement group. ArcGIS Pro uses the Maplex Label Engine, which gives fine control.

*[ON SCREEN: placement styles]*

Choose placement: for points, a preferred position around the symbol; for lines, along the line with curved or straight text; for rivers and roads, Maplex has dedicated styles. For polygons, horizontal in the centre or straight across the shape.

*[ON SCREEN: Conflict resolution > priority, weight]*

When labels compete, priority decides who wins — set it in List By Labeling. Feature weight stops labels covering important features. "Never remove" forces a label to show, even if it overlaps.

*[ON SCREEN: View Unplaced labels]*

Turn on View Unplaced on the Labeling tab to see which labels didn't fit.

### Lesson 13.3: Converting Labels to Annotation  (5 min)

**Objective:** Turn labels into annotation you can place by hand.

*[ON SCREEN: right-click layer > Convert Labels > To Annotation]*

Labels are placed automatically and move as you pan and zoom. For a finished print map, you may want each piece of text exactly where you put it. That's annotation.

Right-click the layer, Convert Labels, Convert Labels To Annotation. Set the reference scale — the scale the map will be printed at — and the output geodatabase.

*[ON SCREEN: editing annotation]*

Annotation is stored as features. Use the Edit tab tools to move, rotate, resize or delete individual text, and to edit wording.

Use annotation for final cartography, and keep labels for maps that change often.

#### Module quiz

1. How do you label only cities with more than one million people?  
   **Answer:** Create a label class with an SQL query — Label classes can each have their own SQL query and style.

2. Annotation differs from labels because annotation…  
   **Answer:** Is stored as editable text features — Annotation is stored text you can position individually.

3. Which label engine does ArcGIS Pro use by default?  
   **Answer:** Maplex — ArcGIS Pro uses the Maplex Label Engine by default.

## M14 — Layouts and Map Production

### Lesson 14.1: Creating a Layout and Map Frame  (6 min)

**Objective:** Set up a page and place a map on it.

*[ON SCREEN: Insert tab > New Layout]*

On the Insert tab, click New Layout and pick a page size and orientation, such as A4 landscape.

*[ON SCREEN: Insert > Map Frame]*

Click Map Frame and choose which map to show. Drag on the page to draw it.

*[ON SCREEN: Layout tab > Activate]*

To change what part of the map is shown, select the frame and click Activate. Now you can pan and zoom inside it. Click Close Activation when done. For a fixed scale, set it in the scale box while activated, or in the frame's properties.

*[ON SCREEN: guides and rulers]*

Right-click the rulers to add guides, and snap elements to them for a tidy layout.

> **Tip:** Import a ready-made layout from Insert, Import Layout, to save time.

### Lesson 14.2: Legends, North Arrows, Scale Bars and Text  (7 min)

**Objective:** Add and format map surround elements.

*[ON SCREEN: Insert tab > Map Surrounds]*

On the Insert tab, Map Surrounds group, add a Legend, North Arrow and Scale Bar. Each is linked to a map frame, so it updates when the map changes.

*[ON SCREEN: legend properties]*

In the Format Legend pane, choose which layers appear, rename layer headings in Contents, and set columns and fonts. Untick "Show in legend" for reference layers.

*[ON SCREEN: scale bar units]*

Set scale bar units to kilometres or miles and the number of divisions.

*[ON SCREEN: Dynamic Text]*

Add a title with Text. Use Dynamic Text for things that should update themselves — the date, the coordinate system, the map's scale, or the author.

Check alignment with the Align tools on the Arrange group.

### Lesson 14.3: Exporting Layouts and Map Series  (6 min)

**Objective:** Export print-ready maps and produce many pages automatically.

*[ON SCREEN: Share tab > Export Layout]*

On the Share tab, click Export Layout. Choose PDF for print, or PNG or JPEG for slides and social posts. Set the resolution — 300 dpi for print, 150 for screens.

*[ON SCREEN: PDF options: layers and attributes]*

PDF options let you include layers and feature attributes, so readers can switch layers in Acrobat.

*[ON SCREEN: Layout tab > Map Series > Spatial]*

A map series makes a page for each feature in an index layer — one map per district, for example. On the Layout tab, click Map Series, Spatial. Choose the index layer, the name field and the sort field.

*[ON SCREEN: Map Series pages in Contents]*

Page through them in Contents, add dynamic text for the page name, then export all pages to one PDF.

#### Module quiz

1. Which element shows the map's content in a layout?  
   **Answer:** Map frame — A map frame displays a map or scene on the layout page.

2. What does a map series create?  
   **Answer:** One page per feature in an index layer — Map series produce a page for each index feature.

3. Where do you export a layout to PDF?  
   **Answer:** Share tab > Export Layout — Export Layout writes PDF, PNG, JPEG and more.

## M15 — Geoprocessing Essentials

### Lesson 15.1: The Geoprocessing Pane, History and Environments  (6 min)

**Objective:** Find, run and track geoprocessing tools.

*[ON SCREEN: Analysis tab > Tools]*

On the Analysis tab, click Tools to open the Geoprocessing pane. Search for any tool by name, or browse the Toolboxes tab. Favorite the tools you use often.

*[ON SCREEN: tool with red/yellow validation icons]*

Fill in parameters from top to bottom. Red icons mean a problem you must fix; yellow ones are warnings. Click Run.

*[ON SCREEN: Environments tab]*

The Environments tab sets rules for the run: output coordinate system, processing extent, cell size for rasters. Set them for the whole project from the Analysis tab, Environments.

*[ON SCREEN: Catalog > History]*

Every run is recorded in History, in the Catalog pane. Double-click an entry to reopen the tool with the same settings — great for repeating work.

### Lesson 15.2: Overlay Tools: Buffer, Clip, Intersect and Union  (8 min)

**Objective:** Answer "what's near" and "what overlaps" questions with overlay tools.

*[ON SCREEN: Pairwise Buffer on rivers]*

Buffer draws zones a set distance around features. Run Pairwise Buffer on rivers with 500 metres, and set Dissolve Type to dissolve all for one merged zone.

*[ON SCREEN: Pairwise Clip roads to city]*

Clip works like a cookie cutter: it keeps the parts of the input inside the clip features. Clip roads to the city boundary.

*[ON SCREEN: Pairwise Intersect]*

Intersect keeps only where all inputs overlap, and combines their attributes — for example land parcels inside the flood buffer, with the parcel and flood fields together.

*[ON SCREEN: Union]*

Union keeps everything from both inputs, split where they overlap, so you can see what's inside, outside, or both.

> **Tip:** The Pairwise versions are faster on large data and are the right choice for most jobs.

### Lesson 15.3: Dissolve, Merge and Append  (5 min)

**Objective:** Combine and aggregate datasets.

*[ON SCREEN: Dissolve districts by province]*

Dissolve merges features that share a value. Dissolve districts by Province to get province boundaries. Add statistics fields to sum population while you dissolve.

*[ON SCREEN: Merge tool]*

Merge combines several datasets of the same geometry into a new one — say, roads from three neighbouring regions. Use field mapping to line up fields with different names.

*[ON SCREEN: Append tool]*

Append adds features into an existing dataset instead of creating a new one. Use it when you get monthly updates to load into a master layer.

#### Module quiz

1. Which tool keeps only the part of roads inside a city boundary?  
   **Answer:** Clip — Clip cuts input features to the clip feature's outline.

2. Which tool combines adjacent polygons that share a value?  
   **Answer:** Dissolve — Dissolve aggregates features by a field.

3. Where do you set the output coordinate system for every tool?  
   **Answer:** Geoprocessing environments — Environment settings apply to every tool that honours them.

# ArcGIS · Advanced

## M16 — Raster Analysis with Spatial Analyst

### Lesson 16.1: Terrain Analysis: Hillshade, Slope and Aspect  (7 min)

**Objective:** Derive terrain surfaces from a digital elevation model.

*[ON SCREEN: DEM added to map]*

Start with a digital elevation model — a raster where each cell holds a height. Surface tools need the Spatial Analyst or 3D Analyst extension; check Licensing if they're greyed out.

*[ON SCREEN: Surface Parameters / Hillshade raster function]*

Hillshade simulates sunlight on the terrain. Set the sun's azimuth and altitude; the default 315 and 45 works well. Lay a semi-transparent elevation colour ramp over it for a classic relief map.

*[ON SCREEN: Slope in degrees]*

Slope calculates steepness in each cell, in degrees or percent. It's key for landslide risk, construction and hiking routes.

*[ON SCREEN: Aspect with directional colours]*

Aspect gives the compass direction each slope faces — useful for solar panels, vineyards and snow studies.

> **Tip:** Raster functions on the Imagery tab preview results instantly without writing files. Run the geoprocessing tool when you need a permanent output.

### Lesson 16.2: Reclassify and the Raster Calculator  (7 min)

**Objective:** Convert raster values into classes and combine rasters with map algebra.

*[ON SCREEN: Reclassify tool]*

Reclassify replaces ranges of values with new ones. For slope: 0 to 5 degrees becomes 1, 5 to 15 becomes 2, over 15 becomes 3. Click Classify to choose a method and number of classes, or type the ranges directly.

*[ON SCREEN: Raster Calculator]*

The Raster Calculator does maths cell by cell. Double-click rasters and operators to build an expression, such as "Elevation" > 1000, which returns 1 where true and 0 where false.

*[ON SCREEN: Con expression]*

Use Con for if-then logic: Con("Slope" < 10, 1, 0) marks gentle slopes. Combine conditions with & for and, | for or.

*[ON SCREEN: environments: cell size, extent, mask]*

Set Environments — cell size, processing extent and mask — so outputs line up exactly.

### Lesson 16.3: Suitability Modeling with Weighted Overlay  (8 min)

**Objective:** Find the best locations by combining weighted criteria.

*[ON SCREEN: problem statement: best site for a solar farm]*

Let's find the best place for a solar farm: gentle slopes, south-facing, near roads, away from protected areas.

*[ON SCREEN: input rasters]*

Prepare one raster per criterion: slope, aspect, distance to roads — from the Distance Accumulation tool — and protected areas.

*[ON SCREEN: Weighted Overlay tool]*

Open Weighted Overlay. Add each raster, set the evaluation scale — 1 to 9 — and give each class a score, with Restricted for places that must be excluded. Then set each raster's percent influence so they add up to 100.

*[ON SCREEN: output map]*

The result scores every cell. Highest values are the best sites.

*[ON SCREEN: Suitability Modeler]*

For a guided, interactive version, try the Suitability Modeler on the Analysis tab, which shows the result update as you change weights.

#### Module quiz

1. Which tool shows terrain as if lit by the sun?  
   **Answer:** Hillshade — Hillshade simulates illumination for a shaded-relief look.

2. Why reclassify rasters before a suitability overlay?  
   **Answer:** To put different criteria on one common scale — Reclassify turns metres, degrees and categories into comparable scores.

3. In Weighted Overlay, the percentage influences must add up to…  
   **Answer:** 100 — The influences share 100 percent among the criteria.

## M17 — Imagery and Remote Sensing

### Lesson 17.1: Band Combinations and Raster Functions  (6 min)

**Objective:** Display multispectral imagery and compute indices like NDVI.

*[ON SCREEN: Landsat or Sentinel-2 image]*

Satellite images have several bands — blue, green, red, near-infrared and more. Select the image and use the Raster Layer tab, Band Combination, to choose which bands show as red, green and blue.

*[ON SCREEN: natural colour vs colour infrared]*

Natural colour uses red, green, blue. Colour infrared puts near-infrared in the red channel, so healthy vegetation glows red — great for spotting crops and forests.

*[ON SCREEN: Imagery tab > Raster Functions > NDVI]*

On the Imagery tab, open Raster Functions and search NDVI. Pick the near-infrared and red band numbers for your sensor and run. Values near 1 mean dense vegetation; near zero or below means bare ground, water or buildings.

> **Tip:** Band numbers differ between sensors — check them before computing indices.

### Lesson 17.2: Image Classification  (8 min)

**Objective:** Classify land cover with the Image Classification Wizard.

*[ON SCREEN: Imagery tab > Classification Wizard]*

Select the image and open the Classification Wizard on the Imagery tab. Choose Supervised, pixel-based, and a schema — the default land-cover classes or your own.

*[ON SCREEN: Training Samples Manager]*

Draw training samples for each class: water, forest, urban, cropland, bare soil. Draw several small samples per class, spread across the image.

*[ON SCREEN: classifier choice]*

Choose a classifier. Random Trees and Support Vector Machine are strong defaults.

*[ON SCREEN: classified preview, merge classes, reclassifier]*

Preview the result, then use the wizard's reclassifier to fix obvious errors.

*[ON SCREEN: accuracy assessment page]*

The wizard can run an accuracy assessment that creates random points and a confusion matrix, giving overall accuracy and a kappa value.

### Lesson 17.3: Change Detection  (6 min)

**Objective:** Compare two dates of imagery to map what changed.

*[ON SCREEN: two NDVI rasters, 2018 and 2025]*

To find change, compare the same area at two dates. With continuous data such as NDVI, subtract the earlier date from the later one in the Raster Calculator. Strongly negative values show vegetation loss; positive values show growth.

*[ON SCREEN: Imagery tab > Change Detection Wizard]*

The Change Detection Wizard on the Imagery tab guides you through it, and also handles categorical change — comparing two land-cover classifications to show, for example, cropland that became urban.

*[ON SCREEN: change matrix]*

For categorical change, the output tells you each from-to transition, which you can summarise into an area table for reports.

#### Module quiz

1. Which bands does NDVI use?  
   **Answer:** Near-infrared and red — NDVI compares near-infrared and red reflectance.

2. In supervised classification, training samples are…  
   **Answer:** Areas you draw that represent each class — You teach the classifier with samples of known classes.

3. What does an accuracy assessment produce?  
   **Answer:** A confusion matrix — The confusion matrix compares classified and reference points.

## M18 — Spatial Statistics and Patterns

### Lesson 18.1: Density and Hot Spot Analysis  (8 min)

**Objective:** Map where events concentrate and test whether clusters are significant.

*[ON SCREEN: crime points]*

A dot map of incidents can be misleading — dots overlap and the eye picks false patterns. Let's measure instead.

*[ON SCREEN: Kernel Density result]*

Kernel Density spreads each point into a smooth surface. Choose a cell size and search radius; a larger radius gives a smoother map. It's a great visual, but it doesn't test significance.

*[ON SCREEN: Optimized Hot Spot Analysis]*

Optimized Hot Spot Analysis does. Give it the incident points and a polygon grid or district layer. It aggregates the points, picks a scale of analysis, and calculates Getis-Ord Gi* for each area.

*[ON SCREEN: hot and cold spots with confidence levels]*

Red areas are hot spots, blue are cold spots, at 90, 95 or 99 percent confidence. Grey means not significant.

> **Tip:** Read the tool's messages — they explain the choices it made.

### Lesson 18.2: Spatial Autocorrelation and Clustering  (7 min)

**Objective:** Measure clustering across a whole dataset and group similar features.

*[ON SCREEN: Spatial Autocorrelation (Global Moran's I)]*

Spatial Autocorrelation, Global Moran's I, asks: are similar values near each other across the whole study area? Run it on income by district and open the HTML report.

*[ON SCREEN: report: z-score and p-value]*

A positive, significant z-score means values are clustered; negative means dispersed; near zero is random.

*[ON SCREEN: Cluster and Outlier Analysis]*

To find where, run Cluster and Outlier Analysis (Anselin Local Moran's I). It marks high-high and low-low clusters, and outliers like a wealthy district surrounded by poorer ones.

*[ON SCREEN: Density-based Clustering]*

For points, Density-based Clustering finds groups of points close together, with noise points left out.

#### Module quiz

1. Hot Spot Analysis uses which statistic?  
   **Answer:** Getis-Ord Gi* — Hot Spot Analysis computes Getis-Ord Gi* for each feature.

2. A positive, significant Moran's I means values are…  
   **Answer:** Clustered — Positive spatial autocorrelation means similar values cluster.

3. Kernel Density outputs…  
   **Answer:** A smooth raster surface of density — Kernel Density spreads point values into a continuous surface.

## M19 — Geocoding and Network Analysis

### Lesson 19.1: Geocoding Addresses  (6 min)

**Objective:** Turn a table of addresses into points on the map.

*[ON SCREEN: Map tab > Locate]*

For one address, use the Locate pane on the Map tab: type it and press Enter.

*[ON SCREEN: Geocode Table / Geocode Addresses]*

For a whole table, right-click it in Contents and choose Geocode Table, or run Geocode Addresses. Pick the locator — the ArcGIS World Geocoding Service, or a locator your organisation built — and map the address fields.

*[ON SCREEN: credits warning]*

Batch geocoding with the World Geocoding Service uses ArcGIS Online credits, so check your allowance first.

*[ON SCREEN: Rematch Addresses pane]*

Review the results. Status M is matched, T is tied, U is unmatched. Use Rematch Addresses to fix unmatched and low-score records by hand.

> **Tip:** Build your own locator with Create Locator if you have local address data and need to geocode often.

### Lesson 19.2: Routes and Service Areas  (7 min)

**Objective:** Solve routing and drive-time problems with Network Analyst.

*[ON SCREEN: Analysis tab > Network Analysis > Route]*

Network Analyst works on a network dataset or on ArcGIS Online services. On the Analysis tab, open Network Analysis and choose Route. A route layer appears in Contents.

*[ON SCREEN: adding stops, Route tab]*

On the Route tab, click Import Stops or Create Features to add stops. Pick a travel mode — driving time, walking time, trucking — and click Run. Tick Reorder Stops to find the best sequence.

*[ON SCREEN: Directions pane]*

Open Directions for turn-by-turn instructions you can print or share.

*[ON SCREEN: Service Area]*

Service Area creates polygons of everywhere reachable within set times — 5, 10 and 15 minutes from each fire station. These are perfect for coverage and accessibility studies.

> **Tip:** Solving with ArcGIS Online network services uses credits; a local network dataset doesn't.

### Lesson 19.3: Closest Facility and Origin-Destination Analysis  (6 min)

**Objective:** Match demand to facilities with network-based distance.

*[ON SCREEN: Closest Facility layer]*

Closest Facility finds the nearest one or more facilities for each incident, by travel time or distance along the network. Load hospitals as facilities and accident locations as incidents, set the number to find, and run.

*[ON SCREEN: routes drawn to nearest hospital]*

You get a route for each pair, with travel time — much more realistic than straight-line distance.

*[ON SCREEN: OD Cost Matrix]*

For big tables of travel times — every school to every neighbourhood, for example — use the Origin-Destination Cost Matrix. It outputs straight lines with network travel cost, fast to compute at scale.

*[ON SCREEN: Location-Allocation]*

To decide where to put new facilities, Location-Allocation picks the best sites from a list of candidates.

#### Module quiz

1. Using the ArcGIS World Geocoding Service to batch geocode…  
   **Answer:** Consumes ArcGIS Online credits — Batch geocoding with Esri's online service uses credits.

2. Which analysis finds all streets reachable within 10 minutes of a station?  
   **Answer:** Service Area — Service Area creates drive-time or walk-time zones.

3. Which analysis finds the nearest hospital for each incident?  
   **Answer:** Closest Facility — Closest Facility routes each incident to its nearest facilities.

## M20 — 3D, Lidar and Animation

### Lesson 20.1: Extruding Features and 3D Symbology  (6 min)

**Objective:** Turn 2D footprints into 3D buildings.

*[ON SCREEN: building footprints in a local scene]*

Add building footprints to a local scene and drag them into 3D Layers.

*[ON SCREEN: Appearance tab > Type > Max Height]*

On the Feature Layer Appearance tab, set the extrusion type — Max Height is a good default — and choose the height field, such as HEIGHT_M, with the right units.

*[ON SCREEN: realistic 3D symbology]*

In Symbology, apply 3D symbols: realistic textures for trees and street furniture, or procedural building symbols with windows and roofs.

*[ON SCREEN: Layer 3D To Feature Class]*

To make the 3D shapes permanent as multipatch features, run Layer 3D To Feature Class.

### Lesson 20.2: Working with Lidar Point Clouds  (7 min)

**Objective:** Load LAS data, filter classes and build elevation surfaces.

*[ON SCREEN: Create LAS Dataset]*

Lidar arrives as LAS or LAZ files. Create LAS Dataset references many tiles as one layer and builds statistics. Add it to a scene.

*[ON SCREEN: LAS Dataset Layer tab > Filters]*

On the LAS Dataset Layer tab, filter by classification: ground, vegetation, buildings. Colour points by elevation, class, intensity or RGB.

*[ON SCREEN: LAS Dataset To Raster with ground filter]*

To build a terrain model, filter to ground points and run LAS Dataset To Raster for a DEM. Use all first returns for a surface model that includes trees and roofs.

*[ON SCREEN: Raster Calculator DSM minus DEM]*

Subtract the DEM from the surface model to get object heights — a canopy height model for forests.

### Lesson 20.3: Visibility Analysis: Line of Sight and Viewshed  (6 min)

**Objective:** Find what can be seen from a location.

*[ON SCREEN: Analysis tab > Exploratory 3D Analysis]*

In a scene, the Exploratory 3D Analysis tools give instant answers. Line of Sight shows green where a target is visible and red where it's blocked. Viewshed and View Dome show what can be seen from a point.

*[ON SCREEN: Viewshed geoprocessing tool]*

For a permanent result, run the Viewshed or Geodesic Viewshed tool on a DEM with observer points, setting observer height — say 1.7 metres for a person or 30 metres for a mast.

*[ON SCREEN: viewshed result over terrain]*

Use it to plan telecom towers, watchtowers, or to check how visible a new wind farm will be.

### Lesson 20.4: Creating Animations and Exporting Video  (7 min)

**Objective:** Build a flythrough and export it as a video.

*[ON SCREEN: View tab > Animation > Add]*

On the View tab, click Animation, then Add. The Animation tab and the timeline appear.

*[ON SCREEN: Create first keyframe]*

Navigate to your first view and click Create first keyframe. Move to the next view and click the plus button to add another. ArcGIS Pro flies smoothly between them.

*[ON SCREEN: keyframe properties: transition, duration]*

Adjust each keyframe's duration and transition, add text and image overlays, and preview with Play.

*[ON SCREEN: Export > Movie > YouTube preset]*

Click Movie in the Export group. Pick a preset — there's one for YouTube — set resolution and frame rate, and export to MP4.

> **Tip:** These flythroughs make great intros and B-roll for your own course videos.

#### Module quiz

1. Which file type stores lidar point clouds?  
   **Answer:** LAS / LAZ — Lidar data is commonly stored as LAS or compressed LAZ.

2. What does a viewshed show?  
   **Answer:** Areas visible from an observer — Viewsheds map what can be seen from observer points.

3. In the Animation timeline, each saved view is a…  
   **Answer:** Keyframe — Animations move smoothly between keyframes.

## M21 — Automation with ModelBuilder and Python

### Lesson 21.1: ModelBuilder Basics  (7 min)

**Objective:** Chain tools into a reusable workflow.

*[ON SCREEN: Analysis tab > ModelBuilder]*

ModelBuilder lets you build a workflow visually. On the Analysis tab, click ModelBuilder.

*[ON SCREEN: dragging Buffer and Clip into the model]*

Drag tools from the Geoprocessing pane onto the canvas. Drag a layer onto a tool to connect it as input. Double-click a tool to set its parameters; the output becomes the input for the next tool.

*[ON SCREEN: Validate and Run]*

Click Validate, then Run. Each tool turns from white to coloured as it completes.

*[ON SCREEN: Save to toolbox]*

Save the model in your project toolbox. Rename it with a clear name and description — it now behaves like any other tool.

> **Tip:** Use Auto Layout and group related tools to keep big models readable.

### Lesson 21.2: Model Parameters and Iterators  (7 min)

**Objective:** Turn a model into a flexible tool that runs over many inputs.

*[ON SCREEN: right-click variable > Parameter]*

Right-click an input or setting, such as buffer distance, and choose Parameter. A P appears. When someone opens the model from the toolbox, they can set it like any tool.

*[ON SCREEN: Insert > Iterators > Iterate Feature Classes]*

Iterators repeat the model over many items. Iterate Feature Classes loops through every feature class in a geodatabase. Iterate Field Values loops once per unique value.

*[ON SCREEN: inline variable %Name% in output]*

Use inline variable substitution so each output gets a unique name: name the output Buffer_%Name%, and the iterator fills in each input's name.

*[ON SCREEN: Export > Export to Python file]*

You can export a model to a Python script — a good bridge into the next lesson.

### Lesson 21.3: The Python Window and ArcPy Basics  (8 min)

**Objective:** Run ArcPy commands and loop over data with Python.

*[ON SCREEN: Analysis tab > Python > Python Window]*

Open the Python window from the Analysis tab. Type import arcpy — it's already loaded — and press Enter.

*[ON SCREEN: arcpy.env.workspace and ListFeatureClasses]*

Set the workspace: arcpy.env.workspace = the path to your geodatabase. Then arcpy.ListFeatureClasses() returns every feature class name.

*[ON SCREEN: running a tool]*

Every geoprocessing tool is a function: arcpy.analysis.Buffer("roads", "roads_buf", "100 Meters").

*[ON SCREEN: for loop]*

Loop over the list to run the same tool on all of them, building output names from each input.

*[ON SCREEN: arcpy.da.SearchCursor]*

Read attribute values with a cursor: with arcpy.da.SearchCursor("cities", ["NAME", "POP"]) as cursor, then loop over rows. Use UpdateCursor to change values.

> **Tip:** Drag a tool from History into the Python window to see its Python code.

### Lesson 21.4: ArcGIS Notebooks and Script Tools  (7 min)

**Objective:** Document analysis in notebooks and share scripts as tools.

*[ON SCREEN: Insert tab > New Notebook]*

On the Insert tab, click New Notebook. ArcGIS Notebooks are Jupyter notebooks inside your project, with ArcPy ready to use.

*[ON SCREEN: markdown cell and code cell]*

Mix explanation cells and code cells, and run them one at a time. Outputs added to the active map appear right away. Notebooks are a great way to keep a repeatable, documented analysis.

*[ON SCREEN: New > Script tool]*

To share a Python script with non-programmers, make it a script tool. Right-click your toolbox, New, Script. Define parameters on the Parameters tab, and paste your code on the Execution tab, reading inputs with arcpy.GetParameterAsText.

*[ON SCREEN: script tool dialog]*

Now your script looks and runs like any other geoprocessing tool.

#### Module quiz

1. In ModelBuilder, a variable marked P becomes…  
   **Answer:** A tool parameter users can set — Parameters appear on the model tool's dialog.

2. Which ArcPy object reads rows from a table one at a time?  
   **Answer:** arcpy.da.SearchCursor — SearchCursor iterates over rows and fields.

3. Which feature runs Jupyter notebooks inside ArcGIS Pro?  
   **Answer:** ArcGIS Notebooks — Insert > New Notebook opens a Jupyter notebook in the project.

## M22 — Arcade and Data Quality

### Lesson 22.1: Arcade Expressions for Pop-ups, Labels and Symbology  (7 min)

**Objective:** Write Arcade expressions that work across ArcGIS Pro and ArcGIS Online.

*[ON SCREEN: Arcade expression builder]*

Arcade is Esri's expression language. Write it once and it works in ArcGIS Pro, ArcGIS Online and mobile apps.

*[ON SCREEN: label expression]*

Reference fields with $feature. Round(($feature.POP / $feature.AREA_KM2), 1) + " people/km²" makes a tidy density label.

*[ON SCREEN: symbology expression with When]*

In Symbology, click the expression button next to the field to classify by a calculated value. When($feature.POP > 1000000, "Large", $feature.POP > 100000, "Medium", "Small") creates categories on the fly — no new field needed.

*[ON SCREEN: pop-up expression]*

In pop-ups, add Arcade expressions to show calculated values or friendlier text.

> **Tip:** Use Console() inside an expression to print values while you debug.

### Lesson 22.2: Topology and Geometry Checks  (7 min)

**Objective:** Find and fix spatial errors in your data.

*[ON SCREEN: Check Geometry tool]*

Start with Check Geometry. It lists problems like self-intersections, null geometry and bad ring order. Repair Geometry fixes most of them automatically.

*[ON SCREEN: Create Topology in a feature dataset]*

For rules between features, create a geodatabase topology inside a feature dataset. Add the participating feature classes and rules — parcels Must Not Overlap, Must Not Have Gaps, or roads Must Not Have Dangles.

*[ON SCREEN: Validate and Error Inspector]*

Validate the topology. Errors appear on the map, and the Error Inspector on the Edit tab lists them. Select an error to see fixes like Subtract or Merge, or mark true exceptions.

*[ON SCREEN: map topology]*

For quick shared-edge editing without a geodatabase topology, use map topology on the Edit tab.

#### Module quiz

1. In Arcade, how do you reference a field called POP?  
   **Answer:** $feature.POP — Arcade uses $feature to access the current feature's fields.

2. A topology rule "Must Not Overlap" finds…  
   **Answer:** Polygons in the same layer that overlap — Topology rules flag spatial errors like overlaps.

3. Which tool fixes problems like self-intersections?  
   **Answer:** Repair Geometry — Repair Geometry fixes invalid geometry found by Check Geometry.

## M23 — Sharing and Capstone Project

### Lesson 23.1: Publishing Web Layers and Web Maps  (7 min)

**Objective:** Share your work to ArcGIS Online or ArcGIS Enterprise.

*[ON SCREEN: Share tab > Web Layer > Publish Web Layer]*

Make sure you're signed in to your portal. Select a layer and click Web Layer, Publish Web Layer on the Share tab.

*[ON SCREEN: General tab: name, summary, tags, layer type]*

Give it a name, summary and tags. Choose Feature for interactive data or Tile for fast basemap-style display. Choose where to save it and who to share with.

*[ON SCREEN: Analyze, then Publish]*

Click Analyze. Fix errors; review warnings. Then Publish.

*[ON SCREEN: Share Web Map]*

To share a whole map with its layers and symbology, use Web Map. The map opens in ArcGIS Online Map Viewer, ready for dashboards, apps and StoryMaps.

> **Tip:** Use Overwrite Web Layer to update a published layer without breaking links.

### Lesson 23.2: Packages: Sharing Projects and Maps Offline  (5 min)

**Objective:** Bundle maps and data into a single shareable file.

*[ON SCREEN: Share tab > Package group]*

Packages bundle everything someone needs into one file. A map package (.mpkx) holds a map and its data. A project package (.ppkx) holds the whole project — maps, layouts, data, toolboxes.

*[ON SCREEN: Package Project dialog]*

Click Project Package, choose to save it to a file or upload it to your portal, fill in summary and tags, Analyze, and Package.

*[ON SCREEN: opening a package]*

Your colleague just double-clicks the package; ArcGIS Pro unpacks it with all paths working.

This is the reliable way to hand over a project — no more broken links.

### Lesson 23.3: Capstone: An End-to-End Site Selection Project  (10 min)

**Objective:** Combine skills from every level into one complete project.

*[ON SCREEN: brief: choose a site for a new clinic]*

Let's bring it all together. Our brief: choose the best site for a new health clinic.

*[ON SCREEN: geodatabase with inputs]*

Basics: create a project and a file geodatabase, add districts, roads, existing clinics, population and a DEM.

*[ON SCREEN: select and join]*

Intermediate: join population data to districts, calculate density, and use Select By Location to find districts more than 5 kilometres from any clinic.

*[ON SCREEN: service areas and suitability]*

Advanced: build 10-minute service areas for existing clinics, find underserved areas, compute slope, and run a weighted overlay favouring high density, gentle slope and road access.

*[ON SCREEN: ModelBuilder of the whole workflow]*

Wrap the workflow in a model so it can be rerun with new data.

*[ON SCREEN: final layout and web map]*

Finish with a print layout and a web map shared to your team.

Congratulations — you've gone from installing ArcGIS Pro to running a full spatial analysis project.

#### Module quiz

1. Which item lets you share data plus maps as one file?  
   **Answer:** A project or map package — Packages bundle data and maps for sharing.

2. Where do you publish a web layer?  
   **Answer:** Share tab — The Share tab holds web layer, web map and package options.

3. Before publishing, the Analyze step…  
   **Answer:** Reports errors and warnings to fix — Analyze checks the content for problems before sharing.

# ArcGIS · Online & Apps

## M24 — ArcGIS Online Essentials

### Lesson 24.1: Your ArcGIS Online Organization: Users, Roles and Credits  (6 min)

**Objective:** Understand how an ArcGIS Online organization, its users and its credits work.

*[ON SCREEN: sign in at arcgis.com, home page]*

ArcGIS Online is Esri's cloud platform for maps, apps and data. Sign in at arcgis.com with the same account you use in ArcGIS Pro.

*[ON SCREEN: Organization > Members]*

Your organization is the shared space for your team. Each member has a user type, which decides which apps they can use, and a role, which decides what they can do — Viewer, Data Editor, User, Publisher or Administrator.

*[ON SCREEN: Organization > Overview > Credits]*

Credits are ArcGIS Online's currency. Storing data, running analysis, geocoding and routing use credits; viewing maps doesn't. Administrators can set credit budgets per user.

*[ON SCREEN: app launcher]*

The app launcher at the top right opens every app you're licensed for: Map Viewer, Scene Viewer, StoryMaps, Dashboards, Experience Builder, Survey123, Field Maps and more.

> **Tip:** Ask your administrator which user type you have before planning a project; it decides which apps you can use.

### Lesson 24.2: Content, Items and Hosted Feature Layers  (7 min)

**Objective:** Upload data and manage items in My Content.

*[ON SCREEN: Content > My Content]*

Everything in ArcGIS Online is an item: web maps, layers, apps, files. They live in Content, My Content, organised in folders.

*[ON SCREEN: New item > drag a CSV]*

Click New item and drag in a CSV with addresses or coordinates, a zipped shapefile, a file geodatabase or a GeoJSON file. Choose to create a hosted feature layer, check the location fields, and click Next.

*[ON SCREEN: item details page]*

The item page is the item's home. Add a summary, description, tags and terms of use — good item details make your content findable and trustworthy.

*[ON SCREEN: Settings tab: Enable editing]*

On the Settings tab of a hosted feature layer you can enable editing, allow exports, turn on sync for offline use, and enable delete protection.

*[ON SCREEN: Data tab]*

The Data tab shows the table and fields, where you can add fields and calculate values online.

### Lesson 24.3: Making Web Maps in Map Viewer  (8 min)

**Objective:** Build a web map with styled layers and configured pop-ups.

*[ON SCREEN: Map Viewer, Add > Browse layers]*

Open Map Viewer from the app launcher. Click Add, Browse layers, and add your hosted layer or search Living Atlas.

*[ON SCREEN: Styles pane]*

Click Styles. Choose an attribute and Map Viewer suggests smart styles — Counts and Amounts, Types, Color and Size, Heat map, Dot density. It's the same thinking as symbology in ArcGIS Pro, with live suggestions.

*[ON SCREEN: Pop-ups pane]*

Click Pop-ups to choose fields, add text, charts, images and Arcade expressions.

*[ON SCREEN: Filter, Labels, Basemap]*

Add a filter, turn on labels, and choose a basemap.

*[ON SCREEN: Save as]*

Save the web map with a title, tags and summary. This web map is the building block for dashboards, story maps and apps.

> **Tip:** Use Review map to check your map's performance before sharing it widely.

### Lesson 24.4: Sharing, Groups and Scene Viewer  (6 min)

**Objective:** Share content safely and create 3D web scenes.

*[ON SCREEN: Share dialog]*

Every item starts private. Click Share to choose who can see it: only you, groups, your organization, or everyone. Sharing a map or app also asks to update the sharing of the layers inside it — say yes, or viewers will see blank maps.

*[ON SCREEN: Groups > Create group]*

Groups are the safest way to share with a team. Create a group, invite members, and share items to it. Shared update groups let members edit each other's items.

*[ON SCREEN: Scene Viewer]*

For 3D, open Scene Viewer. Add 3D buildings, trees and terrain, set lighting and daylight, and save a web scene. You can also publish scenes from ArcGIS Pro with Share, Web Layer.

*[ON SCREEN: Pro Portal tab]*

In ArcGIS Pro, the Catalog pane's Portal tab shows the same content, so you can open web maps and layers on your desktop.

#### Module quiz

1. What is a hosted feature layer?  
   **Answer:** Data stored in ArcGIS Online that you can query and edit — Hosted feature layers live in your organization's ArcGIS Online storage.

2. Which analysis tools in Map Viewer can consume credits?  
   **Answer:** Most analysis tools — Analysis, geocoding and routing use credits; viewing maps does not.

3. The best way to share content with a project team only is…  
   **Answer:** A group — Groups control who can see and use items.

## M25 — ArcGIS Living Atlas of the World

### Lesson 25.1: Finding and Using Living Atlas Content  (6 min)

**Objective:** Find authoritative data in Living Atlas and use it in your maps.

*[ON SCREEN: livingatlas.arcgis.com]*

ArcGIS Living Atlas of the World is a curated collection of maps, layers, imagery and apps from Esri and its partners: demographics, boundaries, land cover, weather, satellite imagery and much more.

*[ON SCREEN: Map Viewer > Add > Living Atlas]*

In Map Viewer, click Add, then switch the source to Living Atlas. Search "land cover" or "population" and add a layer in one click.

*[ON SCREEN: ArcGIS Pro Catalog > Portal > Living Atlas]*

In ArcGIS Pro, find the same content in the Catalog pane, Portal tab, Living Atlas.

*[ON SCREEN: item badges]*

Check the item page for the source, update frequency and badges. Subscriber content needs an organizational sign-in; premium content can also use credits.

> **Tip:** Live feeds like current weather and earthquakes update automatically — great for dashboards.

### Lesson 25.2: Basemaps and the Vector Tile Style Editor  (5 min)

**Objective:** Choose and customise basemaps for your brand.

*[ON SCREEN: Basemap gallery]*

Basemaps set the tone. Light and dark grey canvases make your data stand out. Imagery gives real-world context. Topographic and streets help orientation.

*[ON SCREEN: open a vector basemap in the Vector Tile Style Editor]*

Esri's vector basemaps can be restyled. Open one in the Vector Tile Style Editor, change colours for water, roads and land, hide layers you don't need, and save it as your own basemap.

*[ON SCREEN: Organization > Settings > Map: custom basemap gallery]*

Administrators can set a custom basemap gallery so everyone in the organization uses the same branded basemaps.

#### Module quiz

1. What is ArcGIS Living Atlas?  
   **Answer:** A curated collection of ready-to-use maps, layers and imagery — Living Atlas offers authoritative content from Esri and partners.

2. Some Living Atlas layers are marked as subscriber or premium. Premium content…  
   **Answer:** Can consume credits — Premium content needs an organizational account and may use credits.

3. A vector tile basemap can be restyled with…  
   **Answer:** The Vector Tile Style Editor — The style editor changes colours and labels of vector basemaps.

## M26 — ArcGIS StoryMaps

### Lesson 26.1: Building Your First Story  (8 min)

**Objective:** Create a story with text, media and maps.

*[ON SCREEN: StoryMaps home > New story]*

ArcGIS StoryMaps combines narrative text with maps, images, video and embedded content. From the app launcher, open StoryMaps and click New story. You can also start from a template, or import a PDF or Word document to get a draft.

*[ON SCREEN: cover and block palette]*

Add a title and cover image. Then use the plus button to add blocks: text, image, video, map, embed, button, timeline, infographic.

*[ON SCREEN: adding a web map, configuring map view]*

Add a map block, choose your web map, and set the exact extent, visible layers and pop-ups for that moment in the story.

*[ON SCREEN: Express map]*

For quick annotations, use an express map: draw points, routes and areas directly, with numbered places and pop-up images.

*[ON SCREEN: Design panel]*

In Design, choose a theme and fonts, or apply your organization's theme.

### Lesson 26.2: Immersive Blocks: Sidecar, Slideshow and Map Tour  (7 min)

**Objective:** Create scroll-driven, immersive storytelling sections.

*[ON SCREEN: insert Sidecar]*

Immersive blocks make stories cinematic. A sidecar keeps a map or image fixed on one side while text scrolls on the other. Each slide can change the map's extent and layers.

*[ON SCREEN: Docked vs floating layout]*

Choose docked or floating panel layouts; floating suits full-screen imagery.

*[ON SCREEN: Guided map tour]*

A map tour links a list of places with photos to points on a map — perfect for field trips, heritage trails and site visits. Choose a guided or explorer layout.

*[ON SCREEN: Swipe block]*

A swipe block compares two maps or images, like before-and-after a flood.

*[ON SCREEN: Outline drag-and-drop]*

Use the outline panel to reorder sections by dragging.

### Lesson 26.3: Collections, Briefings and Frames  (6 min)

**Objective:** Pick the right StoryMaps format for each audience.

*[ON SCREEN: Collection builder]*

A collection groups stories, maps, apps and files into one browsable experience — a portfolio or a course hub.

*[ON SCREEN: Briefing builder]*

A briefing is slide-based, built for presenting to decision-makers. Each slide has a layout with map, media and text, and briefings can be used offline in the ArcGIS StoryMaps Briefings app.

*[ON SCREEN: Frames on a phone]*

Frames is the newest format: short, mobile-first stories that work like social media posts, with embedded maps and apps.

*[ON SCREEN: Publish options]*

When you publish, choose the audience. Remember that the maps and layers in the story must be shared with the same audience.

#### Module quiz

1. In a story, an immersive block that keeps a map fixed while text scrolls past is a…  
   **Answer:** Sidecar — Sidecars pair a fixed media panel with scrolling narrative.

2. Which story type is designed for slide-style presentations?  
   **Answer:** Briefing — Briefings are slide-based stories built for presenting.

3. Express maps in StoryMaps are…  
   **Answer:** Simple maps you draw directly in the story — Express maps let you sketch points, lines and areas inside the builder.

## M27 — ArcGIS Dashboards

### Lesson 27.1: Creating a Dashboard  (7 min)

**Objective:** Build a dashboard from a web map with indicators, charts and lists.

*[ON SCREEN: Dashboards > Create dashboard]*

ArcGIS Dashboards shows key numbers, charts and maps on one screen for monitoring operations — incidents, assets, inspections, sales. From the app launcher, open Dashboards and click Create dashboard.

*[ON SCREEN: Add element > Map]*

Add a Map element and choose your web map. Then add an Indicator: pick the layer, choose Statistic — count or sum of a field — and set a title and icon.

*[ON SCREEN: Serial chart and Pie chart]*

Add a Serial chart to show values by category or over time, and a List for the latest records.

*[ON SCREEN: Layout: drag and dock elements]*

Drag elements to dock them into a grid. Use the Header for a title and logo, and the Sidebar for selectors.

> **Tip:** Set a refresh interval on layers that update often, so the dashboard stays current without reloading.

### Lesson 27.2: Interactivity: Selectors, Actions and Focus Mode  (7 min)

**Objective:** Make a dashboard respond to the user's choices.

*[ON SCREEN: Category selector in header]*

Selectors let viewers filter the dashboard. Add a category selector for district, a date selector for time period, or a number selector for thresholds.

*[ON SCREEN: Actions tab]*

On each element's Actions tab, choose what it controls. A selector filters the map, indicator and chart. A map extent change can filter the list to what's on screen. Clicking a chart bar can zoom the map.

*[ON SCREEN: Focus mode]*

Focus mode lets viewers expand one element to full screen for detail, then return.

*[ON SCREEN: Advanced formatting with Arcade]*

Use Advanced formatting with Arcade to colour indicators red or green based on targets.

### Lesson 27.3: Layout, Mobile Views and Sharing  (5 min)

**Objective:** Make dashboards readable on any screen and share them.

*[ON SCREEN: desktop vs phone preview]*

Dashboards adapt to screen size. Preview at tablet and phone widths and stack elements so the most important number shows first.

*[ON SCREEN: Theme settings]*

Choose a light or dark theme, set colours that match your brand, and keep charts consistent.

*[ON SCREEN: Share and embed]*

Share the dashboard to a group, the organization or the public, together with its web map and layers. Embed it in a StoryMap or a website with the URL.

> **Tip:** A good operations dashboard answers three questions in five seconds: what's happening, where, and is it getting better or worse?

#### Module quiz

1. A dashboard element that shows a single headline number is an…  
   **Answer:** Indicator — Indicators summarise one value, such as a count or sum.

2. Selectors in a dashboard…  
   **Answer:** Filter other elements based on a user's choice — Category, number and date selectors filter connected elements.

3. Map actions let a dashboard…  
   **Answer:** Filter charts and lists to the features in the map's extent — Actions link elements so they respond to each other.

## M28 — Experience Builder and Instant Apps

### Lesson 28.1: Your First Web App in Experience Builder  (8 min)

**Objective:** Build a responsive web app with widgets and pages.

*[ON SCREEN: Experience Builder > Create new > template gallery]*

Experience Builder is a drag-and-drop builder for web apps and websites. It replaced Web AppBuilder in ArcGIS Online. Open it, click Create new, and choose a template, such as Keystone, or a blank layout.

*[ON SCREEN: Insert panel: Map, List, Text, Legend, Search]*

Drag widgets onto the page: Map, Legend, Layer List, Search, List, Chart, Text, Button. Connect each data widget to your web map or layers.

*[ON SCREEN: Page panel, multiple pages and views]*

Use pages for separate screens — Home, Map, About — and views inside a section for tabs.

*[ON SCREEN: device preview: large, medium, small]*

Switch between large, medium and small screen layouts and arrange widgets for each.

*[ON SCREEN: Publish]*

Click Save, then Publish. Share the app item and its data with your audience.

### Lesson 28.2: Data, Actions and Interactive Widgets  (7 min)

**Objective:** Connect widgets so the app responds to users.

*[ON SCREEN: Data panel, add data and views]*

In the Data panel, add layers and create data views — filtered versions of a layer, such as "Open requests".

*[ON SCREEN: List widget bound to data]*

Configure a List to show features with their attributes. Format cards with text, images and buttons bound to fields.

*[ON SCREEN: Action tab: Record selection changes > Zoom to]*

On a widget's Action tab, set message actions: when a record is selected in the list, zoom the map to it and filter the chart.

*[ON SCREEN: Filter, Query, Edit, Near Me widgets]*

Add Filter, Query, Edit or Near Me widgets for richer tools. A QuickCapture widget can even bring field collection into the app.

### Lesson 28.3: ArcGIS Instant Apps  (5 min)

**Objective:** Build a focused app in minutes from a template.

*[ON SCREEN: Instant Apps gallery]*

ArcGIS Instant Apps are ready-made templates for common jobs. Pick one by purpose: Basic for simple maps, Sidebar for map plus details, Media Map, Nearby to find what's close, Category for browsing by type, Attachment Viewer for photos, Countdown, Chart Viewer and more.

*[ON SCREEN: Express setup vs full setup]*

Choose your web map, step through the express setup, and publish. Full setup offers more options like search, theme and interactivity.

*[ON SCREEN: comparison table: Instant Apps vs Experience Builder]*

Use Instant Apps for a quick, single-purpose app. Use Experience Builder when you need multiple pages, custom layouts or many connected widgets.

#### Module quiz

1. In Experience Builder, what links one widget to another, such as a list filtering a map?  
   **Answer:** Message actions — Widgets talk to each other through message actions.

2. When is an Instant App the better choice?  
   **Answer:** You need a focused app quickly with no layout design — Instant Apps are configurable templates for common jobs.

3. Which product replaced Web AppBuilder in ArcGIS Online?  
   **Answer:** Experience Builder (and Instant Apps) — Web AppBuilder was retired from ArcGIS Online; Experience Builder is its successor.

## M29 — Field Data Collection

### Lesson 29.1: ArcGIS Field Maps: Preparing Maps for the Field  (8 min)

**Objective:** Configure a web map for mobile data collection.

*[ON SCREEN: Field Maps Designer]*

ArcGIS Field Maps is Esri's main mobile app for viewing maps, collecting and editing data, and tracking location. Preparation happens in Field Maps Designer on the web.

*[ON SCREEN: hosted layer with editing enabled]*

Start with a web map whose layers have editing enabled.

*[ON SCREEN: Forms builder]*

In Designer, open Forms. Drag in fields, group them, add choice lists, mark fields required, set default values, and use Arcade for calculated values and conditional visibility.

*[ON SCREEN: Offline > add map area]*

On Offline, enable offline use and define map areas so crews can download data before going out of coverage.

*[ON SCREEN: Tasks]*

Use Tasks in Field Maps to assign work to mobile workers. Tasks replaces ArcGIS Workforce, which is being retired.

> **Tip:** Test your form on a phone before you send it to the field; a long form on a small screen is hard to use.

### Lesson 29.2: Collecting and Editing Data with Field Maps  (6 min)

**Objective:** Collect features, photos and offline edits on a mobile device.

*[ON SCREEN: phone: Field Maps map list]*

Sign in to the Field Maps app on iOS or Android. Your maps appear in the list. Tap one to open it, or download an offline area.

*[ON SCREEN: tap plus, choose layer, collect point at GPS location]*

Tap the plus button, choose a layer, and collect at your GPS location or a point on the map. Fill in the form, add photos, and submit.

*[ON SCREEN: streaming a line]*

For lines and polygons, add vertices by tapping or stream them while walking.

*[ON SCREEN: sync]*

Offline edits are saved on the device and sync when you reconnect.

*[ON SCREEN: location sharing]*

With location sharing turned on by an admin, supervisors can see where crews have been, for safety and reporting.

### Lesson 29.3: ArcGIS QuickCapture: High-Speed Data Collection  (5 min)

**Objective:** Design a QuickCapture project for one-tap collection.

*[ON SCREEN: QuickCapture web designer > Create project]*

ArcGIS QuickCapture is built for speed: big buttons that record a feature with one tap, ideal from a moving vehicle — road damage, wildlife sightings, debris after a storm.

*[ON SCREEN: buttons grid]*

Create a project from a feature layer. Each button records a feature type. Set colours, a grid layout and default attribute values for each button.

*[ON SCREEN: line button streaming]*

Line and polygon buttons can stream your GPS track while held on.

*[ON SCREEN: user input and photos]*

Add user inputs for values you type before tapping, and enable photos when needed.

> **Tip:** Pair QuickCapture for fast observation with Field Maps for detailed follow-up inspections.

### Lesson 29.4: ArcGIS Survey123: Forms and Surveys  (8 min)

**Objective:** Build smart forms with the web designer and Survey123 Connect.

*[ON SCREEN: Survey123 website > New survey > web designer]*

ArcGIS Survey123 is a form-centric app. On survey123.arcgis.com, create a survey in the web designer: drag in questions — single choice, number, date, image, signature, geopoint.

*[ON SCREEN: rules, required, default values]*

Add rules to show questions only when relevant, and set required answers. The Survey123 assistant can draft a survey from a description.

*[ON SCREEN: Survey123 Connect with XLSForm]*

For advanced surveys, use Survey123 Connect on the desktop. You design in an Excel spreadsheet called an XLSForm: calculations, repeats for multiple records, cascading selects and pulling data from existing layers.

*[ON SCREEN: Data tab, analyze, feature report]*

Publish, then share the survey link or QR code. Responses go into a hosted feature layer. The website's Analyze and Data tabs summarise results, and feature reports turn each response into a formatted PDF.

#### Module quiz

1. Where do you build forms and offline areas for ArcGIS Field Maps?  
   **Answer:** Field Maps Designer — Field Maps Designer configures forms, offline areas and tasks.

2. QuickCapture is best for…  
   **Answer:** Collecting data very quickly with big buttons, often while moving — QuickCapture is designed for one-tap, high-speed collection.

3. In Survey123, advanced logic like calculations and repeats is built with…  
   **Answer:** Survey123 Connect and XLSForm — Connect uses an Excel-based XLSForm for advanced surveys.

## M30 — ArcGIS Hub and Sharing with the Public

### Lesson 30.1: ArcGIS Hub Sites and Open Data  (7 min)

**Objective:** Build a public website with open data, maps and apps.

*[ON SCREEN: Hub home > Sites > Create site]*

ArcGIS Hub creates websites for sharing data, maps and apps with the public, and for engaging communities. Hub Basic is included with ArcGIS Online; Hub Premium adds engagement tools like events and discussions.

*[ON SCREEN: site editor: rows, cards]*

Create a site, choose a layout, and add cards: text, images, maps, charts, apps and a search bar for data.

*[ON SCREEN: content catalog]*

Add content to the site's catalog. Public items become searchable open data, with downloads in formats like CSV, shapefile, GeoJSON and KML, and API links for developers.

*[ON SCREEN: workspaces]*

Manage everything from your Hub workspaces.

*[ON SCREEN: custom domain, theme]*

Set a theme and a friendly site address that matches your organization.

#### Module quiz

1. ArcGIS Hub is mainly used for…  
   **Answer:** Public-facing sites, open data and community engagement — Hub builds sites and initiatives for engaging the public.

2. Open data published through a Hub site can be…  
   **Answer:** Downloaded in formats like CSV and shapefile — Hub provides downloads and APIs for shared data.

3. In Hub, which feature replaced classic edit mode?  
   **Answer:** Workspaces — Hub's workspaces replaced the retired classic edit mode.

## M31 — Web Analysis, Notebooks and Data Pipelines

### Lesson 31.1: Analysis Tools in Map Viewer  (7 min)

**Objective:** Run spatial analysis in the browser.

*[ON SCREEN: Map Viewer > Analysis button]*

Map Viewer has a full set of analysis tools — no desktop needed. Click Analysis, then Tools.

*[ON SCREEN: tool categories]*

Tools are grouped by question: Summarize data, Find locations, Use proximity — including Create buffers and Create drive-time areas — Enrich data, Analyze patterns and raster analysis.

*[ON SCREEN: Create drive-time areas, credit estimate]*

Run Create drive-time areas around clinics. Before running, Map Viewer estimates the credits. The result becomes a new hosted layer in your content.

*[ON SCREEN: ModelBuilder in Map Viewer]*

Chain tools with ModelBuilder in Map Viewer, and publish models as web tools so others can run them.

### Lesson 31.2: ArcGIS Notebooks and Data Pipelines  (7 min)

**Objective:** Automate web GIS with Python and no-code pipelines.

*[ON SCREEN: Notebook in ArcGIS Online]*

ArcGIS Notebooks run Python in the browser with the ArcGIS API for Python. Create one from the app launcher and connect with gis = GIS("home").

*[ON SCREEN: search content, update layer, schedule task]*

Script admin jobs: list inactive users, update a layer from an external source, or generate reports. Notebooks can run on a schedule as tasks.

*[ON SCREEN: Data Pipelines editor]*

Data Pipelines is a no-code alternative for data integration. Connect inputs — CSV and Parquet files, cloud storage, databases, or feature layers — then add tools like filter, join, calculate field, create buffers and find and replace, and output to a hosted feature layer.

*[ON SCREEN: schedule and email notifications]*

Schedule the pipeline to run daily and get an email when it finishes or fails.

#### Module quiz

1. Data Pipelines in ArcGIS Online are for…  
   **Answer:** Connecting, cleaning and loading data on a schedule without code — Data Pipelines is a no-code ETL tool.

2. ArcGIS Notebooks in ArcGIS Online run…  
   **Answer:** Python with the ArcGIS API for Python — Hosted notebooks run Python in the browser.

3. Before running a Map Viewer analysis tool you should check…  
   **Answer:** The estimated credits — Map Viewer shows a credit estimate before running.

## M32 — More of the ArcGIS System

### Lesson 32.1: ArcGIS Enterprise vs ArcGIS Online  (6 min)

**Objective:** Explain when an organization chooses ArcGIS Enterprise.

*[ON SCREEN: diagram: Online (SaaS) vs Enterprise (self-hosted)]*

ArcGIS Online is software as a service — Esri runs it for you. ArcGIS Enterprise is the same idea installed on your own servers or private cloud.

*[ON SCREEN: Enterprise components: Portal, Server, Data Store, Web Adaptor]*

Enterprise includes Portal for ArcGIS, ArcGIS Server, ArcGIS Data Store and a Web Adaptor. Most apps you've seen — Map Viewer, Dashboards, Experience Builder, StoryMaps, Survey123, Field Maps — also run in Enterprise.

*[ON SCREEN: reasons]*

Organizations choose Enterprise for data that must stay on their network, integration with in-house databases, or strict security rules. Many use both, sharing between them with distributed collaboration.

### Lesson 32.2: ArcGIS Earth, Urban, Business Analyst and Velocity  (7 min)

**Objective:** Know what other ArcGIS products do and when to use them.

*[ON SCREEN: ArcGIS Earth]*

ArcGIS Earth is a free 3D globe for desktop and mobile. Open KML, shapefiles and web layers, measure, and sketch — great for sharing 3D views with non-GIS colleagues.

*[ON SCREEN: ArcGIS Urban]*

ArcGIS Urban is for city planning in 3D: zoning, development projects and scenario comparisons.

*[ON SCREEN: ArcGIS Business Analyst Web App]*

ArcGIS Business Analyst combines demographic and spending data with analysis for site selection, market areas and infographic reports.

*[ON SCREEN: ArcGIS Velocity]*

ArcGIS Velocity ingests real-time feeds — vehicle locations, sensors, weather — analyses them as they stream, and triggers alerts.

*[ON SCREEN: ArcGIS Solutions gallery]*

ArcGIS Solutions deploys ready-made sets of maps, apps and workflows for local government, utilities, public safety and more, in a few clicks.

### Lesson 32.3: Building Your Own Apps with ArcGIS Maps SDKs  (5 min)

**Objective:** Understand the developer path in the ArcGIS system.

*[ON SCREEN: developers.arcgis.com]*

When configurable apps aren't enough, developers use the ArcGIS Maps SDKs. The Maps SDK for JavaScript builds web apps; native SDKs cover Kotlin, Swift, .NET, Qt and game engines.

*[ON SCREEN: short JavaScript snippet loading a web map by ID]*

Every web map and layer you made in this course can be loaded in code by its item ID, so the work in ArcGIS Online is reused directly.

*[ON SCREEN: Experience Builder Developer edition]*

Experience Builder Developer edition lets developers write custom widgets and host apps themselves — a bridge between no-code and full development.

#### Module quiz

1. ArcGIS Enterprise is…  
   **Answer:** Esri's software you run on your own infrastructure — Enterprise gives organizations a self-hosted portal and servers.

2. Which product is a free desktop globe for exploring 3D and KML?  
   **Answer:** ArcGIS Earth — ArcGIS Earth is a lightweight 3D globe viewer.

3. ArcGIS Velocity is designed for…  
   **Answer:** Real-time and big data from sensors and feeds — Velocity ingests and analyses streaming data.

## M33 — Capstone: From Field to Dashboard

### Lesson 33.1: Capstone: A Complete Field-to-Dashboard Workflow  (10 min)

**Objective:** Connect ArcGIS Pro, ArcGIS Online and the field apps in one project.

*[ON SCREEN: brief: city tree inventory]*

Our final project: a city tree inventory, from data model to public story.

*[ON SCREEN: ArcGIS Pro: geodatabase with domains, publish web layer]*

Step one, ArcGIS Pro: design a Trees feature class with species and condition domains, then publish it as a hosted feature layer with editing enabled.

*[ON SCREEN: Field Maps Designer form, QuickCapture project, Survey123 form]*

Step two, field apps: build a Field Maps form for inspectors, a QuickCapture project for fast street surveys, and a Survey123 form for residents to report damaged trees.

*[ON SCREEN: Dashboard with indicators and map]*

Step three, monitoring: a dashboard with total trees, trees in poor condition, and reports this week, filtered by district.

*[ON SCREEN: Experience Builder app and StoryMap]*

Step four, sharing: an Experience Builder app for city staff and a StoryMap explaining the urban forest to the public, with live maps from Living Atlas for context.

*[ON SCREEN: course recap]*

That's the whole ArcGIS system working together. Congratulations on completing the course!

#### Module quiz

1. In the capstone, where does field data from Survey123 and Field Maps end up?  
   **Answer:** A hosted feature layer — Both apps write to hosted feature layers in ArcGIS Online.

2. Which app shares the final results as a narrative for the public?  
   **Answer:** ArcGIS StoryMaps — StoryMaps tells the story with maps and media.

3. Why prepare the data model in ArcGIS Pro first?  
   **Answer:** To design fields, domains and layers once for every app — A good data model makes forms, dashboards and apps consistent.

# QGIS · Basics

## Q1 — Getting Started with QGIS

### Lesson Q1.1: What Is QGIS? Download and Install  (6 min)

**Objective:** Install QGIS and choose between the Long Term Release and the latest release.

*[ON SCREEN: qgis.org home page]*

QGIS is a free and open-source desktop GIS. It runs on Windows, macOS and Linux, it's used by governments, universities and companies worldwide, and there are no licence fees.

*[ON SCREEN: download page: LTR vs Latest]*

On qgis.org, open Download. You'll see two versions. The Long Term Release, or LTR, is the stable choice for everyday work and training. The latest release has the newest features but changes every four months. For this course, install the LTR.

*[ON SCREEN: QGIS 4 splash screen]*

QGIS 4 moved to a new graphics framework, Qt6. Day to day, the interface is very close to QGIS 3, so most tutorials still apply. Some older plugins need updating to work with QGIS 4.

*[ON SCREEN: Windows installer]*

On Windows, run the standalone installer and accept the defaults. On macOS, open the disk image and drag QGIS to Applications. On Linux, use your distribution's packages from qgis.org.

> **Tip:** You can install the LTR and the latest release side by side to try new features safely.

### Lesson Q1.2: A Tour of the QGIS Interface  (7 min)

**Objective:** Name the main parts of the QGIS window.

*[ON SCREEN: QGIS with a project open, regions highlighted]*

At the top is the menu bar: Project, Edit, View, Layer, Settings, Plugins, Vector, Raster, Database, Web, Mesh, Processing and Help. Below it are toolbars with the most-used tools.

*[ON SCREEN: Browser and Layers panels]*

On the left are two key panels. The Browser shows your folders, GeoPackages, databases and web services. The Layers panel lists what's on the map; drag layers to change drawing order.

*[ON SCREEN: map canvas]*

In the middle is the map canvas. Scroll to zoom, hold the mouse wheel to pan, or use the Pan tool.

*[ON SCREEN: status bar: coordinate, scale, magnifier, rotation, CRS button]*

The status bar shows the pointer coordinates, scale, magnifier, rotation and, at the far right, the project's coordinate reference system.

*[ON SCREEN: locator bar, type 'buffer']*

Bottom left is the locator bar. Press Ctrl+K and type the name of any tool, layer or setting to find it instantly.

*[ON SCREEN: View > Panels]*

Turn panels on and off from View, Panels, or by right-clicking any toolbar.

### Lesson Q1.3: Projects, Settings and Plugins at a Glance  (5 min)

**Objective:** Save projects safely and set useful options.

*[ON SCREEN: Project > Save As]*

Save your work with Project, Save As. QGIS projects use the .qgz extension. Like ArcGIS projects, a QGIS project points to data; it doesn't contain it.

*[ON SCREEN: Project > Properties > General > relative paths]*

In Project Properties, General, keep paths relative. That way you can move the project folder, or zip it for a colleague, without breaking links.

*[ON SCREEN: Settings > Options]*

Settings, Options holds application-wide preferences: default CRS for new projects, rendering, and the language of the interface.

*[ON SCREEN: Plugins > Manage and Install Plugins]*

Plugins add features. Plugins, Manage and Install Plugins opens the plugin manager; we'll install some favourites in the Advanced level.

> **Tip:** Keep data in the project folder with relative paths, then zip the folder to share a complete project.

#### Module quiz

1. Which QGIS version is recommended for production work?  
   **Answer:** The Long Term Release (LTR) — LTR versions get a year of bug fixes and are built for stability.

2. What file extension does a QGIS project use?  
   **Answer:** .qgz — QGIS saves projects as .qgz (a zipped .qgs).

3. Which panel lets you browse folders, databases and web services?  
   **Answer:** Browser — The Browser panel works like a file explorer for spatial data.

## Q2 — Adding Data and Coordinate Systems

### Lesson Q2.1: Adding Vector and Raster Layers  (6 min)

**Objective:** Load spatial data with the Browser and the Data Source Manager.

*[ON SCREEN: drag a GeoPackage layer from Browser to canvas]*

The quickest way to add data is to drag it from the Browser panel onto the map.

*[ON SCREEN: Layer > Data Source Manager]*

For more control, open the Data Source Manager with Ctrl+L. Tabs on the left cover Vector, Raster, Delimited Text, GeoPackage, PostgreSQL, XYZ, WMS and more.

*[ON SCREEN: Vector tab: browse to shapefile]*

On the Vector tab, browse to a shapefile, GeoJSON or KML and click Add.

*[ON SCREEN: GeoPackage in Browser]*

QGIS's recommended format is GeoPackage, a single .gpkg file that can hold many vector and raster layers, with long field names and no 2 GB limit.

*[ON SCREEN: Raster tab: GeoTIFF]*

Rasters like GeoTIFF elevation models and satellite images are added on the Raster tab.

> **Tip:** Right-click a layer and choose Export, Save Features As, to convert shapefiles into a GeoPackage.

### Lesson Q2.2: Basemaps, CSV Files and Web Services  (6 min)

**Objective:** Add basemaps, point data from spreadsheets, and web map services.

*[ON SCREEN: Browser > XYZ Tiles > OpenStreetMap]*

In the Browser, expand XYZ Tiles and double-click OpenStreetMap to add a basemap. Add more tile services by right-clicking XYZ Tiles, New Connection.

*[ON SCREEN: QuickMapServices plugin menu]*

The QuickMapServices plugin adds a menu of popular basemaps in one click.

*[ON SCREEN: Data Source Manager > Delimited Text]*

To map a CSV of coordinates, use Delimited Text. Pick the file, check the delimiter, choose Point coordinates, set the X field to longitude and the Y field to latitude, and set the CRS — usually EPSG:4326.

*[ON SCREEN: WMS/WFS connection]*

Add web services from WMS and WFS servers, such as national mapping agencies, with a new connection on the WMS/WMTS or WFS tab.

### Lesson Q2.3: Coordinate Reference Systems in QGIS  (7 min)

**Objective:** Manage the project CRS and fix or convert layer CRSs.

*[ON SCREEN: CRS button in status bar]*

Every project has a CRS, shown at the bottom right. QGIS reprojects layers on the fly, so different layers line up on screen.

*[ON SCREEN: Project Properties > CRS, search EPSG]*

Click the CRS button to change it. Search by name or EPSG code — 4326 for WGS 84, 3857 for web maps, or a UTM zone for measuring.

*[ON SCREEN: Layer Properties > Source > Assigned CRS]*

Each layer has its own CRS. If a layer's CRS is wrong but its coordinates are fine, fix it with Set Layer CRS. This is like Define Projection in ArcGIS.

*[ON SCREEN: Processing > Reproject layer]*

To convert the coordinates into a new CRS and save a new file, use Reproject Layer in the Processing Toolbox — like Project in ArcGIS.

*[ON SCREEN: datum transformation dialog]*

When layers use different datums, QGIS may ask which transformation to use. Pick the one with the best accuracy for your area.

#### Module quiz

1. Which format is QGIS's recommended default for vector data?  
   **Answer:** GeoPackage — GeoPackage stores many layers in one file without shapefile limits.

2. How do you add an OpenStreetMap basemap without a plugin?  
   **Answer:** XYZ Tiles in the Browser — QGIS ships with an OpenStreetMap XYZ tile connection.

3. The coordinates are fine but the layer has the wrong CRS assigned. What do you use?  
   **Answer:** Set layer CRS — Setting the CRS fixes the label; reprojecting changes the coordinates.

## Q3 — Styling and Labeling

### Lesson Q3.1: Symbology Basics and the Layer Styling Panel  (7 min)

**Objective:** Style layers with single symbols and the Layer Styling panel.

*[ON SCREEN: double-click layer > Symbology]*

Double-click a layer to open Layer Properties, then Symbology. Or press F7 to open the Layer Styling panel, which applies changes as you make them.

*[ON SCREEN: renderer drop-down]*

The renderer drop-down lists the methods: Single Symbol, Categorized, Graduated, Rule-based, and for points, Point Cluster, Point Displacement and Heatmap. Polygons also offer Inverted Polygons and 2.5D.

*[ON SCREEN: Single symbol: fill, stroke]*

With Single Symbol, click the symbol layer to set fill colour, stroke colour and width. Add symbol layers with the plus button to build richer symbols, such as a dashed outline over a soft fill.

*[ON SCREEN: data-defined override button]*

The small button next to most settings is a data-defined override. It lets a field or expression control size, colour or rotation — like Vary symbology by attribute in ArcGIS.

*[ON SCREEN: Style > Save Style]*

Save a style as a .qml file, or to the GeoPackage, to reuse it later.

### Lesson Q3.2: Categorized, Graduated and Rule-based Styles  (8 min)

**Objective:** Map categories and quantities and build custom rules.

*[ON SCREEN: Categorized on land use]*

Categorized gives each unique value a symbol. Choose the field, pick a colour ramp and click Classify.

*[ON SCREEN: Graduated on population density]*

Graduated classifies numbers. Choose the value — you can type an expression like "POP" / $area to normalise — pick the mode: Equal Count (Quantile), Equal Interval, Natural Breaks (Jenks), Standard Deviation or Pretty Breaks, set the number of classes and click Classify. Switch the method from Color to Size for graduated symbols.

*[ON SCREEN: Histogram tab]*

The Histogram tab shows the data distribution and your class breaks.

*[ON SCREEN: Rule-based]*

Rule-based styling uses expressions you write: one rule for "type" = 'motorway', another for primary roads, each with its own symbol and scale range.

*[ON SCREEN: Point cluster and heatmap]*

For dense points, try Point Cluster or Heatmap renderers.

### Lesson Q3.3: Labels and Expressions  (6 min)

**Objective:** Add clear, well-placed labels.

*[ON SCREEN: Layer Properties > Labels > Single Labels]*

Open Layer Properties, Labels, and choose Single Labels. Pick the field to label with.

*[ON SCREEN: expression builder: "NAME" || '\n' || "POP"]*

Click the expression button to combine fields. "NAME" || '\n' || format_number("POP", 0) shows the name with population below.

*[ON SCREEN: Text, Buffer, Placement tabs]*

Use the Text tab for font and size, Buffer for a halo that keeps labels readable, and Placement for positions: around the point, along lines, or inside polygons.

*[ON SCREEN: Rule-based labeling]*

Choose Rule-based Labeling to label large cities larger than small towns, each with its own scale range.

*[ON SCREEN: Rendering tab: show all labels, priority]*

In Rendering, set priority and whether labels may overlap.

#### Module quiz

1. Which renderer gives each category its own colour?  
   **Answer:** Categorized — Categorized symbology assigns a symbol per unique value.

2. Which panel lets you style layers live without opening the properties dialog?  
   **Answer:** Layer Styling panel (F7) — The Layer Styling panel applies changes instantly.

3. Rule-based styling lets you…  
   **Answer:** Style features with your own expressions and scale ranges — Rules combine filters, symbols and visibility ranges.

## Q4 — Print Layouts

### Lesson Q4.1: Creating a Print Layout  (8 min)

**Objective:** Design a map page with legend, scale bar and north arrow.

*[ON SCREEN: Project > New Print Layout]*

Click Project, New Print Layout, and give it a name. The layout designer opens in its own window.

*[ON SCREEN: right-click page > Page Properties]*

Right-click the page to set the size and orientation, such as A4 landscape.

*[ON SCREEN: Add Map tool, drag rectangle]*

Use Add Map and drag a rectangle. In Item Properties set an exact scale, and use the Move Item Content tool to pan the map inside the frame.

*[ON SCREEN: Add Legend, Scale Bar, North Arrow, Label]*

Add a Legend — untick Auto update to rename or remove entries — a Scale Bar with sensible units, a North Arrow, and a Label for the title. Labels can include expressions like the current date.

*[ON SCREEN: Align and Distribute tools]*

Use the alignment tools and guides to line things up.

### Lesson Q4.2: Atlas and Exporting  (6 min)

**Objective:** Produce a map book automatically and export it.

*[ON SCREEN: Atlas panel: Generate an atlas]*

An atlas makes one page per feature in a coverage layer — one map per district, for example. Open the Atlas panel, tick Generate an atlas and choose the coverage layer and page name.

*[ON SCREEN: map item: Controlled by Atlas]*

On the map item, tick Controlled by Atlas so it zooms to each feature. Add a label with the expression [% @atlas_pagename %] for page titles.

*[ON SCREEN: Atlas toolbar preview]*

Turn on Preview Atlas and step through the pages.

*[ON SCREEN: Export as PDF, Image, SVG]*

Export the layout as PDF for print, PNG for slides, or SVG for editing in design software. Atlases export as one PDF or one file per page.

#### Module quiz

1. Which feature creates one map page per feature of a coverage layer?  
   **Answer:** Atlas — Atlas generates a page for each feature.

2. How do you change what part of the map shows inside a layout map item?  
   **Answer:** Move Item Content tool — Move Item Content pans the map inside the frame.

3. Which export keeps vector quality for print?  
   **Answer:** PDF or SVG — PDF and SVG keep vectors sharp.

# QGIS · Intermediate

## Q5 — Attribute Data and Expressions

### Lesson Q5.1: The Attribute Table and Selecting Features  (6 min)

**Objective:** Explore attributes and select features by expression.

*[ON SCREEN: right-click layer > Open Attribute Table (F6)]*

Open the attribute table with F6. Each row is a feature. Click a row number to select it; the feature turns yellow on the map.

*[ON SCREEN: Show Selected Features filter]*

The menu at the bottom left switches between all features, selected features and features visible on the map.

*[ON SCREEN: Select Features Using an Expression]*

Click Select Features Using an Expression (Ctrl+F3) and write "POP" > 100000 AND "TYPE" = 'City'.

*[ON SCREEN: Layer > Filter]*

To hide non-matching features entirely, use a filter: right-click the layer, Filter. It's like a definition query in ArcGIS.

*[ON SCREEN: Statistics panel]*

The Statistics panel gives count, sum, mean and more for any field.

### Lesson Q5.2: The Field Calculator and Expressions  (7 min)

**Objective:** Create and update fields with QGIS expressions.

*[ON SCREEN: Field Calculator]*

Open the Field Calculator (Ctrl+I). Create a new field or update an existing one, and write an expression.

*[ON SCREEN: $area / 1000000]*

Geometry functions are built in: $area for area, $length for length, $x and $y for point coordinates. "POP" / ($area / 1000000) gives density per square kilometre in a projected CRS.

*[ON SCREEN: CASE WHEN expression]*

For conditions use CASE: CASE WHEN "DENSITY" > 1000 THEN 'High' ELSE 'Low' END.

*[ON SCREEN: Create virtual field checkbox]*

Tick Create virtual field to make a field that updates automatically whenever the data changes.

*[ON SCREEN: function list with help]*

The function list on the right explains every function with examples — the same expressions work in labels, styles and layouts.

### Lesson Q5.3: Table Joins and Spatial Joins  (6 min)

**Objective:** Combine data by a common field or by location.

*[ON SCREEN: Layer Properties > Joins > plus]*

To join a table by a shared field, open Layer Properties, Joins, click plus, and choose the join layer, join field and target field. The join is live and temporary.

*[ON SCREEN: Join attributes by field value]*

To create a permanent new layer, use Join Attributes by Field Value in the Processing Toolbox.

*[ON SCREEN: Join attributes by location]*

Join Attributes by Location adds attributes based on where features are — for example, add the district name to every school.

*[ON SCREEN: Count points in polygon]*

For counts, Count Points in Polygon adds a field with the number of points inside each polygon.

#### Module quiz

1. Which keyboard shortcut opens the Field Calculator?  
   **Answer:** Ctrl+I — Ctrl+I opens the Field Calculator when a layer is selected.

2. A virtual field…  
   **Answer:** Is recalculated automatically and not stored in the data — Virtual fields live in the project and update when data changes.

3. Which tool joins attributes from polygons to the points inside them?  
   **Answer:** Join attributes by location — Spatial joins match features by location.

## Q6 — Editing and Digitizing

### Lesson Q6.1: Digitizing Features with Snapping  (7 min)

**Objective:** Create and reshape features precisely.

*[ON SCREEN: Layer > Create Layer > New GeoPackage Layer]*

Create a new layer with Layer, Create Layer, New GeoPackage Layer. Choose geometry type, CRS and fields.

*[ON SCREEN: Toggle Editing pencil, Add Polygon Feature]*

Select the layer and click Toggle Editing. Click Add Polygon Feature, left-click to add vertices, and right-click to finish. Fill in the attributes form.

*[ON SCREEN: Snapping toolbar]*

Turn on snapping from the Snapping toolbar so new features meet existing ones. Enable tracing to follow existing edges, and Avoid overlap to prevent gaps and overlaps between polygons.

*[ON SCREEN: Vertex Tool]*

Use the Vertex Tool to move, add or delete vertices. The Advanced Digitizing panel lets you enter exact distances and angles.

*[ON SCREEN: Save Layer Edits]*

Click Save Layer Edits often, and Toggle Editing again when you're done.

### Lesson Q6.2: Attribute Forms and Widgets  (6 min)

**Objective:** Build easy, error-free data entry forms.

*[ON SCREEN: Layer Properties > Attributes Form]*

Open Layer Properties, Attributes Form. Each field has a widget that controls how it's edited.

*[ON SCREEN: Value Map widget]*

Use Value Map for a drop-down list of allowed values, Range for numbers within limits, Date/Time for a calendar, and Attachment for photos.

*[ON SCREEN: Drag and Drop Designer]*

Switch to the Drag and Drop Designer to group fields into tabs and sections.

*[ON SCREEN: Constraints and Defaults]*

Set constraints, like not null, and default values, like now() for the date. These forms also travel to QField on mobile.

#### Module quiz

1. What must you do before you can edit a layer?  
   **Answer:** Toggle Editing — The pencil icon puts a layer into edit mode.

2. Which tool moves, adds and deletes individual vertices?  
   **Answer:** Vertex Tool — The Vertex Tool edits feature geometry vertex by vertex.

3. Value Map in the attribute form…  
   **Answer:** Shows a drop-down list of allowed values — Widgets like Value Map control how fields are edited.

## Q7 — Processing and Vector Analysis

### Lesson Q7.1: The Processing Toolbox and Batch Processing  (6 min)

**Objective:** Find, run and repeat geoprocessing algorithms.

*[ON SCREEN: Processing > Toolbox]*

The Processing Toolbox (Ctrl+Alt+T) holds hundreds of algorithms from QGIS, GDAL and GRASS. Search by name at the top.

*[ON SCREEN: tool dialog with Run button]*

Open a tool, set inputs and parameters, and choose to save the output to a file or keep a temporary layer. Click Run.

*[ON SCREEN: Run as Batch Process]*

Click Run as Batch Process to run the same tool on many inputs, filling the table with Autofill.

*[ON SCREEN: Processing > History]*

Processing History records every run, so you can reopen a tool with the same settings.

> **Tip:** Edit in place lets some tools, like Buffer, change features directly in an editable layer.

### Lesson Q7.2: Overlay Analysis: Buffer, Clip, Intersection and Dissolve  (8 min)

**Objective:** Answer proximity and overlap questions with vector tools.

*[ON SCREEN: Vector > Geoprocessing Tools menu]*

The classic overlay tools are in Vector, Geoprocessing Tools, and in the Processing Toolbox.

*[ON SCREEN: Buffer 500 m, dissolve result]*

Buffer creates zones around features. Use a projected CRS so the distance is in metres, and tick Dissolve result to merge overlaps.

*[ON SCREEN: Clip]*

Clip keeps the parts of the input inside the overlay layer — roads within a city.

*[ON SCREEN: Intersection and Union]*

Intersection keeps only overlapping areas, combining attributes from both layers. Union keeps everything, split where they overlap. Difference removes the overlay area from the input.

*[ON SCREEN: Dissolve by field]*

Dissolve merges features that share a value, like districts into provinces.

> **Tip:** Use Fix Geometries first if a tool reports invalid geometry.

#### Module quiz

1. Which shortcut opens the Processing Toolbox?  
   **Answer:** Ctrl+Alt+T — Ctrl+Alt+T toggles the Processing Toolbox panel.

2. Which tool keeps only the parts of a layer inside another layer?  
   **Answer:** Clip — Clip cuts an input to the overlay layer's extent.

3. How can you run one tool on many files at once?  
   **Answer:** Run as Batch Process — Batch processing runs a tool over a list of inputs.

## Q8 — Georeferencing and Spatial Databases

### Lesson Q8.1: Georeferencing Scanned Maps  (7 min)

**Objective:** Place a scanned map in its real-world location with the Georeferencer.

*[ON SCREEN: Layer > Georeferencer]*

Open Layer, Georeferencer, and add your scanned map with Open Raster.

*[ON SCREEN: Add Point, From Map Canvas]*

Click Add Point, click a recognisable spot on the scan, then choose From Map Canvas and click the same spot on a basemap in the main window. Add at least four well-spread ground control points.

*[ON SCREEN: Transformation Settings]*

In Transformation Settings, choose the transformation type — Polynomial 1 for most scans, Thin Plate Spline for distorted ones — the target CRS, the resampling method and the output file.

*[ON SCREEN: GCP table residuals]*

Check the residuals in the GCP table and remove points with large errors.

*[ON SCREEN: Start Georeferencing]*

Click Start Georeferencing. The new GeoTIFF is added to your map.

### Lesson Q8.2: GeoPackage, PostGIS and DB Manager  (6 min)

**Objective:** Store data in databases and query it with SQL.

*[ON SCREEN: GeoPackage with many layers]*

GeoPackage is perfect for single users and sharing: one file, many layers, styles saved inside.

*[ON SCREEN: Browser > PostgreSQL > New Connection]*

For teams and large data, use PostgreSQL with PostGIS. Create a connection in the Browser with host, port, database and credentials. Drag layers in to import them.

*[ON SCREEN: Database > DB Manager > SQL Window]*

Database, DB Manager lets you browse databases and run SQL. SELECT name, ST_Area(geom) FROM parcels returns areas, and Load as new layer puts the result on the map.

*[ON SCREEN: Execute SQL in Processing]*

Execute SQL in the Processing Toolbox runs SQL against any layer, even shapefiles.

#### Module quiz

1. Where is the Georeferencer in QGIS 4?  
   **Answer:** Layer menu — The Georeferencer is under the Layer menu.

2. Which database extension adds spatial types to PostgreSQL?  
   **Answer:** PostGIS — PostGIS adds geometry and spatial functions to PostgreSQL.

3. In the Georeferencer, GCP stands for…  
   **Answer:** Ground control point — GCPs link image positions to map coordinates.

# QGIS · Advanced

## Q9 — Raster Analysis

### Lesson Q9.1: Terrain Analysis: Hillshade, Slope and Contours  (7 min)

**Objective:** Derive terrain products from a DEM.

*[ON SCREEN: DEM with Singleband pseudocolor]*

Load a DEM and style it with Singleband pseudocolor for elevation colours.

*[ON SCREEN: Raster > Analysis > Hillshade]*

Raster, Analysis, Hillshade creates shaded relief. Set the Z factor if the elevation units differ from the horizontal units. Put the hillshade under a semi-transparent DEM.

*[ON SCREEN: Slope and Aspect]*

Slope and Aspect are in the same menu.

*[ON SCREEN: Raster > Extraction > Contour]*

Raster, Extraction, Contour creates contour lines at an interval you choose, with an elevation field for labels.

*[ON SCREEN: hillshade renderer in Symbology]*

For a quick look without new files, choose the Hillshade renderer in the layer's symbology.

### Lesson Q9.2: Raster Calculator, Reclassify and Zonal Statistics  (7 min)

**Objective:** Combine and summarise rasters.

*[ON SCREEN: Raster > Raster Calculator]*

The Raster Calculator does cell-by-cell maths. Reference bands as "dem@1". ("dem@1" > 1000) * 1 marks cells above 1,000 metres.

*[ON SCREEN: NDVI expression]*

For NDVI: ("nir@1" - "red@1") / ("nir@1" + "red@1").

*[ON SCREEN: Reclassify by table]*

Reclassify by Table turns value ranges into classes for suitability scoring.

*[ON SCREEN: Clip raster by mask layer]*

Clip Raster by Mask Layer cuts a raster to a polygon boundary.

*[ON SCREEN: Zonal statistics]*

Zonal Statistics adds mean, sum, min or max of a raster to each polygon — average elevation per district, for example.

### Lesson Q9.3: Land Cover Classification with the SCP Plugin  (8 min)

**Objective:** Classify satellite imagery with the Semi-Automatic Classification Plugin.

*[ON SCREEN: install Semi-Automatic Classification Plugin]*

Install the Semi-Automatic Classification Plugin from the plugin manager. Check that the version supports your QGIS release.

*[ON SCREEN: SCP Download products]*

SCP can search and download Sentinel-2 and Landsat imagery, and pre-process it with atmospheric correction.

*[ON SCREEN: Band set]*

Create a band set of the bands you want to use.

*[ON SCREEN: training input: draw ROIs]*

Create a training input and draw regions of interest for each class: water, vegetation, built-up, bare soil.

*[ON SCREEN: classification algorithm and output]*

Choose an algorithm such as Random Forest or Maximum Likelihood, preview, then run the classification. Use the accuracy tool with reference points to check results.

#### Module quiz

1. Which tool sums raster values inside each polygon?  
   **Answer:** Zonal statistics — Zonal statistics summarises a raster within polygons.

2. The Semi-Automatic Classification Plugin is used for…  
   **Answer:** Land cover classification of satellite imagery — SCP downloads and classifies remote-sensing imagery.

3. Raster Calculator expressions refer to bands as…  
   **Answer:** "layer@band" — For example "dem@1" is band 1 of the dem layer.

## Q10 — Automation: Graphical Modeler and PyQGIS

### Lesson Q10.1: The Graphical Modeler  (7 min)

**Objective:** Build reusable workflows without code.

*[ON SCREEN: Processing > Graphical Modeler]*

Open Processing, Graphical Modeler. It's QGIS's equivalent of ModelBuilder.

*[ON SCREEN: Inputs tab: Vector Layer, Number]*

From the Inputs tab, drag in inputs like a vector layer and a number for buffer distance.

*[ON SCREEN: Algorithms tab: Buffer then Clip]*

From the Algorithms tab, add Buffer and connect it to the inputs, then Clip using the buffer output. Name the final output.

*[ON SCREEN: Run model, Save]*

Run the model to test it, then save it. It appears in the Processing Toolbox under Models, where you can run it like any tool — even in batch mode.

*[ON SCREEN: Export as Python script]*

You can export the model as a Python script.

### Lesson Q10.2: PyQGIS: The Python Console and Scripts  (8 min)

**Objective:** Automate QGIS with Python.

*[ON SCREEN: Plugins > Python Console]*

Open the Python Console with Ctrl+Alt+P.

*[ON SCREEN: layer = iface.activeLayer()]*

iface gives you the interface. layer = iface.activeLayer() grabs the selected layer, and layer.featureCount() counts its features.

*[ON SCREEN: for f in layer.getFeatures(): print(f["NAME"])]*

Loop through features with layer.getFeatures() and read attributes by field name.

*[ON SCREEN: processing.run("native:buffer", {...})]*

Run any tool with processing.run, passing the algorithm ID and a dictionary of parameters. Find the exact call in Processing History or the tool dialog's Advanced, Copy as Python Command.

*[ON SCREEN: Show Editor, save script]*

Click Show Editor to write longer scripts and save them as .py files.

#### Module quiz

1. What file extension do Graphical Modeler models use?  
   **Answer:** .model3 — Models are saved as .model3 files.

2. Which object gives you access to the QGIS interface in the Python Console?  
   **Answer:** iface — iface is the QgisInterface instance.

3. How do you run a Processing algorithm from Python?  
   **Answer:** processing.run() — processing.run takes the algorithm ID and a parameter dictionary.

## Q11 — Plugins, 3D, Field and Web

### Lesson Q11.1: Essential Plugins  (6 min)

**Objective:** Extend QGIS with the most useful plugins.

*[ON SCREEN: Plugins > Manage and Install Plugins > All]*

Open the plugin manager and search. Check each plugin's page for ratings, last update and QGIS 4 compatibility.

*[ON SCREEN: QuickOSM query]*

QuickOSM downloads OpenStreetMap data — for example all hospitals in a city — as a layer.

*[ON SCREEN: QuickMapServices]*

QuickMapServices adds dozens of basemaps.

*[ON SCREEN: DataPlotly charts]*

DataPlotly creates interactive charts from layer attributes, linked to selections.

*[ON SCREEN: MMQGIS and others]*

Other favourites include MMQGIS for geocoding and data tools, and qgis2web for web maps.

### Lesson Q11.2: 3D Maps and Elevation Profiles  (7 min)

**Objective:** Visualise terrain and buildings in 3D.

*[ON SCREEN: View > 3D Map Views > New 3D Map View]*

Open View, 3D Map Views, New 3D Map View. A 3D window docks beside the map.

*[ON SCREEN: Project Properties > Terrain / Elevation]*

Set the terrain: choose a DEM as the elevation source so the map drapes over real topography. Adjust vertical exaggeration.

*[ON SCREEN: Layer Properties > 3D View: extrude buildings]*

For buildings, open Layer Properties, 3D View, choose Single symbol and set extrusion to a height field.

*[ON SCREEN: point cloud LAZ]*

QGIS also displays lidar point clouds in LAS, LAZ and COPC formats, in 2D and 3D.

*[ON SCREEN: View > Elevation Profile]*

The Elevation Profile tool draws a cross-section along a line you draw, from DEMs, point clouds and 3D layers.

*[ON SCREEN: animation keyframes]*

Create camera animations in the 3D view and export frames for video.

### Lesson Q11.3: Field Data Collection with QField  (6 min)

**Objective:** Take a QGIS project into the field with QField.

*[ON SCREEN: QField app on a phone]*

QField is a free mobile app for Android and iOS that opens QGIS projects, with your styles and forms.

*[ON SCREEN: install QFieldSync plugin]*

Install the QFieldSync plugin. Configure each layer: offline editing, copy, or keep as is.

*[ON SCREEN: QFieldCloud sync]*

Package the project for QField, copy it to the device, or use QFieldCloud to sync over the internet.

*[ON SCREEN: collecting a point with photo]*

In the field, collect points, lines and polygons with GPS, fill your attribute forms, and take photos.

*[ON SCREEN: synchronise back]*

Back in the office, synchronise to bring the edits into your QGIS project.

### Lesson Q11.4: Publishing Web Maps  (6 min)

**Objective:** Share QGIS maps on the web.

*[ON SCREEN: Web > qgis2web > Create web map]*

The qgis2web plugin exports your project as a Leaflet or OpenLayers web page, with styles, pop-ups and a layer list. Preview, then export a folder you can host anywhere — even GitHub Pages.

*[ON SCREEN: QGIS Server diagram]*

QGIS Server publishes projects as standard OGC services — WMS, WFS and OGC API Features — so other apps can use them. It runs on a web server and uses your .qgz project directly.

*[ON SCREEN: Project Properties > QGIS Server tab]*

Configure published layers and service metadata in Project Properties, QGIS Server.

*[ON SCREEN: QGIS course recap]*

That wraps up the QGIS track: from installation to databases, automation, 3D, field work and web publishing.

#### Module quiz

1. Which mobile app works with QGIS projects for field data collection?  
   **Answer:** QField — QField opens QGIS projects on Android and iOS.

2. Which plugin exports a QGIS map to a Leaflet or OpenLayers web page?  
   **Answer:** qgis2web — qgis2web generates a static web map.

3. Where do you open a 3D view of the project?  
   **Answer:** View > 3D Map Views — 3D map views show terrain and extruded features.

# gIQ (Space42)

## G1 — Getting Started with gIQ

### Lesson G1.1: What Is gIQ? The Platform at a Glance  (6 min)

**Objective:** Explain what gIQ does and how data flows through the platform.

*[ON SCREEN: giq.ae home page]*

gIQ is a cloud-based geospatial intelligence platform from Space42. It brings together satellite imagery acquisition, AI models, a 3D globe, collaborative workspaces, reports and a marketplace in one browser-based system.

*[ON SCREEN: who it's for: planners, environmental scientists, GIS professionals, decision-makers]*

It's designed for urban planners, environmental scientists, GIS professionals and decision-makers.

*[ON SCREEN: platform flow diagram]*

Data comes in three ways: uploads through File Manager, imagery from the Acquire module, and results from analytical jobs. Everything passes through Ingestion, where it's processed, validated and stored.

*[ON SCREEN: Explore, File Manager, Workspace branches]*

From there you can examine it in Explore, organise it in File Manager, or analyse it in a Workspace. AI models produce detections, inference turns them into insights, and you share findings as reports and stories.

> **Tip:** Keep the official documentation at docs.giq.ae open while you learn; module names in this course follow it.

### Lesson G1.2: Logging In, Roles and Navigation  (6 min)

**Objective:** Sign in to gIQ and understand how roles shape what you see.

*[ON SCREEN: gIQ login page]*

Open the platform URL in an up-to-date Chrome or Edge browser. Sign in with your username and password, or with UAE Pass using your Emirates ID, email or phone number. On your first login, you'll be asked to change the password your admin sent you.

*[ON SCREEN: Signup as Guest]*

If you don't have an account, Signup as Guest gives limited access after you verify your email.

*[ON SCREEN: navigation panel with modules]*

The navigation panel lists modules: Globes, Collaborate, Data, Acquire, AI, Market and more. Which ones you see depends on the platform version, your role, and the permissions assigned to it.

*[ON SCREEN: Profile menu]*

The profile menu shows your profile and permissions; admins also reach users, roles and settings from here.

*[ON SCREEN: Help, Notifications, AI Assistant icons]*

Notifications, Help and the AI Assistant are always close at hand.

#### Module quiz

1. What is gIQ?  
   **Answer:** A cloud geospatial intelligence platform with AI, imagery acquisition and collaboration — gIQ is a SaaS ecosystem for geospatial intelligence by Space42.

2. Why might two users see different modules in gIQ?  
   **Answer:** Modules depend on version, role and permissions — Roles and permissions decide which modules appear.

3. Through which entry point does analytical job output enter the platform?  
   **Answer:** Analytical Jobs Results Upload — The platform flow names three entry points: File Manager upload, Acquire and job results.

## G2 — Globes and the Explore Module

### Lesson G2.1: The Explore Module and the 3D Globe  (7 min)

**Objective:** Find and view layers on the gIQ globe.

*[ON SCREEN: Globes > Explore]*

Explore is your data command centre and opens by default when you log in. You'll also find it under Globes, Explore.

*[ON SCREEN: Layers panel: search, sort, filter, footprints]*

On the left is the Layers panel. Search for a layer, sort and filter the list, and toggle footprints to see where each dataset covers. The context header switches between layers, AOIs and targets.

*[ON SCREEN: layer More Options: zoom, perspective view]*

Select a layer to view it. Its More Options menu zooms to it or switches to a perspective view.

*[ON SCREEN: Action Menu: search coordinates, full screen, 2D/3D, translucency]*

The map's Action Menu lets you search for a place or paste coordinates, go full screen, switch between 2D and 3D, and adjust globe and basemap translucency. Change the basemap between satellite imagery and streets.

*[ON SCREEN: zooming from globe to street level]*

Zoom from the whole globe down to street level; the platform loads more detail as you go.

### Lesson G2.2: Layer Details: Properties, Render, Detection and Relations  (6 min)

**Objective:** Inspect a dataset's metadata, display and AI results.

*[ON SCREEN: Contextual Details panel]*

Selecting a layer opens the Contextual Details panel. The tabs depend on the layer type.

*[ON SCREEN: Properties tab with STAC properties]*

Properties shows metadata, including STAC properties for imagery, and lists the workspaces that use the layer.

*[ON SCREEN: Render tab histogram]*

Render controls how imagery displays, with a histogram to adjust contrast.

*[ON SCREEN: Detection tab]*

Detection is where you run AI models on the image, view model run history, and search, filter and download detections by category.

*[ON SCREEN: Relations tab]*

Relations lists the analytical jobs run on the layer: when, how long they took, and who ran them.

#### Module quiz

1. Which Contextual Details tab lets you run models and view detections?  
   **Answer:** Detection — The Detection tab handles model runs and their results.

2. How does the Explore module differ from a workspace's Exploration tab?  
   **Answer:** Explore covers all platform data; Exploration covers only that workspace's layers — Exploration is scoped to a workspace and supports editing.

3. Which tab shows render configuration and a histogram?  
   **Answer:** Render — The Render tab controls how a raster is displayed.

## G3 — Data: Uploads, Ingestion and Jobs

### Lesson G3.1: Uploading Data and Ingestion Jobs  (6 min)

**Objective:** Bring your own data into gIQ and track its processing.

*[ON SCREEN: Upload / File Manager]*

Upload your own data through File Manager. gIQ supports vector and raster data, archives such as ZIP and TAR from many satellite vendors, documents and video.

*[ON SCREEN: Data > Jobs > Ingestion]*

Every upload becomes an ingestion job. Open Data, Jobs, Ingestion to watch it.

*[ON SCREEN: Queued and In-Progress/Completed tabs]*

The dashboard shows jobs by status on Queued and In-Progress/Completed tabs. Use quick filters, sort columns, search, and filter by type, status or user.

*[ON SCREEN: job details with processing log]*

Open a job's details to read its processing log — the first place to look if something fails.

*[ON SCREEN: ingested layer in Explore]*

When ingestion completes, the data appears in Explore and is ready for workspaces and AI models.

### Lesson G3.2: Data Manager, AOIs, Targets and Alerts  (5 min)

**Objective:** Organise data assets and set up monitoring.

*[ON SCREEN: Data module: Data Manager, Alerts, Jobs]*

The Data module has three parts: Data Manager, Alerts and Jobs.

*[ON SCREEN: File Manager, AOI Manager, Target Manager]*

Data Manager is where you organise, catalogue and maintain data assets: files, areas of interest (AOIs) and targets — the specific sites you monitor.

*[ON SCREEN: Alerts configuration]*

Alerts and Alerts Configuration set up notifications for the areas and targets you care about.

*[ON SCREEN: Exports]*

Exports keeps track of data you've exported from the platform.

> **Tip:** Define AOIs early; they're reused for searching imagery, ordering, and monitoring.

### Lesson G3.3: Monitoring Inference Jobs  (5 min)

**Objective:** Track AI model runs on your imagery.

*[ON SCREEN: Data > Inference]*

Inference jobs run AI models over imagery. They can be started manually by you or automatically by the system. Open Data, then Inference, to see them.

*[ON SCREEN: inference jobs list, newest first]*

The list shows the newest jobs first. Status buttons filter by state, and the action menu shows the model and image each job used.

*[ON SCREEN: bulk rerun and stop]*

Select several jobs to rerun or stop them in bulk.

*[ON SCREEN: detections in Explore]*

Finished results appear as detections on the image's Detection tab in Explore and in workspaces.

#### Module quiz

1. Every dataset is processed and validated in which step before analysis?  
   **Answer:** Ingestion — All data passes through Ingestion.

2. Where do you monitor queued, in-progress and completed data processing?  
   **Answer:** Data > Jobs > Ingestion — The Ingestion jobs dashboard tracks processing status.

3. Inference jobs can be started…  
   **Answer:** Manually by a user or automatically by the system — Both manual and automatic inference are supported.

## G4 — Acquire: Buying Satellite Imagery

### Lesson G4.1: Searching the Imagery Archive  (7 min)

**Objective:** Find and buy existing satellite images for an area.

*[ON SCREEN: Acquire > Buy > Search Archive]*

The Acquire module buys imagery from many vendors in one place. Open Acquire, Buy, Search Archive.

*[ON SCREEN: draw AOI, set dates]*

Define your area of interest and date range.

*[ON SCREEN: provider filters: cloud cover, resolution, off-nadir]*

Each provider has its own filters: cloud coverage for optical imagery, resolution and off-nadir angle for Airbus and Maxar, product type for Planet and BlackSky, and collect mode and polarisation for Capella SAR.

*[ON SCREEN: imagery types table]*

Know your imagery types. Multispectral, from providers like Airbus, Maxar, Planet and Sentinel-2, shows colour and vegetation. Panchromatic is sharp black-and-white. SAR, from Capella, Sentinel-1 and Space42, sees through clouds and at night. Thermal comes from SatVu.

*[ON SCREEN: clipping option]*

Some providers, including Airbus, Maxar and Planet, can clip the image to your area. All times are shown in UTC.

### Lesson G4.2: Tasking a Satellite  (6 min)

**Objective:** Commission new imagery that doesn't exist yet.

*[ON SCREEN: Acquire > Buy > Tasking]*

When the archive doesn't have what you need, task a satellite to capture it. Tasking is offered by Airbus, BlackSky, Capella, Planet, Space42 and Satellogic.

*[ON SCREEN: drawing tools: point, rectangle, polygon]*

Depending on the provider, mark your target with a point, rectangle or polygon.

*[ON SCREEN: tasking options]*

Set the options: product, cloud cover, incidence angle, imaging mode — such as Planet's single, stereo or tri-stereo — and, for Space42 SAR, product, pass direction and look side.

*[ON SCREEN: Space42 SAR products: Spot, Dwell, Strip, Scan]*

Space42's SAR products include Spot, Dwell, Strip and Scan modes, trading area against detail.

> **Tip:** The AI Assistant can help you order future tasking with a conversational request.

### Lesson G4.3: Orders and Continuous Collection  (5 min)

**Objective:** Track orders and automate recurring imagery collection.

*[ON SCREEN: Acquire > Orders]*

Acquire, Orders lists everything you've requested, with its status and details. Depending on your role, orders may go through an approval workflow.

*[ON SCREEN: Acquire > Continuous Collection]*

Continuous Collection sets up recurring collection for an area. When new Landsat, Sentinel-1 or Sentinel-2 imagery matches your settings, it's acquired automatically.

*[ON SCREEN: monitoring use case]*

Use it to monitor construction, coastlines or crops week after week without placing new orders.

#### Module quiz

1. What is the difference between archive and tasking?  
   **Answer:** Archive is existing imagery; tasking commissions a new capture — Archive buys what exists; tasking orders future collection.

2. Which imagery type sees through clouds and works at night?  
   **Answer:** SAR — Synthetic aperture radar is an active sensor.

3. Continuous Collection is available for…  
   **Answer:** Landsat, Sentinel-1 and Sentinel-2 — The docs list these open missions for recurring collection.

## G5 — Collaborate: Workspaces, Annotation and Reports

### Lesson G5.1: Workspaces  (7 min)

**Objective:** Create a workspace and organise layers, features and insights.

*[ON SCREEN: Collaborate > Workspaces dashboard]*

A workspace is a meta-project for a theme or client. It holds layers, files — imagery, GeoJSON, PDFs, CSVs — analyst tools, insights, a dashboard, stories, reports and comments. Open Collaborate, Workspaces.

*[ON SCREEN: quick filters: Active, Archived, Created by me, Shared with me, Favorites]*

The Workspaces dashboard shows active workspaces. Quick filters show archived ones, those you created, those shared with you, and favourites. Sort by date or name, or search.

*[ON SCREEN: create workspace]*

Create a new workspace and set its purpose, theme and privacy.

*[ON SCREEN: workspace tabs]*

Inside, tabs run along the top: Exploration, Insights, Dashboard, Story, Reports and Comments.

### Lesson G5.2: The Exploration Tab and Analyst Tools  (6 min)

**Objective:** Add, draw and analyse layers inside a workspace.

*[ON SCREEN: Exploration tab, plus button in Layers panel]*

The Exploration tab looks like Explore but shows only this workspace's layers. Use the plus button to add drawing or vector layers, organise them into collections, and bring in layers from other modules.

*[ON SCREEN: create point, line, polygon features]*

Here you can create, edit, delete and export point, line and polygon features.

*[ON SCREEN: Analyst Tools]*

Analyst Tools are available in Exploration and Annotation, not in Explore.

*[ON SCREEN: Run Auto AI Model decision]*

From a workspace you can let the platform pick and run suitable AI models automatically, or choose a model and parameters yourself.

### Lesson G5.3: Annotation Projects  (7 min)

**Objective:** Label imagery as a team with a review workflow.

*[ON SCREEN: Collaborate > Annotation Project]*

Annotation projects label features in imagery — buildings, roads, vehicles — for analysis and for training AI. Open Collaborate, Annotation Project.

*[ON SCREEN: supported inputs]*

Projects accept TIF imagery and vendor archives such as ICEYE, Maxar, Sentinel-1, Pleiades, Landsat and STAC.

*[ON SCREEN: Project Categories panel]*

Set up label categories in the Project Categories panel.

*[ON SCREEN: workflow: setup, assign, annotate, review, rework]*

The workflow has five steps. A manager creates the project and images. Jobs are assigned to annotators. Annotators draw bounding boxes, label them and submit. Reviewers approve or reject each job. Rejected jobs go back for rework.

*[ON SCREEN: Job Analytics and Export annotations]*

Track progress in the Job Analytics panel and export annotations when the project is done.

### Lesson G5.4: Reports and Stories  (6 min)

**Objective:** Turn analysis into reports and narrative stories.

*[ON SCREEN: workspace Reports and Story tabs]*

Inside a workspace, Reports create standardised analytical reports, and Stories present findings as a narrative for decision-makers. Stories can be published to the marketplace.

*[ON SCREEN: Reports module list]*

The Reports module collects reports from all workspaces in your organisation, with name, creator, classification, status and dates.

*[ON SCREEN: statuses: Draft, Approved, Downloadable, Failed]*

Draft reports can be edited and approved. Any report can be previewed, duplicated, exported as PDF, as report data or as a system report, or deleted.

*[ON SCREEN: Templates, Reports Map]*

Templates keep reports consistent, and the Reports Map shows reports by location.

#### Module quiz

1. Which workspace tab is the default landing page?  
   **Answer:** Exploration — Workspaces open on the Exploration tab.

2. In an annotation project, who approves or rejects jobs?  
   **Answer:** Users with the Review Job permission — QA reviewers approve or reject submitted jobs.

3. A report in Draft status can be…  
   **Answer:** Edited and approved — Draft-only actions are Edit and Approve.

## G6 — AI in gIQ

### Lesson G6.1: AI Models: Upload, Configure and Run  (7 min)

**Objective:** Manage AI models and run them on imagery.

*[ON SCREEN: AI > Models]*

The AI module manages models through their whole life: upload, configuration, publishing, troubleshooting and monitoring. Open AI, Models. You need the Upload Model or Admin Models permission to see it.

*[ON SCREEN: model upload with YAML and categories]*

Uploading a model involves its files, a YAML configuration and category mapping, so detections get meaningful class names.

*[ON SCREEN: Explore Detection tab: Select AI Model]*

To run a model, select an image in Explore and open the Detection tab, or work from a workspace. Choose a model yourself or let the platform run suitable models automatically.

*[ON SCREEN: detections overlay]*

Detections appear as a layer you can filter by category and download.

*[ON SCREEN: publishing to marketplace]*

Publishing a model to the marketplace needs both Admin Models and Marketplace Creator permissions.

### Lesson G6.2: AMD, AI Sandbox and the AI Assistant  (6 min)

**Objective:** Train custom models and get help from the AI Assistant.

*[ON SCREEN: AI > AMD]*

AMD, Auto Model Development, is where you train and manage custom models. Labelled imagery from annotation projects is the raw material for training. It needs the AMD Creator or AMD Admin permission.

*[ON SCREEN: AI > AI Sandbox]*

The AI Sandbox sits alongside Models and AMD. Check its overview in the docs to see what's enabled for your organisation.

*[ON SCREEN: AI Assistant chat]*

The AI Assistant is a conversational helper. Ask it to search the documentation, find imagery from multiple vendors, order future tasking, or generate a summary report for a location.

*[ON SCREEN: limitations page]*

Read the Limitations page in the docs, and always check the assistant's results before acting on them.

#### Module quiz

1. Which permission do you need to upload and configure a model?  
   **Answer:** Upload Model — Upload Model (or Admin Models) controls model uploads.

2. AMD stands for…  
   **Answer:** Auto Model Development — AMD is gIQ's automated model training.

3. Which of these can the AI Assistant help with?  
   **Answer:** Ordering satellite tasking and summarising locations — The docs list documentation search, acquisition, tasking and location summaries.

## G7 — Market, Geostream and Administration

### Lesson G7.1: The Marketplace, Seller Central and Geostream  (5 min)

**Objective:** Buy and sell digital assets and showcase work.

*[ON SCREEN: Market > Marketplace]*

The Market module has two sides. The Marketplace is where you find digital assets published by organisations on gIQ — AI models, applications, reports and stories.

*[ON SCREEN: Market > Seller Central]*

Seller Central is the vendor side: publish your assets, manage them, and see analytics on how they perform.

*[ON SCREEN: Geostream]*

Geostream showcases your brand and geospatial data as video. Add videos to the platform, then add or remove them from the stream.

### Lesson G7.2: Administration: Users, Roles and Credits  (6 min)

**Objective:** Set up users and roles safely.

*[ON SCREEN: Profile avatar > Admin Panel]*

Administrators open the Admin Panel from the profile avatar.

*[ON SCREEN: Super User and System Administrator roles]*

The Super User is the only role defined at setup. It creates roles, assigns permissions, manages organisations, posts announcements, manages basemaps and configures LLM Chat. Other roles, like a System Administrator, see only the modules they're granted.

*[ON SCREEN: roles mapped to org chart]*

Good practice: map roles to your organisation, grant the least privilege each role needs, create role templates for common jobs, keep very few Super User accounts, and audit them regularly.

*[ON SCREEN: Credits > Credit Usage, Credit Pricing]*

The Credits section shows credit usage and pricing, so teams can track spending.

*[ON SCREEN: gIQ course recap]*

That completes the gIQ track — from logging in to acquiring imagery, running AI, collaborating and managing the platform.

#### Module quiz

1. Where do sellers publish and manage their digital assets?  
   **Answer:** Seller Central — Seller Central is the vendor side of the Market module.

2. Geostream is used to…  
   **Answer:** Showcase your brand and geospatial data as video — Geostream presents video content on the platform.

3. Which principle should guide permission assignment?  
   **Answer:** Least privilege — Grant only what each role needs.

---
## Intro / outro templates

**YouTube intro:** Hi, and welcome back to the [Introduction to ArcGIS series / QGIS course / gIQ course]. This is lesson [N]: [Title]. By the end of this video, you'll be able to [objective].

**YouTube outro:** That's it for [Title]. If this helped, give the video a like and subscribe so you don't miss the next lesson, where we cover [next lesson]. Questions? Leave them in the comments.

**LinkedIn intro:** In this video, we'll look at [title]. [Objective]

**LinkedIn outro:** Up next: [next lesson].
