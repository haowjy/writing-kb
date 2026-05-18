# Wiki Operations Log

Append-only chronological record of ingests, queries worth saving, and
lint passes. Latest entries at the bottom.

Format: `[YYYY-MM-DD] [op] description`

Operations:
- `init` --- one-time setup
- `ingest` --- new source integrated into wiki
- `lint` --- health-check pass
- `query-saved` --- query result filed as a wiki page
- `migrate` --- bulk move from legacy structure

---

[2026-05-09] [init] Wiki initialized. Layout per `AGENTS.md`. Empty until
content migration from `wiki/` and `future/` (main repo) lands.

[2026-05-09] [migrate] Phase A complete. 80 files bulk-copied from wiki/ and
future/ to kb/wiki/. Includes: 9 characters, 8 places, 3 organizations, 16
lore subfolder files (crime, government, history, mechanics, tech,
trainer-systems split files), timeline, arc 1 outline + 4 events, team
file, kyle-kong, 5 future arcs, 5 future plot threads (mewtwo-thread
underscore dropped). Originals still present in main repo until Phase F
cleanup. Cross-refs not yet rewritten --- Phase G handles that.

[2026-05-09] [migrate] Phase B complete. Lore cluster splits done.
- aura: split into aura-system.md (concept) and aura-mechanics.md (deep dive)
- economy: renamed to economics/index.md (kept pokeball-pricing alongside)
- trainer-systems: 3 new pages from old big file --- cultural-history,
  licensing, career-paths. Old big trainer-systems.md content distributed.
- world-mechanics: split into 4 pages --- pokemon-sustenance (new),
  pokemon-fainting (existing stub expanded), pokeball-technology (new),
  power-scaling (new). Aura section was redundant with aura-mechanics
  (discarded). _plot-secrets.md is just a redirect index --- skip.

[2026-05-09] [migrate] Phase C partial. Worldbuilding decomposition started.
- Currency contradiction filed at contradictions/currency-notation.md
  (resolution: ₽ canon, ¥ legacy --- being dropped via migration)
- Stubs: sabrina.md, 8 gym stubs (pewter, cerulean, vermillion, fuchsia,
  lavender-ghost, viridian-forest-bug, east-coast-water, route-11-ground)
- Substantive new pages: viridian-gym (with TR HQ overlay),
  saffron-fighting-dojo, saffron-psychic-gym, world-opening-timeline,
  plot-threads/saffron-gym-rivalry.
Still pending in Phase C: clan-system page, 4 substantial clan pages,
clans/index.md, team-rocket.md updates (Madame Boss canon), character
page updates for Amber/Kyle economic positioning, Giovanni page (deferred
until other Giovanni-relevant files processed).

[2026-05-09] [migrate] Phase E bulk done. tone.md (from TONE.md),
themes/core-story-elements.md (from future/core/themes.md), and 4
workspace docs (current-direction, open-questions, archive, meta-notes)
all copied to their new locations.

[2026-05-09] [migrate] Phase C complete. Clan + Giovanni cluster done.
- Clan core: lore/clan-system.md (Johto vs Kanto framework, drafting status)
- Clans index: organizations/clans/index.md (14 clans cataloged + lightweight
  Kanto family mentions)
- Substantive clan pages: clans/silvertail.md (Madame Boss / TR origin canon),
  clans/viridian-house.md (Giovanni parentage / dual inheritance canon)
- Team-rocket update: appended Clan & Family Origins section linking to
  silvertail, viridian-house, and explaining the dual inheritance + org split
- Giovanni character page created: characters/giovanni.md (consolidates from
  gym-system-detailed.md, clan-system Viridian House entry, and references
  the existing plot-thread files)
- Character economic position updates: amber-mc.md gets walking-by-choice
  Oak-supported framing; kyle-kong.md gets family-money + Fighting Dojo
  desperation framing
- All currency notation in updates uses ₽ (per the contradiction resolution)

[2026-05-09] [migrate] Stubs copied (decision #10). 6 stub files migrated as
TODO markers to their new kb destinations:
- events/{kyle-meeting,pewter-gym-brock,route1-solo}.md
- arcs/{arc2-hoenn,arc3-beyond,arc-pikachu-handoff}.md
The future/plot/saffron-gym-rivalry stub is superseded by the substantive
plot-threads/saffron-gym-rivalry.md and not migrated separately.

[2026-05-09] [status] Migration content phases (A, B, C, D-stubs, E) complete.
116 markdown files in kb/. Remaining work:
- Phase D continued: content checks on plot-threads/* and arcs/* (some
  cross-cutting content may need redistribution to entity pages, e.g.
  giovanni-fuji-jail content into the new giovanni.md page)
- Phase F: delete wiki/ and future/ from main repo (destructive --- needs
  user OK)
- Phase G: cross-reference rewriting (wiki/ and future/ relative paths
  inside migrated files need normalization to kb [[wiki-link]] style)
- Phase H: populate wiki/index.md catalog
- Phase I: creative-writing-skills package update (separate repo)

[2026-05-09] [migrate] Phase G complete. 2 broken internal refs fixed in
trainer-systems/gym-system.md and trainer-systems/conference-system.md ---
both were "Primary design reference" citation links pointing to
future/worldbuilding/ source files. Converted to plain-text source notes
("content incorporated into this page") so they won't break when Phase F
removes future/ from the main repo. All other "wiki/" grep matches in kb/
are external bulbapedia URLs --- no action needed.

[2026-05-09] [migrate] Phase H complete. wiki/index.md populated with
one-line summaries for all 93 wiki pages, grouped by type: 13 characters,
19 places, 6 organizations, 7 events, 9 arcs, 6 plot-threads, 28 lore
pages across 7 subfolders, 1 theme page, 1 timeline, 1 contradiction.
Also flagged cinnabar-gym.md / cinnabar-island.md as partial duplicates
pending consolidation.

[2026-05-09] [status] Migration complete except Phase F (deletion of wiki/
and future/ from main repo --- awaiting user OK) and Phase I (separate
repo). Phase D re-evaluation: giovanni-fuji-jail.md is scene planning
content, appropriately separate from the giovanni.md entity page which
already cross-refs it. No redistribution needed.

[2026-05-09] [migrate] Phase F complete. Deleted wiki/ (43 files) and
future/ (29 files) from main repo via git rm --- 81 files total staged for
removal. All content was previously migrated to .meridian/kb/. Migration
fully complete (Phases A–H done). Remaining: Phase I (creative-writing-skills
package update, separate repo).

[2026-05-17] [ingest] Canon/planning decisions ingested from top-level conversation (c10).
- New page: characters/alonso-quijano.md — Alonso Quijano character (Paldean adventuring knight, early mentor, endgame ally)
- New page: lore/trainer-systems/adventurer-system.md — Adventurer System (informal cultural identity, Kanto vs Paldea myths, interregional travel context)
- New page: plot-threads/rainbow-rocket-endgame.md — Rainbow Rocket endgame direction (Giovanni conquest vs Amber, obsession variants culmination)
- Updated: characters/amber-mc-team.md — Charcadet entry now includes Alonso origin context
- Updated: themes/core-story-elements.md — added Section 6 (Obsession, Drive, and Ambition)
- Updated: arcs/saga-overview.md — refined ages, Amber as historical outlier, Rainbow Rocket endgame paragraph, cross-refs
- Updated: wiki/index.md — added Alonso, adventurer-system, rainbow-rocket-endgame entries

## 2026-05-17 — Replaced old Charcadet origin with Alonso direction

- Updated Arc 1, saga overview, and Mewtwo thread to use the Alonso-origin direction: Alonso brings Charcadet to Kanto; Amber is why Charcadet stays.
- Current version centers the Route 1 camp/cave mini-arc, Team Rocket, Teddiursa/Ursaring, and the Mew-adjacent ore thread.
## 2026-05-17 — Softened Alonso obsession framing

- Revised Alonso/Rainbow Rocket/theme wording to avoid treating Alonso as simply "healthy" or "clean" obsession.
- Alonso now represents ambition as a chosen ideal: sincere, disciplined, brave, quest-seeking, and generous before ambition curdles into possession or conquest.
## 2026-05-17 — Lightened Alonso ambition language

- Reduced overcorrected risk/flaw wording around Alonso's obsession.
- Alonso remains non-moralized, but the emphasis is now on generative ambition rather than recklessness or danger-romanticizing.
## 2026-05-17 — Synced Route 1 Ch. 20/21 replacement into KB

- Updated `arcs/arc1-kanto-year1.md` and `arcs/saga-overview.md` to split the old Day 2 cave sequence into Ch. 20 Team Rocket camp / Alonso introduction and Ch. 21 guarded cave / Ursaring rampage / rescue.
- Updated `plot-threads/mewtwo-thread.md` so the Mew-adjacent ore is a long payoff thread from the Viridian cave incident, not a bonding device or old Charcadet guardian premise.
- Updated `characters/alonso-quijano.md`, `characters/amber-mc-team.md`, and `plot-threads/rainbow-rocket-endgame.md` to remove stale dead-master loyalty framing and reflect Alonso/Charcadet/Teddiursa decisions.
- Added `plot-threads/charcadet-to-ceruledge-throughline.md` and `plot-threads/ursaring-rescue-thread.md`.
- Current Ch. 20/21 facts: Amber promises to help Teddiursa save mother Ursaring; Teddy recognizes Team Rocket; Alonso saves Amber after she protects Teddy; Charcadet notices but does not join; Rocket removes mother Ursaring after an almost-reunion; Teddy + Charcadet + Ditto escape to fetch rescue; Amber's promise remains unfulfilled.
## 2026-05-18 — Cleaned Alonso/Kyle/Sabrina drive language

- Cleaned Alonso framing: he should not speak in archaic knight diction; his adventuring ideal shows through plainspoken conviction and action. Core instinct: someone has to.
- Revised Sabrina from potential companion/ambitious rival into Kyle's monstrous natural-talent boss: raw psychic power without drive, emotionally distant from psychic overload.
- Revised Saffron rivalry: Kyle eventually defeats Sabrina at the critical public moment, preserving/restoring the Fighting Dojo's claim, then realizes the inherited mission is too small and leaves toward adventuring.
- Updated Kyle, Sabrina, Saffron rivalry, Arc 1, Saffron gym place pages, core themes, and index summaries.
## 2026-05-18 — Added Alonso's Paldean crew

- Added `characters/beatriz-romero.md`: quiet Paldean crew naturalist whose dream is to discover and catalog every Pokemon.
- Added `characters/ciro-salvatierra.md`: semi-shady Paldean crew hustler whose dream is to get rich enough to choose his own life, with a code against abandoning the vulnerable.
- Revised Alonso to age 17 and clarified his goal as becoming the Greatest Adventurer; knighthood remains values/action, not archaic speech.
- Updated Adventurer System, Arc 1, and Ch. 20/21 plans so Alonso is separated from his crew near Route 1 and Charcadet/Ditto/Teddiursa can find the crew for the cave rescue.
## 2026-05-18 — Renamed Alonso crew companions to ABC trio

- Renamed `characters/ines-romero.md` → `characters/beatriz-romero.md`. Beatriz remains the quiet Paldean crew naturalist whose dream is to discover and catalog every Pokemon.
- Renamed `characters/mateo-salvatierra.md` → `characters/ciro-salvatierra.md`. Ciro remains the semi-shady money-minded crew hustler with a code.
- Updated Alonso, Adventurer System, Arc 1, Ch. 21, index, and cross-links to use Alonso / Beatriz / Ciro.

