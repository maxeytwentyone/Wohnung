# Interactive Browser-Based 3D Apartment Planners & Web Rendering Techniques for a Professional Look

> Method note for the report writer: Research was done 2026-11-06 via web search. Direct page fetches of threejs.org, discourse.threejs.org and drei.docs.pmnd.rs failed in this session (host not reachable from the sandbox), and the GitHub API for mrdoob/three.js was not available. Most citations therefore point at URLs whose content I saw only as search-result excerpts and summaries, not full pages. Vendor feature claims mostly come from help centers (good) or from review/aggregator sites (weaker); both kinds are labeled. Points under "Inferences" that rest on general three.js practice I could not check against a source this session are marked **[background, unverified]**.

## 1. What features do leading interactive planners offer, and how does their UI work?

### Takeaway
The leading planners all offer roughly the same core: draw walls and rooms in 2D with automatic dimensions and areas, switch to 3D with one click, view the 3D model either from an orbiting "dollhouse" camera above or by walking through at eye level, drag furniture from a large catalogue with snapping to walls and other pieces, and make renders or images. They differ mainly in catalogue size, rendering quality (live WebGL vs. photoreal cloud renders), scanning/AR (IKEA Kreativ, Roomle) and how they show the interior through the walls (see Q4).

### Cited Findings

**RoomSketcher**
- Has a "Live 3D" walkthrough for checking circulation and spacing. Walkthroughs can be shared for feedback, and some 3D features are paid add-ons. — [RoomSketcher space planning](https://www.roomsketcher.com/floor-plans/space-planning-software/)
- Offers a first-person eye-level view in the 3D screen. Walls snap neatly and rooms stay to scale in 2D. The furniture library (>4,000 items per the vendor) is called decent but weaker than SketchUp 3D Warehouse. — [MacHow2 review](https://machow2.com/roomsketcher-review/); [RoomSketcher](https://www.roomsketcher.com/floor-plans/space-planning-software/)
- Walls can be moved and resized directly, and many objects support drag-and-drop. — [FileHorse](https://www.filehorse.com/download-roomsketcher/)
- Furniture snaps to a wall automatically when moved close to it, and snapping can be switched on or off. — [RoomSketcher Help: snapping](https://help.roomsketcher.com/hc/en-us/articles/115001610525)
- Wall "cut height" is set per floor, and items above it are removed from the plan view. The 3D preview ignores the cut height and always shows all items. — [RoomSketcher Help: wall height](https://help.roomsketcher.com/hc/en-us/articles/360014732378)
- User complaint: "snap in place" while moving furniture in 3D does not always land where wanted, so users need workarounds. — [Capterra reviews](https://www.capterra.com/p/164021/RoomSketcher/reviews/?page=2)

**Planner 5D**
- Drag-and-drop design in 2D and 3D modes with a seamless switch, plus a "virtual walk-through" view of the result. — [App Store listing](https://apple.co/2UO1Sws); [Planner 5D vs Floorplanner (vendor blog)](https://planner5d.com/blog/planner-5d-vs-floorplanner/)
- Catalogue size differs by source and date: 5,000+, 6,000, and 8,400+ items. The free tier limits the catalogue and furniture customization. — [App Store](https://apple.co/2UO1Sws); [Planner 5D blog](https://planner5d.com/blog/planner-5d-vs-floorplanner/) (the figures conflict, probably because they come from different years)
- The 2D/3D switch sits in the editor menu on web and macOS. iOS and Android use a 3D button, and Windows uses a mode switch in the app menu. — [Planner 5D Help: 3D mode](https://support.planner5d.com/en/articles/15112460-how-to-use-3d-mode)
- Rotation on touch: tap an item to get a selection frame, then drag a small green rotation handle. — [Planner 5D Help: rotate items](https://support.planner5d.com/en/articles/15859960-how-to-rotate-items)

**Floorplanner**
- The 3D view is one click from the 2D plan and is generated from the walls, openings and furniture placed, with no separate modelling. The library holds over 260,000 3D models at no extra cost, filterable by room and furniture type. — [Floorplanner.com](https://floorplanner.com/); [Capterra](https://www.capterra.com/p/164017/Floorplanner/)
- Free accounts get SD 2D/3D images and paid tiers get HD; the vendor claims renders up to 8K. Renders are made in the cloud. — [Floorplanner.com](https://floorplanner.com/); [illustrarch review](https://illustrarch.com/interior-design/floor-plans/111930-floorplanner-review.html)
- 2018 editor manual: wall thickness and height are set before drawing, dimensions appear automatically, clicking the inner dimensions lets you type an exact room size, a space enclosed by walls becomes a room with a floor surface automatically, zooming far enough in the 3D view puts you inside a room, and a camera button creates a render of the current view that is emailed. — [Floorplanner editor manual (2018)](https://cdn.floorplanner.com/static/brochures/Floorplanner+editor+manual+version+050718.pdf) (old; the current UI may differ)
- I found no evidence of an auto-furnish feature. — [Capterra](https://www.capterra.com/p/164017/Floorplanner/)

**Homestyler**
- Runs entirely in the browser with no install. Its strengths are photorealistic renders, material fidelity, lighting realism and 360° panoramas. It also has AI sketch-to-render and layout suggestions. — [Homestyler vs RoomSketcher (vendor article)](https://www.homestyler.com/article/trends/choosing-between-homestyler-and-roomsketcher); [Homestyler FAQ](https://www.homestyler.com/learn/faq)
- Sources conflict on whether free cloud renders are watermarked or capped, and on whether "flexible material switching" is Pro-only. — [Homestyler FAQ](https://www.homestyler.com/learn/faq) vs. third-party reviews in the same search

**IKEA Kreativ**
- The mobile app captures the room, either as a photo-based "wide-angle scan" or a LiDAR "full room scan" on supported iOS devices. Designing works on mobile and web, but capture is mobile-only. — [IKEA Help: scan a room](https://www.ikea.com/gb/en/customer-service/knowledge/articles/250fg37g-2498-40gg-916c-f27d354683f0.html); [IKEA newsroom AU](https://www.ikea.com/au/en/newsroom/range-news/ai-powered-design-experience-ikea-kreativ-launches-pubcf6362b0/)
- An Eraser tool (with "Hide all", "Show all", and clicking yellow-outlined items) removes existing furniture from wide-angle scans. Full-room scans start empty. More than 50 furnished, semi-furnished or empty 3D showrooms are available. — [IKEA Help: clear out space](https://www.ikea.com/ie/en/customer-service/knowledge/articles/eb340375-ede4-419g-9e19-gcb8178021gf.html); [Engadget](https://www.engadget.com/ikea-ar-app-lets-you-preview-its-furniture-in-your-own-house-130004284.html)
- Product rotation sits in an "Action Panel". On mobile it appears as a slider. — [IKEA Help: interact on web](https://www.ikea.com/be/en/customer-service/knowledge/articles/cfca8e04-6083-4943-9094-bfbbfcc62d43.html); [IKEA Help: interact on mobile](https://www.ikea.com/in/en/customer-service/knowledge/articles/81fe36ec-cd36-4146-a4fd-8d02edb196fc.html)

**Roomle**
- Roomle retired its old Unity-based Web Planner. 3D room planning and AR now run in the iOS app. — [Roomle sunset notice](https://roomle.com/en/sunset-webapp)
- B2B focus: furniture configurators, live 3D configuration, DXF floor-plan import, and browser AR via ARKit/ARCore with no app. Paid tiers include a material configurator from about €280/month and a room designer from about €650/month. — [Roomle floorplanner](https://roomle.com/floorplanner); [KI-Syndikat review (DE)](https://www.ki-syndikat.de/tools/roomle/) (prices from a third party)

**Matterport (dollhouse, from scanned real spaces)**
- The Showcase web viewer has Dollhouse, Floor Plan and walk-through views, plus a measurement mode: click two points to get a length, with a metric/imperial switch, usable by anyone with the link in a browser. — [Matterport Academy: Intro to Showcase](https://matterport.com/matterport-academy/intro-to-showcase/intro-to-showcase); [Invision Studio](https://invisionstudio.com/measure-twice-shoot-once-how-matterport-3d-tours-make-property-dimensions-easy/)
- Measurement lines drawn in one view do not carry over to the others. Dollhouse navigation: left-drag moves, right-drag rotates. — [WeGetAround video/forum](https://www.wegetaroundnetwork.com/topic/12734/video-understanding-matterport-mesh-view-keyboard-tips-for-matterport/) (secondary source)
- SDK 25.4.1 makes a "unified dollhouse and floorplan mode" the default, with mouse behaviour matching the former floorplan mode. A URL parameter turns it off. — [Matterport Showcase SDK changelog](https://matterport.github.io/showcase-sdk/sdk_changelog.html)

**Sweet Home 3D (open-source desktop/Java, also an online version)**
- You draw in 2D while watching a live 3D view, which offers an "aerial view" (orbit) and a "virtual visit" (eye-level visitor). — [Neowin: Sweet Home 3D 7.0](https://www.neowin.net/software/sweet-home-3d-70/); [klaatu guide](https://gopherproxy.meulie.net/sdf.org/0/users/klaatu/techfiles/home3d.md)
- Version 3.5 added edge-to-edge furniture magnetism and better magnetism along walls, including round walls, with a collision check. Version 7.0 added a toolbar button to toggle magnetism. — [windowsforum.kr (3.5 changelog mirror)](https://windowsforum.kr/data/3276551); [Neowin 7.0](https://www.neowin.net/software/sweet-home-3d-70/)

**Houzz Pro (a useful reference for dollhouse settings)**
- Floor-plan view settings include a toggle for room-area labels. Dollhouse settings include a "Show Cutaway Walls" checkbox. — [Houzz Pro Help: 3D settings](https://pro.houzz.com/pro-help/r/how-to-adjust-3d-floor-plan-settings)

### Inferences
- The baseline feature set a "professional" web planner is expected to have: a 2D plan with live dimensions and room areas; a 3D dollhouse orbit view; a first-person walk mode; drag-and-drop catalogue items with wall and edge snapping that can be toggled; rotation; a material/colour picker; a wall cutaway setting; and image or render export. Live WebGL is used for editing, while "photoreal" output is usually a separate cloud render (Floorplanner, Homestyler). I saw no evidence that any vendor achieves photorealism in the live view.
- Clearance checks such as walkway width or door-swing collisions are rare and set a product apart (see Q2, Madegood).

### Gaps
- I could not open RoomSketcher's or Floorplanner's current help pages on 3D cutaway modes, so their exact 2026 cutaway UI is unconfirmed.
- I found no source on the rendering technology of the current Planner 5D or Homestyler web viewers (WebGL engine, post-processing).
- I found no reliable data on whether these planners offer m² per room in the 3D view, as opposed to only in 2D.

## 2. Which UI/UX patterns make furniture placement intuitive on desktop and on mobile/touch?

### Takeaway
The common pattern is: tap or click to select, which shows a selection frame; drag to move along the floor plane; rotate with a dedicated handle or ring that snaps to 45° steps (or a slider on mobile); snap to walls and other edges automatically, with a modifier key or toggle to turn snapping off; and give clear visual feedback for conflicts. On touch, one-finger drag on empty space pans or orbits and pinch zooms, so dragging an object must start on a selected object to avoid gesture conflicts.

### Cited Findings
- Planner 5D on iPhone/iPad: tap → selection frame → drag the small green rotation handle. — [Planner 5D Help](https://support.planner5d.com/en/articles/15859960-how-to-rotate-items)
- Houzz Pro: a rotate ring that can be dragged freely or snapped in 45° steps, plus alignment aids for lining items up. — [Houzz Pro Help: move items](https://pro.houzz.com/pro-help/r/how-to-perfectly-line-up-floor-plan-items)
- IKEA Kreativ mobile: rotation is a slider in an Action Panel rather than a direct-manipulation handle. — [IKEA Help (mobile)](https://www.ikea.com/in/en/customer-service/knowledge/articles/81fe36ec-cd36-4146-a4fd-8d02edb196fc.html)
- RoomSketcher: snaps to a wall when an item comes close, and the toggle is in settings. — [RoomSketcher Help](https://help.roomsketcher.com/hc/en-us/articles/115001610525)
- ArchiSketch: hold Ctrl to move or rotate freely without snapping. — [ArchiSketch docs](https://docs.archisketch.com/user-en/arranging-furniture/furniture-placement)
- Sweet Home 3D: magnetism to edges and walls with a collision check, and a toolbar toggle. — [windowsforum.kr](https://windowsforum.kr/data/3276551); [Neowin](https://www.neowin.net/software/sweet-home-3d-70/)
- Phone gesture scheme in a consumer planner: tap to select, drag to move, drag empty space to pan. Pinch to zoom in another app. — [Madegood Room Planner](https://madegooddesigns.com/?p=138074); [Room Layout Planner (App Store)](https://apps.apple.com/app/id6759184642)
- Constraint feedback: Madegood outlines in red any walkway narrower than 90 cm, wardrobes, desks or sideboards without room in front, furniture in a door's swing, and anything that overlaps or sticks out of the room. — [Madegood Room Planner](https://madegooddesigns.com/?p=138074)
- A RoomSketcher user complaint shows that snapping in 3D can feel unpredictable. — [Capterra](https://www.capterra.com/p/164021/RoomSketcher/reviews/?page=2)

### Inferences
- **[background, unverified]** In three.js, the usual approach is to raycast against an invisible floor plane, which avoids depth jitter, and to move the object only in XZ. During a drag, disable `OrbitControls` (`controls.enabled = false`) and re-enable it on pointerup. Use Pointer Events (`pointerdown/move/up` + `setPointerCapture`) so mouse, pen and touch share one code path. Set CSS `touch-action: none` on the canvas.
- **[background, unverified]** Snapping in plan space: compute the nearest wall segment, and if the object's back edge is within a threshold (for example 10–15 cm), set its rotation to the wall's angle and push it flush against the wall's inner face. Edge snapping to other furniture uses 2D OBB (oriented bounding box) tests in the XZ plane, which also serve as cheap collision detection.
- Showing a live dimension readout while dragging (distance to the nearest walls) and room m² labels are typical "professional" cues, as in Houzz room-area labels and the Floorplanner manual's automatic dimensions ([Houzz](https://pro.houzz.com/pro-help/r/how-to-adjust-3d-floor-plan-settings); [Floorplanner manual](https://cdn.floorplanner.com/static/brochures/Floorplanner+editor+manual+version+050718.pdf)).
- On mobile, a bottom-sheet action panel (rotate, duplicate, delete, material) is more reliable than small on-canvas handles, as IKEA's slider choice suggests.

### Gaps
- I found no source documenting two-finger twist-to-rotate for furniture in any of the named planners.
- I found no usability studies comparing handle-, slider- and gesture-based rotation.

## 3. Which Three.js/WebGL rendering techniques create a professional archviz look?

### Takeaway
A current (r152+, ideally r16x–r18x) three.js setup for a polished floor plan needs:
- correct colour management (sRGB output, and sRGB colour textures marked as such);
- PBR `MeshStandardMaterial`/`MeshPhysicalMaterial` lit by a PMREM-processed environment, either `RoomEnvironment` or an HDRI;
- a filmic tone mapper (AgX from r160, Khronos PBR Neutral from r162, or ACES);
- soft shadows, ideally baked or accumulated once because a floor plan is static;
- screen-space AO such as N8AO;
- MSAA or SMAA anti-aliasing.

Several older APIs have been renamed or removed: `outputEncoding`, `texture.encoding`, `GammaCorrectionShader`, `PCFSoftShadowMap` (r182), and the stencil buffer is no longer on by default (r163).

### Cited Findings

**Colour management (r152 and later)**
- In r152, `renderer.outputEncoding` became `renderer.outputColorSpace` and `texture.encoding` became `texture.colorSpace`. Output now defaults to sRGB, `THREE.ColorManagement.enabled` defaults to true, and CSS/hex colours are treated as sRGB. — [three.js forum: Updates to Color Management in r152](https://discourse.threejs.org/t/updates-to-color-management-in-three-js-r152/50791)
- With post-processing, replace the old `GammaCorrectionShader` pass with `OutputPass`. Custom `ShaderMaterial`s need the tone-mapping and colour-space shader chunks included. — [r152 thread](https://discourse.threejs.org/t/updates-to-color-management-in-three-js-r152/50791)
- After upgrading, scenes can look different, with less contrast, and lighting or tone mapping may need re-tuning. — [forum: palette change 150→152](https://discourse.threejs.org/t/why-the-color-palette-change-from-v0-150-1-to-v0-152-2/51417)

**Tone mapping**
- `AgXToneMapping` arrived in r160, and the gamut-mapping step was added in r161. — [forum: Is AgX implemented correctly?](https://discourse.threejs.org/t/is-agx-tonemapping-implemented-correctly/60609); [three.js issue #27362](https://github.com/mrdoob/three.js/issues/27362)
- `NeutralToneMapping` (Khronos PBR Neutral) needs r162 or later and was updated in r163. — [r162 release notes](https://newreleases.io/project/github/mrdoob/three.js/release/r162); [r163 release](https://www.github.com/mrdoob/three.js/releases/tag/r163)
- AgX is Blender 4.x's default view transform (Filmic was 3.x's), which matters for matching Blender-baked assets. — [forum: matching Blender with three.js](https://discourse.threejs.org/t/matching-blender-with-threejs-colors/60716/3)
- pmndrs `postprocessing` / react-postprocessing provide their own ToneMapping effect with modes including AgX and Neutral. — [react-postprocessing ToneMapping](https://react-postprocessing.docs.pmnd.rs/effects/tone-mapping); [pmndrs ToneMappingMode](https://pmndrs.github.io/postprocessing/public/docs/file/src/enums/ToneMappingMode.js.html)

**Environment lighting**
- `RoomEnvironment` is a procedural studio-room `Scene`. Pass it to `new PMREMGenerator(renderer).fromScene(new RoomEnvironment())` and assign `.texture` to `scene.environment`, and all PBR materials receive image-based lighting without a per-material `envMap`. `DebugEnvironment` is for development only, and `RoomEnvironment` is recommended for production. — [three.js docs: RoomEnvironment](https://threejs.org/docs/pages/RoomEnvironment.html); [DebugEnvironment](https://threejs.org/docs/pages/DebugEnvironment.html)
- PBR lighting from `scene.environment` is only correct if the map is PMREM-processed. A higher-quality source HDR (4K) improved results more than a larger PMREM target did (one user's report). — [forum: environment map quality](https://discourse.threejs.org/t/environment-map-quality-problem/24921)
- Regenerating PMREM every frame is very slow. Build it once. — [forum: animating PMREM](https://discourse.threejs.org/t/bad-performances-when-animating-a-pmremgenerator-environment/48043)

**Shadows**
- `PCFSoftShadowMap` was removed in r182 because the reworked `PCFShadowMap` is already soft. There is no automatic fallback, and some users report pixelation and point-light bias issues after upgrading. — [forum: shadow pixelation r182](https://discourse.threejs.org/t/shadow-pixelation-issue-in-three-js-0-182-0/88746); [forum: r182 point light shadows](https://discourse.threejs.org/t/upgrading-to-r182-incorrect-point-light-shadows/88891)
- Sources disagree on whether `shadow.radius` has an effect under `PCFShadowMap` or `PCFSoftShadowMap`. One commenter says all three types now share an implementation that uses radius, but that claim concerns point lights only. — [forum: WebGPU shadow tests](https://discourse.threejs.org/t/webgpu-shadow-tests-and-findings/82561) (unresolved)
- drei `AccumulativeShadows` + `RandomizedLight`: a planar shadow catcher that accumulates many jittered-light frames into soft, raytrace-like shadows and AO, with "zero performance impact after all frames have accumulated". Defaults are `frames=40` and `limit=20`, and `temporal` spreads the accumulation over frames. — [drei docs: AccumulativeShadows](https://drei.docs.pmnd.rs/staging/accumulative-shadows); [drei staging docs mirror (tessl)](https://tessl.io/registry/tessl/npm-react-three--drei/files/docs/staging.md)
- drei `ContactShadows` defaults to `frames=Infinity`. Use `frames={1}` for static scenes. — [R3F lighting guide](https://www.remoteopenclaw.com/skills/enzed/r3f-skills/r3f-lighting) (community); [tessl drei mirror](https://tessl.io/registry/tessl/npm-react-three--drei/files/docs/staging.md)
- The forum consensus for "Airbnb-ad-like" stylised interiors: bake soft shadows for static scenes, because real-time soft shadows are costly. — [forum: Airbnb ad scene](https://discourse.threejs.org/t/three-js-scene-like-in-airbnb-ad/68281)

**Ambient occlusion**
- N8AO: in vanilla three.js, `N8AOPass` replaces `RenderPass` in the `EffectComposer`. For pmndrs postprocessing, use `N8AOPostPass` after a `RenderPass`. Key parameters are `aoRadius` (world units), `distanceFalloff`, `intensity` (2 is subtle, 5 is strong) and `color`. Version 2.0 computes AO at half resolution and upsamples. — [N8AO GitHub](https://github.com/N8python/n8ao); [react-postprocessing N8AO](https://react-postprocessing.docs.pmnd.rs/effects/n8ao)
- For WebGPU/TSL, three.js ships `GTAONode` (and SSGI), and a community port `n8ao-webgpu` requires three ≥ 0.182. — [three.js docs: GTAONode](https://threejs.org/docs/pages/GTAONode.html); [n8ao-webgpu](https://github.com/MarioAndF/n8ao-webgpu)

**Anti-aliasing**
- pmndrs `EffectComposer` has a `multisampling` option (WebGL2 MSAA for its buffers; 0 disables it). The sample count cannot be changed after the buffers are created, so the composer rebuilds them. — [pmndrs EffectComposer source](https://pmndrs.github.io/postprocessing/public/docs/file/src/core/EffectComposer.js.html); [forum: multisample sample count](https://discourse.threejs.org/t/updating-sample-count-on-webglmultisamplerendertarget/14224)
- react-postprocessing uses WebGL2 MSAA by default. If some effects show artefacts, set `multisampling={0}` and use an SMAA pass. — [react-postprocessing SMAA](https://react-postprocessing.docs.pmnd.rs/effects/smaa)

**Section caps / cut walls**
- The three.js `webgl_clipping_stencil` technique fills a clipping-plane cut with a solid cap. It needs watertight, non-overlapping geometry. Since r163 the `WebGLRenderer` `stencil` context attribute defaults to false, so pass `stencil: true`. Caps can flicker unless the cap plane is placed along the clip-plane normal. — [forum: render caps like webgl_clipping_stencil](https://discourse.threejs.org/t/how-to-render-caps-like-webgl-clipping-stencil/36727); [forum: clipping plane stencil capping](https://discourse.threejs.org/t/clipping-plane-stencil-capping/74018); [forum: capping BufferGeometry](https://discourse.threejs.org/t/capping-clipped-planes-using-stencil-on-a-buffergeometry/18407); [forum: merged faces cap misalignment](https://discourse.threejs.org/t/clipping-geometry-made-from-merged-faces-stenciled-cap-face-not-aligning-properly/19280); [forum: cut section with filled surface](https://discourse.threejs.org/t/creating-a-cut-section-with-a-filled-surface/69464)

### Inferences
- **Recommended pipeline [background, unverified in detail]:**
  - Renderer: `new WebGLRenderer({ antialias: true })` (MSAA when not using a composer); `outputColorSpace = SRGBColorSpace` (the default); `toneMapping = AgXToneMapping` or `NeutralToneMapping` with `toneMappingExposure` about 1.0–1.2.
  - Lighting: `scene.environment = pmrem.fromScene(new RoomEnvironment(), 0.04).texture`, plus one shadow-casting `DirectionalLight` acting as the "sun through the window", with a tight orthographic shadow camera fitted to the apartment's bounds and `mapSize` 2048 on desktop / 1024 on mobile.
  - Post-processing: `RenderPass` → `N8AOPass` (or `GTAOPass`/`SAOPass`) → `OutputPass`, or a pmndrs composer with `multisampling` / SMAA.
  - Why Neutral: Khronos PBR Neutral aims to keep base colours close to their sRGB values, which suits furniture and flooring colour fidelity. AgX gives a more filmic, desaturated highlight roll-off.
- **Static scene = bake or accumulate:** An apartment plan is mostly static, so the best cost-to-quality approach is to (a) bake AO and lightmaps in Blender for walls and floors (exported as glTF with `aoMap`/`lightMap`), or (b) render shadows once (`renderer.shadowMap.autoUpdate = false`; set `needsUpdate = true` after a furniture edit), or (c) use drei `AccumulativeShadows` on the floor plane. This follows from the "zero cost after accumulation" and "bake for static" findings above.
- **PBR materials and procedural textures [background]:** Wood floors and tiles can be generated procedurally on a `<canvas>` (planks with colour jitter and seams; a tile grid with grout lines) as `CanvasTexture` with `colorSpace = SRGBColorSpace` for albedo. Roughness and normal maps stay linear (`NoColorSpace`). Use `RepeatWrapping` with `repeat` tied to metres (for example one texture repeat per 1 m) so texel density stays constant across rooms, and set `anisotropy = renderer.capabilities.getMaxAnisotropy()` for floors seen at grazing angles. Keep floor roughness around 0.4–0.7 so the environment map gives subtle sheen without mirror-like reflections.
- **Edge outlines [background]:** A crisp "architectural model" look comes from `EdgesGeometry(geom, thresholdAngle≈20–30°)` + `LineSegments` in dark grey. WebGL ignores `linewidth > 1`, so use `LineSegments2`/`LineMaterial` from `three/addons/lines/` for thicker lines. A screen-space alternative is `OutlinePass` (highlighting selected items) or a normal/depth edge-detection pass.
- **Camera [background]:** Use an `OrthographicCamera` for a clean top-down "plan" view (no perspective distortion, which suits dimension lines and m² labels) and a `PerspectiveCamera` with a moderate FOV (about 35–50°) for the dollhouse orbit. First-person walk mode uses eye height about 1.6 m and FOV about 60–75°. `OrbitControls` should limit `maxPolarAngle` (for example < 85°) so the camera never goes under the floor, and clamp `minDistance`/`maxDistance`. `MapControls` suits the plan view.
- **Dark wall caps [background]:** Lowered or cut walls read best with a dark (near-black or charcoal) top face, the architectural "poché". If the walls are generated procedurally as extruded wall polygons (`ExtrudeGeometry`/custom BufferGeometry), the simplest method is to give the top face its own material group in dark grey. That avoids stencil capping entirely. Stencil caps are only needed when cutting arbitrary imported meshes with a clipping plane.
- Deprecated or legacy approaches to avoid: `outputEncoding`/`sRGBEncoding`, `GammaCorrectionShader`, `PCFSoftShadowMap` (removed in r182), `WebGLMultisampleRenderTarget` (old; MSAA now goes through the `samples` option on render targets **[background]**), and relying on `linewidth` for thick lines.

### Gaps
- I could not open threejs.org docs or release notes directly to verify exact version numbers (AgX r160, Neutral r162, PCFSoftShadowMap removal r182, stencil default r163). These come from forum and release-note excerpts. Verify before quoting as fact.
- I found no authoritative 2024–2026 article on "archviz in WebGL" best practice. The recipe above is assembled from component docs and forum threads.
- I could not verify the status of `GTAOPass` and `SAOPass` (WebGL) in current three.js.

## 4. How do planners handle wall cutaways so the interior is visible from an angled view?

### Takeaway
There are three common strategies:
1. Hide or make transparent the walls facing the camera, as Planner 5D does by default on web and Houzz does with its "Show cutaway walls" option.
2. Lower all walls, or chosen walls, to a "low wall" height, as in Cyncly 3CAD and Coohom.
3. Use a cut plane at a fixed height, as RoomSketcher does for 2D plans.

In three.js the camera-facing test is a dot product between each wall's outward normal and the camera direction. Opacity fades or raycast-based occlusion hiding are alternatives.

### Cited Findings
- Planner 5D web: by default walls are transparent in 3D "for an unobstructed view", and a toggle makes them visible. On iOS the option is "Show walls in 3D" under the gear/Settings menu. — [Planner 5D Help: see through walls (web)](https://support.planner5d.com/en/articles/8630453-see-through-walls-in-3d-mode-web); [Planner 5D Help (iOS)](https://support.planner5d.com/en/articles/8889752-see-through-walls-in-3d-ios)
- Houzz Pro Dollhouse: a "Show Cutaway Walls" checkbox controls whether front walls hide the interior. Unchecking it removes the front walls. — [Houzz Pro Help](https://pro.houzz.com/pro-help/r/how-to-adjust-3d-floor-plan-settings)
- RoomSketcher: a per-floor wall cut height for the plan view, while the 3D preview always shows full walls. — [RoomSketcher Help](https://help.roomsketcher.com/hc/en-us/articles/360014732378)
- Cyncly 3CAD: a 3D wall-visibility menu raises or lowers all walls or individual walls. Coohom Cloud Design 5.0: a wall can be set to a low height in the sidebar. — [Cyncly 3CAD help](https://3cad.support.cyncly.com/hc/en-us/articles/41926743390481); [Coohom help](https://helpcenter.coohom.com/en/articles/8010370-cloud-design-5-0-how-to-adjust-wall-height-draw-low-walls-and-columns)
- Matterport's Dollhouse shows the scanned mesh from above, with ceilings removed so the interior is visible. In SDK 25.4.1+ dollhouse and floor plan are unified by default. — [Matterport SDK changelog](https://matterport.github.io/showcase-sdk/sdk_changelog.html)
- three.js forum techniques:
  - hide a wall when its outward normal faces the camera, e.g. `wall.visible = v.dot(u) > 0` with v and u being the wall normal and camera direction, or fade opacity instead;
  - give opposite walls consistent outward orientation (rotate by 180°) so the test is not inverted;
  - split thick walls into inner and outer faces with normals pointing into the room;
  - use `side = BackSide` so outside faces drop out without per-frame maths;
  - raycast from the camera and switch blocking walls to wireframe or low opacity. — [forum: Interior Design Wall Visibility](https://discourse.threejs.org/t/interior-design-wall-visibility/67140); [forum: hide walls based on camera position](https://discourse.threejs.org/t/how-to-hide-walls-when-dynamic-based-on-camera-position/76334); [forum: visible from one side](https://discourse.threejs.org/t/is-it-possible-to-make-a-3d-wall-visible-only-from-one-side-in-three-js/57521); [forum: hide objects that obstruct the camera](https://discourse.threejs.org/t/hide-objects-that-obstruct-the-cameras-view/34278); [forum: hide faces facing camera](https://discourse.threejs.org/t/how-to-hide-faces-of-a-model-facing-the-camera/24040) (seen as search excerpts; which answer appears in which thread may be mixed up)

### Inferences
- **Recommended for a polished apartment dollhouse [background, unverified]:** Offer a 3-state wall toggle like The Sims ("full walls / cutaway / low walls").
  - "Low walls": scale all walls to about 0.9–1.2 m, or rebuild them at that height, with a dark top cap. This is stable and view-independent, works well on mobile, and keeps doors and windows readable as notches.
  - "Cutaway": per frame, for each exterior or interior wall segment compute `dot(wallOutwardNormal, cameraToWallDir)`. Walls facing the camera are lowered to cap height (or hidden), and the others stay full height. Animate the height change (about 150–250 ms) to avoid popping. Use the wall's mid-point and the camera position rather than the camera's view direction, so behaviour is correct at wide FOVs.
  - In first-person walk mode always use full walls. In the ortho top view use a cut plane at about 1.0–1.2 m with poché caps. That is the standard architectural plan convention and matches RoomSketcher's "cut height" concept.
- Planner 5D's choice of transparent-by-default walls on web suggests that users mainly want to see the interior. Hiding walls entirely loses spatial context, though, so lowered walls plus caps tend to look more "architectural".

### Gaps
- I found no published technical write-up from any commercial planner on its actual cutaway implementation.
- I could not confirm whether Floorplanner, RoomSketcher 3D or Homestyler offer automatic camera-dependent cutaway in their live 3D view.

## 5. Performance considerations for mobile (shadow map size, pixel ratio, instancing) in a single-page app

### Takeaway
The levers that matter most on phones are a capped device pixel ratio (about 1.5–2), few draw calls (merge static architecture, use `InstancedMesh` for repeated items), few shadow-casting lights with modest shadow-map sizes (512–1024) or no real-time shadows, rendering only on demand, and baking static lighting. Post-processing passes such as AO cost fill rate, so run AO at half resolution (as N8AO 2.0 does) or turn it off on low-end devices.

### Cited Findings
- Cap `setPixelRatio`: one guide suggests 1.5 on mobile and 2 on desktop, e.g. `Math.min(devicePixelRatio, 1.5)`. High DPR is a common cause of mobile slowdowns. — [three best practices (skills.cat)](https://skills.cat/skills/emalorenzo/three-agent-skills/three-best-practices); [threejs-performance (ui-skills)](https://www.ui-skills.com/skills/cloudai-x/threejs-performance) (community guides; rules of thumb, not official)
- Shadow maps: 512×512 on mobile, or disable shadows on mobile; typical range 512–4096. Each shadow-casting light re-renders its casters and adds draw calls. — [threejs-graphics-optimizer (skillselion)](https://skillselion.com/skills/ovachiever/droid-tings/threejs-graphics-optimizer); [ui-skills](https://www.ui-skills.com/skills/cloudai-x/threejs-performance)
- Draw calls are the main bottleneck. Aim for fewer than about 100 per frame, use `InstancedMesh` for identical objects, merge static meshes that share a material, monitor `renderer.info.render.calls`, use 3 or fewer active lights, and use LOD and frustum culling. — [skills.cat](https://skills.cat/skills/emalorenzo/three-agent-skills/three-best-practices); [ui-skills](https://www.ui-skills.com/skills/cloudai-x/threejs-performance)
- N8AO 2.0 computes AO at half resolution and upsamples, which cuts its fill-rate cost. — [N8AO GitHub](https://github.com/N8python/n8ao)
- AccumulativeShadows has no per-frame cost once accumulated. ContactShadows with `frames={1}` renders once. — [drei docs](https://drei.docs.pmnd.rs/staging/accumulative-shadows); [R3F lighting guide](https://www.remoteopenclaw.com/skills/enzed/r3f-skills/r3f-lighting)
- Do not regenerate PMREM environments per frame. — [forum](https://discourse.threejs.org/t/bad-performances-when-animating-a-pmremgenerator-environment/48043)
- The stencil buffer has been off by default since r163 for performance reasons. Enable it only if you use stencil caps. — [forum: render caps](https://discourse.threejs.org/t/how-to-render-caps-like-webgl-clipping-stencil/36727)
- Planner 5D's own troubleshooting for slow 3D: go back to 2D, close other apps, free storage. 3D is slow on weak devices even in commercial apps. — [Planner 5D Help](https://support.planner5d.com/en/articles/15112460-how-to-use-3d-mode)
- Sweet Home 3D's "virtual visit" view is suggested for better performance on modest hardware. — [klaatu guide](https://gopherproxy.meulie.net/sdf.org/0/users/klaatu/techfiles/home3d.md)

### Inferences
- **[background, unverified]**
  - Render on demand: re-render only on controls `change`, pointer drags or animations. In R3F use `frameloop="demand"` + `invalidate()`. A static apartment then uses almost no battery when idle.
  - Use a quality tier: detect mobile or low-end GPUs via `navigator.hardwareConcurrency`, a frame-time probe, or `matchMedia('(pointer: coarse)')`, and switch off AO, reduce `shadow.mapSize` to 1024 or 512, use DPR 1.5, and drop MSAA in favour of SMAA or none.
  - Fit the directional light's shadow camera tightly to the apartment's bounding box so a small shadow map still looks sharp.
  - Set `shadowMap.autoUpdate = false` and update only after edits.
  - Use compressed textures (KTX2/Basis via `KTX2Loader`) and Draco/Meshopt geometry for catalogue models, and keep catalogue thumbnails as 2D images rather than live 3D previews.
  - Generate walls and floors as a few merged meshes per material (one per room floor material, one wall mesh), not one mesh per wall face.
  - SPA hygiene: `dispose()` geometries, materials, textures and render targets when switching views or unloading models, and handle `webglcontextlost`.

### Gaps
- I found no official three.js or vendor benchmark of shadow-map size versus frame rate on specific phones. The numbers above are community rules of thumb.
- I found no source on how the commercial planners scale quality on mobile.

## 6. Open-source examples and libraries that implement floor planners

### Takeaway
The classic open-source web floor planners, blueprint3d (three.js) and cvdlab/react-planner (React with 2D SVG editing and a three.js 3D view), are dormant or kept alive only in forks with outdated three.js versions. They are useful as references for the data model (walls, corners, rooms, items) and interaction logic, not as a modern rendering base. For rendering quality, the pmndrs ecosystem (drei: Environment, AccumulativeShadows, ContactShadows, Edges/Outlines; react-postprocessing: N8AO, SMAA, ToneMapping) and N8AO are the current building blocks. Newer React Three Fiber/Zustand planners on GitHub exist but are of unverified maturity.

### Cited Findings
- cvdlab/react-planner: a React component for drawing a 2D floor plan and navigating it in 3D, with about 1.4k stars. It is largely dormant, and users in the issue tracker ask for active forks. — [react-planner issue #240](https://www.github.com/cvdlab/react-planner/issues/240); [relatedrepos: react-planner](https://relatedrepos.com/gh/cvdlab/react-planner)
- blueprint3d (furnishup, with forks): a customizable three.js application for designing interiors such as a home or apartment. The original and the aalavandhaann fork are reported inactive. The palm/blueprint3d TypeScript fork lists updating to current three.js as a goal. — [fducom/blueprint3d](https://github.com/fducom/blueprint3d); [palm/blueprint3d](https://github.com/palm/blueprint3d); [react-planner issue #240](https://www.github.com/cvdlab/react-planner/issues/240)
- The GitHub "floor-planner" topic lists newer projects: a Next.js + React Three Fiber 3D floor planner with walls, furniture and export (updated July 2026), and an open-source 3D home designer using React, three.js and Zustand with synced 2D and 3D views. — [GitHub topic: floor-planner](https://github.com/topics/floor-planner?l=javascript)
- nickorzha/threejs-room-planner: a React + three.js room planner and product configurator. — [ecosyste.ms entry](https://awesome.ecosyste.ms/projects/github.com%2Fnickorzha%2Fthreejs-room-planner)
- Sweet Home 3D is the mature open-source (GPL, Java) reference for feature scope: magnetism, aerial view and virtual visit. — [Neowin](https://www.neowin.net/software/sweet-home-3d-70/); [SourceForge news](https://sourceforge.net/p/sweethome3d/news)
- Rendering building blocks:
  - drei `AccumulativeShadows`/`RandomizedLight` and `ContactShadows`. — [drei docs](https://drei.docs.pmnd.rs/staging/accumulative-shadows); [tessl drei staging mirror](https://tessl.io/registry/tessl/npm-react-three--drei/files/docs/staging.md)
  - N8AO for vanilla three.js and pmndrs. — [N8AO](https://github.com/N8python/n8ao); [react-postprocessing N8AO](https://react-postprocessing.docs.pmnd.rs/effects/n8ao)
  - react-postprocessing SMAA and ToneMapping. — [SMAA](https://react-postprocessing.docs.pmnd.rs/effects/smaa); [ToneMapping](https://react-postprocessing.docs.pmnd.rs/effects/tone-mapping)
  - three.js `RoomEnvironment`. — [three.js docs](https://threejs.org/docs/pages/RoomEnvironment.html)
- three.js official examples relevant to planners: `webgl_clipping_stencil` (section caps), referenced in the forum threads. — [forum: render caps like webgl_clipping_stencil](https://discourse.threejs.org/t/how-to-render-caps-like-webgl-clipping-stencil/36727)

### Inferences
- For a single-page apartment planner in vanilla three.js (no React), the most practical stack is: three.js r17x/r18x (WebGLRenderer), `OrbitControls`/`MapControls`/`PointerLockControls` for orbit, plan and walk modes, `RoomEnvironment` + PMREM, `EffectComposer` with `N8AOPass` → `OutputPass`, an `EdgesGeometry` overlay, and a custom 2D wall graph (corners plus wall segments, rooms detected as cycles) like blueprint3d's model. **[background, unverified]**
- Other relevant drei helpers I know of but could not verify this session: `<Environment>` with `<Lightformer>`, `<SoftShadows>` (PCSS), `<Edges>`/`<Outlines>`, `<Bvh>`, `<Instances>`, `<PerformanceMonitor>`/`<AdaptiveDpr>` for automatic quality scaling. **[background, unverified]**

### Gaps
- I could not check current commit activity, licences or star counts of the newer R3F planners (the GitHub API was not available and the pages could not be fetched).
- I found no maintained, modern (r160+) vanilla-three.js open-source floor planner with polished archviz rendering. This may be a real gap in the ecosystem or a limit of the search.
