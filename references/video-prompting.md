# Video Prompt Engineering Guide

> Universal guide for AI video generation prompting. Works across VEO, Sora, Runway, Kling, and other video generation models.
> Optimized for production-quality clips that don't look AI-generated.

---

## Core Principles

### 1. Direct Like a Filmmaker, Not a Tagger
AI video models respond dramatically better to narrative scene descriptions than keyword lists. Write prompts as if you're briefing a director of photography.

| Weak | Strong |
|------|--------|
| "a dog running, park, sunset" | "A golden retriever bounds through tall grass in a sun-drenched meadow, camera tracking at dog level, golden hour backlight creating a halo around its fur, dust particles floating in the warm light" |
| "car driving, night, city" | "Slow tracking shot of a vintage Porsche 911 gliding through rain-slicked Tokyo streets at midnight, neon signs reflecting in puddles, the camera mounted low on the passenger side" |
| "food being made" | "Overhead crane shot slowly descending as a barista pours steamed milk into a latte, creating a rosetta pattern, warm side lighting from a cafe window catching the steam" |

### 2. Describe Motion Explicitly (CRITICAL)
Unlike images, video requires clear motion direction for every element in the scene.

**What needs motion direction:**
- **Camera** — How the camera moves (or doesn't)
- **Subject** — What the main subject is doing
- **Background** — What moves in the environment
- **Light** — How light changes (clouds passing, sunset shifting)
- **Props/Details** — Small movements that add life (steam rising, curtains swaying)

**Motion vocabulary:**

| Category | Terms |
|----------|-------|
| **Camera** | Dolly in/out, pan left/right, tilt up/down, crane up/down, tracking shot, Steadicam, handheld, locked-off, orbit, whip pan, rack focus |
| **Subject** | Walking, running, turning, gesturing, reaching, creating, typing, painting, dancing, reacting |
| **Environment** | Clouds drifting, leaves rustling, water flowing, traffic streaming, particles floating, shadows shifting |
| **Pacing** | Slow-motion, real-time, time-lapse, speed ramp, freeze frame |

### 3. Set a Temporal Arc
Every video clip should have a beginning, middle, and end — even in 4 seconds. Something should change.

| Duration | Arc Guidance |
|----------|-------------|
| 4 seconds | One clear action: camera push-in reveals subject; or hand places object down |
| 6 seconds | Action + reaction: person enters frame, pauses, turns to camera |
| 8 seconds | Mini story: establishing shot → action → reveal or emotional beat |

### 4. Describe Lighting as Dynamic
In video, light changes over time. Static lighting descriptions produce flat results.

**Static (weaker):** "warm lighting"
**Dynamic (stronger):** "late afternoon sun slowly shifting across the room, warm light catching dust particles as it moves"

**Lighting vocabulary for video:**
- Shifting shadows
- Light playing across surfaces
- Flickering practical lights (candles, neon)
- Passing clouds casting moving shadows
- Sunrise/sunset golden hour progression
- Light leaks and flares entering frame

### 5. Include Audio Direction
Many video models now generate synchronized audio. Describe what should be heard.

**Audio categories:**

| Category | Examples |
|----------|----------|
| **Dialogue** | `"This is beautiful," she whispers.` (always in quotes) |
| **Ambient** | "Distant city traffic, birds chirping, wind through leaves" |
| **Sound effects** | "Coffee cup clinking on saucer, keyboard typing, footsteps on marble" |
| **Music mood** | "Soft lo-fi beats" or "building orchestral tension" (not specific songs) |
| **Silence** | "Intentional near-silence with only ambient room tone" |

---

## Camera & Cinematography Language That Works

### Camera Movements

| Movement | Effect | Best For |
|----------|--------|----------|
| `Slow dolly push-in` | Building intimacy, focus | Product reveals, emotional moments |
| `Slow dolly pull-out` | Revealing context, scale | Establishing shots, reveals |
| `Lateral tracking` | Following action, energy | Walking subjects, process shots |
| `Steadicam follow` | Immersive, documentary | Behind-the-scenes, authentic feel |
| `Locked-off tripod` | Stability, contemplation | Ambient, architectural, time-lapse |
| `Handheld` | Urgency, authenticity | Documentary, BTS, raw energy |
| `Crane up/down` | Grandeur, reveal | Establishing shots, event coverage |
| `Drone aerial` | Scale, perspective | Landscapes, architecture, events |
| `Whip pan` | Energy, transition | Reels, fast-paced content, reveals |
| `Orbit/arc` | Dimensionality | Product showcase, portraits |
| `Rack focus` | Directing attention | Storytelling, product detail |

### Lens & Camera References

| Reference | Effect |
|-----------|--------|
| `Anamorphic 40mm` | Cinematic widescreen, oval bokeh, flare |
| `85mm f/1.4` | Portrait compression, creamy background blur |
| `24mm f/2.8` | Wide, environmental, slight barrel distortion |
| `Macro lens` | Extreme close-up, texture detail |
| `Vintage Helios 44-2` | Swirly bokeh, vintage character |
| `Arri Alexa` | Cinematic color science, organic highlight roll-off |
| `RED V-Raptor` | Sharp, high-dynamic-range, modern cinema |
| `Canon C300` | Natural skin tones, documentary versatile |

### Film Stock & Grade References

| Reference | Look |
|-----------|------|
| `Kodak Vision3 500T` | Warm tungsten tones, visible grain, classic cinema |
| `Kodak Vision3 250D` | Daylight balanced, natural colors, subtle grain |
| `ETERNA Vivid` | Saturated, punchy, broadcast-quality |
| `Teal and orange grade` | Hollywood blockbuster contrast |
| `Lifted shadows / milky blacks` | Faded vintage film look |
| `High contrast with crushed blacks` | Dramatic, noir-inspired |
| `Cross-processed` | Shifted colors, experimental, retro |
| `LOG / flat profile` | Maximum dynamic range, muted (for color grading reference) |

---

## Breaking the AI-Generated Look (CRITICAL)

### Why AI Videos Look "AI"
- **Too smooth** — No grain, no texture artifacts, no lens character
- **Robotic camera movement** — Too precise, too steady, inhuman smoothness
- **Perfect everything** — No imperfection in lighting, framing, or surfaces
- **Morphing artifacts** — Objects or faces subtly shifting/melting
- **Generic environments** — Clean, sterile, stock-footage-feeling spaces
- **Flat audio** — Missing ambient detail, room tone, or natural sound layers

### Anti-AI Techniques for Video

| Technique | What to Add to Prompts |
|-----------|----------------------|
| **Handheld micro-motion** | "Subtle handheld camera drift, not robotically smooth" |
| **Film grain** | "Visible film grain consistent with Kodak Vision3 500T" |
| **Lens breathing** | "Natural lens breathing during focus transitions" |
| **Lens flare** | "Anamorphic lens flare from practical light sources" |
| **Environmental particles** | "Dust particles floating through light beams" |
| **Imperfect framing** | "Slightly asymmetric handheld framing, not perfectly centered" |
| **Rack focus** | "Foreground element drifts in and out of focus naturally" |
| **Surface texture** | "Visible wear and texture on all surfaces" |
| **Ambient sound layers** | "Layered ambient sounds: room tone, distant traffic, subtle hum" |
| **Natural light behavior** | "Light subtly shifting as clouds pass" |

### Words That Produce Generic AI Video (AVOID)

**Banned in prompts**: stunning, sleek, futuristic, cutting-edge, vibrant, dynamic, elegant, breathtaking, cinematic (when used alone), epic (when used alone)

**Use instead**: specific, grounded descriptors. "Warm overhead key light" not "stunning lighting." "Tracking at subject speed" not "dynamic camera." "Anamorphic widescreen" not "cinematic."

---

## Prompts by Use Case

### Landing Page Hero Background
```
Slow, ambient drift through a sunlit creative studio space. Camera barely moves —
a gentle leftward drift over 8 seconds. Golden afternoon light streams through
floor-to-ceiling windows, casting slow-moving shadows across work surfaces.
A moodboard wall with colorful reference images blurs softly in the background.
Dust particles float through warm light beams. Designed as a seamless background
video — no sudden movements, no hard cuts, meditative pacing.
```

### Social Reel / Short
```
Bold opening: camera whip-pans to reveal a young creator painting on a digital
tablet, bold colors exploding onto the screen. Quick push-in to their focused
expression, then cut to their hand swiping across the display. Warm amber
neon light from the left, cool cyan accent from the right. Energetic, scroll-
stopping energy. 9:16 vertical format. Sound: upbeat lo-fi beat with satisfying
digital brush sounds.
```

### Product Demo
```
Clean studio environment, warm directional key light from upper-left. Hands pick
up a smartphone and begin editing a photo — smooth tracking shot follows the
device as it's held at a natural angle. Camera slowly orbits 45 degrees as the
user taps through editing tools. Shallow depth of field isolates the device
against a soft cream background. Sound: gentle UI interaction clicks, soft
ambient music.
```

### Cinematic Brand Film
```
Slow crane shot descending through morning fog to reveal a diverse group of
young creators working in an open-plan studio. Shot on Arri Alexa with Cooke
anamorphic lenses. Kodak Vision3 500T film grain. As the camera settles at
eye level, one creator looks up and smiles — warm, genuine, not posed. Late
morning light pours through industrial windows. Sound: distant keyboard typing,
soft conversations, a coffee machine in the background. The mood is focused
creative energy — alive but not frantic.
```

---

## Common Mistakes to Avoid

1. **No motion direction**: "A mountain landscape" → static image territory. Add: "Slow drone push-in over mist-covered peaks at dawn, clouds flowing through valleys"
2. **Too many simultaneous actions**: Models handle 1-2 clear motions well. 5+ concurrent actions cause confusion
3. **Contradictory movement**: "Static locked camera with dynamic whip pans" — pick one dominant movement
4. **Missing temporal arc**: Every clip needs something that changes, even subtly
5. **Generic audio**: Leaving audio to chance. Always describe ambient sound, even if just "quiet room tone"
6. **Duration mismatch**: Trying to fit a complex narrative into 4 seconds. Match story complexity to duration
7. **Ignoring resolution constraints**: Some models require specific durations for higher resolutions
8. **Over-prompting**: 500+ word prompts confuse the model. Keep under 300 words
9. **No anti-AI cues**: Clean, perfect prompts produce clean, AI-looking output. Add imperfection
10. **Forgetting the context**: Hero background videos need to loop; reels need a hook in second 1

---

## Aspect Ratio Guidance

| Ratio | Best For | Feel |
|-------|----------|------|
| `16:9` | Website backgrounds, YouTube, presentations, ads | Cinematic, wide, environmental |
| `9:16` | Instagram Reels, TikTok, YouTube Shorts, Stories | Intimate, immersive, mobile-first |

---

## Duration Strategy

| Duration | Best For | Story Capacity |
|----------|----------|----------------|
| `4s` | Quick cuts, transitions, loops | One action or reveal |
| `6s` | Standard clips, reels | Action + reaction |
| `8s` | Full scenes, demos, narratives | Mini story with arc |
| `8s × extend` | Longer content | Extended narrative (if model supports extension) |
