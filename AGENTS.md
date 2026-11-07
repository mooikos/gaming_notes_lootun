# AGENTS.md — Lootun Gaming Notes

## Project Overview
We organize, maintain, and expand structured Markdown (`.md`) gaming notes and progression milestones for **Lootun** (Steam AppID `1960270`, by *ArrowSoftGames*) in this repository (`gaming_notes_lootun`).
The site is built with Jekyll using the [Just the Docs](https://just-the-docs.com) theme from the `docs/` directory and prepared for GitHub Pages (`https://mooikos.github.io/gaming_notes_lootun`).

## Core Principle: Always Keep Everything Up-to-Date
- **Always keep all files and references up-to-date.** Whenever you create, edit, rename, or remove a `.md` file:
  1. Update `docs/index.md` and the relevant section `index.md` (`docs/milestones/index.md`, `docs/general/index.md`, `docs/classes/index.md`, `docs/items-crafting/index.md`, `docs/progression/index.md`, and any nested subfolder `index.md`).
  2. Verify Jekyll frontmatter (`permalink`, `parent`, `grand_parent`, `nav_order`, `has_children`) matches the folder hierarchy and link targets.
  3. Check and update cross-links across all `.md` files and `README.md` so no broken links or stale references exist.
  4. Keep this `AGENTS.md` file (and the workspace-root `../AGENTS.md` if project-level metadata changes) up-to-date whenever project structure, conventions, or workflows evolve.
  5. Keep commits scoped cleanly to this Git repository (`gaming_notes_lootun`).

## Interactive Documentation Workflow
- When helping expand notes for **Lootun**, use iterative, focused questions to help organize:
  - **Short-term, mid-term, and long-term milestones** (`docs/milestones/`), moving completed goals into a completed log as progress is made.
  - **In-game discoveries & personal notes**, such as party rosters, favorite skill masteries, crafting priorities, target-farming drops, and boss/raid counters.
- Cross-check game mechanics against authoritative sources:
  - **In-Game Glossary**: Primary reference for item drop locations, monster damage profiles, and exact skill/affix wording.
  - **[Lootun Steam Community Guides](https://steamcommunity.com/app/1960270/guides/)**: Developer *Deep Dive* posts, *Choosing gear for your team*, tank/DPS breakdowns, and 6-man raid build guides.
  - **[Lootun Steam Store & Patch Notes](https://store.steampowered.com/app/1960270/Lootun/)** and **[r/Lootun](https://www.reddit.com/r/Lootun/)**.

## Game Domain Reference
- **Base Classes & Level-100 Ascendancies** (+50 Ascendancy levels & passive trees):
  - **Warrior**: `Barbarian`, `Juggernaut`, `Warden`
  - **Ranger**: `Assassin`, `Marksman`, `Renegade`
  - **Mage**: `Archmage`, `Vizier`, `Battlemage`
  - **Paladin**: `Templar`, `Crusader`, `Inquisitor`
- **Skills & Masteries**:
  - **Default Attacks**: Require a matching weapon archetype; scale with Weapon Damage % and Attack Time.
  - **Cooldown Skills**: Offensive, defensive, and utility abilities automated via the **Barracks**; each skill supports up to **20 Mastery Levels** that modify skill behavior, target caps, or damage conversions.
- **Base Buildings & Professions**:
  - **Core Facilities**: `Scrapper` (automated salvaging), `Blacksmith` (crafting & upgrading), `Barracks` (skill auto-cast & target priority), `Artisan` (attribute transmutation & endgame crafting).
  - **Profession Hall**: Unlocks passive gathering nodes (`Mine`, `Forest`, `Farm`) enhanced by worker slots and monster-dropped **Profession Tools**.
- **Endgame Systems**: Missions & Map Expertise, Dungeons, Heroic / Agony scaling, Endless waves, Mythic/Fated itemization, Enchants, Gems, Flasks, Relics, and 6-player Raids.

## Repository Structure (`saves/` & `docs/`)
- `saves/` — Tracked plain-text copy-paste **Lootun** save exports (`saves/README.md` + raw save snapshots, kept outside `docs/` so Jekyll ignores them; informal filenames are welcome during active play)
- `docs/index.md` — Home page (`nav_exclude: true`)
- `docs/milestones/` — Phase-by-phase exploration plan plus short-term, mid-term, and long-term progression milestones
- `docs/general/` — Core game concepts, glossary terms, combat/defense layers, base buildings, and professions
- `docs/classes/` — Base class guides (`warrior/`, `ranger/`, `mage/`, `paladin/`), Ascendancy builds, and 3-man / 6-man party compositions
- `docs/items-crafting/` — Equipment tiers, affixes, Blacksmith/Artisan workflows, enchants, gems, flasks, and relics
- `docs/progression/` — Region missions, dungeons, boss target-farming, Agony/Endless notes, and raid strategies

## Formatting & Naming Conventions
- **File names & Permalinks**: Use `kebab-case` (e.g., `party-compositions.md`, `permalink: classes/party-compositions`). Avoid leading underscores (`_`) in content file names so Jekyll does not ignore them.
- **In-note identifiers**: Use `snake_case` or inline code formatting when referencing raw stat identifiers or specific affixes/enchants, and keep terminology consistent across pages.
- **Markdown quality**: Ensure proper heading hierarchy (`#` -> `##` -> `###`), valid list indentation, clean tables, and valid relative/permalink URLs.
