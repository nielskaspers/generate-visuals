# Advanced AI Image & Video Generation — Prompting Research

> Research compiled from multiple sources on advanced prompting techniques for AI-generated visuals.
> Covers: prompt structure, anti-AI aesthetics, advanced patterns, and marketing workflows.

---

## 1. AI Image Generation — Advanced Prompting

### Core Prompting Philosophy

**Write like a creative director, not a tag list.**

| Bad (tag soup) | Good (narrative) |
|---------------|-----------------|
| `dog, park, 4k, realistic` | `A golden retriever mid-leap catching a frisbee in a sun-dappled city park, shallow depth of field, late afternoon light` |
| `Cool car, neon, city, night, 8k` | `Cinematic wide shot of a sports car speeding through rainy Tokyo at night, neon reflections on wet asphalt` |
| `dramatic lighting` | `Single key light positioned 45 degrees above left of subject, creating natural shadow fall on right side of face, secondary fill light at 25% intensity` |

### The 6-Factor Prompt Structure

Every prompt should include:
1. **Subject** — who/what is in the image
2. **Composition** — camera angle, framing, shot type
3. **Action** — what is happening
4. **Environment** — where, what setting
5. **Lighting** — quality, direction, color temperature
6. **Style/Mood** — emotional tone, artistic reference

### Golden Rules

1. **Edit, don't re-roll** — If an image is 80% correct, use conversational editing: "Change the lighting to sunset and make the text neon blue." Never regenerate from scratch when you're close.
2. **Natural language over tags** — Write descriptive paragraphs, not keyword lists. Models understand narrative context.
3. **Specificity matters** — "Sophisticated elderly woman wearing vintage Chanel-style suit" beats "a woman."
4. **Provide context** — Include the "why" or "for whom": "sandwich for a Brazilian high-end gourmet cookbook" helps the model infer professional plating and lighting.
5. **Include materiality** — "brushed steel," "soft velvet," "crumpled paper" — specific material descriptions massively improve output.
6. **Use positive framing** — Describe what you want, not what you don't. "Empty street" instead of "no cars."

### Key Capabilities Across Modern AI Models

| Capability | How to Use It |
|-----------|--------------|
| **Text rendering** | Place text in quotation marks. Specify font style, size, color: `Write "HELLO WORLD" in bold red serif font on the sign` |
| **Infographics** | Request "compression" of dense content into visual aids. Specify style: "polished editorial," "technical diagram," "hand-drawn whiteboard" |
| **Character consistency** | Use "Identity Locking": "Keep facial features exactly the same as the first image." Describe expression/pose changes while maintaining identity |
| **Dimensional translation** | Convert 2D floor plans to 3D renders, or 3D scenes to 2D illustrations |
| **Sequential narratives** | Generate multi-part image stories. Specify: "16:9 landscape format, one image at a time." Maintain character consistency |
| **Layout control** | Upload sketches, wireframes, or grids to enforce composition. Models follow positional structure |
| **Conversational editing** | Semantic instructions without manual masking: "Remove tourists and fill space with matching textures" |

### Advanced Prompt Patterns

**Data Ingestion Pattern:**
```
Generate [visual format] summarizing [content]. Include [specific elements] and highlight [key information] in [stylized element].
```

**Consistency Pattern:**
```
Keep [subject attribute] exactly the same as [reference], but change [specific element]. [Action description].
```

**Context-Rich Pattern:**
```
Create [asset] as if [professional context]. Style: [descriptor]. Lighting: [descriptor]. Quality: [technical specification].
```

**Narrative Pattern:**
```
Create a [tone] [number]-part story featuring [characters]. Story should have [emotional arc]. Keep [identity elements] consistent, but [variation directive]. Format: [aspect ratio].
```

**Face Preservation Directive:**
```
Keep the facial features of the person in the uploaded image exactly consistent. Do not change the face.
```

### JSON-Structured Prompts (Advanced)

For complex compositions, use JSON to organize parameters. Some models handle this well:
```json
{
  "subject": "young woman, age 22",
  "expression": "confident half-smile",
  "clothing": "oversized vintage denim jacket, white t-shirt",
  "photography": {
    "camera": "Canon EOS R5",
    "lens": "85mm f/1.4",
    "lighting": "golden hour, warm rim light from behind"
  },
  "background": "urban rooftop, city skyline out of focus",
  "mood": "aspirational, warm, authentic",
  "preserve_original": true
}
```

---

## 2. Prompt Architecture by Use Case

### Photorealistic Scenes
```
A photorealistic [shot type] of [subject], [action], set in [environment]. Illuminated by [lighting], creating [mood]. Captured with [camera details]. [Aspect ratio].
```

### Stylized Illustrations
```
[Style] illustration of [subject] with [key characteristics]. Color palette: [colors]. Line style: [thick/thin/varied]. Shading: [cel/gradient/flat]. Background: [color/scene].
```

### Product Mockups
```
Studio product shot of [product description] on [surface]. Three-point lighting: key light from [direction], fill from [direction], backlight creating [effect]. Shot with [lens], focus on [detail]. [Resolution].
```

### Text in Images
```
Write the text "[EXACT TEXT]" in [font style], [color], [size] on [surface/location]. Design approach: [style]. Color scheme: [palette].
```

### Photographic/Cinematic Language That Works

| Term | Effect |
|------|--------|
| `wide-angle shot` | Expansive, environmental context |
| `macro shot` | Extreme close-up, texture detail |
| `low-angle perspective` | Power, dominance |
| `85mm portrait lens` | Natural compression, flattering portraits |
| `Dutch angle` | Tension, unease |
| `shallow depth of field` | Subject isolation, bokeh |
| `three-point lighting` | Professional studio look |
| `golden hour` | Warm, flattering natural light |
| `Rembrandt lighting` | Dramatic portraiture |
| `f/1.4 aperture` | Maximum background blur |

### Multi-Image & Editing

- **Conversational editing**: Make incremental refinements in follow-up prompts
- **Multi-image composition**: Specify which elements from each image to combine
- **Style transfer**: Transform photos into specific artistic styles while maintaining composition
- **Aspect ratio**: Many models adopt the ratio of the **last** provided image
- **Character consistency**: Establish detailed character description in first prompt; model maintains across edits
- **If features drift**: Restart with comprehensive description rather than trying to correct incrementally

---

## 3. Anti-AI Aesthetic Techniques

### Why AI Images Look "AI"

The core problem: AI images are the **average of aesthetic desires** — neither jarringly unique nor transcendentally beautiful. They exhibit:
- **Excessive smoothness** — no grain, no texture artifacts
- **Perfect symmetry** — unnatural bilateral precision
- **Glossy surfaces** — everything looks polished and new
- **Generic lighting** — flat, even, corporate-feeling
- **Sterile environments** — no mess, no lived-in quality
- **Uncanny faces** — too perfect skin, vacant expressions

### 7 Prompt Techniques That Break the AI Look

| Technique | What to Add to Prompts | Why It Works |
|-----------|----------------------|-------------|
| **1. Camera/lens specifics** | "Shot on Nikon Z9, 50mm f/1.4, studio lighting" | Forces photographic qualities over generic output |
| **2. Natural imperfections** | "Weathered face, slight asymmetry, natural skin texture, freckles, visible pores" | Reality has flaws; sterile perfection = AI |
| **3. Environmental context** | "Loft studio, afternoon light through dusty windows, music sheets scattered" | Prevents "floating in void" appearance |
| **4. Material specificity** | "Full-grain brown leather with visible grain, cracked seams" or "brushed stainless steel, tiny fingerprints" | Tactile detail = believability |
| **5. Candid moments** | "Caught mid-stride, turning head, genuine laughter, natural surprise" | Static poses scream AI; motion = life |
| **6. Film stock references** | "Kodak Portra 400," "Ilford HP5 pushed one stop," "high grain," "light-leak" | Invokes organic photochemical artifacts |
| **7. Negative prompting** | "--no plastic skin, glossy surfaces, artificial lighting, extra limbs, cartoonish" | Directly removes common AI artifacts |

### Anti-AI Design Principles (for post-processing and design)

**1. Intentional Imperfection (Wabi-Sabi)**
- Add texture overlays at 5-15% opacity using multiply blend mode
- Use typefaces that simulate ink spread or letterpress
- Apply `filter: contrast(110%) brightness(95%)` to soften digital perfection

**2. Hand-Drawn Elements**
- Slight variations in repeated characters prove human creation
- Mix AI output with one hand-drawn element (icon, lettering, illustration)
- Vectorize hand-drawn work but preserve inconsistencies

**3. Tactile Materiality**
- Apply high-res material textures (wood, fabric, metal) at 3-8% opacity
- CSS: `background-blend-mode: overlay` with `opacity: 0.05`
- Consider the physical feel — grain, weight, texture

**4. Brutalist Typography**
- Tight line-height: 0.8-0.95
- Negative letter-spacing: -1px to -3px
- CSS transforms: `transform: skewY(-3deg)` or `rotate(-1deg)`
- Break the grid — every perfect alignment signals "template"

**5. Controlled Chaos**
- Asymmetric image placement
- Extreme scale variations (120px headline + 11px tagline)
- Overlap typography over images with negative margins
- Subtle rotation: `transform: rotate(-1deg) skewX(1deg)`

### Style Directions That Feel Less AI

| Style | Prompt Additions | Effect |
|-------|-----------------|--------|
| **Lo-fi nostalgia** | "Soft film grain, light leaks, warm muted tones, vintage processing" | Retro, lived-in, authentic |
| **Biophilic** | "Natural elements, lush plants, organic materials, natural lighting" | Grounded, calming, real |
| **Old money** | "Timeless details, soft natural light, classic elegance, understated" | Sophistication without flash |
| **Ghibli aesthetic** | "Soft colors, magical atmosphere, hand-drawn look, warm" | Emotional, nostalgic |
| **Kodak Portra** | "Kodak Portra 400 film stock, golden hour, subtle grain, soft focus" | Classic cinematic warmth |
| **1990s camera** | "35mm lens, direct flash, high contrast, film texture" | Raw, unpolished, authentic |

### Post-Processing Checklist

- [ ] Add grain overlay at 10-30% opacity (start subtle, increase)
- [ ] Apply film halation (subtle glow around highlights)
- [ ] Reduce overall saturation slightly
- [ ] Add slight color shift (warm shadows, cool highlights)
- [ ] Introduce micro-texture on smooth surfaces
- [ ] Check for telltale AI symmetry — crop slightly off-center if needed
- [ ] Verify hands, text, and small details

---

## 4. Marketing & Landing Page Visuals

### What AI Image Generation Is Best For

| Use Case | Why AI Works | Quality Level |
|----------|-------------|--------------|
| Blog post headers | Speed + volume, A/B testable | Good enough standalone |
| Social media posts | Rapid variation, trend-responsive | Good with light editing |
| Concept exploration | 3-6 variations in minutes | Starting point, not final |
| Product mockups | Quick visualization, multiple angles | Needs designer polish |
| A/B test variants | Change one element, measure impact | Purpose-built for testing |
| Process diagrams | Metaphorical visuals, flows | Good with text refinement |

### What to Avoid for Marketing

| Risk | Why | Alternative |
|------|-----|------------|
| Homepage hero images | Too high-stakes; AI artifacts damage trust | Professional photography or heavily edited AI |
| Product photography | Customers need authentic representation | Real product shots |
| Regulated industries | Legal compliance issues | Human-created + compliance review |
| Mimicking artists/celebrities | IP/legal risk | Original concepts |
| Final print materials | Resolution and detail requirements | Designer-finished |

### Effective Marketing Image Prompts

**Hero Section:**
```
Professional product photography of [product] on [surface]. Soft studio lighting, clean background in [brand color]. Shot with 85mm lens, f/2.8. Warm, inviting mood. High resolution, suitable for web hero banner at 1920x1080.
```

**Lifestyle/Feature Section:**
```
Authentic candid photograph of [persona] using [product/tool] in [real environment]. Natural window light, slight depth of field. Mood: [aspirational/professional/creative]. Shot on [camera], [film stock]. Imperfect framing, genuine expression.
```

**Illustration/Icon Style:**
```
Clean [style] illustration of [concept]. Color palette: [brand colors]. Line weight: [consistent/varied]. Background: [transparent/white/color]. Minimal, modern, suitable for landing page feature section.
```

**Before/After Comparison:**
```
Split image showing transformation: Left side [before state], right side [after state]. Same lighting, same angle, clear visual difference. Clean dividing line. Professional product demonstration style.
```

### A/B Testing Framework with AI Images

1. **Pick one variable** — color, headline placement, photo vs. illustration, person vs. no person
2. **Generate 2-4 variations** changing only that element
3. **Run test** measuring CTR, conversions, time on page
4. **Keep winner, iterate** on the next variable
5. **Document** the prompt, tool, date, and approver for each version

### Quality Checklist Before Publishing

- [ ] Brand colors and fonts match guidelines
- [ ] People, props, and settings look realistic (check hands, teeth, text)
- [ ] No resemblance to copyrighted work or famous faces
- [ ] Representation is fair and inclusive
- [ ] Resolution and format correct for platform
- [ ] Alt text prepared for accessibility
- [ ] Prompt and approval documented
- [ ] A/B test variant prepared if high-traffic placement

### Marketing Visual Workflow

```
1. Define goal + audience + message
2. Write detailed prompt (style, colors, aspect ratio, mood, purpose)
3. Generate 3-6 variations
4. Select best options
5. Apply anti-AI post-processing (grain, texture, slight imperfection)
6. Verify brand guidelines compliance
7. Optimize file format (WebP for web, PNG for transparency)
8. Deploy + measure
```

---

## Quick Reference: Prompt Enhancers

### Add to ANY prompt for better results:

**For realism:**
```
Shot on [camera model] with [lens focal length] at [aperture]. [Film stock]. Natural skin texture with visible pores. Subtle environmental imperfections.
```

**For mood:**
```
[Time of day] light creating [shadow quality]. Color temperature: [warm/cool/neutral]. Atmosphere: [descriptor]. Emotional tone: [feeling].
```

**For composition:**
```
[Shot type] with [subject] positioned at [rule of thirds location]. Foreground element: [detail]. Background: [depth description]. Negative space: [where].
```

**For anti-AI authenticity:**
```
Subtle film grain, natural color variation, slight lens distortion at edges. Candid, unposed moment. Imperfect framing suggesting real photographer.
```

---

## Sources

- Google Developers Blog: Image Generation Prompting Tips
- Community prompting guides and research
- Anti-AI Design Trends 2026 — crea8ivesolution.net
- Prompt Engineering Best Practices — various sources
- AI Image Trends 2025-2026 — bulkimagegeneration.com
- WordStream: AI Image Prompts Guide
- Marketing AI Image Generation — thatagency.com
