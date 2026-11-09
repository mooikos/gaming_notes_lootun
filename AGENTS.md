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
- **Strict Separation — Confirmed vs. Unconfirmed**:
  - Keep **user-confirmed decisions, builds, and in-game findings** in the main/active sections of each page.
  - Keep **anything not yet confirmed or input by the user** (future post-Phase-1 milestones, general game/community reference notes, tentative build ideas) in a clearly labeled **`Unconfirmed / Future Reference`** section so active focus (`Phase 1`) stays clean and unambiguous.
- **Deduplicate & Cluster Fragmented Findings Logically**:
  - Never repeat duplicate item/mechanic observations across multiple dungeons, and **do not list individual standard slot pieces** (`Helmet`, `Boots`, `Gloves`, etc.) once a standard equipment tier prefix is identified.
  - Record **global standard base tiers by their Tier/Type prefix only** across Monster Level Bands (`Lv. 1–14` `Basic`/`Leather`/`Copper`, `Lv. 15–49` `Cloth`/`Rough`/`Iron`, `Lv. 50–99` `Woven`/`Heavy`/`Lead`), noting only important weapon-category exceptions (e.g., `Hammers` skipping the `Iron` tier so `Iron Spear` is used).
  - Keep **Dungeon-Specific tables** strictly focused on boss/zone-exclusive (`Notable` & `Divine`) drops.
- **Current Active Focus (`Phase 1`)**:
  - Solo 1-character-at-a-time exploration runs (`Warrior` [Done] -> `Ranger` [Active] -> `Mage` -> `Paladin`) from `Lv. 1 -> 100` inside the **same shared save file**, using **Two-Handed (`2H`) weapons** to minimize item-slot complexity, upgrading basic gold structures only (no gear crafting), advancing dungeons immediately when unlocked, and logging item unlocks by **Monster Level Band & Dungeon**.
- When helping expand notes for **Lootun**, use iterative, focused questions to help organize:
  - **Active Phase 1 exploration logs & milestones** (`docs/milestones/`, `docs/classes/<class>/leveling-builds/`, `docs/items-crafting/by-level.md`).
  - **User-fed discoveries**, such as dungeon/boss/monster item drops, skill combinations, and progression walls.
- Cross-check game mechanics against authoritative sources when needed:
  - **In-Game Glossary**: Primary reference for monster/boss item drop locations, damage profiles, and exact skill/affix wording.
  - **[Lootun Steam Community Guides](https://steamcommunity.com/app/1960270/guides/)**, **[Lootun Steam Store](https://store.steampowered.com/app/1960270/Lootun/)**, and **[r/Lootun](https://www.reddit.com/r/Lootun/)**.

## Game Domain Reference
- **Base Classes & Level-100 Ascendancies** (+50 Ascendancy levels & passive trees):
  - **Warrior**: `Barbarian`, `Juggernaut`, `Warden`
  - **Ranger**: `Assassin`, `Marksman`, `Renegade`
  - **Mage**: `Archmage`, `Vizier`, `Battlemage`
  - **Paladin**: `Templar`, `Crusader`, `Inquisitor`
  - *Ascendancy Respec Mechanics*: Ascendancies can be **freely unlearned and swapped** anytime; each Ascendancy saves its earned Ascendancy Level (`1–50`) & XP independently when switching back later, and unequipped Ascendancy Relics are automatically locked so they cannot be scrapped.
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
- `docs/milestones/` — Phase-by-phase Solo Class Exploration plan (`Lv. 1 -> 100`) plus mid-term and long-term progression milestones
- `docs/general/` — Core game concepts, glossary terms, combat/defense layers, base buildings, and professions
- `docs/classes/` — Base class directories (`warrior/`, `ranger/`, `mage/`, `paladin/`), each containing:
  - `index.md` — Class overview (`parent: Classes & Ascendancies`, `has_children: true`)
  - `leveling-builds/` — Exploration & leveling builds (`Lv. 1 -> 100`, Two-Handed focus in Phase 1) evolving with Dungeon / Boss / Monster item unlocks (`parent: <Class>`, `grand_parent: Classes & Ascendancies`)
  - `endgame-builds/` — Unconfirmed / future `Lv. 100+` Ascendancy & raid builds (`parent: <Class>`, `grand_parent: Classes & Ascendancies`)
- `docs/items-crafting/` — Equipment notes and [Items by Dungeon / Boss / Monster](docs/items-crafting/by-level.md) (`by-level.md`), populated progressively as zones/bosses are encountered
- `docs/progression/` — Region missions, dungeons, boss target-farming, Agony/Endless notes, and raid strategies

## Formatting & Naming Conventions
- **File names & Permalinks**: Use `kebab-case` (e.g., `party-compositions.md`, `permalink: classes/party-compositions`). Avoid leading underscores (`_`) in content file names so Jekyll does not ignore them.
- **In-note identifiers**: Use `snake_case` or inline code formatting when referencing raw stat identifiers or specific affixes/enchants, and keep terminology consistent across pages.
- **Markdown quality**: Ensure proper heading hierarchy (`#` -> `##` -> `###`), valid list indentation, clean tables, and valid relative/permalink URLs.
