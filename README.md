# final-design
Synthesized from taste-design and huashu-design. 

# Frontend Design & Prototyper

A unified agent skill for high-fidelity frontend design, interactive prototyping, and production-grade UI engineering. Synthesizes [Huashu Design](https://github.com/anthropics/skills/tree/main/huashu-design) (asset protocols, design advisor, narrative-driven animation, multi-format export) with Design Taste (baseline-driven config, Tailwind/React architecture, Framer Motion, Bento 2.0 dashboards, engineering constraints).

---

## What This Skill Does

This skill transforms an AI agent into a senior design engineer capable of:

| Capability | Examples |
|------------|----------|
| **High-fidelity prototypes** | Interactive HTML demos, iOS/Android mockups, clickable app flows |
| **Production frontend** | React/Next.js components, Tailwind layouts, motion-engineered dashboards |
| **Slide decks** | Multi-file HTML presentations with keyboard nav, PDF/PPTX export |
| **Motion & animation** | CSS transitions, Framer Motion choreography, GSAP scroll-telling, narrative explainer videos |
| **Design direction advisory** | When the brief is vague, recommend 3+ differentiated styles from 20 philosophies |
| **Audio-integrated video export** | MP4 with SFX + BGM, voiceover-driven long-form animations |
| **Expert design critique** | 5-dimension scoring (Philosophy Consistency, Visual Hierarchy, Detail Execution, Functionality, Innovation) |

---

## Quick Start

### Installation

Copy the skill file into your agent's skills directory:

```bash
# Claude Code
cp SKILL.md ~/.claude/skills/frontend-design-prototyper/

# Codex
cp SKILL.md ~/.agents/skills/frontend-design-prototyper/
```

The skill references external assets and scripts (`assets/`, `scripts/`, `references/`). These paths are relative to the skill's root directory. For full functionality, clone the entire repository and point your agent to it.

### Triggering the Skill

The skill activates when you request:
- High-fidelity prototypes or UI demos
- Design exploration ("I need a design direction for...")
- iOS/Android app mockups
- Slide decks or presentations
- Animated explainers or motion design
- Production frontend with premium quality constraints
- Design review or critique

---

## Core Philosophy

**Medium Shifting** — HTML is the tool. The output changes. Embody the right expert: slide designer for decks, animator for motion, UX designer for prototypes. A deck should never feel like a dashboard.

**Honest Placeholder** — A grey block with a label beats a bad AI attempt every time. Never draw crude SVG faces or product silhouettes. Real assets or labelled placeholders only.

**Variations, Not Final Answers** — Every design prompt produces 3+ distinct variants across visual, interaction, layout, and motion dimensions. From by-the-book to novel.

**Fact Verification First** — Before any design work, verify product existence, release status, and specs via web search. Never assume from training data.

---

## Key Design Constraints

- **No AI Purple/Blue** — The default LLM neon aesthetic is banned. Use zinc/slate neutrals with a single high-contrast accent.
- **No Inter Font** — Use Geist, Outfit, Cabinet Grotesk, or Satoshi.
- **No 3-Card Row** — The generic feature grid is banned. Use zig-zag, asymmetric, or horizontal scroll.
- **No Emojis** — Phosphor or Radix icons only.
- **No Pure Black** — Use Off-Black, Zinc-950, or Charcoal.
- **`min-h-[100dvh]`** — Never `h-screen` (iOS Safari viewport bug).
- **Real assets over CSS silhouettes** — Brand work requires logos and product images, not hand-drawn shapes.

---

## Environment-Specific Behavior

The skill adapts to the execution environment:

| Context | Stack | Motion |
|---------|-------|--------|
| Prototypes / demos / slides | Single-file HTML + inline React/Babel + Tailwind CDN | CSS transitions, `assets/animations.jsx`, GSAP via CDN |
| Production frontend | React/Next.js + Tailwind (build) | Framer Motion, `layoutId`, spring physics |

---

## Repository Structure

```
├── SKILL.md                          # Main skill document (the agent reads this)
├── README.md                         # This file
├── assets/
│   ├── ios_frame.jsx                 # iPhone 15 Pro device bezel
│   ├── android_frame.jsx             # Android device bezel
│   ├── macos_window.jsx              # macOS window chrome
│   ├── browser_window.jsx            # Browser chrome
│   ├── design_canvas.jsx             # Side-by-side variation display
│   ├── animations.jsx                # Standalone animation engine
│   ├── narration_stage.jsx           # Voiceover-driven animation stage
│   ├── deck_index.html               # Multi-file slide aggregator
│   ├── deck_stage.js                 # Single-file slide web component
│   └── sfx/                          # 37 premade sound effects
├── scripts/
│   ├── render-video.js               # Record 25fps MP4
│   ├── convert-formats.sh            # Derive 60fps MP4 + GIF
│   ├── add-music.sh                  # Add BGM (6 mood options)
│   ├── narrate-pipeline.mjs          # TTS → voiceover + timeline
│   ├── mix-voiceover.sh              # Mix voiceover into video
│   ├── render-narration.sh           # Full narration render
│   ├── export_deck_pdf.mjs           # HTML slides → PDF
│   └── export_deck_pptx.mjs          # HTML slides → editable PPTX
└── references/
    ├── workflow.md                   # Question templates
    ├── content-guidelines.md         # Anti-slop details
    ├── react-setup.md                # React/Babel pinned versions
    ├── slide-decks.md                # Slide deck conventions
    ├── editable-pptx.md              # PPTX export constraints
    ├── animation-pitfalls.md         # 14 rules from real failures
    ├── animation-best-practices.md   # Narrative/motion grammar
    ├── voiceover-pipeline.md         # Narration-driven animation
    ├── tweaks-system.md              # Live-tuning control panel
    ├── design-context.md             # Fallback when no context
    ├── design-styles.md              # 20 design philosophies
    ├── scene-templates.md            # Templates by output type
    ├── verification.md               # Playwright verification
    ├── critique-guide.md             # 5-dimension scoring
    ├── video-export.md               # MP4/GIF export flow
    ├── sfx-library.md                # Sound effect catalog
    ├── audio-design-rules.md         # BGM+SFX mixing rules
    ├── apple-gallery-showcase.md     # 3D tilt + floating cards
    └── hero-animation-case-study.md  # Gallery ripple + multi-focus
```

---

## Merged Source Skills

This skill is a synthesis of two independently developed, battle-tested skills:

- **[Huashu Design](https://github.com/anthropics/skills/tree/main/huashu-design)** — Chinese-origin design skill specializing in HTML prototypes, asset protocols, the Design Direction Advisor, narrative-driven animation pipelines, and multi-format export (MP4, GIF, PDF, PPTX).
- **Design Taste** — Senior UI/UX engineering skill enforcing baseline-driven configuration, Tailwind/React architecture, Framer Motion choreography, the Bento 2.0 dashboard paradigm, and anti-slop design engineering rules.

All original rules from both skills are preserved. Overlaps have been unified into single authoritative sections. Contradictions have been resolved by environment-gating (standalone HTML vs. production Next.js).

---

## Contributing

This skill follows the [skill authoring best practices](https://docs.anthropic.com/en/docs/agents-and-tools/agent-skills) from Anthropic. The skill was built using the TDD-for-documentation methodology from the `writing-skills` skill — every constraint was validated by running pressure scenarios with sub-agents before inclusion.

To suggest improvements:
1. Identify a specific failure pattern (what the agent does wrong without the skill)
2. Propose the minimal constraint addition that fixes it
3. Verify the fix with a pressure scenario

---

## License

Apache License 2.0
```
