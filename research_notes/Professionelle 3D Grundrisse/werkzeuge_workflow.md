# Tools and Production Workflow for Professional 3D Floor Plans of Apartments (2D Plan + Room Photos -> 3D-Grundriss)

*How these notes were made (please read): this session's network rules blocked every page fetch tried (immobilienscout24.de, visualisierungen.immoviewer.com, ohne-makler.net, help.roomsketcher.com all failed with ENOTFOUND). So every finding below comes from **search-engine result summaries and snippets**, not from reading the full pages. Prices and figures are what the providers themselves state, as the search engine summarised them (status Nov 2026). Some summaries did not say clearly which provider a number belongs to. Where that happens, the note says "attribution unclear". Check figures on the provider's live page before quoting them as final. Vendor marketing claims are marked **[vendor claim]**. Independent tests and forum reports are marked **[independent]** or **[forum/anecdotal]**.*

## 1. Which software is used, and for which kind of output?

### Takeaway
The market splits into three tiers:
- **Fast real-estate floor-plan tools and services** (RoomSketcher, Cedreo, Floorplanner, Planner 5D and the German "Grundriss-Service" firms) produce standard isometric or top-down 3D floor plans cheaply and within 1–4 days.
- **Archviz studios** use general 3D/DCC software (3ds Max + Corona/V-Ray, SketchUp, Blender) for photoreal, custom-furnished 3D floor plans. They cost several hundred euros.
- **Capture apps** (magicplan, Polycam, Canvas, RoomPlan-based apps, Matterport) are used on site to *create* the dimensional base rather than to make the final presentation.

BIM/CAD tools (Archicad, Revit, Vectorworks, Chief Architect) are the architect's route when construction-grade documentation is needed. This session found little evidence on how much they are used for marketing-type 3D floor plans.

### Cited Findings
- RoomSketcher (Pro/Team subscription) lets users upload a blueprint image, scale it and trace over it. It also offers an "AI Convert" feature that turns a blueprint into a floor plan after the scale is set — [RoomSketcher: Trace a Blueprint](https://www.roomsketcher.com/features/pro-features/draw-from-a-blueprint); [RoomSketcher Help: From Blueprint to Floor Plan – AI Conversion & Tracing](https://help.roomsketcher.com/hc/en-us/articles/31885247016605)
- RoomSketcher also sells a done-for-you drawing service: upload a sketch, blueprint or existing plan (JPG/PNG/PDF). The plan is delivered the next business day and stays editable in the app — [RoomSketcher: Order Floor Plans](https://www.roomsketcher.com/order-floor-plans/); [RoomSketcher Help: How Do I Order Floor Plans](https://help.roomsketcher.com/hc/en-us/articles/202273701)
- Third-party software listings describe Cedreo as aimed at residential builders/remodelers, "best for 2D and 3D floor plans" with photorealistic renderings and automatic roofing, from about $49 per project. RoomSketcher is described as most suitable for real-estate layouts, from about $49/year — [SoftwareTestingHelp: Top Floor Plan Software 2026](https://www.softwaretestinghelp.com/?p=167456); [Software Advice: Cedreo vs RoomSketcher 2026](https://www.softwareadvice.com/architecture/cedreo-profile/vs/roomsketcher/)
- Chief Architect is positioned for firms that need detailed construction documentation and advanced technical drawing. Cedreo's own comparison page says it needs a high-end PC (16 GB+ RAM, a ray-tracing-capable GPU) **[vendor claim by a competitor]**. Capterra/GetApp rate it about 4.4/5 — [Cedreo: Alternative to Chief Architect](https://cedreo.com/compare/chief-architect/); [Capterra: Chief Architect vs Cedreo](https://www.capterra.co.uk/compare/80035/177284/chief-architect/vs/cedreo); [Cedreo blog: Chief Architect vs SketchUp vs Cedreo](https://cedreo.com/blog/chief-architect-vs-sketchup-vs-cedreo/)
- Cedreo and Planner 5D both market 3D-Grundriss creation to German-speaking users — [Cedreo DE: 3D Grundriss](https://cedreo.com/de/grundriss-zeichnen/3d/); [Planner 5D DE: 3D-Grundriss](https://planner5d.com/de/use/3d-grundriss)
- In freelance archviz, sellers name SketchUp (often with V-Ray), 3ds Max with Corona or V-Ray, and Lumion as their tools. One listing prices Lumion work at about 75–85% of 3ds Max work. Studios typically ask for a .skp/.max model or a 2D drawing to model from — [Fiverr: photorealistic Corona 3D floor plans](https://fiverr.com/khiem194/create-3d-floor-plan-from-your-cad-plan-and-render-with-corona); [Fiverr: SketchUp model from floor plans](https://fiverr.com/thepalashjain/model-your-floor-plan-into-3d-on-sketchup-professionally); [CADCrowd: 3D floor plan rendering services, costs](https://www.cadcrowd.com/blog/?p=32471)
- Archviz training (3ds Max + Corona) teaches importing an AutoCAD DWG plan, tracing and extruding walls, then merging furniture models in a separate pass. This is the classic studio pipeline — [Udemy: M6 Archviz Masterclass 3ds Max Corona](https://www.udemy.com/course/m6-archviz-masterclass-in-3ds-max-corona-render/); [Elephorm: 3ds Max + Corona, importing an AutoCAD plan (FR)](https://www.elephorm.com/formation/3d/3ds-max/apprendre-corona-renderer-et-3ds-max-2021-atelier-creatif-darchitecture/reglages-du-logiciel-et-importation-du-plan)
- Blender is used for floor-plan-to-3D work, including through the **Archimesh** add-on (parametric walls, doors, windows, floors, ceilings) — [Blenderian: Blender 3D Floor Plan tutorial](https://blenderian.com/blender-3d-floor-plan-complete-architectural-modeling-tutorial/); [Envato Tuts+: 3D floor plan from a schematic in Blender](https://design.tutsplus.com/tutorials/create-a-3d-floor-plan-model-from-an-architectural-schematic-in-blender--cg-13350)
- Capture apps: magicplan (LiDAR scan plus a Bluetooth laser option), Polycam (LiDAR "Space" mode, exportable to AutoCAD), Canvas (LiDAR scan-to-CAD) and Matterport (camera-based capture producing "schematic" floor plans) — [magicplan Help: How does LiDAR scan work](https://help.magicplan.app/how-does-lidar-scan-work); [Polycam: Export Space Mode to AutoCAD](https://learn.poly.cam/hc/en-us/articles/41491709457684); [Canvas FAQ: Accuracy](https://canvas-app-faq.helpscoutdocs.com/article/642-accuracy); [Open Homes: Are CubiCasa or Matterport floor plans accurate?](https://www.open-homes.com/faqs/are-cubicasa-or-matterport-floor-plans-accurate/)
- AI "photo of a plan -> 3D" tools also aim at the German market: ImmoStage (3D-Grundriss from a plan photo) and Rendair (AI 3D view from a 2D plan) — [ImmoStage: 3D Grundriss erstellen aus Foto](https://www.immostage.ai/ratgeber/3d-grundriss-erstellen-aus-foto/); [Rendair DE FAQ](https://rendair.ai/de/faq/can-i-create-a-3d-view-from-a-2d-floorplan-using-ai)

### Inferences
- The low prices of German mass providers (about €25–€70 per floor, see Q6) and their 24–72 h turnaround only make sense with template-based real-estate floor-plan software and standard furniture libraries. Bespoke 3ds Max/Corona scenes cost hundreds of euros. *Which* software each German service uses internally is not published in the material found.
- The output type depends on the tool tier. "Stylised isometric/top-down with standard furniture" comes from RoomSketcher/Cedreo-type tools. "Photoreal hero image with custom materials and lighting" comes from 3ds Max+Corona/V-Ray, SketchUp+V-Ray, Blender Cycles or Lumion.

### Gaps
- No usable sources were found on how often Archicad, Revit or Vectorworks are used for *marketing* 3D floor plans of existing apartments. Floorplanner was not specifically researched.
- No source states which software German services (McGrundriss, Grundriss-Butler, Grundrisstausch) use internally.

## 2. Step-by-step workflow (trace/vectorise -> scale -> walls -> openings -> materials -> furniture -> lighting -> render -> labels)

### Takeaway
All tool tiers follow the same skeleton:
1. Import the plan as an underlay.
2. Calibrate the scale against one known dimension and check it against a second one.
3. Lock the underlay.
4. Trace walls and extrude them to room height.
5. Cut door and window openings.
6. Add floor materials.
7. Merge furniture in a second pass.
8. Remove the ceiling and cut away or lower walls for the 3D "dollhouse" view.
9. Set lighting and camera, then render.
10. Add labels and area annotations.

DWG/CAD input skips the tracing step. Raster/PDF/photo input needs manual tracing or AI conversion.

### Cited Findings
- **Blender:** place the plan image at the world origin, lower its opacity and disable selection so it cannot be moved while modelling. Scale by making a cube of a known plan dimension and scaling the image to match (pivot set to the 3D cursor), then check against other dimensions — [whatmakeart: Scale a Floor Plan in Blender](https://whatmakeart.com/3d-modeling/blender/scale-floor-plan-blender/); [Blenderian tutorial](https://blenderian.com/blender-3d-floor-plan-complete-architectural-modeling-tutorial/)
- **Blender:** trace walls by extrusion or with Archimesh. Cut door and window openings with the knife tool or Archimesh's hole tools — [Blenderian tutorial](https://blenderian.com/blender-3d-floor-plan-complete-architectural-modeling-tutorial/); [Envato Tuts+](https://design.tutsplus.com/tutorials/create-a-3d-floor-plan-model-from-an-architectural-schematic-in-blender--cg-13350)
- **3ds Max + Corona:**
  - Set working units (metres or centimetres) *before* import.
  - Clean the AutoCAD plan, explode groups and put it on a dedicated layer.
  - Import the DWG with layer selection ("Sort by Layer, Split by Material") and place it at the origin.
  - If dimensions come in wrong, fix them with "Rescale World Units".
  - Trace walls with snapping, then extrude them.
  - Furniture/accessories are a second phase: merge models, arrange them from the top view, align them to the floor, and use instances rather than copies.
  - Convert materials to Corona Physical materials and relink missing maps.

  Sources: [Elephorm 3ds Max/Corona course (FR)](https://www.elephorm.com/formation/3d/3ds-max/apprendre-corona-renderer-et-3ds-max-2021-atelier-creatif-darchitecture/reglages-du-logiciel-et-importation-du-plan); [Udemy Archviz Masterclass](https://www.udemy.com/course/m6-archviz-masterclass-in-3ds-max-corona-render/); [Autodesk 3ds Max Design 2011 help: Importing the DWG file (dated)](https://download.autodesk.com/us/3dsmaxdesign/2011/help/files/WS1a9193826455f5ff-e569a012180ce5891326e.htm)
- Common CAD-import problem: broken splines from vertices that do not connect or from duplicate lines. These need linework cleanup. DWG is called the most reliable input because it keeps layers and splines; FBX keeps materials **[vendor blog]** — [Coohom: Import AutoCAD floor plans into 3ds Max](https://www.coohom.com/article/how-to-import-autocad-floor-plans-into-3ds-max-for-modeling)
- **RoomSketcher:**
  - Upload the image.
  - Set the scale by dragging the Scale Bar along a wall of known length, clicking "Set Length" and entering the measurement.
  - Optionally rotate or crop.
  - The image then becomes the tracing layer, or it is AI-converted.

  Sources: [RoomSketcher Help: AI Conversion & Tracing](https://help.roomsketcher.com/hc/en-us/articles/31885247016605); [RoomSketcher Help: Draw a floor plan from a blueprint](https://help.roomsketcher.com/hc/en-us/articles/213842649)
- RoomSketcher can rescale all walls afterwards without changing furniture or fixtures. This is a fix for a wrong initial scale — [RoomSketcher Help: Scale all walls without affecting furniture](https://help.roomsketcher.com/hc/en-us/articles/360000048978)
- By convention, a 3D floor plan has no ceiling, so the view into the rooms is not blocked — [Wikipedia: 3D floor plan](https://en.wikipedia.org/wiki/3D_floor_plan)
- German services sell extras on top of the base 3D plan, which shows the later workflow steps are modular:
  - additional perspectives (for example €23.80 per extra perspective at Grundriss-Butler)
  - a living-area calculation (Wohnflächenberechnung, €59.50)
  - photo-based bathroom, kitchen and floor fit-outs (see Q4)

  Source: [Grundriss-Butler: 3D Grundriss](https://www.grundriss-butler.de/3d-grundriss); [Grundriss-Butler: Preise](https://www.grundriss-butler.de/preise)

### Inferences
- Professional throughput comes from skipping steps: when a DWG exists, tracing disappears. Template tools (RoomSketcher/Cedreo) bundle walls, openings, materials, furniture, lighting and rendering into presets, so a standard apartment takes minutes to hours of operator time. Custom DCC pipelines spend most of their time on furnishing, materials and lighting.
- Labels (room names, m², sometimes dimension lines) are usually added at the end, either automatically by the floor-plan tool or in post-production. The separate price for "bemaßte Grundrisse" (dimensioned plans) at Grundriss-Butler suggests dimensions are an optional add-on, not the default ([Grundriss-Butler: Bemaßte Grundrisse](https://www.grundriss-butler.de/bemasste-grundrisse)).

### Gaps
- Default wall heights and cutaway heights used by German services (for example full height vs. cut at about 1 m) were not found.
- Specific lighting and render settings (for example HDRI plus sun for isometric plans) were not found in the sources reached.

## 3. How is scale set when the plan has no dimensions, and how are inconsistent or inaccurate plans handled?

### Takeaway
The standard method is to calibrate against **one reliably known dimension** (a dimensioned wall, a graphic scale bar or a standard-size element such as a door, bathtub or kitchen worktop) and then **check against a second element**. Distorted scans (taken at an angle, low resolution, rescaled PDFs) are either straightened and recalibrated or redrawn from scratch. When source documents conflict, German services ask clarifying questions and charge for corrections caused by missing or contradictory client input.

### Cited Findings
- On plans without dimensions, users look for standard-size elements (door width, kitchen worktop depth, bathtub width) as scale anchors. Even a door or window gives an approximate result as long as the proportions are right **[forum]** — [Sweet Home 3D forum thread](https://www.sweethome3d.com/support/forum/printthread_thread,7906_printall,yes)
- Worked method: measure the door opening on the plan, convert it, and check that it gives a standard door width as a sanity check — [CodeSignal: Reading & scaling floor plans](https://codesignal.com/learn/courses/measuring-space-at-home/lessons/reading-scaling-floor-plans)
- Cross-check with a second element, for example a bathroom known to be about 5 ft (≈1.52 m) wide because the bathtub is 5 ft long **[forum]** — [r/floorplan thread (via redlib)](https://redlib.hyperreal.coffee/r/floorplan/comments/1kuibi0/help_with_dimensions_of_this_existing_floorplan)
- Scale from one known dimension, then check against others, in Blender — [whatmakeart](https://whatmakeart.com/3d-modeling/blender/scale-floor-plan-blender/)
- Scan distortion comes from photographing the plan at an angle, low resolution or uncalibrated image scaling. Fix: import as a reference layer, set one confirmed measurement as the baseline, and lock the scale before detailing. Small scale errors multiply across the whole drawing and produce large floor-area errors. Redraw instead of patching badly distorted scans **[vendor blog]** — [Coohom: Common scale ruler mistakes](https://www.coohom.com/article/common-scale-ruler-mistakes-in-floor-plans-and-how-to-fix-them); [Coohom: Problems converting floor plans to 3D](https://www.coohom.com/article/common-problems-when-converting-floor-plans-into-3d-models-and-how-to-fix-them)
- Distortion can also come from printing or PDF export. RoomSketcher recommends printing from Adobe Reader and checking the printer's scaling settings — [RoomSketcher Help: Printed floor plan not to scale](https://help.roomsketcher.com/hc/en-us/articles/202332952)
- Practitioners discuss rescaling distorted ground-floor layouts and adjusting imported plans whose dimensions do not add up in SketchUp and Chief Architect **[forum]** — [SketchUcation: Scaling of distorted ground floor layout](https://community.sketchucation.com/post/1167143); [SketchUp forum: dimensions need adjusting](https://forums.sketchup.com/t/new-floor-plan-but-dimensions-need-adjusting/70066); [Chief Architect HomeTalk: measurements don't add up](https://hometalk.chiefarchitect.com/topic/2758-measurements-dont-add-up/)
- German services: only **one source document per plan** should be submitted. Several documents with contradictory information about the same property lead to extensive follow-up questions and longer processing. Corrections are judged against the data supplied at order; further change requests count as paid correction rounds — [Grundriss-Butler: 3D Grundriss](https://www.grundriss-butler.de/3d-grundriss); [Grundriss-Butler: Korrekturschleifen](https://www.grundriss-butler.de/bestellung/korrekturschleifen)
- Simple inputs (hand sketches, old building plans) are accepted. Missing information is clarified before work starts. *(This comes from German provider pages in the result set; the summary did not say exactly which one: [RoomSketcher DE: Grundriss zeichnen lassen](https://www.roomsketcher.de/grundriss-zeichnen-lassen/) and/or [Linsenspektrum blog](https://linsenspektrum.de/blog/3d-grundriss-erstellen-lassen).)*

### Inferences
- In practice, operators check internal consistency. Room dimensions should add up to the overall dimensions, wall thicknesses should be plausible, and standard elements should measure correctly. When the checks disagree, the operator either asks the client for a tape or laser measurement or picks the most reliable dimension and treats the result as "nicht maßstabsgetreu" (not true to scale).
- For German apartments, standard door leaf and opening widths (DIN 18101) and typical ceiling heights would be the natural reference elements. This was **not verified** in this session (see Gaps).

### Gaps
- DIN 18101 standard door dimensions (for example Baurichtmaß 885 mm or 1010 mm) and typical German window/radiator sizes, as scale references, were not looked up and verified here.
- No German provider page found states its exact rule for plans with no dimensions at all (for example "we need at least one dimensioned wall").

## 4. How are room photos used, and are photogrammetry or LiDAR used?

### Takeaway
For 2D-to-3D services, room photos are **optional add-on input** used to match floor coverings, bathroom/WC/kitchen fit-outs and (similar-looking) furniture, usually for a surcharge. They are not used to derive geometry. Geometry comes from the plan. Where no reliable plan exists, professionals measure on site with LiDAR/AR apps (magicplan, Polycam, Canvas, RoomPlan-based apps) or Matterport. For precise dimensions they add a Bluetooth laser distance meter, because LiDAR alone gives centimetre-to-decimetre errors.

### Cited Findings
- German providers: photos are optional but help with bathroom, kitchen and floor covering. One provider's briefing lists existing floor plans, property photos (if available) and style/furnishing wishes. *(Attribution unclear between [Linsenspektrum](https://linsenspektrum.de/blog/3d-grundriss-erstellen-lassen) and [Maverickframe: Grundriss-Visualisierung](https://maverickframe.com/de/leistungen/grundriss-visualisierung/).)*
- A German mass provider sells, as surcharges: bathroom/WC/kitchen fit-out "nach Fotovorlage" (from a photo, about €3 per plan), custom furniture "ähnlich einer Fotovorlage" (similar to a photo), and custom floor coverings (from about €1 per plan per room) — *(prices from a search summary; most likely [Grundrisstausch price table](https://grundrisstausch.de/preistabelle-3d-grundrisse-erstellen-lassen/), not confirmed by a page fetch)*
- Other services build floor plans *from room photos* and ask for each room to be photographed from several angles. Plan-photo services accept JPG/PNG at smartphone quality — [ImmoStage: Grundriss aus Foto](https://www.immostage.ai/grundriss-erstellen/aus-foto/); [ImmoStage: 3D Grundriss aus Foto](https://www.immostage.ai/ratgeber/3d-grundriss-erstellen-aus-foto/) *(attribution of the "several angles" detail is unclear)*
- magicplan: room-scan accuracy depends heavily on lighting. Pairing a Bluetooth laser measure is the recommended route to exact dimensions **[vendor]**. The vendor claims under 1% error for LiDAR auto-scan **[vendor claim]**. In April 2025 it launched "PrecisionLink" for laser-verified field measurements — [magicplan Help: How accurate is magicplan](https://help.magicplan.app/how-accurate-is-magicplan); [magicplan blog: Pen vs Laser vs LiDAR](https://magicplan.app/blog/pen-vs-laser-vs-lidar-floor-plan-comparison); [Claims Journal: magicplan launches PrecisionLink (2025-04-08)](https://amp.claimsjournal.com/services/newswire/2025/04/08/329930.htm)
- Independent tests (2020/2021): LiDAR-only magicplan was fairly weak. LiDAR combined with a Bluetooth laser meter was "spot-on". Average error was about 150 mm in a large test room and about 170 mm in complex rooms, so device-only measurement "should not be relied on when precision matters" **[independent]** — [Mavric Research: MagicPlan with LiDAR (2020)](https://mavricresearch.com/2020/11/10/magicplan-now-with-added-lidar-%F0%9F%A7%82); [Mavric Research: LiDAR contenders (2021)](https://mavricresearch.com/2021/02/02/more-lidar-contenders-how-do-they-measure-up%f0%9f%93%8f/)
- Polycam's LiDAR has a usable range of about 5 m (16 ft). Moving too fast is the most common cause of poor accuracy **[vendor]** — [Polycam: How accurate are Polycam captures](https://learn.poly.cam/hc/en-us/articles/27488763119892); [Polycam: Improving scan accuracy for interiors](https://learn.poly.cam/hc/en-us/articles/34295265957140-Improving-Scan-Accuracy-Best-Practices-for-Interior-Spaces)
- Apple publishes no accuracy figure for its LiDAR scanner or RoomPlan. RoomPlan apps can run on non-LiDAR iPhones but lose a lot of accuracy (Apple developer forum) — [SimplyWise: iPhone LiDAR accuracy 2026](https://www.simplywise.com/blog/iphone-lidar-construction-accuracy/); [Apple Developer Forums: RoomPlan without LiDAR](https://developer.apple.com/forums/thread/776280)
- LiDAR is described as strong for scoping, room dimensions and material rough-out at short indoor range, but it drifts over longer distances — [SimplyWise](https://www.simplywise.com/blog/iphone-lidar-construction-accuracy/)

### Inferences
- In the 2D-plan-plus-photos workflow, photos most likely also serve to check window positions and sill heights, radiators, built-ins, the kitchen layout and floor-material changes that a sketchy plan leaves out. No provider page found states this explicitly beyond floors, bathroom, WC, kitchen and furniture.
- True photogrammetry (reconstructing geometry from ordinary photos) is not part of standard 3D-Grundriss services. Geometry capture on site is done with LiDAR/AR apps or Matterport, and the photos remain visual references.

### Gaps
- No source found describes how German services turn photos into materials (for example matching texture libraries vs. projecting photo textures).
- No independent study of photogrammetry-only (non-LiDAR) floor-plan accuracy was found.

## 5. What do German "3D-Grundriss" providers ask clients to supply?

### Takeaway
German services ask for:
- **one** source plan per floor (photo, scan, PDF, hand sketch or old building plan; smartphone-quality JPG/PNG is fine for some)
- choices made at order time: furnishing, floor coverings, bathroom/kitchen fit-out, number of perspectives, roof type for houses
- optional photos for fit-outs and materials
- add-ons ordered separately: dimensioning and living-area calculation

The key rule is that later changes are judged against what was supplied at order, so a complete brief avoids paid correction rounds.

### Cited Findings
- **One source document per plan.** Contradictory documents cause follow-up questions and delays — [Grundriss-Butler: 3D Grundriss](https://www.grundriss-butler.de/3d-grundriss)
- Accepted inputs: hand sketches, old building plans, scaled drawings. Incomplete documents are possible and gaps are clarified before work starts *(attribution unclear: [RoomSketcher DE](https://www.roomsketcher.de/grundriss-zeichnen-lassen/) / [Linsenspektrum](https://linsenspektrum.de/blog/3d-grundriss-erstellen-lassen))*
- Plan photo or scan upload, JPG/PNG at smartphone quality — [ImmoStage](https://www.immostage.ai/ratgeber/3d-grundriss-erstellen-aus-foto/)
- RoomSketcher's order service accepts sketch, blueprint or existing plan as JPG, PNG or PDF. No subscription is needed for a single order — [RoomSketcher Help: Ordering](https://help.roomsketcher.com/hc/en-us/articles/202273701)
- Options configured at order (Grundriss-Butler): extra perspectives, roof type (the price changes with roof selection, for example €23.80 -> €47.60), living-area calculation €59.50, dimensioned plans as a separate product — [Grundriss-Butler: Preise](https://www.grundriss-butler.de/preise); [Grundriss-Butler: Bemaßte Grundrisse](https://www.grundriss-butler.de/bemasste-grundrisse)
- Correction rounds: corrections are measured against the data supplied at order. Pre-booking a correction round at order is cheaper (3D: €23.80 pre-booked vs €28.56 regular). Unused pre-booked rounds are not refunded. Costs apply per round and per plan/floor — [Grundriss-Butler: Korrekturschleifen](https://www.grundriss-butler.de/bestellung/korrekturschleifen)
- Some studios include one correction round in the visualisation price — [Maverickframe blog: Was kostet eine 3D-Visualisierung (June 2026)](https://maverickframe.com/blog/was-kostet-eine-3d-visualisierung/)
- Photo-based fit-out and floor options are sold as surcharges (see Q4) — [Grundrisstausch price table](https://grundrisstausch.de/preistabelle-3d-grundrisse-erstellen-lassen/) *(attribution probable, not fetched)*

### Inferences
A practical client checklist distilled from these rules (not a single provider's list):
1. A clear, flat, unskewed scan or photo of the plan, or a PDF/DWG.
2. At least one or two verified dimensions, or confirmation that the plan is dimensioned.
3. Room names and use.
4. Wanted furnishing style, or "unfurnished".
5. Floor covering per room.
6. Bathroom/kitchen fit-out photos.
7. Positions of windows, doors, balcony and built-ins if they differ from the plan.
8. Orientation (north arrow) and which perspective(s) are wanted.
9. Whether dimensions or m² labels should be shown.
10. Output format and resolution.
11. Branding or logo.

### Gaps
- Official checklists from immoviewer, McGrundriss and ImmobilienScout24's McGrundriss product could not be read (fetch blocked). No complete published German checklist was retrieved verbatim.

## 6. Typical prices and turnaround in Germany/Europe (2024–2026), per floor plan or per m²

### Takeaway
German providers charge **per floor/plan, not per m²**:
- **Mass real-estate 3D-Grundriss services:** about **€25–€70 per floor** (often capped by room count, for example up to 7 rooms), delivered in **24–72 h or 1–4 working days**.
- **Photographer/agency add-ons:** about **€149–€349** depending on furnishing.
- **Bespoke archviz studios:** about **€250–€600 for a standard apartment** (up to about €1,100 for complex spaces).
- **Per-image interior renders:** €250–€1,500.
- **AI tools:** from about €29.

Internationally, the range runs from about $8 (Fiverr basic) through $38 (RoomSketcher service) and $70 (Bella Virtual) to $299+ (render studios).

### Cited Findings
- **McGrundriss:** 3D graphics from €25. Delivery within 48–72 h if received during office hours — [McGrundriss: Produkte – 3D Graphiken](https://www.mcgrundriss.de/produkte/?p=3DGraphiken). A competitor's comparison gives €24–€42 for 3D and 48 h normal delivery **[competitor source, about 1 year old]** — [RoomSketcher DE: McGrundriss vs RoomSketcher](https://www.roomsketcher.de/blog/mcgrundriss-vs-roomsketcher/); an older article gives 2–3 days — [Neue Immo: McGrundriss](https://neue.immo/mcgrundriss-visualisierung-von-grundrissen/)
- **Grundriss-Butler:** 3D-Grundriss from €41.65 per plan (up to 7 rooms), delivery in 1–4 working days. Extra perspective €23.80. Living-area calculation €59.50 — [Grundriss-Butler: 3D Grundriss](https://www.grundriss-butler.de/3d-grundriss); [Grundriss-Butler: Preise](https://www.grundriss-butler.de/preise)
- **Grundrisstausch** (for real-estate professionals): 3D floor plans "alles inclusive €24.98". It advertises drawing within 24 hours — [Grundrisstausch: Preistabelle 3D](https://grundrisstausch.de/preistabelle-3d-grundrisse-erstellen-lassen/); [Grundrisstausch](https://grundrisstausch.de/)
- **Vienna real-estate photographer:** 3D-Grundriss €149 (standard) / €249 (furnished) / €349 (premium) — [immobilien-fotograf.wien: 3D Grundriss](https://www.immobilien-fotograf.wien/services/3d-grundriss)
- **ImmoStage (AI, from a plan photo):** single package from €29 — [ImmoStage](https://www.immostage.ai/ratgeber/3d-grundriss-erstellen-aus-foto/)
- One provider quotes €69 per floor *(attribution unclear; candidates [immofotografx](https://www.immofotografx.de/grundrisse), [immoyes](https://immoyes.com/3d-grundriss/), [Linsenspektrum](https://linsenspektrum.de/blog/3d-grundriss-erstellen-lassen))*
- Turnaround claims seen across German providers: 3–5 working days standard with 24–48 h express at a surcharge; 3–4 working days; 24 h for 2D and 48 h for 3D *(provider attribution unclear in summary)*
- **German archviz studio (Maverickframe, June 2026):** 3D floor plan €250–€1,100 per plan. Standard apartment €250–€600, complex commercial space up to €1,100. Price driven mainly by complexity and level of detail. One correction round included — [Maverickframe blog](https://maverickframe.com/blog/was-kostet-eine-3d-visualisierung/); [Maverickframe: Grundriss-Visualisierung](https://maverickframe.com/de/leistungen/grundriss-visualisierung/) *(range attributed via search summary)*
- Interior visualisation, per image: €250–€1,500 (German provider in result set) — [Maverickframe blog](https://maverickframe.com/blog/was-kostet-eine-3d-visualisierung/) *(attribution probable)*
- Furnishing/interior-design project with 3D (Diotti): from €450 — [Diotti: 3D-Projekt Wohnbereich](https://www.diotti.com/de/interior-design/ihr-haus-online-einrichten/3d-projekt-wohnbereich)
- Forum (Germany): about €150 for an individual floor plan is called a sign of standardised or automated production with no structural or regulatory check **[forum]** — [bau.de forum: Grundriss digitalisieren](https://bau.de/forum/dig/10121.php). Another forum user recalls "about €50 net per floor in 3D" **[anecdotal, unverified]** — [KNX-User-Forum: 3D Grundriss](https://knx-user-forum.de/forum/öffentlicher-bereich/knx-eib-forum/1282574-3d-grundriss)
- **RoomSketcher order service:** pay-as-you-go **USD 38 per floor** (other pages say "from USD 20"; subscriptions get better rates). Delivered the next business day, except 1 Jan, 1 May and 25 Dec; large orders take longer — [RoomSketcher: Order Floor Plans](https://www.roomsketcher.com/order-floor-plans/); [RoomSketcher Help: Delivery terms](https://help.roomsketcher.com/hc/en-us/articles/4410169574417)
- **Bella Virtual:** 3D floor plans from $69.95 per plan, 2–4 business days — [Bella Virtual: 3D Floor Plans](https://www.bellavirtual.com/pages/3d-floor-plans)
- **Render3DQuick (2026 guide):** 3D floor plans from $299 per floor, 3–4 days. Some done in 24–48 h; custom colours and textures take longer — [Render3DQuick: 2026 cost of renderings](https://render3dquick.com/blog/how-much-does-3d-rendering-cost); [Render3DQuick FAQ](https://www.render3dquick.com/faq)
- An international guide (in German translation) gives apartment 3D floor-plan rendering at $250–$1,500 with 3–7 days — [MyArchitectAI: Kosten für 3D-Rendering 2026](https://www.myarchitectai.com/de/blog/3d-architectural-rendering-cost) *(attribution probable)*
- **Freelance marketplaces:** Fiverr tiers from $8/$40/$75; others $100–$200 with 9-day delivery; 3ds Max sellers often 2–4 days. Upwork: $150–$400 for a SketchUp model and $150–$500 per V-Ray render **[seller-stated]** — [Fiverr: 3D floor plan quick](https://fiverr.com/jessica_3d/create-3d-floor-plan-a-fast-and-beautiful); [Upwork: 3D floor plan renderings](https://www.upwork.com/services/product/design-beautiful-3d-floor-plan-renderings-1315445415368032256)

### Inferences
- **Per-m² pricing is not used** by any provider found. Dividing gives a rough order of magnitude: for a 70 m² apartment, mass services come to about €0.35–€1/m² and bespoke studios to about €3.50–€8.50/m². This is a derived figure, not a market price.
- Price drivers: number of rooms or floors, furnishing (standard vs. photo-matched), custom materials, number of perspectives, dimensioning or area calculation, correction rounds, and express delivery.

### Gaps
- immoviewer and ImmobilienScout24 (McGrundriss) price pages could not be fetched.
- No independent German price survey from 2024–2026 was found; all figures are provider self-statements.
- VAT treatment (net vs. gross) is often unclear in the summaries. Grundriss-Butler's €41.65 / €23.80 / €59.50 look like gross prices (multiples of 1.19), but this is not confirmed.

## 7. What accuracy tolerances are typical, and how is uncertainty communicated?

### Takeaway
A 3D-Grundriss traced from a plan is only as accurate as its source plan and the chosen scale reference. Errors are typically quoted as **about 1–2% of length** for good capture systems (Matterport, Canvas, magicplan, all vendor claims). Independent and forum tests show **10–17 cm errors in complex rooms** with LiDAR alone, and **area differences of about 7–10%** from schematic plans. Providers communicate uncertainty mainly through disclaimers ("for visualisation, not to scale/estimated dimensions"), by making the client responsible for input data, and by selling dimensioning and area calculation as separate, explicitly accountable products.

### Cited Findings
- **Matterport:** measurements are "generally accurate to within 1% of reality"; floor-plan linear measurements between opposing walls are "generally accurate to within 0 to 2%". No claim is made about square footage **[vendor claim, quoted via forum]**. 1% equals about 6 in over 50 ft (≈15 cm over 15 m). One user reports a schematic plan 280 sq ft (9.2%) below an appraiser's figure **[forum]** — [We Get Around Network: How accurate are Matterport 2D schematic floor plans](https://wegetaroundnetwork.com/topic/10105/how-accurate-are-matterport-2d-schematic-floor-plans-use-sq-ft-in-mls)
- Open Homes (2026) concludes that Matterport/CubiCasa plans are not accurate enough for square-footage calculations and recommends professionally drafted plans where area matters — [Open Homes FAQ](https://www.open-homes.com/faqs/are-cubicasa-or-matterport-floor-plans-accurate/)
- Houssmax claims over 7% discrepancy for schematic plans vs. under 4% for its own measured plans **[competitor marketing]**. Discrepancies usually come from hidden closets and wrong exterior-wall thickness — [Houssmax support](https://support.houssmax.ca/?p=383); Matterport-style plans give "estimated dimensions suitable for visualization but not precise architectural measurements" **[vendor blog]** — [Coohom: Accuracy limits of automated Matterport floor plans](https://www.coohom.com/article/accuracy-limits-of-automated-matterport-floor-plans)
- **Polycam:** standard interior accuracy ±½ in (≈±1.3 cm); larger spaces (>5,000 ft² ≈ 465 m²) vary more **[vendor]**. A blog post claims up to 98% accuracy in optimal conditions **[vendor, different metric]** — [Polycam Help: How accurate are Polycam scans](https://learn.poly.cam/hc/en-us/articles/50434745985556-How-Accurate-Are-Polycam-Scans); [Polycam blog: Best floor plan software compared](https://poly.cam/blog/best-floor-plan-software-compared-accuracy-speed-and-cost-for-every-budget)
- **Canvas:** "99% accurate on most measurements" **[vendor]**. A company rep on the Chief Architect forum says 1–2% when scanned correctly and admits it may not suit users needing 1/8-in (3 mm) accuracy on a first visit. One user reports about 10% error per room **[forum]** — [Canvas FAQ: Accuracy](https://canvas-app-faq.helpscoutdocs.com/article/642-accuracy); [ChiefTalk: Canvas.io warning thread](https://chieftalk.chiefarchitect.com/topic/33908-canvasio-warning-output-verry-verry-verry-bad-then-they-ripped-me-off-on-the-price)
- **magicplan:** under 1% claimed for LiDAR auto-scan **[vendor]**, vs. about 150–170 mm average error measured independently in large or complex rooms (LiDAR/corner modes) **[independent, 2020–21 hardware]** — [magicplan blog: LiDAR auto scan](https://magicplan.app/blog/lidar-auto-scan); [Mavric Research 2021](https://mavricresearch.com/2021/02/02/more-lidar-contenders-how-do-they-measure-up%f0%9f%93%8f/)
- **RoomPlan-based app (RoomScan Pro):** about 1 in (≈1–3 cm) in normal rooms, which counts as documentation/scoping accuracy, not the sub-centimetre control needed for permit or fabrication drawings **[single review]** — [illustrarch: RoomScan Pro review](https://illustrarch.com/articles/design-softwares/110334-roomscan-pro-review.html). A Polycam/RoomPlan test found larger discrepancies in a small room with posts and obstacles in the corners — [lidar3d.io: Testing the precision of Apple's RoomPlan API](https://www.lidar3d.io/post/testing-the-precision-of-apple-s-ios-roomplan-api-a-polycam-lidar-3d-scanning-app-feature-review)
- Scale errors from the source plan multiply across the drawing and grow into large area errors — [Coohom: Scale ruler mistakes](https://www.coohom.com/article/common-scale-ruler-mistakes-in-floor-plans-and-how-to-fix-them)
- How uncertainty is handled contractually (Germany): corrections are tied to the data the client supplied at order — [Grundriss-Butler: Korrekturschleifen](https://www.grundriss-butler.de/bestellung/korrekturschleifen). Low-cost plans come with no structural or regulatory check, and an architect or Bauzeichner is needed for permit-grade plans **[forum]** — [bau.de forum](https://bau.de/forum/dig/10121.php)

### Inferences
- For a marketing 3D-Grundriss, a realistic expectation is that it is **proportionally faithful to the source plan** (within the line weight of the trace, a few cm at apartment scale). Absolute accuracy is limited by the source plan's own errors. For old or undimensioned plans scaled from a door width, errors in the range of a few percent of length are plausible (door widths vary by ±5–10 cm), and area errors are about twice the linear percentage. This is an estimate derived from the findings, not a measured figure.
- Best practice for communicating uncertainty:
  - label the plan "nicht maßstabsgetreu / Maße circa / ohne Gewähr" (not to scale / approximate dimensions / no warranty)
  - show room areas only if they come from a proper Wohnflächenberechnung
  - state the scale reference used
  - keep a verified-dimension list

### Gaps
- The exact wording of German providers' disclaimers ("unverbindlich", "nicht maßstabsgetreu", "Abweichungen möglich") could not be checked because the pages could not be fetched.
- No German source was found that quantifies typical deviations between 3D marketing floor plans and Wohnfläche under the WoFlV (German living-area ordinance).
- No controlled, peer-reviewed benchmark of iPhone LiDAR/RoomPlan on current (2024–2026) hardware was found. The independent magicplan figures date from 2020–21.
