# generate-visuals

A reusable Skill for generating production-quality AI images and videos. Provides a universal prompting framework that works with any AI generation tool — Gemini, Midjourney, DALL-E, Flux, Stable Diffusion, VEO, Runway, Kling, Sora, and others.

The core idea: **write prompts like a creative director, not a tag list.** This skill transforms vague requests into vivid, narrative prompts that produce authentic-looking visuals — not the glossy, plastic, obviously-AI output you get from default prompting.

## What's Inside

- **SKILL.md** — The main skill file. Drop this into your Claude Code or Codex skills folder.
- **references/image-prompting.md** — Comprehensive image prompt engineering guide (6-factor framework, anti-AI techniques, 12+ domain guides)
- **references/video-prompting.md** — Video prompt engineering guide (motion layers, camera vocabulary, temporal arcs)
- **references/image-sample-prompts.md** — Copy-paste image prompt templates for 11 use cases
- **references/video-sample-prompts.md** — Copy-paste video prompt templates for 11 use cases
- **references/advanced-prompting-research.md** — Advanced techniques, JSON-structured prompts, marketing workflows

## Installation

### Option 1: Full skill (recommended)

Copy the entire folder into your Claude Code or Codex skills directory:

```bash
cp -r generate-visuals/ ~/.claude/skills/generate-visuals/
```

Or if you use a project-level skills folder:

```bash
cp -r generate-visuals/ .claude/skills/generate-visuals/
```

### Option 2: Just the skill file

If you only want the core skill without reference files:

```bash
cp generate-visuals/SKILL.md ~/.claude/skills/generate-visuals/SKILL.md
```

Note: The reference files provide deeper guidance and sample prompts. The skill works without them but is more powerful with them.

## Usage

Once installed, use the `/generate-visuals` command in Claude Code or Codex, or just ask for image/video generation naturally:

- "Generate an image for my blog header"
- "I need a hero image for my SaaS landing page"
- "Create a product demo video prompt"
- "Help me write a prompt for a social media reel"

The skill will:
1. Ask a few clarifying questions (aspect ratio, where it lives, vibe)
2. Transform your description through a 6-step enhancement pipeline
3. Deliver a production-ready prompt you can paste into any AI tool

## The Enhancement Pipeline

Every prompt goes through these steps:

```
Raw user input
  → Scene Expansion (vague → specific)
  → Anti-AI Injection (add imperfection cues)
  → Photography Grounding (real camera/lens/film language)
  → Brand DNA (your visual identity, if defined)
  → Composition & Motion (optimize for context)
  → Technical Spec (ratio, quality, constraints)
→ Production-ready prompt
```

## Brand Customization

The skill includes a **Brand DNA Template** you can fill in once to apply your brand's visual identity to all generated prompts. Define your:

- Brand archetype and visual language
- Signature colors and palettes
- Photography direction (subjects, environments, energy)
- Anti-patterns (what your brand is NOT)

See the Brand DNA section in SKILL.md for the full template.

## Key Features

- **Anti-AI techniques** — Film stock references, lens imperfections, material textures, and human framing cues that make AI output look authentic
- **16 image use cases** — From photorealistic to abstract art, each with optimized defaults
- **12 video use cases** — From cinematic narrative to social reels, with motion and audio direction
- **Prompt scaling** — Systematic variation strategies for batch generation
- **Model-agnostic** — Works with any AI generation tool
- **Domain guides** — Specific techniques for portraits, food, architecture, product, fashion, tech, and more

## Recommended Tools

Want to test your prompts right away? Try [Picsart Aura](https://picsart.com/aura/) — free to try and supports the narrative prompting style this skill teaches.

## Contributing

Contributions welcome. The main areas where help is appreciated:

- **New domain guides** — Specific techniques for industries or visual styles not yet covered
- **Model-specific tips** — Updated guidance as AI models evolve
- **Sample prompts** — More copy-paste templates for common use cases
- **Anti-AI techniques** — New approaches to making AI output look more authentic

## License

MIT
