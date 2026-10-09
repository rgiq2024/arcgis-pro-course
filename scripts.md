# Introduction to ArcGIS Pro — Lesson Scripts
Each script: objective, narration with [ON SCREEN] recording cues, tip. Intro/outro lines differ for YouTube vs LinkedIn (see notes at end).

# M1 — Getting Started with ArcGIS Pro

## Lesson 1.1: How to Install ArcGIS Pro  (6 min)

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

## Lesson 1.2: Opening ArcGIS Pro and Signing In  (4 min)

**Objective:** Launch ArcGIS Pro and sign in with a named user license.

*[ON SCREEN: Start menu > ArcGIS Pro]*

Open the Start menu and click ArcGIS Pro. You can also pin it to your taskbar so it's one click away next time.

*[ON SCREEN: sign-in dialog]*

The first time ArcGIS Pro starts, it asks you to sign in. Most people use a named user license, which is tied to your ArcGIS Online or ArcGIS Enterprise account. Type your username and password, or use your organization's single sign-on button.

Tick "Sign me in automatically" if this is your own computer — it saves you a step every time.

*[ON SCREEN: Settings > Licensing]*

If you use a different license type, like a single use or concurrent license, you can change it later from Settings, then Licensing. That page also shows which extensions are licensed for you, such as Spatial Analyst or 3D Analyst.

> **Tip:** If you see a sign-in error, check you're signing in to the right portal URL — ArcGIS Online versus your company's Enterprise portal.

## Lesson 1.3: The Start Page and How It Differs from ArcMap  (5 min)

**Objective:** Read the ArcGIS Pro start page and understand the project-based workflow.

*[ON SCREEN: ArcGIS Pro start page]*

After signing in, you land on the start page. On the left are your recent projects. In the middle are the templates for creating a new project: Map, Catalog, Global Scene, Local Scene, and Start without a template. You can also open a project from your computer or your portal, and reach Settings at the bottom left.

*[ON SCREEN: split screen, ArcMap vs ArcGIS Pro]*

If you're coming from ArcMap, this is the biggest change. ArcMap opened straight into a single map document, an MXD, with one map and one layout. ArcGIS Pro opens into a project. A project can hold many maps, many layouts, scenes, toolboxes, databases and folder connections — all together in one place.

ArcMap also needed separate apps — ArcCatalog for data, ArcScene and ArcGlobe for 3D. In ArcGIS Pro, all of that lives in one 64-bit application.

> **Tip:** Projects created in a 3.x release won't open in the older 2.x releases, so keep that in mind when sharing with colleagues.

## Lesson 1.4: Creating a Project: File Extension and Folder Structure  (6 min)

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

## Lesson 1.5: Project Types: Map, Global Scene, Local Scene, Catalog, No Template  (7 min)

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

## Lesson 1.6: Saving and Closing a Project  (3 min)

**Objective:** Save your work safely and close a project.

*[ON SCREEN: Quick Access Toolbar save icon]*

Save your project with the save icon at the top left, the Project tab, or Ctrl+S. ArcGIS Pro shows an asterisk in the title bar when there are unsaved changes.

*[ON SCREEN: Project tab > Save As]*

Use Save As when you want a copy of the project under a new name.

*[ON SCREEN: closing the app with unsaved changes prompt]*

To close a project, either open or create a different project from the Project tab, or close ArcGIS Pro with the X at the top right. If there are unsaved changes, ArcGIS Pro asks whether to save.

Note that unsaved edits to data are handled separately from the project. If you've been editing features, save or discard the edits from the Edit tab first.

> **Tip:** ArcGIS Pro can auto-save project backups — turn this on under Settings, Options, General.

# M2 — The ArcGIS Pro Interface

## Lesson 2.1: A Tour of the ArcGIS Pro Interface  (6 min)

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

## Lesson 2.2: The Ribbon, Tabs and the Project Tab  (6 min)

**Objective:** Find tools on the ribbon and use the Project tab.

*[ON SCREEN: ribbon tabs]*

The ribbon organizes tools into tabs, and each tab into groups. The Map tab holds navigation, layers, selection and labeling. Insert adds new maps, layouts and toolboxes. Analysis opens geoprocessing tools. View controls panes and windows. Edit holds editing tools. Share is for publishing and exporting.

*[ON SCREEN: clicking a layer reveals Feature Layer tab]*

Some tabs are contextual — they only appear when relevant. Click a feature layer in Contents and the Feature Layer tab appears, with Appearance, Labeling and Data.

*[ON SCREEN: Project tab backstage]*

The Project tab is different. It opens a full-screen page where you create, open and save projects, manage portal connections and licensing, change Options, and manage Python environments and add-ins. Press Escape or the back arrow to return.

*[ON SCREEN: ArcMap menu bar vs Pro ribbon]*

In ArcMap, tools were in drop-down menus and floating toolbars you had to switch on. In ArcGIS Pro, the ribbon shows the tools for what you're doing right now. If you can't find something, use the Command Search box at the top — type the tool name and run it directly.

## Lesson 2.3: The Contents Pane and the Attribute Table  (5 min)

**Objective:** Use Contents to manage layers and open an attribute table.

*[ON SCREEN: Contents pane]*

The Contents pane lists everything in the active map: the map itself, your layers, and the basemap. Checkboxes switch layers on and off. The order of layers is the drawing order — layers at the top draw on top.

If Contents is closed, reopen it from View tab, Contents.

*[ON SCREEN: right-click > Attribute Table]*

Every feature layer has an attribute table — the information behind each feature. Right-click a layer and choose Attribute Table, or press Ctrl+T with the layer selected.

The table opens as its own view below the map. Each row is a feature, each column is a field. Click a row header to select that feature on the map; double-click it to zoom to it.

We'll explore Contents in much more depth in Module 6.

## Lesson 2.4: The View Tab  (4 min)

**Objective:** Open, close and reset panes from the View tab.

*[ON SCREEN: View tab]*

The View tab is your control centre for windows. Its Windows group opens the Catalog pane, Catalog view, Contents, Geoprocessing, Python window and Tasks. Reset Panes restores a standard layout for mapping, geoprocessing or editing.

*[ON SCREEN: Link Views]*

Link Views keeps two maps in step — great for comparing before-and-after images side by side.

*[ON SCREEN: Convert to scene]*

You'll also find Convert, which turns a 2D map into a global or local scene, and the Accessibility options for appearance and keyboard use.

> **Tip:** Most panes have a keyboard shortcut. Hover over a button to see it.

## Lesson 2.5: The Catalog Pane and Catalog View  (5 min)

**Objective:** Browse project items and data with Catalog.

*[ON SCREEN: Catalog pane]*

The Catalog pane shows everything that belongs to the project. The Project tab inside it lists Maps, Toolboxes, Databases, Styles, Folders and Locators. The Portal tab lists your online content, and Favorites keeps connections you use in every project.

*[ON SCREEN: expanding Databases and Folders]*

Expand Databases to see the project's default geodatabase. Expand Folders to browse folders you've connected — we'll add our own folder connection in Module 4.

*[ON SCREEN: Catalog view]*

For bigger data-management jobs, open the Catalog view from the View tab. It's like a file explorer for GIS data, with a details panel showing previews and metadata.

> **Tip:** Drag a dataset from Catalog straight onto the map to add it.

# M3 — Navigating Maps and Scenes

## Lesson 3.1: The Map View, Explore Tool and Identify  (5 min)

**Objective:** Pan, zoom and identify features with the Explore tool.

*[ON SCREEN: Map tab > Explore]*

The Explore tool is your all-in-one navigation tool. It's on the Map tab, in the Navigate group, and it's active by default.

Drag with the left mouse button to pan. Roll the mouse wheel to zoom in and out. Hold the right button and drag to zoom smoothly.

*[ON SCREEN: clicking a feature, pop-up appears]*

Click a feature and a pop-up appears showing its attributes. This is how you identify features in ArcGIS Pro — in ArcMap this was the separate Identify tool.

If several features overlap, the pop-up lists them all; click each one to see its details.

*[ON SCREEN: Explore drop-down]*

Use the drop-down under Explore to choose which layers it identifies: the topmost layer, visible layers, selectable layers, or selected layers in Contents.

## Lesson 3.2: Zoom Controls, Full Extent, Previous Extent and Scale  (5 min)

**Objective:** Control what part of the map you see.

*[ON SCREEN: Navigate group buttons]*

Next to Explore are more navigation buttons. Full Extent zooms to show all layers in the map. Fixed Zoom In and Fixed Zoom Out step in or out around the centre.

Previous Extent and Next Extent work like back and forward in a web browser — very useful after you've zoomed too far.

*[ON SCREEN: right-click layer > Zoom To Layer]*

To jump to one layer, right-click it in Contents and choose Zoom To Layer.

*[ON SCREEN: scale box at bottom]*

At the bottom left of the map is the scale. Type a value like 1:50,000 and press Enter, or pick one from the list. Small-scale numbers like 1:1,000,000 show a large area; large-scale numbers like 1:1,000 show detail.

> **Tip:** Create bookmarks from the Map tab to save views you return to often.

## Lesson 3.3: Status Bar: Snapping, Grid, Coordinates, Refresh and Pause  (6 min)

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

## Lesson 3.4: Global Scenes and the Navigator Tool  (6 min)

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

## Lesson 3.5: Local Scenes  (4 min)

**Objective:** Navigate a local scene and understand when to use it.

*[ON SCREEN: Local scene of a city]*

A local scene displays 3D content on a flat plane in a projected coordinate system. Navigation is the same as a global scene: Explore to pan and zoom, middle-drag or V-drag to tilt and rotate, and the Navigator for precise control.

*[ON SCREEN: navigating below ground]*

The big advantage is that you can enable underground navigation and look beneath the surface — perfect for utilities, geology, or basements of buildings. Turn it on in the scene properties, then make the ground semi-transparent.

*[ON SCREEN: View > Convert]*

You can convert any 2D map to a local or global scene from the View tab. ArcGIS Pro asks which type; pick local for city-sized areas.

# M4 — Shapefiles

## Lesson 4.1: What Is a Shapefile? The Files That Make It Up  (6 min)

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

## Lesson 4.2: Create a Shapefile in a Catalog Project  (6 min)

**Objective:** Make a folder connection and create a new shapefile with a coordinate system.

*[ON SCREEN: start page > Catalog template]*

Start a project with the Catalog template. In the Catalog pane, right-click Folders and choose Add Folder Connection. Browse to the folder where you keep your data and click OK. A folder connection is a shortcut — ArcGIS Pro won't copy or move anything.

*[ON SCREEN: right-click folder > New > Shapefile]*

Right-click the folder and choose New, then Shapefile. The Create Feature Class tool opens with the location already filled in.

Type a name — let's call it Schools. Set the Geometry Type: Point, Polyline, Polygon, Multipoint or Multipatch. We'll choose Point.

*[ON SCREEN: Coordinate System picker]*

Now the coordinate system. Click the globe icon. Choose a geographic system like WGS 1984, or a projected system for your area, such as a UTM zone. Searching by name or EPSG code is quickest. Click OK.

Click Run. The new, empty shapefile appears in the folder, ready for editing.

## Lesson 4.3: Second Way: the Create Feature Class Tool  (4 min)

**Objective:** Create a shapefile from the Geoprocessing pane.

*[ON SCREEN: Analysis tab > Tools]*

You can also start from the tool itself. On the Analysis tab click Tools, search for Create Feature Class, and open it.

*[ON SCREEN: tool parameters]*

For Feature Class Location, browse to a folder — not a geodatabase. That's what makes the output a shapefile rather than a geodatabase feature class.

Fill in the name, geometry type and coordinate system as before. Use the Template Dataset option if you want to copy the fields of an existing layer.

Click Run. Because you're in a map project, the new layer is added to the map automatically.

## Lesson 4.4: Third Way: the Quick Method  (4 min)

**Objective:** Create a shapefile in seconds from the Catalog pane of a map project.

*[ON SCREEN: map project, Catalog pane]*

The quickest route is from a map project. In the Catalog pane, expand Folders, right-click your folder, choose New, then Shapefile. Give it a name, a geometry type and a coordinate system, and click Run.

*[ON SCREEN: layer appears in Contents]*

The shapefile is created and added straight to your map, so you can start drawing features immediately from the Edit tab, Create.

The strengths of this method: it's fast, it uses the folders you already have connected, and it drops you right into editing. Use it when you need a working layer for a quick task — digitizing a few sites, sketching a study area, or practising editing.

# M5 — Adding Data

## Lesson 5.1: Adding Data and Shapefiles, and Fixing Invisible Layers  (6 min)

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

## Lesson 5.2: Adding Raster Data and Georeferenced Images  (5 min)

**Objective:** Add rasters and understand what makes an image georeferenced.

*[ON SCREEN: Add Data > GeoTIFF]*

Raster data — satellite images, scanned maps, elevation models — is added the same way: Add Data, or drag from Catalog. Common formats are GeoTIFF, JPEG 2000, IMG and rasters inside geodatabases.

ArcGIS Pro may ask to build pyramids and statistics. Say yes for large images; it makes them draw much faster.

*[ON SCREEN: image lines up with basemap]*

A georeferenced image knows where it belongs on Earth. That information is either built in, as in a GeoTIFF, or stored in a small side file called a world file, like .tfw or .jgw, plus an .aux.xml.

*[ON SCREEN: un-georeferenced scan]*

If your image lands in the wrong place or not at all, it isn't georeferenced. Use the Imagery tab, Georeference, to add control points and fix it.

## Lesson 5.3: Adding Layers to Global and Local Scenes  (5 min)

**Objective:** Add data to 3D scenes and control how layers sit on the surface.

*[ON SCREEN: scene Contents with categories]*

In a scene, Contents is split into categories: 3D Layers, 2D Layers, and Elevation Surfaces. Add Data works just as in a map; ArcGIS Pro sorts each layer into the right category.

*[ON SCREEN: dragging a layer from 2D to 3D]*

2D layers are draped flat over the ground. Drag a layer into 3D Layers to give it height.

*[ON SCREEN: Layer Properties > Elevation]*

Then open the layer's Properties, Elevation. Choose On the ground, Relative to the ground — with an offset in metres — or At an absolute height. For buildings, use the Appearance tab to extrude them using a height field.

> **Tip:** Use Elevation Surfaces to add your own DEM for more accurate terrain.

## Lesson 5.4: Adding KML and KMZ Files  (5 min)

**Objective:** View Google Earth data in ArcGIS Pro and convert it for analysis.

*[ON SCREEN: Add Data > .kmz]*

KML and KMZ are the formats used by Google Earth. ArcGIS Pro can add them directly: Add Data and choose the file. You'll see the placemarks, lines and polygons, with their styling.

*[ON SCREEN: KML layer properties]*

A KML layer added this way is read-only. You can view it, identify features with pop-ups, and change some display properties, but you can't edit its features or run most analysis tools on it.

*[ON SCREEN: KML To Layer tool]*

To work with the data fully, convert it with the KML To Layer tool. It creates a file geodatabase with feature classes for points, lines and polygons, plus a layer file that keeps the original look.

To go the other way, Layer To KML exports your ArcGIS layers for Google Earth.

# M6 — Mastering the Contents Pane

## Lesson 6.1: Elements of Contents and Comparison with ArcMap  (4 min)

**Objective:** Understand the parts of the Contents pane.

*[ON SCREEN: Contents toolbar]*

At the top of Contents is a search box and a row of buttons. These buttons switch the list mode — how your layers are listed. Below them is the map name, then layers and group layers, then the basemap.

*[ON SCREEN: ArcMap Table of Contents vs Pro Contents]*

In ArcMap the Table of Contents had a few tabs. ArcGIS Pro's Contents does more: it adds views for selection, editing, snapping and labeling, and it changes to match the active view — a map, a scene, a layout or a table each show their own contents.

## Lesson 6.2: List by Drawing Order, Data Source and Selection  (5 min)

**Objective:** Switch Contents views to answer different questions.

*[ON SCREEN: List By Drawing Order]*

List By Drawing Order is the default. The order here is the order things draw. Drag layers to restack them.

*[ON SCREEN: List By Data Source]*

List By Data Source groups layers by where the data lives — which folder or geodatabase. It's the quickest way to spot broken data links, shown with a red exclamation mark.

*[ON SCREEN: List By Selection]*

List By Selection shows how many features are selected in each layer and lets you set which layers are selectable. Untick a layer here, and the selection tools ignore it.

## Lesson 6.3: List by Editing, Snapping and Labeling, and Searching Layers  (5 min)

**Objective:** Control editing, snapping and labels per layer.

*[ON SCREEN: List By Editing]*

List By Editing shows which layers are editable. Untick a layer to protect it while you edit others.

*[ON SCREEN: List By Snapping]*

List By Snapping lets you choose which layers your pointer snaps to — useful when a busy map makes snapping jump to the wrong thing.

*[ON SCREEN: List By Labeling]*

List By Labeling shows which layers have labels switched on and their label classes. Here's the key difference from Drawing Order: Drawing Order controls how layers stack, while Labeling controls which labels show and their priority — the order of layers in Labeling does not change drawing at all.

*[ON SCREEN: typing in search box]*

On a map with dozens of layers, type part of a name into the Search box at the top of Contents to filter the list instantly.

## Lesson 6.4: The Layer Menu: Copy, Remove, Attribute Table, Zoom To  (5 min)

**Objective:** Use the most common layer right-click commands.

*[ON SCREEN: right-click layer menu]*

Right-click any layer to open its menu. Let's use the most common commands.

Copy — then right-click the map or another map and choose Paste. The copy keeps its symbology, so it's a fast way to show the same data two ways.

Remove — takes the layer off the map. The data on disk is not deleted.

Attribute Table — opens the table.

Zoom To Layer — zooms to the layer's full extent.

*[ON SCREEN: Make Default / Data / Sharing submenus]*

Further down you'll find submenus for Data, Sharing, Symbology, Labeling and Properties, which we'll cover next.

## Lesson 6.5: Selection, Labels and Pop-ups from the Layer Menu  (6 min)

**Objective:** Manage selection, labels and pop-ups for a layer.

*[ON SCREEN: Map tab > Select]*

To select features, use the Select tool on the Map tab. To identify them, use Explore. Remember to check which layers are selectable — right-click a layer, Selection, Make This The Only Selectable Layer.

*[ON SCREEN: Selection submenu]*

The Selection submenu also has Zoom To Selection, Clear Selection, and Switch Selection, which flips the selection — selected becomes unselected and the other way round. Great for "select everything except these".

*[ON SCREEN: right-click > Label]*

Click Label in the menu to switch labels on. ArcGIS Pro uses the layer's display field; change it on the Labeling tab.

*[ON SCREEN: Enable/Disable Pop-ups]*

The layer menu also has an option to enable or disable pop-ups. Disable them on reference layers so clicking only shows the data you care about.

## Lesson 6.6: Export Features, Metadata and Layer Properties  (6 min)

**Objective:** Save a layer to new data, view metadata and explore Layer Properties.

*[ON SCREEN: Data > Export Features]*

Right-click, Data, Export Features. If features are selected, only those are exported — a quick way to make a new dataset from a subset. Choose an output in a geodatabase or a folder and click OK.

*[ON SCREEN: View Metadata]*

View Metadata shows who made the data, when, and how. Edit Metadata lets you add a summary, tags and credits — always worth doing before you share.

*[ON SCREEN: Layer Properties dialog]*

Finally, Properties. The pages include General, Metadata, Source, Elevation, Selection, Display, Definition Query, Time, Range, Joins and Relates.

Compared with ArcMap, symbology and labeling have moved out of the properties dialog into their own panes, which stay open while you work, so you see changes immediately.

# M7 — Symbology

## Lesson 7.1: Opening the Symbology Pane and the Types of Symbology  (6 min)

**Objective:** Open the Symbology pane and know which methods exist.

*[ON SCREEN: right-click > Symbology]*

Right-click a layer and choose Symbology, or select the layer and click Symbology on the Feature Layer tab, Appearance group. The Symbology pane opens on the right.

*[ON SCREEN: Primary symbology drop-down]*

At the top is Primary symbology. The main choices are Single Symbol, Unique Values, Graduated Colors, Graduated Symbols, Proportional Symbols, Unclassed Colors, Bivariate Colors, Dot Density, Charts, and for points, Heat Map.

The options depend on geometry. Points, lines and polygons all get the core methods, but Dot Density is only for polygons and Heat Map is only for points.

*[ON SCREEN: pane tabs]*

Under the method you'll see tabs: Primary symbology, Vary symbology by attribute, and Advanced symbology options. We'll use all three in the coming lessons.

## Lesson 7.2: Single Symbol and Vary Symbology by Attribute  (7 min)

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

## Lesson 7.3: Unique Values  (7 min)

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

## Lesson 7.4: Graduated Colors  (8 min)

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

## Lesson 7.5: Graduated Symbols  (7 min)

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

## Lesson 7.6: Unclassed Colors  (5 min)

**Objective:** Show a continuous colour ramp without classes.

*[ON SCREEN: Unclassed Colors]*

Unclassed Colors shades features along a continuous colour ramp. Instead of five or six steps, every value gets its own exact shade between the lowest and highest colour.

That's why it's called unclassed: there are no class breaks — the colour is calculated straight from the value.

*[ON SCREEN: compare with Graduated Colors]*

The trade-off: graduated colours are easier to read from a legend, because each colour means a range. Unclassed colours show subtle differences more faithfully, but readers can't easily tell exact values apart.

*[ON SCREEN: upper and lower labels]*

You can set the upper and lower values and their labels, so outliers don't stretch the ramp.

## Lesson 7.7: Proportional Symbols  (6 min)

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

## Lesson 7.8: Dot Density  (7 min)

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

## Lesson 7.9: Choosing the Right Symbology and Course Wrap-up  (5 min)

**Objective:** Match the symbology method to the data and the message.

*[ON SCREEN: decision chart]*

Let's pull it together.

Categories, like land use: Unique Values.

Rates, percentages or densities across areas: Graduated Colors, or Unclassed Colors for subtle variation.

Counts or totals: Graduated Symbols or Proportional Symbols.

Counts spread across areas where distribution matters: Dot Density.

Everything the same, just a reference layer: Single Symbol.

*[ON SCREEN: recap montage]*

In this course you installed ArcGIS Pro, created projects, learned the interface, navigated maps and scenes, created shapefiles, added data, mastered Contents, and designed maps with every core symbology method.

*[ON SCREEN: next steps]*

Next, practise by mapping a dataset from your own city using three different symbology methods, and compare what each one tells you.

---
## Intro / outro templates

**YouTube intro:** Hi, and welcome back to the Introduction to ArcGIS Pro series. This is lesson [N]: [Title]. By the end of this video, you'll be able to [objective].

**YouTube outro:** That's it for [Title]. If this helped, give the video a like and subscribe so you don't miss the next lesson, where we cover [next lesson]. Questions? Leave them in the comments.

**LinkedIn intro:** In this video, we'll look at [title]. [Objective]

**LinkedIn outro:** Up next: [next lesson].
