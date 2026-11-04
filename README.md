# Once Human — Fusion Pod Planner

A single-page tool for planning Deviation fusions in Once Human's Fusion Pod. Pick a Deviation, variant and traits, and it lays out each fusion step (collect traits on a carrier → combine → clone → move into the target → raise to x/5 → 5/5) with the odds for each step.

หน้าเว็บช่วยวางแผนการผสม Deviation ใน Fusion Pod ของเกม Once Human · 七日世界 Fusion Pod 融合规划工具

## Use

Open `index.html` in a browser. Nothing to install. Languages: English (default), ไทย, 中文.

Tabs:

- **Fusion plan** — choose a target and get step-by-step pod layouts with odds.
- **Fusion Pod simulator** — place your own parents and up to 3 materials and see species, trait and Skill/Activity odds.
- **Trait list** — search and filter every known trait.
- **Settings & rules** — adjust the numbers used, see the rules and sources.

### Save and share a plan

- **Save plan to file** downloads a `.json` file with the target, settings and simulator layout, plus the steps in readable form.
- **Open plan file** loads that file back. Send the file to a friend and they can open it the same way.
- If a viewer blocks downloads, the page shows the plan code instead; copy it, and open it later with **Paste plan code**.

## Rules used

1. Offspring species can only be a parent's species. Odds = Deviations of that species (parents + materials) ÷ all Deviations of the parents' species.
2. Four trait slots: General, Type (Combat/Territory/Crafting), Deviated, Stat (SCP). At most one trait per slot.
3. Unique variants use the Type slot by default (a real Deviation carries a variant, Power Rewind 2, Moonlight Assault and Crit DMG 3 together). This can be switched to the General slot in Settings.
4. Type traits never cross types.
5. Competing traits: odds = sources of that trait ÷ all sources in the slot.
6. One trait in a slot: 2+ sources = 100%; one source = 50% + 10% per Deviation without a trait in that slot, up to 80%.
7. Skill/Activity come from either parent, with a small chance of +1 (~9.8%) or −1 (~2%).

These numbers are community estimates, not confirmed by the developer. Check the in-game preview before fusing. Sources are listed in the Settings tab.

Fan-made project, not affiliated with Starry Studio.
