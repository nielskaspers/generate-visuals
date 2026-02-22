# AI Image & Video Prompt Engineering Guide

> Universal prompting guide for AI-generated visuals. Works across Gemini, Midjourney, DALL-E, Flux, Stable Diffusion, VEO, Sora, and others.
> Optimized for production-quality assets that don't look AI-generated.

---

## Table of Contents

1. [Core Philosophy](#core-philosophy)
2. [The Universal Prompt Framework](#the-universal-prompt-framework)
3. [The Enhancement Pipeline](#the-enhancement-pipeline)
4. [Breaking the AI Look](#breaking-the-ai-look)
5. [Domain-Specific Guides](#domain-specific-guides)
6. [Video Prompting](#video-prompting)
7. [Style Families](#style-families)
8. [Platform & Context Optimization](#platform--context-optimization)
9. [Text Rendering](#text-rendering)
10. [Editing & Iteration](#editing--iteration)
11. [Common Mistakes](#common-mistakes)
12. [Quick Reference Cheat Sheet](#quick-reference-cheat-sheet)
13. [Brand Customization](#brand-customization)

---

## Core Philosophy

### Write Like a Creative Director, Not a Tag List

AI models respond dramatically better to narrative scene descriptions than keyword lists.

| Bad (tag soup) | Good (narrative) |
|---------------|-----------------|
| `dog, park, 4k, realistic` | `A golden retriever mid-leap catching a frisbee in a sun-dappled city park, shallow depth of field, late afternoon golden light` |
| `Cool car, neon, city, night, 8k` | `Cinematic wide shot of a matte-black sports car speeding through rainy Tokyo at night, neon reflections fracturing on wet asphalt, shot on 35mm anamorphic` |
| `woman, portrait, beautiful` | `Close-up portrait of a woman in her 40s with deep laugh lines, silver-streaked hair tucked behind one ear, afternoon window light casting soft shadows across her face, shot on Kodak Portra 400` |
| `food, plate, restaurant` | `Overhead flat-lay of a rustic brunch spread — sourdough toast with charred edges, smashed avocado, two poached eggs with runny yolks, espresso in a handmade ceramic cup, natural window light from the left, linen napkin with visible weave` |
| `office, team, meeting` | `A product team huddled around a whiteboard covered in colorful sticky notes, one person sketching a wireframe, afternoon light through floor-to-ceiling windows, half-empty coffee cups on the table` |

**Why this works**: Narrative prompts give the model a coherent scene to render. Keywords force it to average unrelated concepts, producing generic output.

### Five Golden Rules

1. **Be specific, not vague** — Every detail you leave out, the model guesses. Its guesses are always generic.
2. **Ground in reality** — Reference real cameras, lenses, film stocks, materials, locations. Real references produce real-looking output.
3. **Describe what you want, not what you don't** — "Empty street" works better than "street with no cars." Save negatives for artifacts.
4. **Include context** — "Sandwich for a Brazilian gourmet cookbook" helps the model infer professional plating, lighting, and styling.
5. **Add imperfection** — Perfect = AI-looking. Real = imperfect. Always add grain, texture, or human touch.

---

## The Universal Prompt Framework

### For Images: 6 Factors

Every image prompt should include these six elements:

| Factor | Question | Example |
|--------|----------|---------|
| **1. Subject** | Who or what is in the scene? | "A ceramicist in her 60s with clay-dusted hands" |
| **2. Composition** | How is the camera positioned? | "Close-up, shot from slightly below, rule of thirds" |
| **3. Action** | What is happening? | "Carefully shaping the rim of a bowl on a kick wheel" |
| **4. Environment** | Where is this? What's the setting? | "A sunlit pottery studio with shelves of bisque-fired pieces" |
| **5. Lighting** | What's the light source, direction, quality? | "North-facing window light, soft and even, warm color temperature" |
| **6. Style/Mood** | What's the emotional tone and visual treatment? | "Quiet, meditative, documentary photography feel, shot on Fuji Pro 400H" |

**Assembled prompt:**
> Close-up portrait of a ceramicist in her 60s with clay-dusted hands, carefully shaping the rim of a bowl on a kick wheel in a sunlit pottery studio. Shelves of bisque-fired pieces visible in the background. North-facing window light, soft and even with warm color temperature. Quiet, meditative, documentary photography feel. Shot on Fuji Pro 400H with an 85mm f/1.8 lens.

### For Video: 8 Factors

Video adds two critical elements — **motion** and **audio**:

| Factor | Question | Example |
|--------|----------|---------|
| **1. Subject** | Who or what is in the scene? | "A barista in a craft coffee shop" |
| **2. Action/Motion** | What's happening and how do things move? | "Pouring a latte, milk swirling into espresso" |
| **3. Camera movement** | How does the camera move? | "Slow push-in from medium shot to close-up on the cup" |
| **4. Environment** | Where? What details? | "Industrial-chic coffee shop, exposed brick, morning rush" |
| **5. Lighting** | Source, direction, quality | "Morning sun through large front windows, warm and directional" |
| **6. Style/Mood** | Emotional tone | "Warm, ritualistic, intimate — like a specialty coffee documentary" |
| **7. Audio** | Sound design | "Espresso machine hissing, ceramic cup clinking on saucer, quiet ambient chatter" |
| **8. Pacing** | Speed and rhythm | "Slow, deliberate — real-time pour, no rush" |

---

## The Enhancement Pipeline

Transform any raw description into a production-grade prompt in 5 steps:

```
Raw user input
  ↓
Step 1: SCENE EXPANSION — Turn vague descriptions into specific, tangible scenes
  ↓
Step 2: ANTI-AI INJECTION — Add imperfection cues that break the AI-generated look
  ↓
Step 3: REALITY GROUNDING — Anchor in real camera/lens/film/medium language
  ↓
Step 4: COMPOSITION FOR CONTEXT — Optimize layout for where the asset lives
  ↓
Step 5: TECHNICAL SPEC — Aspect ratio, quality, hard constraints
  ↓
Enhanced prompt
```

### Step 1 — Scene Expansion

Never pass a vague prompt through. Expand every element with tangible, specific details.

| Vague input | Expanded scene |
|-------------|---------------|
| "A person editing photos" | "A young creative professional sitting cross-legged on a mustard-yellow velvet couch, laptop balanced on their knees, colorful mood board pinned to the exposed-brick wall behind them, afternoon sunlight cutting diagonal shadows across the floor" |
| "A nice restaurant" | "A dimly lit corner table at a Mediterranean restaurant — a single candle in a glass holder, olive oil in a ceramic dish, fresh rosemary sprig on a terracotta plate, exposed stone wall with warm sconce lighting" |
| "A car" | "A dusty 1974 Porsche 911 Carrera parked on a gravel shoulder road overlooking the Pacific coast, late afternoon fog rolling in, paint faded to a warm patina of Tangerine Orange" |
| "Someone running" | "A trail runner mid-stride on a single-track mountain path at dawn, breath visible in the cold air, mud-splattered compression tights, distant peaks catching the first pink light of sunrise" |
| "Office workspace" | "A standing desk setup with a 27-inch monitor showing code, a half-drunk pour-over coffee in a double-walled glass, a well-loved mechanical keyboard with visible key wear, afternoon light through bamboo blinds casting striped shadows" |

### Step 2 — Anti-AI Injection

The most important step. See [Breaking the AI Look](#breaking-the-ai-look) for the full system.

Add 2-3 imperfection cues from this list:
- Film stock reference ("Shot on Kodak Portra 400")
- Lens imperfection ("Slight chromatic aberration at edges")
- Environmental detail ("Dust particles caught in the light beam")
- Material texture ("Visible weave in the fabric")
- Human framing ("Slightly off-center, as if shot handheld")

### Step 3 — Reality Grounding

**For photography:**
```
Camera:     "Shot on Canon 5D Mark IV / Sony A7III / Hasselblad 500C"
Lens:       "35mm f/1.4 / 85mm f/1.8 / 24-70mm f/2.8"
Film/look:  "Kodak Portra 400 / Fuji Pro 400H / cross-processed Ektachrome"
Processing: "Slightly lifted blacks / matte finish / pushed one stop"
```

**For illustration/graphic design:**
```
Medium:     "Gouache on textured paper / screen print with misregistration / risograph in 3 colors"
Technique:  "Visible brush strokes / hand-drawn with ink bleed / woodcut with grain"
Surface:    "Cold-pressed watercolor paper / recycled kraft stock / smooth Bristol board"
```

**For video/cinema:**
```
Camera:     "Shot on Arri Alexa Mini / RED V-Raptor / Canon C300 Mark III"
Lens:       "Anamorphic 40mm / Cooke S4 50mm / vintage Helios 44-2 swirl bokeh"
Movement:   "Slow dolly push-in / smooth Steadicam follow / locked-off tripod"
Film:       "Kodak Vision3 500T tungsten / LOG-graded cinema / ETERNA Vivid"
Grade:      "Teal and orange grade / lifted shadows / milky blacks"
```

**For 3D/product:**
```
Render:     "Cinema 4D style / Blender Cycles / Octane render"
Material:   "Subsurface scattering on skin / caustics in glass / physically-based metals"
Light:      "Three-point studio setup / HDRI environment / single area light with bounce"
```

### Step 4 — Composition for Context

Where an image or video lives determines its composition:

| Context | Composition Rules |
|---------|-------------------|
| **Website hero** | Leave 40% negative space for headline overlay. Subject anchored to opposite side. Gradient or blur toward text zone. |
| **Blog/article header** | Wider, more atmospheric. Subject can be smaller. Mood over detail. |
| **Social post** | Fill the frame. Bold, immediate impact. Works at thumbnail size. |
| **Social story/reel** | Vertical 9:16. Subject centered. Key content in center 60% (edges get cropped). |
| **Thumbnail** | Extreme contrast. Face or key object fills 60%+. Space for 2-3 word overlay. |
| **Ad creative** | Product/result front and center. Clear visual hierarchy. CTA-ready zone. |
| **Presentation slide** | Clean background. Subject well-separated. Works at low resolution on projectors. |
| **Email header** | Simple, high contrast. Important content in top half (below-fold gets clipped). |
| **Product page** | Clean background (white or contextual). Multiple angles. Consistent lighting across set. |
| **Print (poster/flyer)** | High resolution critical. Allow bleed area. CMYK-friendly colors. |

### Step 5 — Technical Spec

Always append these constraints:

**For images:**
```
Aspect ratio: {ratio}
Output: Single high-fidelity image, production-ready
No watermarks, no AI artifacts, no placeholder text
No generic stock-photo compositions
```

**For video:**
```
Aspect ratio: {ratio}
Duration: {seconds} seconds
Resolution: {resolution}
Smooth, natural motion — no jittering or morphing artifacts
No watermarks, no placeholder text overlays
```

---

## Breaking the AI Look

The biggest problem with AI visuals isn't quality — it's that they look AI-generated. That clinical, too-perfect, oddly smooth aesthetic is instantly recognizable.

### Why AI Output Looks "AI"

- **Excessive smoothness** — no grain, no texture artifacts
- **Perfect symmetry** — unnatural bilateral precision
- **Glossy surfaces** — everything looks polished and new
- **Generic lighting** — flat, even, corporate-feeling
- **Sterile environments** — no mess, no lived-in quality
- **Uncanny faces** — too-perfect skin, vacant expressions
- **Blue-purple gradients** — the default AI color palette

### The Anti-AI Toolkit

#### 1. Film & Camera Anchors

| Technique | Prompt Fragment | Best For |
|-----------|----------------|----------|
| Film stock | "Shot on Kodak Portra 400" | Portraits, lifestyle, warm tones |
| Film stock | "Ilford HP5 pushed one stop" | B&W, gritty, documentary |
| Film stock | "Fuji Superia grain" | Casual, everyday, nostalgic |
| Film stock | "Cross-processed Ektachrome" | Bold colors, experimental |
| Camera body | "Shot on Hasselblad 500C" | Medium format, fashion, fine art |
| Camera body | "Shot on Canon 5D Mark IV" | General professional |
| Camera body | "Shot on disposable camera" | Lo-fi, authentic, party vibes |
| Lens | "85mm f/1.4 portrait lens" | Portraiture, shallow DOF |
| Lens | "24mm wide angle with barrel distortion" | Environmental, documentary |
| Lens | "Vintage Helios 44-2 with swirl bokeh" | Dreamy, artistic |

#### 2. Imperfection Cues (Pick 2-3 Per Prompt)

| Category | Examples |
|----------|----------|
| **Film artifacts** | "Subtle film grain", "gentle halation around highlights", "slightly lifted blacks", "light leak in corner" |
| **Lens physics** | "Natural vignette at corners", "slight chromatic aberration at edges", "hexagonal bokeh shapes", "soft focus at extreme edges" |
| **Environmental** | "Dust particles in the light beam", "condensation on glass", "atmospheric haze", "morning dew on surfaces" |
| **Texture** | "Visible fabric weave", "skin pores and micro-texture", "fingerprints on glass", "scratches on wood surface" |
| **Human framing** | "Slightly asymmetric — as if handheld", "not perfectly centered", "foreground element slightly soft" |
| **Light behavior** | "Lens flare from practical light source", "light spill from off-frame window", "caustic reflections on wall" |
| **Wear & age** | "Paint chipping on the doorframe", "worn leather showing patina", "coffee ring stain on the table" |

#### 3. Material Specificity

Generic materials produce generic results. Be tactile:

| Generic (looks AI) | Specific (looks real) |
|--------------------|-----------------------|
| "leather jacket" | "worn full-grain leather jacket with visible cracking at the elbows and a tarnished brass zipper" |
| "wooden table" | "reclaimed oak table with ring stains, knife marks, and a crack filled with dark resin" |
| "glass of water" | "thick-walled tumbler with condensation droplets and a single lime wedge resting on the rim" |
| "fabric" | "raw linen with visible slub texture, slightly wrinkled from wear, fraying at the hem" |
| "metal" | "brushed aluminum with fine directional scratches catching the light" |
| "concrete" | "poured concrete with visible aggregate, hairline crack, and water staining at the base" |
| "paper" | "heavy cotton rag paper with deckled edges and a slight ivory tint" |
| "stone" | "tumbled travertine with natural pitting and warm honey-toned veining" |
| "plastic" | "matte-finish injection-molded plastic with a visible parting line and slight sink mark" |

#### 4. Words That Produce Generic AI Output (AVOID)

These words trigger the model's "default beautiful" mode:

**Banned**: stunning, sleek, futuristic, cutting-edge, vibrant, dynamic, elegant, breathtaking, jaw-dropping, mesmerizing, gorgeous, epic, dramatic (as standalone adjective), ultra-realistic, hyper-detailed, 8k, masterpiece

**Use instead**: specific, grounded descriptors.

| Instead of... | Use... |
|---------------|--------|
| "stunning" | "warm" / "arresting" / describe what makes it striking |
| "vibrant" | "saturated coral" / "rich emerald" / name the actual color |
| "sleek" | "minimal with beveled edges" / describe the actual form |
| "dynamic" | "asymmetric" / "off-balance" / describe the actual energy |
| "elegant" | "restrained" / "sparse" / describe what's elegant about it |
| "dramatic lighting" | "Single key light positioned 45 degrees above left, hard shadow fall on the right side" |

---

## Domain-Specific Guides

### Portrait Photography

**Template:**
```
[Shot type] portrait of [subject description], [action/expression].
[Location/setting]. [Lighting setup].
Shot on [camera] with [lens] at [aperture].
[Film stock or processing]. [Imperfection cues].
[Mood descriptor].
```

**Example — Editorial portrait:**
> Waist-up portrait of a chef in her mid-30s, arms crossed, standing in a dimly lit restaurant kitchen. Flour dusted on her black apron, a few wisps of hair escaped from her chef's hat. Single bare bulb hanging behind her right shoulder creating a warm rim light, kitchen's stainless steel surfaces reflecting soft glows. Shot on a Canon 5D Mark IV with an 85mm f/1.4 lens. Kodak Portra 800 pushed one stop — visible grain, warm skin tones. Slight lens vignette at corners. Mood: confident, tired, proud.

**Example — Environmental portrait:**
> Wide environmental portrait of an elderly fisherman sitting on the bow of his weathered wooden boat, mending a fishing net with practiced hands. Early morning light over a calm harbor, other boats soft in the background fog. Shot on Fuji GFX 50S with a 45mm lens. Fuji Pro 400H color science — muted, slightly desaturated. Natural skin texture, deep wrinkles catching the side light. Rope textures, peeling paint on the hull. Handheld, slightly imperfect framing.

### Food & Beverage

**Template:**
```
[Angle: overhead/45-degree/eye-level] [shot type] of [dish/drink description].
[Plating/presentation details]. [Props and surface].
[Lighting: natural/studio]. [Color mood].
[Context: cookbook, restaurant menu, social media, editorial].
[Style reference].
```

**Example — Restaurant dish:**
> 45-degree close-up of a miso-glazed black cod fillet on a handmade ceramic plate, charred scallion and pickled ginger garnish, sauce dots in an arc. Reclaimed walnut table surface, linen napkin with visible weave, pair of ebony chopsticks. Natural window light from the left with a white bounce card on the right for fill. Warm, earthy tones. Styled for a high-end restaurant's Instagram — effortlessly elegant, not fussy. Shot on Sony A7III with a 90mm macro at f/4. Slight steam rising from the fish.

**Example — Cocktail:**
> Straight-on eye-level shot of a Negroni in a heavy-bottomed rocks glass with a single large ice sphere, blood orange peel curled on top. Dark marble bar surface, bartender's hands blurred in the background. Warm tungsten backlight from bar bottles creating amber glow through the drink. Condensation on the glass catching light. Shot on 50mm f/1.8, shallow depth of field. Moody, intimate speakeasy atmosphere. Slight lens flare from the backlight.

### Architecture & Interior Design

**Example — Exterior architecture:**
> Wide establishing shot of a brutalist concrete library at blue hour. The building's board-formed concrete facade catches the last deep blue light of dusk, while warm amber light glows from floor-to-ceiling windows on three levels. A few silhouetted figures visible inside. Rain-wet plaza in the foreground reflecting the building's geometry. Shot on a 24mm tilt-shift lens, corrected verticals. Atmospheric haze. Subtle film grain. Mood: monumental yet inviting.

**Example — Interior design:**
> Wide-angle interior of a Japandi-style living room. Low walnut coffee table with a single ceramic vase holding dried pampas grass. Bouclé sofa in warm cream against a limewashed wall. Floor-to-ceiling linen curtains filtering soft afternoon light, casting long diffused shadows across a sisal rug. A stack of art books on the floor, one open. Shot on a 28mm lens at f/5.6 for deep focus. Warm, muted palette — cream, walnut, sage, charcoal. Lived-in, not showroom. Slight overcast light with gentle directionality.

### Product & E-commerce

**Example — Clean product shot:**
> Studio product photograph of a matte-black ceramic travel mug with a cork grip band on a seamless warm gray background. Three-point lighting: soft key light at 45 degrees from upper left, subtle fill from right, rim light from behind creating a thin bright edge. Slight reflection on the surface below. Shot on a 90mm macro at f/8 for full depth of field. Visible texture in the ceramic glaze — not perfectly smooth, slight surface variation. One small water droplet on the lid catching a highlight.

**Example — Lifestyle product shot:**
> A pair of minimalist white leather sneakers on a sun-faded concrete step outside a Mediterranean cafe. One shoe on its side, laces slightly loose. Warm afternoon light, long shadow. A folded newspaper and an espresso cup in the background, soft focus. The leather shows natural creasing — these are worn, not new. Shot on Kodak Portra 400 with a 50mm f/1.4. Casual, effortless, lived-in lifestyle.

### Nature & Landscape

**Example — Mountain landscape:**
> Wide panoramic shot of a glacial valley at dawn. Jagged granite peaks catching the first orange light of sunrise while the valley floor remains in cold blue shadow. A braided river of milky glacial meltwater winds through the valley, reflecting the sky. Patches of alpine wildflowers — purple lupins and yellow buttercups — in the foreground, slightly soft due to shallow focus. Atmospheric haze layering the mountains in progressively lighter tones of blue-gray. Shot on a 35mm f/2.8, Fuji Velvia 50 — saturated but not unnatural. Slight chromatic aberration at the edges.

**Example — Intimate nature:**
> Close-up of morning dew on a spider web strung between two blades of wild grass. Each water droplet acts as a tiny lens, refracting the out-of-focus green meadow behind it. One droplet catching a single point of warm morning sunlight. Extreme shallow depth of field — only the center droplets are sharp, everything else dissolves into soft green and gold bokeh with hexagonal highlights. Shot on a 100mm macro at f/2.8 on a Canon 5D. Natural, quiet, fragile.

### Technology & SaaS

**Example — SaaS hero:**
> A woman in her 30s at a standing desk, reviewing data on a large curved monitor. Her expression is focused but calm — one hand on the mouse, one holding a coffee mug. The monitor shows blurred colorful charts (not readable, just light patterns). Industrial-chic office: polished concrete floor, plants on a shelf, warm pendant light above. Late afternoon — golden light from a window behind her creating a warm rim light on her hair. Shot on 35mm f/2 with shallow depth of field. Negative space on the left side for headline overlay. NOT a stock photo: real mess on desk (cable, notebook, pens), genuine posture, natural expression.

---

## Video Prompting

Video prompts require everything in image prompts PLUS explicit direction of movement and time.

### The Three Motion Layers

Every video prompt should describe motion in three layers:

| Layer | What Moves | Example |
|-------|-----------|---------|
| **Camera** | The viewer's perspective | "Slow dolly push-in", "handheld following", "crane up revealing" |
| **Subject** | The main focus of the scene | "Walking toward camera", "hands shaping clay", "turning to look" |
| **Environment** | Background and atmosphere | "Clouds drifting", "leaves rustling", "light slowly shifting" |

### Camera Movement Vocabulary

| Movement | Effect | Best For |
|----------|--------|----------|
| **Static / locked-off** | Stability, observation | Interviews, product shots, contemplative scenes |
| **Slow dolly push-in** | Building intimacy or tension | Reveals, emotional moments |
| **Dolly pull-out** | Context reveal, expansion | Establishing shots, endings |
| **Tracking / follow** | Energy, journey | Action, walking, process |
| **Steadicam orbit** | Dimensionality, exploration | Product showcase, architecture |
| **Crane up** | Scale reveal, grandeur | Establishing, transitions |
| **Crane down** | Grounding, arrival | Intros, focusing attention |
| **Handheld** | Authenticity, urgency, documentary | BTS, social content, raw energy |
| **Whip pan** | Transition, surprise | Fast-paced edits, social reels |
| **Tilt up / tilt down** | Vertical reveal | Architecture, full-body reveals |
| **Drone / aerial** | Scale, geography, freedom | Landscapes, real estate, events |

### Temporal Arc

Even a 4-second video needs a beginning, middle, and end. Something must change:

| Duration | Arc Strategy |
|----------|-------------|
| **4 seconds** | One clear action: enter → do → hold. Example: "Hand reaches into frame, picks up coffee cup, brings it toward camera" |
| **6 seconds** | Action + reaction: establish → action → result. Example: "Chef slices through crust (crispy sound), steam rises, camera tilts up to chef's satisfied nod" |
| **8 seconds** | Mini-narrative: setup → development → conclusion. Example: "Wide shot of empty studio, dancer enters from right, begins slow spin, camera pushes in as spin accelerates, ends on close-up of face mid-movement" |

---

## Style Families

### Photorealistic

| Style | Signature Prompt Additions |
|-------|---------------------------|
| **Natural light documentary** | "Available light only, no flash. Slight underexposure in shadows. Handheld, imperfect framing. Kodak Tri-X or Portra 400." |
| **Studio professional** | "Three-point lighting setup. Clean background (white/gray seamless). Shot on medium format for shallow DOF at distance." |
| **Lifestyle editorial** | "Golden hour or window light. Lived-in environment. Candid pose, between moments. Matte processing, slightly desaturated." |
| **Cinematic** | "Anamorphic lens flare. 2.39:1 aspect ratio. Color graded: teal shadows, warm highlights. Shallow DOF with bokeh." |
| **Lo-fi / film** | "Disposable camera aesthetic. Direct flash, red-eye, grain, slightly blown highlights, warm color shift." |

### Illustration

| Style | Signature Prompt Additions |
|-------|---------------------------|
| **Flat vector** | "Clean geometric shapes, limited color palette (4-6 colors), no gradients, bold outlines or no outlines. Suitable for scaling." |
| **Editorial illustration** | "Conceptual, metaphorical. Hand-drawn texture with digital color. Visible brush strokes or pencil lines. Limited palette." |
| **Watercolor** | "Wet-on-wet technique, color bleeding at edges, unpainted white areas showing paper texture. Soft, organic, imprecise edges." |
| **Risograph / screen print** | "2-3 color separation, slight misregistration between layers, halftone dots visible, recycled paper texture." |
| **Line art / ink** | "Black ink on white, varying line weight, cross-hatching for shadow, pen-and-ink texture, no color." |

### 3D & CGI

| Style | Signature Prompt Additions |
|-------|---------------------------|
| **Product render** | "Clean studio render. Physically-based materials. Subtle caustics and reflections. HDRI environment lighting." |
| **Isometric** | "Isometric projection (no perspective). Clean geometry, pastel or bold colors, miniature/diorama feel." |
| **Clay / matte** | "Matte clay material on all surfaces. Soft studio lighting. Pastel palette. Miniature feel." |
| **Hyper-detailed** | "Octane render, subsurface scattering, ray-traced reflections, volumetric fog. Cinematic camera." |

### Graphic Design

| Style | Signature Prompt Additions |
|-------|---------------------------|
| **Swiss / International** | "Grid-based layout, sans-serif typography (Helvetica-style), limited color, maximum whitespace, objective." |
| **Brutalist** | "Raw, unpolished, anti-design. System fonts, harsh contrast, no decoration, exposed structure." |
| **Retro / Vintage** | "Faded colors, halftone dots, aged paper texture, period-appropriate typography and layout." |
| **Maximalist** | "Dense layering, mixed media, clashing patterns, saturated colors, visual overload — intentional and composed." |

---

## Platform & Context Optimization

### Aspect Ratios

| Ratio | Best For | Feel |
|-------|----------|------|
| `1:1` | Instagram feed, profile images, app icons | Square, balanced, social-first |
| `3:2` | Blog headers, editorial, standard photos | Classic photographic landscape |
| `4:5` | Instagram posts, portrait posters, Pinterest | Tall portrait, social-optimized |
| `16:9` | Website heroes, YouTube thumbnails, presentations | Wide, cinematic, professional |
| `9:16` | Stories, Reels, TikTok, mobile screenshots | Vertical, mobile-first |
| `2.39:1` | Cinematic banners, film-style headers | Ultra-wide, dramatic |
| `21:9` | Desktop wallpapers, ultra-wide monitors | Panoramic |

### Mobile Considerations

- **Keep important content in the center 60%** — edges get cropped on mobile
- **Use high contrast** — small screens need strong figure-ground separation
- **Simplify compositions** — complex scenes become noise at phone size
- **Test at thumbnail size** — if you can't tell what it is at 80px, it won't work

### Dark Mode Considerations

- Avoid pure white backgrounds (#FFFFFF) — they blind dark mode users
- Use off-white (#F5F5F5 or warmer) or provide a dark variant
- Ensure sufficient contrast in both light and dark contexts

---

## Text Rendering

Text in AI-generated images is improving but still imperfect. Tips:

1. **Specify exact text in quotes**: `The text reads "HELLO WORLD" in bold sans-serif`
2. **Keep it short**: 1-5 words render most reliably
3. **Describe placement**: "Centered at the top third" or "Bottom-left corner"
4. **Describe font style**: "Bold, uppercase, white text with a subtle drop shadow"
5. **Describe size**: "Large headline text filling 40% of the image width"
6. **Specify color and contrast**: "White text on dark background" or "Dark text on light area"
7. **Avoid**: Long paragraphs, small text, cursive fonts, multiple text blocks
8. **For logos**: Describe the mark/symbol separately from the wordmark

---

## Editing & Iteration

### Image Editing Prompts

When editing existing images:

1. **Describe what to change**: "Replace the sky with a dramatic sunset"
2. **Describe what to keep**: "Keep the foreground buildings and people unchanged"
3. **Be precise about regions**: "In the top-left quadrant, change the tree to a palm tree"
4. **Match style**: "Match the existing lighting, color grade, and grain level"
5. **Use masks**: White areas = regions to edit, black areas = preserve

### Iteration Strategy

Plan for 2-3 rounds:

| Round | Focus | Action |
|-------|-------|--------|
| **1 — Composition** | Layout, scene, subjects, overall feel | Major prompt changes OK |
| **2 — Details** | Lighting, colors, textures, small elements | Targeted refinements only |
| **3 — Polish** | Artifacts, text fixes, final adjustments | Minimal, precise changes |

**Between rounds:**
- Keep what worked, specify only what to change
- Add more detail to weak areas
- Don't rewrite the entire prompt — adjust incrementally
- If 80% correct, use conversational editing: "Keep everything, but change the lighting to sunset"

---

## Common Mistakes

1. **Too short**: "mountain" → model guesses everything. Add scene, time of day, light, style.
2. **Too long / contradictory**: 1000-word prompts confuse the model. Stay under 300 words, 500 max.
3. **Overly abstract**: "the essence of freedom" → models are literal. Describe what freedom LOOKS like.
4. **Mixing incompatible styles**: "realistic oil painting pixel art" → pick one direction.
5. **Forgetting composition**: Great subject + no framing = awkward crop.
6. **Ignoring lighting**: Default lighting looks flat. Always specify source, direction, quality.
7. **Same palette every time**: Blue-purple gradient is the AI cliche. Rotate palettes deliberately.
8. **No imperfection cues**: Perfect = AI-looking. Always add grain, vignette, texture, or human touch.
9. **Generic materials**: "leather" reads AI. "Cracked saddle leather with brass rivets" reads real.
10. **Forgetting where it lives**: Hero without negative space = unusable. Social post too complex = invisible at scroll speed.
11. **Using banned words**: "Stunning dramatic vibrant" produces the most generic possible output.
12. **No motion direction in video**: "A city street" is a photo prompt. "Camera slowly dollies through a city street as pedestrians pass" is a video prompt.
13. **Static video subjects**: If nothing moves, it's a photo. Give subjects action: reaching, turning, walking, creating.
14. **Ignoring audio in video**: Sound is 50% of video. Always specify: ambient, dialogue, music mood, or deliberate silence.

---

## Quick Reference Cheat Sheet

### Prompt Skeleton — Image
```
[Shot type] of [subject with specific details], [action/pose].
[Environment with tangible details]. [Lighting: source, direction, quality].
Shot on [camera] with [lens] at [aperture]. [Film stock or processing].
[2-3 imperfection cues]. [Mood in 2-3 words].
Aspect ratio: [ratio]. No watermarks, no AI artifacts.
```

### Prompt Skeleton — Video
```
[Camera movement] shot of [subject with details], [action with motion description].
[Environment with ambient motion]. [Lighting that changes over time].
Shot on [cinema camera] with [lens]. [Film look/grade].
[Audio: ambient sounds, dialogue, or music mood].
[2-3 imperfection cues]. [Pacing: slow/medium/fast]. [Mood].
Aspect ratio: [ratio]. Duration: [seconds]s.
```

### Quick Enhancers — Copy-Paste

**For realism:**
```
Shot on [camera] with [lens] at [aperture]. [Film stock]. Natural skin texture with visible pores. Subtle environmental imperfections — dust, wear, texture.
```

**For mood:**
```
[Time of day] light creating [shadow quality]. Color temperature: [warm/cool]. Atmosphere: [hazy/crisp/humid]. Emotional tone: [feeling].
```

**For composition:**
```
[Shot type] with subject at [rule of thirds position]. Foreground element: [detail, slightly soft]. Background: [description, falling out of focus]. Negative space on [side] for text.
```

**For anti-AI authenticity:**
```
Subtle film grain, natural color variation, slight lens distortion at edges. Candid moment, unposed. Imperfect handheld framing. [Film stock] color science.
```

**For video motion:**
```
[Camera movement] following [subject] as [action]. Background [environmental motion]. Light [shifts/flickers/moves]. [Sound description]. Pacing: [speed].
```

---

## Brand Customization

This section shows how to layer brand-specific visual DNA on top of the universal framework above. Replace the template values with your own brand's guidelines.

### How to Use Brand Customization

1. **Start with the universal framework** (6-factor prompt, anti-AI techniques, domain guides)
2. **Add your brand layer** as an additional step in the Enhancement Pipeline — between Anti-AI Injection and Composition
3. **Define your brand's visual DNA** using the template below

### Brand DNA Template

```
Brand Archetype: [Your brand archetype — e.g., "The Explorer", "The Sage", "The Creator"]

Visual Language:
- [Trait 1]: [How it manifests in images]
- [Trait 2]: [How it manifests]
- [Trait 3]: [How it manifests]
- [Trait 4]: [How it manifests]

Signature Colors:
- Primary accent: [color + hex]
- Secondary accent: [color + hex]
- Background: [color + hex]
- Text: [color + hex]

Color Palettes (rotate between):
- Palette A: [3-4 colors]
- Palette B: [3-4 colors]
- Palette C: [3-4 colors]

Photography Direction:
- Subjects: [Who appears in brand imagery]
- Environments: [Where scenes take place]
- Energy: [Calm/energetic/contemplative/bold]
- Diversity: [Representation guidelines]

What We Are NOT:
- [Anti-pattern 1]
- [Anti-pattern 2]
- [Anti-pattern 3]
```

### Example: Outdoor Adventure Brand

```
Brand Archetype: "The Explorer" — bold, adventurous, authentic

Visual Language:
- Rugged, not polished: Weathered textures, natural wear, real conditions
- Vast, not confined: Wide landscapes, open skies, environmental scale
- Active, not posed: Movement, journey, real effort — not lifestyle posing
- Warm, not cold: Golden hour preference, warm earth tones, human warmth

Signature Colors:
- Primary: Burnt orange #D4622B
- Secondary: Forest green #2D5016
- Light: Sand #F2E8D4
- Dark: Charcoal #1A1A1A

Color Palettes:
- Burnt orange + deep green + sand highlights
- Warm slate + golden amber + cream
- Deep navy + terracotta + sage green

Photography Direction:
- Subjects: Real adventurers, diverse ages and backgrounds, visible effort
- Environments: Mountains, trails, rivers, campfires, backcountry
- Energy: Determined, awe-struck, peaceful exhaustion
- Diversity: All body types, ages, abilities — adventure is for everyone

What We Are NOT:
- Gym/fitness aesthetic (sterile, indoor, competitive)
- Instagram-perfect wilderness (posed at cliff edges in clean clothes)
- Extreme sports only (we include gentle hikes and campsite mornings)
```

---

## Model-Specific Tips

While this guide is universal, here are notes on model differences:

| Model | Strengths | Watch Out For |
|-------|-----------|---------------|
| **Gemini** | Text rendering, complex constraints, photography terms, conversational editing | Bias toward realism; struggles with intentional absurdity |
| **Midjourney** | Artistic interpretation, aesthetic beauty, style mixing | Can over-stylize; weaker at following precise composition instructions |
| **DALL-E 3** | Prompt adherence, text rendering, safety compliance | Can feel polished/clean; add extra imperfection cues |
| **Flux** | Photorealism, prompt following, faces | Can default to "AI pretty"; needs strong anti-AI direction |
| **Stable Diffusion** | Customizability (LoRAs, ControlNet), precise control | Requires more technical prompt structure; weaker at long narrative prompts |
| **VEO 3** | Natural motion, audio generation, cinematic quality | 8-second max clips; may smooth out requested imperfections |
| **Sora** | Physics understanding, long coherent shots | Can default to "cinematic perfect"; push for imperfection |

**Universal rule**: If a model ignores imperfection cues, double them. Add both a film stock reference AND a lens artifact AND an environmental detail. The more reality anchors, the less "AI" the output.

---

*Version: 2.0 — Universal edition*
