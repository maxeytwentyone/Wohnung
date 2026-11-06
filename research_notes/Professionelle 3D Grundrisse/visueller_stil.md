# Visual style and design conventions of professional 3D floor plans (3D-Grundrisse)

> **Method note for the report writer.** Every WebFetch to provider sites failed in this session: roomsketcher, maverickframe, ohne-makler.net and immobilienscout24.de were all blocked by the network allowlist with a DNS "ENOTFOUND" error. That means I could not look at any portfolio images. All findings below come from WebSearch results, i.e. snippets and summaries of the pages linked. Where a search summary bundled several sources and the exact attribution of a claim was unclear, I say so ("attribution within result set uncertain"). Purely visual facts, such as the exact cap color a German studio uses, could not be checked against images. Those are listed as gaps or marked as unsourced inferences.

## 1. Which perspectives are standard (Draufsicht, isometric/axonometric, Vogelperspektive, dollhouse) and when is each used?

### Takeaway
The German market offers three standard views, usually priced per perspective:
- **3D-Draufsicht:** straight top-down, orthographic or near-orthographic.
- **Vogelperspektive / Schrägansicht:** an angled bird's-eye view, roughly 45–60°, also called dollhouse.
- **Flat isometric:** the "model on a table" look.

The roof or ceiling is always removed. Top-down views are favoured for legibility in Exposés and on portals. Angled views and dollhouse views are used for emotional, "spatial" impact and for multi-storey homes.

### Cited Findings
- eStaging describes its 3D-Grundriss as showing the property from a bird's-eye view **without a roof**, "fully furnished and decorated" like a show apartment (Musterwohnung). — [eStaging 3D-Grundriss Staging](https://www.estaging.de/services/3d-grundriss-staging/)
- visupartner offers two variants, a **3D-Draufsicht (Vogelperspektive)** or a **Schrägansicht** (oblique view). It recommends using them online (own website, property portals) and offline (Exposés, ads, Bauschilder / construction-site signs). — [visupartner 3D-Grundriss](http://www.visupartner.de/immonet/3d-grundriss.php)
- FloorDrafter (German-language page) lets customers choose between three views:
  - **Vogelperspektive**, "for the dollhouse view"
  - **flache Isometrie**, "the model on the table"
  - **reine Draufsicht**, pure top-down
  - [FloorDrafter – Grundriss in 3D umwandeln](https://floordrafter.com/de/floor-plan-to-3d-model)
- GrundrissProfi sells 3D-Grundrisse with a base price that includes **one perspective of the customer's choice**, plus **€3.90 net per additional perspective**. It also offers a separate "3D-Vogelperspektive" product and a 3D site plan (Lageplan) "von senkrecht oben" (from directly above). — [GrundrissProfi 3D-Grundriss](https://www.grundrissprofi.de/3d-grundriss/); [GrundrissProfi 3D-Vogelperspektive](https://www.grundrissprofi.de/3d-vogelperspektive/)
- 360 Render's 2025/2026 developer guide says every top-down floor plan render starts with a camera choice: **orthographic or perspective**. — [360 Render – Developer's Guide to 3D Floor Plan Visualization 2025/2026](https://www.360render.com/architectural-rendering/what-is-3d-floor-plan-visualization-a-comprehensive-guide-for-property-developers/)
- A floor-plan rendering guide recommends rendering with the camera in **orthographic or a shallow perspective** for top-down plans. — attribution within result set uncertain: [Archfine – Rendered Floor Plan](https://archfine.com/architectural-visualization-tutorials/rendered-floor-plan) / [Arakot – Floor Plan to 3D Render](https://www.arakot.com/how-to-turn-floor-plan-into-3d-render/)
- Camera angles cited for bird's-eye rendering:
  - One bird's-eye rendering service describes its views as taken at **45° to 60°**. — [The Arc Engine – Bird-Eye View Rendering](https://thearcengine.com/3d-visualization/bird-eye-view/)
  - A camera-angle guide calls the **45° three-quarter view** a common hero shot and lists a true top-down plan view as a separate option. — [Maverick Frame – 9 Camera Angles in 3D Visualization](https://maverickframe.com/blog/types-of-angles-in-3d-visualization/)
- Matterport's **dollhouse view** is a 3D bird's-eye cutaway of the whole property, and users can "peel back" floors one at a time. Its **floor plan view** is a flat top-down view, described by one commentator as "a schematic floor plan… instead of simple black and white lines, you get to see it in color". Matterport's own marketing sometimes uses "3D floor plan" and "Dollhouse View" as synonyms. — [Matterport blog – 3D Floor Plan Views](https://matterport.com/blog/engage-home-buyers-and-sellers-3d-floor-plan-views); [Matterport – Dollhouse View upgrade](https://matterport.com/it/blog/dollhouse-view-just-got-upgrade); [WeGetAroundNetwork forum](https://www.wegetaroundnetwork.com/topic/15791/comparison-matterport-floor-plans-versus-my-visual-listings-floor-plans/)
- 3D floor plans are typically built to scale and **omit the ceiling** so the interior is visible. — [Wikipedia – 3D floor plan](https://en.wikipedia.org/wiki/3D_floor_plan)
- A US price ladder treats the view types as separate tiers: "3D isometric" at $150–300, "furnished 3D" at $200–350, and "dollhouse or sectional" at $300–500. The ladder is attributed to 3D Praxis on a price-list site. — [VizCraft – 3D Rendering Price List 2026](https://vizcraft.ai/blog/posts/3d-rendering-price-list)

### Inferences
- In the German market, the default deliverable for an apartment Exposé appears to be one top-down (Draufsicht) image, with angled bird's-eye views sold as add-ons. Per-perspective pricing at GrundrissProfi and the visupartner and FloorDrafter menus support this.
- Use each view for a different job:
  - **Top-down orthographic:** factual layout reading. It pairs with the 2D plan and keeps labels readable.
  - **45–60° bird's-eye / dollhouse:** emotional hero image, best for showing wall heights, kitchen fronts and multi-level homes.
  - **Flat isometric:** "miniature model" look, often used for stylized or branded output.
- To replicate the look, a common recipe (inference, not sourced as a standard) is:
  - **Hero image:** a perspective camera with a long focal length (low distortion), pitched about 45–60° down and rotated about 30–45° around the vertical axis.
  - **Plan image:** a pure orthographic top camera.

### Gaps
- I found no source giving exact focal lengths or field of view for professional top-down 3D-Grundrisse, nor any statistic on which view German portals use most.
- Portfolio images could not be inspected (fetch blocked), so I could not check which view German studios use most.

## 2. How are walls shown (cut height, wall-top color, thickness), and how are doors and windows depicted?

### Takeaway
3D-Grundrisse are almost always cutaways. Walls are cut well below ceiling height, at about 1.0–1.3 m in CAD convention. RoomSketcher's examples use about 127 cm, or about 190 cm when wall cabinets should stay visible. Wall tops ("caps") get a solid contrasting color, typically black, dark grey or a brand color, set against white wall faces and light floors. Sources say little about door and window detailing beyond "they must not be missing".

### Cited Findings
- **RoomSketcher cut height.** You can set a wall cut height, which removes everything above it from the 3D render.
  - Its examples use **50 inches (≈127 cm)** for a cutaway view and **75 inches (≈190 cm)** to keep wall cabinets visible.
  - With no cut set, walls render at **full height and run over windows and doors**.
  - Full-height walls on one floor share a single height. Half-height walls are only possible as individual wall sections.
  - [RoomSketcher Help – Change the Height of the Walls](https://help.roomsketcher.com/hc/en-us/articles/360014732378)
- **RoomSketcher customization (Pro/Team).** You can change the 3D perspective, **wall-top color** and **cut height**, and choose whether to show furniture, room names and product labels.
  - Under Styles → 3D Floor Plans you can set wall-top color, text color and arrow colors.
  - Wall-top color can be applied to all walls or to single walls.
  - Hex/RGB codes are supported, and company brand colors can be applied.
  - [RoomSketcher – Customize 3D Floor Plans](https://www.roomsketcher.com/features/pro-features/customize-3d-floor-plans/); [RoomSketcher Help – Customize 3D Floor Plans](https://help.roomsketcher.com/hc/en-us/articles/205289631-How-Can-I-Customize-My-3D-Floor-Plans-in-RoomSketcher); [RoomSketcher Help – Add Color to the Top of a Single Wall](https://help.roomsketcher.com/hc/en-us/articles/360000835785-Add-Color-to-the-Top-of-a-Single-Wall)
- **RoomSketcher style gallery.** Its "Colorful 3D Floor Plans" blog shows **11 styles**, including:
  - **dark wall tops** contrasting with **white walls and light floors**
  - **forest-green wall tops** over light wood floors and white walls
  - **black wall tops** highlighting the room layout against light wood floors
  - **navy wall tops** with white and wood furniture
  - dark blue, sea-glass green, and black-and-beige schemes
  - [RoomSketcher blog – Colorful 3D Floor Plans](https://www.roomsketcher.com/blog/colorful-3d-floor-plans/)
- **Cutting at about a metre.** A floor-plan rendering guide says cutting walls at "around a metre" keeps sightlines into every room. The same guide says to model **real wall heights** first and then cut. — attribution within result set uncertain: [Archfine](https://archfine.com/architectural-visualization-tutorials/rendered-floor-plan) / [Arakot](https://www.arakot.com/how-to-turn-floor-plan-into-3d-render/)
- **1 m walls in user practice.** A Sweet Home 3D forum user sets walls to **100 cm** to get a cutaway plan (a user preference, not a standard). Offision gives typical floor-to-ceiling height as **2.5–3 m** and notes that walls drawn at 1 m are a frequent cause of a "doll's-house" look. — [Sweet Home 3D forum](https://sweethome3d.com/support/forum/viewthread_thread,11288); [Offision – Give objects height](https://offision.com/help/en/map/give-objects-height/)
- **German CAD convention for the 2D Grundriss.**
  - A German-language CAD forum gives usual cut heights (Schnitthöhe) of **1.00–1.25 m**. The source is a forum with mixed answers. — attribution uncertain: [Vectorworks Forum – Wand Aufsicht und Schnitt](https://www.vectorworksforum.eu/topic/7301-wand-aufsicht-und-schnitt/) / [BAU-Forum – Grundriss zeichnen](https://bau.net/forum/dig/10179.php)
  - The Swiss CAD vendor IDC states "Standardmässig schneiden Sie auf **1.30 m**" (by default you cut at 1.30 m). — [IDC Supportdatenbank – Die Grundriss-Schnittebene](https://www.idc.ch/support/supportdatenbank/die-grundriss-schnittebene-/-elementdarstellung)
- **Dark-on-dark warning.** 360 Render warns that dark grey walls combined with dark floors can make a top-down render read as "one undifferentiated dark square". Its fix is to lighten floor finishes slightly in the model or to brighten area rugs. — [360 Render – Developer's Guide](https://www.360render.com/architectural-rendering/what-is-3d-floor-plan-visualization-a-comprehensive-guide-for-property-developers/)
- **Wall tops flush with ceilings.** 360 Render's 2D-to-3D workflow guide says to align ceilings to the top of the walls on each floor, and not to estimate scale. — [360 Render – 2D Floor Plan to 3D Model workflow 2025–2026](https://www.360render.com/rendering-guide/how-to-convert-2d-floor-plan-to-3d-model/)
- **Doors and windows.** Commonly listed 3D floor plan mistakes include **missing doors or windows**, wrong scale, unclear camera angle, oversized furniture, excessive decor and poor room labelling. Quality checklists say to **check wall thicknesses, ceiling heights and door and window sizes** against the drawings. — attribution within result set uncertain: [Maverick Frame – What is a 3D floor plan](https://maverickframe.com/blog/what-is-3d-floor-plan/); [Medium – 3D floor plan design tips](https://shushmitaroy.medium.com/3d-floor-plan-design-tips-539caff46e24); [Rare Design Hive – accuracy](https://raredesignhive.com/blog/3d-floor-plans-accuracy-reduce-design-errors-rework-on-sit/); [Chasing Illusions – common mistakes](https://www.chasingillusions.in/common-mistakes-3d-floor-plan-walkthroughs/)
- **Source-plan quality.** An AI floor-plan-to-3D tool says that clear dark walls and visible doors and windows in the source plan give the best result. This shows that the 3D output's wall and opening placement depends on how clearly the input plan marks them. — [genroom.io](https://genroom.io/de/floor-plan-to-3d-ai)
- **Shadows from cut walls.** A low-poly 3D devlog describes cutaway walls that stop drawing but still cast shadows, using a "shadows-only" mode for the removed upper part. This is a technique for keeping natural room shadows despite the cut. — [Kiln Commons devlog – Cut the wall, keep its shadow](https://goblin-mol.itch.io/kiln-commons/devlog/1695827/cut-the-wall-keep-its-shadow)

### Inferences
- Replication defaults supported by the sources above:
  - Model walls at true height (≈2.5–2.7 m in German apartments) and cut at **≈1.0–1.3 m** for a top-down view. Raise the cut to ≈1.9 m only if wall cabinets or a kitchen must stay visible.
  - Give the cut faces a flat, unlit or matte **solid cap**: black, anthracite (dark grey) or a brand color. Keep wall faces white or off-white and floors light. That cap-vs-floor contrast is what makes the layout readable.
- Optionally let the removed upper wall part still cast shadows (shadow-only), so rooms keep realistic shading under the cut.
- **Wall thickness** should be taken from the plan, not standardized. Exterior walls are visibly thicker than interior partitions, and checklists say to verify thicknesses against drawings.
- **Doors and windows, unsourced inference** based on general familiarity with the genre (verify visually against provider portfolios):
  - Interior doors are typically shown **open**, as a door leaf rotated about 90°, or omitted, leaving an opening. 3D renders generally do not use the 2D quarter-circle swing arc.
  - Windows appear as a cut wall with a light-grey or slightly transparent glass pane and a thin frame or sill, below or at the cut height.

### Gaps
- No source states which wall-cap color German 3D-Grundriss studios such as GrundrissProfi, eStaging or visupartner use by default.
- No source documents door depiction conventions in 3D (open vs. closed door leaves, swing arcs) or how glass is rendered.
- RoomSketcher's own default cut height and cap color could not be confirmed because the help pages were not fetchable. Only the 50"/75" examples from search snippets are available.

## 3. What materials and textures are typical, and how realistic vs. stylized? Photorealistic vs. "clean/minimal" styles?

### Takeaway
The market spans three tiers:
- **Schematic / minimal:** flat colors, few textures.
- **Semi-realistic:** real wood and tile textures, simple furniture. This is the bulk of real-estate output.
- **Photorealistic:** physically based materials, detailed décor, complex lighting. Reserved for premium or new-build marketing.

Floors are almost always light. Providers ask for the actual floor coverings (Bodenbeläge) so the plan can match reality.

### Cited Findings
- **Photorealistic.** High-resolution materials, advanced lighting and detailed décor, recommended for high-end developments, luxury villas or flagship campaigns. **Schematic / non-photorealistic.** Clean lines, flat colors and minimal detail to emphasize layout, suited to technical reviews or early off-plan marketing ("simple shapes, neutral colors, minimal textures"). — [Tripo3D – 3D Floor Plan Rendering guide](https://www.tripo3d.ai/blog/explore/3d-floor-plan-rendering-company); [aiStager – Rendered Floor Plan](https://www.ai-stager.com/blog/rendered-floor-plan); [Rendimension](https://rendimension.com/benefits-3d-floor-plans-real-estate/) (attribution within result set uncertain)
- **Semi-realistic as the norm.** One vendor argues that for most residential properties, semi-realistic 3D floor plans hit the sweet spot between cost, production time and visual impact. This is vendor opinion. — attribution within result set uncertain: [The 2D3D Floor Plan Company](https://the2d3dfloorplancompany.com/services/3d-floor-plan/) / [Bella Virtual](https://www.bellavirtual.com/blogs/news/2d-vs-3d-floor-plans-which-one-does-your-listing-need)
- **Hyper-realistic top-down example.** One guide shows a hyper-realistic rendered floor plan of a furnished living room seen from directly above. — [aiStager](https://www.ai-stager.com/blog/rendered-floor-plan)
- **Freelancer quality ladder:**
  - Basic: simple top-down view, basic textures, $100–200
  - Standard: furnished model, realistic materials, 2–3 camera angles, $300–600
  - Premium: photorealistic, walkthrough video, custom furniture, $600–1,200
  - [RITN3D – How much does a 3D floor plan cost 2026](https://www.ritn3d.com/blog/how-much-does-3d-floor-plan-cost/)
- **Input data.** immoviewer (German visualization service) says the floor plan is basically enough. For a detailed result it also needs room height, windows, **floor coverings (Bodenbeläge)**, sanitary fittings and stairs. — [immoviewer Visualisierungen](https://visualisierungen.immoviewer.com)
- **Material control.** RoomSketcher's library reportedly has "hundreds" of colors and materials, can be set per room or wall, and accepts custom Hex/RGB. — [RoomSketcher Help – Customize](https://help.roomsketcher.com/hc/en-us/articles/205289631-How-Can-I-Customize-My-3D-Floor-Plans-in-RoomSketcher)
- **Light floors in style examples.** RoomSketcher's style examples repeatedly pair **light wood floors** with white walls and a colored or dark cap. — [RoomSketcher blog – Colorful 3D Floor Plans](https://www.roomsketcher.com/blog/colorful-3d-floor-plans/)
- **Avoid dark floors.** 360 Render recommends lightening floor finishes so the top-down view does not go murky. — [360 Render – Developer's Guide](https://www.360render.com/architectural-rendering/what-is-3d-floor-plan-visualization-a-comprehensive-guide-for-property-developers/)
- **AI-generated photorealism.** RoomSketcher published a guide on creating photorealistic floor plan visuals with AI, a 2025/26 trend of AI "re-skinning" of plan renders. — [RoomSketcher blog – Photorealistic Floor Plan Visuals with AI](https://www.roomsketcher.com/blog/how-to-create-photorealistic-floor-plan-visuals-with-ai/)

### Inferences
- Material defaults per room, mostly unsourced and based on general familiarity with the genre (verify against portfolios):
  - Living and bedrooms: light oak parquet or laminate with visible plank direction.
  - Bathrooms and WC: light grey or white large-format tiles, sometimes with a darker shower zone.
  - Kitchen: tiles or the same wood as the living area in open-plan layouts.
  - Hallways: tile or wood.
  - Carpets mainly as area rugs, which also serve as visual "anchors". 360 Render mentions brightening rugs.
  - Balconies and terraces: grey wooden decking or concrete slabs.
- High-end output differs mainly in **material fidelity**: correct plank scale, tile joints at real size, subtle roughness and reflection variation. Cheap output uses repeated, stretched or wrongly scaled textures. The "real-world sizes, not generic blocks" checklist item in section 9 supports this.

### Gaps
- No sources quantified texture resolution or gave rules for tile and plank scale in floor-plan renders.
- No German-market source stated which share of 3D-Grundrisse are photoreal vs. stylized.

## 4. Lighting and rendering: soft shadows, ambient occlusion, daylight, background, drop shadow?

### Takeaway
Lighting for 3D floor plans is deliberately **soft, flat and even**, using overcast-style HDRI daylight. The goal is legibility, not drama, so strong shadows that hide parts of the plan are avoided. The model sits on a **white or transparent background**, often with a light drop shadow around the outer walls.

### Cited Findings
- 360 Render uses an **HDRI environment that mimics soft, overcast daylight**, giving gentle directional shadows and avoiding heavy darkness in room corners. — [360 Render – Developer's Guide 2025/2026](https://www.360render.com/architectural-rendering/what-is-3d-floor-plan-visualization-a-comprehensive-guide-for-property-developers/)
- A floor-plan rendering guide says lighting should be **flat and even rather than dramatic**, because the purpose is legibility and strong shadows hide parts of the plan. — attribution within result set uncertain: [Archfine](https://archfine.com/architectural-visualization-tutorials/rendered-floor-plan) / [Arakot](https://www.arakot.com/how-to-turn-floor-plan-into-3d-render/)
- Tripo3D recommends an **HDRI environment map** for daytime scenes, for realistic ambient light and reflections. — [Tripo3D – 3D Rendering Floor Plans: Best Practices](https://www.tripo3d.ai/blog/explore/3d-rendering-floor-plan)
- GrundrissProfi sells a **transparent background** as an option, at €2.90 surcharge in its 2014 price list (outdated), so the plan can be placed on Exposé layouts. — [GrundrissProfi Übersicht Stilformen (PDF, 2014)](https://grundrissprofi.de/dokumente/prospekte/uebersicht-stilformen.pdf)
- **AI prompt templates** that copy the professional look:
  - An OpenArt prompt: isometric plan with "clean flat colors, **soft shadows, white background**".
  - A MeltFlex prompt: "a **light drop shadow around the building outline**, white background outside the walls".
  - These templates show what the market treats as the default look. — [OpenArt – Floor Plan Prompts](https://openart.ai/blog/midjourney-prompts-for-floor-plan/); [MeltFlex – AI Floor Plan Prompts](https://www.meltflexai.com/blog/ai-floor-plan-prompts)
- **Shadows in CAD floor plans.** In Archicad, a typical shadow setup uses a 50% shadow polygon with black or dark-gray fill. — [Graphisoft Support – Floor plan with shadows](https://support.graphisoft.com/hc/en-us/articles/27940083326737-Can-I-create-a-floor-plan-that-has-shadows)
- **Lighting should match reality.** Quality checklists say lighting and shadows should match the actual property. — attribution within result set uncertain: [Rare Design Hive](https://raredesignhive.com/blog/3d-floor-plans-for-real-estate-marketing/) / [Maverick Frame](https://maverickframe.com/blog/what-is-3d-floor-plan/)

### Inferences
- Replication recipe (inferred from the above; exact values unsourced):
  - Overcast HDRI or large sky dome plus a weak sun or key light from roughly above, slightly off-axis. This gives short, soft shadows that read as "daylight from the windows".
  - Ambient occlusion or contact shadows at wall bases and under furniture to ground objects.
  - Pure white (#FFFFFF) or transparent background.
  - A soft, low-opacity drop shadow outside the outer walls, so the apartment "floats" on the page.
- Strong sunbeams, dark corners and coloured night lighting count as mistakes for plans, though they are fine for interior hero renders.

### Gaps
- No source gave numeric lighting settings: sun angle, shadow softness, AO radius, exposure.
- No source confirmed how widely German studios use drop shadows; this is visible only in portfolios, which I could not fetch.

## 5. Furniture staging: how much, what style, plants, rugs, decorative details?

### Takeaway
Professional German 3D-Grundrisse are typically **fully furnished**, "like a show apartment". The style is neutral and modern, with Scandinavian-leaning light wood, white and muted tones. Furniture must be **true to scale** and must not overcrowd the plan. Plants and rugs act as scale cues and visual anchors. Unfurnished versions exist and cost roughly half.

### Cited Findings
- eStaging: every 3D-Grundriss is "vollständig eingerichtet und dekoriert" (fully furnished and decorated), like a Musterwohnung (show apartment). — [eStaging 3D-Grundriss Staging](https://www.estaging.de/services/3d-grundriss-staging/)
- Swiss portal newhome.ch prices for residential property, implying furnishing roughly doubles the price — [newhome.ch digital services 2021 (PDF)](https://assets01.sdd1.ch/assets/lbwp-cdn/newhome-blog/files/1622119130/digital-services-2021-de.pdf); [newhome.ch Immobilienaufnahmen 2024 (PDF)](https://assets01.sdd1.ch/assets/lbwp-cdn/newhome-blog/files/1706176143/20240119_immobilienaufnahmen-de.pdf):
  - 3D-Grundrissplan **unmöbliert**, 5 images: **CHF 75**
  - **möbliert**, 5 images + video: **CHF 150** (CHF 200 for commercial)
- grundrisstausch.de advertises "3D Grundrisse zeichnen lassen – möbliert, alles inclusive **24,98 €**". — [grundrisstausch.de](https://grundrisstausch.de/3d-grundrisse-zeichnen-lassen-moebliert/)
- Common mistakes include **oversized furniture**, tiny beds or narrow sofas that distort perceived room size, **overcrowding**, and making visuals "decorative instead of informative". Checklists say to use **real-world furniture and appliance sizes, not generic blocks**. — attribution within result set uncertain: [Maverick Frame](https://maverickframe.com/blog/what-is-3d-floor-plan/); [Medium – design tips & mistakes](https://shushmitaroy.medium.com/3d-floor-plan-design-tips-539caff46e24); [Chasing Illusions](https://www.chasingillusions.in/common-mistakes-3d-floor-plan-walkthroughs/)
- Guides recommend including human-scale reference objects such as furniture or **plants** to give an immediate sense of size. — attribution within result set uncertain: [Tripo3D](https://www.tripo3d.ai/blog/explore/3d-rendering-floor-plan) / [Archfine](https://archfine.com/architectural-visualization-tutorials/rendered-floor-plan)
- Buyers often care more about how a home **flows** than raw square metres, so circulation paths should stay clear. — attribution within result set uncertain: [Find a Property Egypt – 3D floor plans that sell faster](https://findapropertyegypt.com/3d-floor-plans/) / [Rare Design Hive](https://raredesignhive.com/blog/3d-floor-plans-for-real-estate-marketing/)
- RoomSketcher style examples use "white and wood furniture" and a palette with "a **Scandinavian feel**" of muted blues, white and earthy tones. — [RoomSketcher blog – Colorful 3D Floor Plans](https://www.roomsketcher.com/blog/colorful-3d-floor-plans/)
- Providers bill a later change of style, furniture or layout as a **new order**, so the furnishing style is fixed at ordering time. — [grundrisstausch.de](https://grundrisstausch.de/3d-grundrisse-zeichnen-lassen-moebliert/) (attribution within result set uncertain; result summary did not name the provider explicitly)
- German digital-staging studios based on floor plans include Spacerenovator ("Digital Staging auf Grundrissbasis von Innenarchitekten", i.e. by interior architects), studio4-homestaging (Grundrissgestaltung), immoyes and BKBN. — [Spacerenovator](https://spacerenovator.de/digital-staging-grundriss); [studio4-homestaging](https://studio4-homestaging.de/grundrissgestaltung-klare-darstellung/); [immoyes](https://immoyes.com/); [BKBN Virtual Staging](https://www.bkbn.com/portfolio/real-estate-virtual-staging)

### Inferences
- Room-by-room furnishing level, inferred from the sources (exact item lists unsourced):
  - Living room: one sofa, coffee table, rug, TV or sideboard, dining table with 4–6 chairs.
  - Bedroom: bed with bedside tables, wardrobe along a wall.
  - Kitchen: true-to-plan kitchen run with appliances.
  - Bathroom: sanitary fittings exactly as built.
  - Balcony: small table and 2 chairs.
  - Extras: one or two plants per main room.
- Keep décor items (books, vases) minimal; they are invisible at plan scale.
- Style: modern Scandinavian-neutral, with light oak, white, beige or grey textiles and occasional muted accent colors (sage, terracotta, navy). Avoid brand-new trend colors that date the image.

### Gaps
- No source quantified "how much" furniture is standard (e.g. items per room) or gave plant and rug guidelines beyond scale cues.

## 6. Labels and information: room names, m² per room, dimensions, compass/north arrow, scale, legend, logos?

### Takeaway
Professional 3D-Grundrisse for the German market usually carry **room names and per-room m²**. Dimensions, north arrow and scale bar appear more often on the companion 2D plan. Logos and brand colors are a paid customization on platforms like RoomSketcher. Area figures should follow WoFlV (Wohnflächenverordnung, the German living-area ordinance) for residential, and a disclaimer ("unverbindliche Visualisierung", non-binding visualization) is recommended.

### Cited Findings
- A studio's 3D floor plan package lists **room labelling, per-room m² figures, dimensioning and furnishing** as included features. — attribution within result set uncertain: [studio4-homestaging – Grundrissgestaltung](https://studio4-homestaging.de/grundrissgestaltung-klare-darstellung/) / [Spacerenovator](https://spacerenovator.de/digital-staging-grundriss)
- The immostage.ai guide advises always adding **each room's m²**. It notes that residential living area is governed by the **WoFlV**, while **DIN 277** yields the largest figure because it applies no deductions. — [immostage.ai – Grundriss erstellen](https://www.immostage.ai/grundriss/erstellen/); [immostage.ai – Grundriss lesen](https://www.immostage.ai/grundriss/lesen/)
- RoomSketcher lets you toggle **room names** and **product labels** in 3D and set **text color and arrow colors**. Company branding (logo, colors) is available for floor-plan orders and Pro/Team. — [RoomSketcher – Customize 3D Floor Plans](https://www.roomsketcher.com/features/pro-features/customize-3d-floor-plans/); [RoomSketcher – Branding for floor plan orders](https://roomsketcher.com/order-floor-plans/options)
- Matterport added **room labels** to the dollhouse view; earlier they appeared only in floor plan view. Measurement lines drawn in floor plan view are not visible in other views. — [Matterport blog](https://matterport.com/blog/engage-home-buyers-and-sellers-3d-floor-plan-views); [WeGetAroundNetwork](https://www.wegetaroundnetwork.com/tag/floor-plan-view)
- "Poor room labelling" is a commonly listed mistake, and plans should be tested for **readability on mobile**. — attribution within result set uncertain: [Maverick Frame](https://maverickframe.com/blog/what-is-3d-floor-plan/) / [Rare Design Hive](https://raredesignhive.com/blog/3d-floor-plans-for-real-estate-marketing/)
- A visualization provider recommends marking 3D visualizations in the Exposé as "**unverbindliche Visualisierung**" so buyers are not misled about the actual condition. — attribution within result set uncertain: [Maverick Frame – 3D-Visualisierung Immobilienmarketing](https://maverickframe.com/de/blog/3d-visualisierung-immobilienmarketing/)
- ohne-makler.net notes that the architect may have to consent before their plan is published. — [ohne-makler.net Ratgeber Grundrisse](https://www.ohne-makler.net/ratgeber/expose/grundrisse/)

### Inferences
- Typical German label block (inferred; layout specifics unsourced):
  - Room name in German (Wohnen/Essen, Küche, Schlafen, Kind, Bad, WC, Flur, Abstellraum, Balkon/Terrasse) with "xx,xx m²" beneath it.
  - Clean sans-serif type, dark grey or black, placed flat on the floor or as a 2D overlay in the top-down view.
- Total living area (Wohnfläche gesamt), a north arrow and a small logo are usually placed in a corner or legend strip of the image or Exposé page.
- Keep labels off furniture and readable at phone width. In angled bird's-eye views, labels are often omitted or simplified, because perspective distorts them.

### Gaps
- No source confirmed how often German 3D-Grundrisse include a compass/north arrow, scale bar or dimension chains in the 3D image itself.
- No typographic conventions (font, size) were found.

## 7. Color palettes and overall aesthetic trends 2024–2026

### Takeaway
The dominant look is still neutral and light: white walls, light wood floors, dark or black wall caps on a white background. Since about 2024 there is a visible move toward **branded or colored wall caps** (navy, forest green, sea-glass) and earthy accent palettes. In 2025/26, **AI-generated photoreal "re-skins"** and instant AI floor-plan-to-3D tools are spreading.

### Cited Findings
- RoomSketcher calls color something that "turns a functional floor plan into a marketing asset" and showcases 11 colored styles:
  - navy, forest green, sea-glass green, black-and-beige
  - a "Scandinavian feel" palette of muted blues, white and earth tones
  - an "organic monochrome" palette of neutral browns
  - [RoomSketcher blog – Colorful 3D Floor Plans](https://www.roomsketcher.com/blog/colorful-3d-floor-plans/)
- **Interior color trends 2025 (not floor-plan specific).**
  - The 1stDibs designer survey found a desire for "earthy and natural tones", with **chocolate brown** as the top color. — [BusinessWire – 1stDibs 2025 Trends](https://www.businesswire.com/news/home/20241112477735/en/1stDibs-Reveals-2025-Trends-from-Its-Annual-Designer-Survey-Highlighting-Upcoming-Color-Furniture-and-Design-Style-Trends)
  - Other trend sources name mocha brown, olive green, terracotta, deep navy and clay pink. — attribution within result set uncertain: [Genense – Interior Color Trends 2025](https://www.genense.com/blog/interior-color-trends-2025-a-palette-of-possibilities/) / [DesignerFurniture – 2025 Color Trends](https://www.designerfurniture.com/blog/2025-color-trends-for-furniture-and-home-decor)
- **AI floor-plan-to-3D and AI staging tools are a 2025/26 phenomenon.** Examples:
  - GetFloorPlan, packages $45–69 — [creati.ai – GetFloorPlan](https://creati.ai/de/ai-tools/getfloorplan/)
  - genroom.io, furnished top-down from an uploaded plan — [genroom.io](https://genroom.io/de/floor-plan-to-3d-ai)
  - Pedra, rendered floor plans "in minutes" — [Pedra](https://pedra.ai/blog/rendered-floor-plan)
  - immostage.ai — [immostage.ai](https://www.immostage.ai/grundriss/erstellen/)
  - RoomSketcher's AI photoreal guide — [RoomSketcher blog](https://www.roomsketcher.com/blog/how-to-create-photorealistic-floor-plan-visuals-with-ai/)
  - 4K export is commonly a paid or Pro feature in AI tools — [Interior360](https://interior360.net/); [Renderahouse – Floor plan to render with AI 2026](https://www.renderahouse.com/blog/floor-plan-to-render-workflow); [floor-plan.ai](https://floor-plan.ai/floor-plan-to-3d)
- **Interactive 3D-Grundrisse as a German broker trend.** BDRA describes an interactive 3D-Grundriss as a "digital pre-viewing" that builds trust, and says it should match the level of the professional photos. — [BDRA – 3D-Grundrisse für Makler](https://bdra.de/makler-profitieren-interaktive-3d-grundrisse/)

### Inferences
- For a timeless 2024–2026 look:
  - white or off-white walls
  - light natural oak floors
  - **anthracite or black caps** (or one muted brand color: navy, deep green)
  - neutral beige, grey and white furniture with one or two earthy accents (terracotta, olive, brown)
  - a white background
- Strong saturated caps or trend colors suit branded developer marketing more than neutral brokerage listings.

### Gaps
- No source quantified palette adoption in the German market specifically. Trend sources are general interior design, not floor-plan rendering.

## 8. Named providers (German/European and international), prices, and what distinguishes high-end from cheap output

### Takeaway
The German-speaking market is split:
- **Low-cost productized services** at about €25 per perspective (GrundrissProfi, profi-grundrisse.de, grundrisstausch.de), often offshore-produced templates.
- **Portal-partner services**: McGrundriss for ImmoScout24, ohne-makler.net, newhome.ch in Switzerland.
- **Staging and visualization studios** at €250–1,100 per plan (Maverick Frame, eStaging, visupartner, immoviewer, Spacerenovator, BKBN).

Internationally, RoomSketcher and Matterport dominate software and capture outputs, with many US/offshore studios at $79–500. High-end output differs in material fidelity, lighting, accuracy checks and bespoke furnishing.

### Cited Findings
- **GrundrissProfi (DE):**
  - Price: base **€24.90 net** including one perspective, **+€3.90** per extra perspective. The 2014 price list showed €29.90 (outdated).
  - Turnaround: "in aller Regel innerhalb von 2–3 Werktagen" (usually within 2–3 working days). Elsewhere on the site it says 24 h, or 1–3 working days, so the figures conflict.
  - Options: colors and shapes "nach Wunsch" (on request), Dachschräge (sloped ceiling), transparent background.
  - [GrundrissProfi 3D-Grundriss](https://www.grundrissprofi.de/3d-grundriss/); [GrundrissProfi Angebot](https://www.grundrissprofi.de/angebot/); [GrundrissProfi Stilformen PDF 2014](https://grundrissprofi.de/dokumente/prospekte/uebersicht-stilformen.pdf)
- **profi-grundrisse.de (DE):** Premium 3D-Grundriss **€25.20 net**, about 3–5 working days. — [profi-grundrisse.de](https://www.profi-grundrisse.de/shop/3d-grundrisszeichnung-layout-1/)
- **grundrisstausch.de (DE):** furnished 3D floor plans "alles inclusive **€24.98**". — [grundrisstausch.de](https://grundrisstausch.de/3d-grundrisse-zeichnen-lassen-moebliert/)
- **McGrundriss / grundrisse.de (DE):** the floor-plan partner promoted by ImmobilienScout24 for commercial listers. — [ImmoScout24 – McGrundriss](https://www.immobilienscout24.de/anbieten/gewerbliche-anbieter/inserieren/weitere-produkte/McGrundriss.html); [McGrundriss](https://mcgrundriss.grundrisse.de/?prid=13)
- **ohne-makler.net (DE):** offers either a "realistic 3D rendering" or a "clear 2D illustration" with online ordering. — [ohne-makler.net Service Grundrisse](https://www.ohne-makler.net/service/grundrisse/)
- **newhome.ch (CH):** CHF 75 unfurnished, CHF 150 furnished (5 images + video). — [newhome.ch 2024 PDF](https://assets01.sdd1.ch/assets/lbwp-cdn/newhome-blog/files/1706176143/20240119_immobilienaufnahmen-de.pdf)
- **Maverick Frame (studio with a German site):** blog dated 8 June 2026 gives **€250–1,100 per 3D-Grundriss** and **€250–600 for a standard apartment**. Works from drawings, CAD or sketches. This is a vendor blog. — [Maverick Frame – Was kostet eine 3D-Visualisierung](https://maverickframe.com/blog/was-kostet-eine-3d-visualisierung/); [Maverick Frame – Grundriss-Visualisierung](https://maverickframe.com/de/leistungen/grundriss-visualisierung/)
- **Other DACH (German-speaking) providers:**
  - eStaging (furnished bird's-eye) — [eStaging](https://www.estaging.de/services/3d-grundriss-staging/)
  - visupartner (Draufsicht or Schrägansicht, Immonet partner page) — [visupartner](http://www.visupartner.de/immonet/3d-grundriss.php)
  - immoviewer (visualizations) — [immoviewer](https://visualisierungen.immoviewer.com)
  - FloorDrafter (three view types) — [FloorDrafter](https://floordrafter.com/de/floor-plan-to-3d-model)
  - Render-Vision (architectural visualization, CGArchitect showcase) — [CGArchitect – Render-Vision](https://cgarchitect.com/images/188995a9)
  - shapemotion media service — [Sellwerk](https://sellwerk.de/firmenprofil/shapemotion-media-service---3d-visualisierung)
  - Self-service software: Cedreo, Planner 5D, RoomSketcher.de — [Cedreo Grundriss Wohnung](https://cedreo.com/de/grundriss/wohnung/); [Planner 5D – 3D Grundriss](https://planner5d.com/de/use/3d-grundriss); [RoomSketcher.de – 3D Grundrisse](https://www.roomsketcher.de/funktionen/3d-grundrisse-planen/)
- **International price points:**
  - The 2D3D Floor Plan Company: Economy **$79**, Premium **$139** per floor up to 2,000 sq ft; output up to **4K (3840×2160 px)** plus web versions in JPEG/PNG/PDF; turnaround quoted variously as 24–48 h, 48–72 h or 3–5 days (conflicting). — [2D3D – 3D Floor Plan Prices](https://the2d3dfloorplancompany.com/pricing/3d-floor-plan/); [2D3D – Services](https://the2d3dfloorplancompany.com/services/3d-floor-plan/)
  - Render3DQuick: $299 per floor, 3–4 days. RealSpace 3D: $300–800, 3–6 days. Rush fees are typically +20–50%. — [VizCraft – 3D Rendering Price List 2026](https://vizcraft.ai/blog/posts/3d-rendering-price-list)
  - A general range of about $100–500, with outliers up to $1,500 per floor. — [Coohom – 3D floor plan pricing](https://www.coohom.com/article/3d-floor-plan-pricing); [RITN3D](https://www.ritn3d.com/blog/how-much-does-3d-floor-plan-cost/)
- **Matterport:** dollhouse plus a colored floor-plan view generated from 3D scan data, with a separate 2D schematic export (black and white only, per an older forum post). Competitors describe its plan accuracy as "approximate", while Matterport claims "99%" accuracy (marketing). — [Matterport blog](https://matterport.com/blog/engage-home-buyers-and-sellers-3d-floor-plan-views); [Realpro / SeeVirtual360 comparison](https://realpro.seevirtual360.com/?p=6750); [WeGetAroundNetwork](https://www.wegetaroundnetwork.com/topic/15791/comparison-matterport-floor-plans-versus-my-visual-listings-floor-plans/)
- **Effect on inquiries.** ImmobilienScout24 has stated (as reported by the Berliner Mieterverein; the article is not dated in the search snippet, and the URL path suggests MieterMagazin 12/2008, so it is old) that listings with a 3D-Grundriss receive **more inquiries**. — [Berliner Mieterverein MieterMagazin 12/2008](https://www.berliner-mieterverein.de/magazin/online/mm1208/120812b.htm)

### Inferences
- **High-end vs. cheap:**
  - **Cheap (≈€25–80):** template furniture, generic textures, one fixed camera, standard dark caps, little or no accuracy check, and furnishing that is often not to scale.
  - **High-end (€250+):** furniture matched to room dimensions, real-scale materials matching actual floor coverings, soft HDRI daylight with AO, multiple perspectives (top-down plus 45° bird's-eye), branded colors and labels, checked against measured plans, and print-grade resolution (4K+).
- The newhome.ch "furnished = 2× unfurnished" ratio and GrundrissProfi's per-perspective pricing suggest furnishing and extra views are the main cost drivers in the low end.

### Gaps
- No German provider's output resolution in pixels was found. Only the US 2D3D company's 4K figure is sourced.
- Raumgleiter and other Swiss/Austrian high-end studios were not covered by search results.
- Current McGrundriss and eStaging prices were not found.
- I could not verify the date of the ImmoScout24 inquiry claim, because the page could not be fetched. The URL path suggests MieterMagazin 12/2008, so the statistic is likely old, and I found no current 2023–2026 equivalent.

## 9. Quality markers and common mistakes

### Takeaway
The most damaging mistake is **inaccuracy**: a 3D plan that does not match the real or measured plan "harms more than none". The next most common are scale errors (oversized or undersized furniture), missing doors and windows, overcrowded décor, unclear camera angle, poor labels, and murky dark-on-dark color schemes. Quality markers are accuracy, legibility, true-scale furnishing, soft even light, and consistency with the listing's photos.

### Cited Findings
- BDRA (German real-estate trade article):
  - A 3D-Grundriss must be checked against the actual plan or a current measurement (Aufmessung) before publication. "Ein 3D-Grundriss, der fehlerhaft ist, schadet mehr als gar keiner" (a faulty 3D floor plan does more harm than none).
  - Second mistake: hiding the plan in the listing instead of placing it prominently.
  - The plan should match the level of the professional photos.
  - [BDRA – 3D-Grundrisse für Makler](https://bdra.de/makler-profitieren-interaktive-3d-grundrisse/)
- Common mistakes: wrong scale, unclear camera angle, oversized furniture, missing doors or windows, excessive décor, poor room labelling, overcrowding, being decorative instead of informative, ignoring flow, ordering the plan late, and working from outdated source drawings. Checklist items:
  - Verify wall thicknesses, ceiling heights and door and window sizes.
  - Use real-world furniture sizes.
  - Make 3D match 2D.
  - Test readability on mobile.
  - Make lighting and shadows match the actual property.
  - Attribution within result set uncertain: [Maverick Frame – What is a 3D floor plan](https://maverickframe.com/blog/what-is-3d-floor-plan/); [Medium – common mistakes](https://shushmitaroy.medium.com/3d-floor-plan-design-tips-539caff46e24); [CADCrowd](https://www.cadcrowd.com/blog/how-3d-interior-rendering-helps-with-real-estate-marketing-for-homebuilders-realtors/); [Rare Design Hive – off-plan](https://raredesignhive.com/blog/3d-floor-plans-for-real-estate-marketing/); [Rare Design Hive – accuracy](https://raredesignhive.com/blog/3d-floor-plans-accuracy-reduce-design-errors-rework-on-sit/); [Construction Review Online](https://constructionreviewonline.com/knowhow/minimising-mistakes-3d-rendering-and-architectural-visualization/); [Chasing Illusions](https://www.chasingillusions.in/common-mistakes-3d-floor-plan-walkthroughs/)
- Dark walls plus dark floors produce an unreadable "dark square" from above. — [360 Render](https://www.360render.com/architectural-rendering/what-is-3d-floor-plan-visualization-a-comprehensive-guide-for-property-developers/)
- Strong, dramatic shadows hide parts of the plan, so lighting should be even. — attribution uncertain: [Archfine](https://archfine.com/architectural-visualization-tutorials/rendered-floor-plan) / [Arakot](https://www.arakot.com/how-to-turn-floor-plan-into-3d-render/)
- Walls left at full height obscure windows and doors (RoomSketcher, no-cut mode). Walls drawn at 1 m in the model itself produce a doll's-house look (Offision). — [RoomSketcher Help](https://help.roomsketcher.com/hc/en-us/articles/360014732378); [Offision](https://offision.com/help/en/map/give-objects-height/)
- Mark visualizations as non-binding in the Exposé. — attribution uncertain: [Maverick Frame DE blog](https://maverickframe.com/de/blog/3d-visualisierung-immobilienmarketing/)
- Matterport auto-generated plans are criticized by competitors as "approximate – not dimensionally reliable". — [Realpro / SeeVirtual360](https://realpro.seevirtual360.com/?p=6750)

### Inferences
- A replication QA checklist, derived from the above:
  1. Room shapes, wall thicknesses and opening positions match the source plan exactly.
  2. The cut height is consistent across the apartment, and every window and door is visible.
  3. Furniture is at real dimensions, with clear walkways (≥ ~80–90 cm). The walkway figure is an unsourced ergonomic rule of thumb.
  4. The floor is lighter than the wall caps, and the caps contrast clearly with the floor.
  5. Soft, even daylight with AO, no blown highlights, no black corners.
  6. Room labels and m² (WoFlV) are legible at phone width.
  7. Clean white or transparent background, with consistent styling across all perspectives and floors.
  8. A disclaimer is present.

### Gaps
- No systematic study (e.g. A/B tests by ImmoScout24 or Immowelt in 2023–2026) on which visual features drive inquiries was found. The only inquiry statistic is old.
- The NAR (US National Association of Realtors), Immowelt and current ImmoScout24 guidance pages could not be fetched (blocked).
