---
name: design-harness
description: "Set up and run a complete design workflow for non-designers using AI agents. Three layers: design skills (borrowed expertise), agent canvases (design surfaces), and inspiration tools (training taste). Trigger when: setting up a design workflow, choosing design tools for agents, wanting to 'design without being a designer', asking 'how should I approach design with AI', improving design taste, or evaluating design skills/plugins for Claude Code, Cursor, or Codex. Based on Neethan Wu's 'Design Without Designing' harness. For specific CSS/Tailwind design techniques, see web-design-system skill."
---

# Design Harness

Three-layer system for shipping design without being a designer. Each layer solves a different problem.

## Layer 1: Skills (Borrowed Expertise)

Design skills are instruction files installed into your AI agent. They transfer someone else's design expertise into your workflow.

### Recommended Skills (ranked by daily usefulness)

**Impeccable** — impeccable.style (by @pbakaus, creator of jQuery UI)
- 20+ commands: `/audit`, `/polish`, `/animate`, `/typeset`, `/arrange`, `/delight`
- Catches the anti-patterns that make AI-generated UI obvious: overused fonts, gray-on-color text, pure blacks, nested cards
- `/delight` is the standout command. Use it frequently, it introduces visual upgrades that change how output looks overnight.
- Most-used skill in this harness.

**Emil Kowalski's Design Engineer Skill** — emilkowal.ski/skill (by @emilkowalski, Linear/Vercel)
- Created by the maker of Sonner and Vaul (15M+ weekly npm downloads)
- Encodes how he thinks about animations, UI polish, and small details most people skip
- Free version borrows his mindset. Full version comes with animations.dev course.

**Interface Design** — interface-design.dev (by @Dammyjay93)
- Solves the biggest problem: agent forgets design decisions between sessions
- Stores specs (spacing grids, color palettes, depth strategies, component patterns) in a persistent system.md that loads automatically
- Critical for multi-session consistency.

**UI Skills** — ui-skills.com (by @ibelick, creator of motion-primitives)
- 15 open-source skills: baseline UI, accessibility, motion, performance, metadata
- Solid foundation for broad coverage, use as a baseline layer.

### Gotchas
- Install Impeccable first, it has the highest immediate impact
- Interface Design's persistent system.md is essential for multi-session projects
- Skills stack, using all four together gives broader coverage than any one alone
- Run `/audit` before shipping anything. It catches embarrassing mistakes.

## Layer 2: Agent Canvases (Design Surfaces)

Canvases are design tools that use YOUR agents as the kernel. The canvas is the shell, your agent (Claude Code, Codex, etc.) is the brain.

**Paper** — paper.design (by @paper)
- Canvas built on real HTML and CSS, not proprietary format. What you design IS code.
- Exposes MCP tools with full read/write access. Works with local agents out of the box.
- Best for: design systems, design tokens, page design iterations
- Use as source of truth and design reference alongside building the product.
- Free tier with limited MCP call quotas.

**Pencil** — pencil.dev (by @tomkrcha)
- JSON-based `.pen` format. Git-diffable and agent-manipulable via MCP.
- Design files sit in your repo, versioned like code.
- **Swarm mode**: Spin up multiple agents (up to six) on your canvas simultaneously. One handles typography, another does layout, a third propagates the design system.
- Currently free. Use alongside Paper.

### When to use which
- Paper: when you want design-as-code (HTML/CSS output). Good for design systems.
- Pencil: when you want versioned design files in your repo. Good for collaborative agent work.

## Layer 3: Inspiration (Training the Eye)

Skills give expertise. Canvases give a surface. But you still need to know what good looks like.

**Variant** — variant.ai (by @variantui)
- Type an idea, scroll through endless non-repeating design interpretations
- **Style Dropper**: Point at any design, it absorbs the visual DNA (color palette, typographic rhythm, spatial density) and transfers it onto another design
- Export as React, copy prompts with HTML references for coding agents
- Use for 20 min/day to warm up before design work. Becomes part of the daily routine.

**Mobbin** — mobbin.com (by @mobbin)
- Curated real app UI patterns (mobile + web)
- Use when you need to see how top apps handle specific flows: onboarding, settings, checkout, etc.
- Has a Figma plugin for pulling references directly.

**Awwwards** — awwwards.com (by @awwwards)
- Jury-scored cutting-edge web design. The highest bar for web craft.

**Cosmos** — cosmos.so (by @thecosmos)
- Collect inspiration and explore others' collections. Web design, typography, interiors, photography.
- Hex color search and vague description search find surprisingly relevant results.
- Use to build clusters of visual references that shape how you think about design.

## The Workflow

1. **Warm up** (10-20 min): Browse Variant, Mobbin, or Cosmos. Save anything that catches your eye.
2. **Set the foundation**: Run Interface Design to load/create your persistent design specs.
3. **Design in canvas**: Open Paper or Pencil. Point your agent at it via MCP. Describe what you want.
4. **Polish with skills**: Run Impeccable `/audit` then `/delight`. Apply Emil's polish pass.
5. **Extract and build**: Take tokens/components from canvas into your codebase. Use web-design-system skill (if installed) for Tailwind implementation patterns.
6. **Ship and iterate**: Run `/audit` one final time before shipping.

## Related Skills
- **web-design-system**: Specific CSS/Tailwind techniques (ring technique, typography, layout patterns). Complements this skill, this is the "what tools", that is the "what techniques".
