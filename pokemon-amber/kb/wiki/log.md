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


## 2026-05-18 — Reframed old Oak's obsession as bond research

- Updated `characters/professor-oak.md` so old Oak is not obsessionless after war/Champion life. His current obsession is the human-Pokemon bond: why connection enables both trainer and Pokemon to grow stronger, and how that strength can be deliberately cultivated without exploitation.
- This makes Oak's research his new form of greatness-seeking, not a retreat from it, and positions him as a banked-fire contrast to Alonso's open-flame adventuring ideal.

## 2026-05-18 — Promoted Drive Spectrum to central theme

- Added `themes/drive-spectrum.md` as a confirmed central theme/reference for the protagonist cast. It tracks what force organizes each character's life: obsession, ambition, duty, survival, attachment, avoidance, curiosity, service, or love.
- Updated `themes/core-story-elements.md` to point to Drive Spectrum and frame Amber, Alonso, Kyle, Mary, Erika, Oak, Sabrina, Fuji, Giovanni, Charcadet/Ceruledge, and Mewtwo through their distinct drives.
- Fixed stale Fighting Dojo wording in core themes: Kyle no longer simply loses/decline-inevitable; he can win back the Dojo's claim and still outgrow the inherited mission.

## 2026-05-18 — Route 1 ore points to Mewtwonite Y / female Mewtwo payoff

- Updated Ch. 20/21 plans so Team Rocket's camp/cave operation involves psychic-reactive Mew-adjacent ore in an unstable off-route cave; the cave is dungeon-adjacent, not a full Mystery Dungeon arc.
- Clarified that Rocket is harvesting/testing the ore for restraint/control/Pokeball telemetry/wild-Pokemon agitation, with Ursaring affected as a field test/captive asset.
- Updated the Mewtwo thread: the ore is the long physical setup for Mewtwonite Y, paying off in a future Unova / New Tork City / Pokemon Hills Genesect crisis where Amber helps the female-coded first Mewtwo access or stabilize Mega Mewtwo Y to defend against Genesect.
- Reaffirmed that the ore is not why Charcadet bonds with Amber; Charcadet chooses Amber because of observed protective action, trust, and promises kept.

## 2026-05-18 — Resolved Explorer vs Adventurer terminology

- Updated `lore/trainer-systems/adventurer-system.md`: adventurer is the canonical informal/cultural umbrella; explorer is only descriptive/synonymous or part of a named private group such as the Horizons Explorers.
- Rejected a separate formal Explorer profession/license/rank/permit/Pokemon Center category. The only formal baseline identity remains registered trainer.
- Marked `/new/explorers-and-adventurers.md` and `/new/open-questions-alonso-explorers.md` so rejected Explorer-profession brainstorming does not get re-imported as canon.

## 2026-05-18 — Canonized Mystery Dungeon-style world phenomenon for later arcs

- Added `lore/mystery-dungeons.md`: Mystery Dungeon-style unstable wilderness zones are canonical, but should be introduced later rather than as a full Ch. 20-21 system.
- Kept Route 1 as dungeon-adjacent only: strange enough to foreshadow the phenomenon, not enough to teach the full world mechanic.
- Integrated Mystery Dungeon work with the existing Pokemon Center quest board categories and Ranger/adventurer culture, while preserving the decision that there is no formal Explorer profession.
- Marked `/new/mystery-dungeons.md` as promoted-with-revisions so useful ideas can be mined without reimporting rejected Explorer formalization.

## 2026-05-18 — Set Alonso's personal origin through Don's stories

- Updated `characters/alonso-quijano.md`: Alonso's Greatest Adventurer dream comes from Don, a rough Paldean adventurer/storyteller his minor noble parents considered disreputable. Don's stories of giant beasts and impossible journeys may be exaggerated or partly false, but they infected Alonso with the belief that greatness can be chosen.
- Updated `lore/trainer-systems/adventurer-system.md` to anchor Alonso's Paldean adventurer myth in personal inspiration rather than formal Explorer/Guild status.
- Marked `/new/alonso-quijano-adventuring-knight.md` and `/new/open-questions-alonso-explorers.md` so the origin is treated as resolved brainstorming promoted into canon.

## 2026-05-18 — Clarified Don Q / Alonso inversion

- Revised Alonso's origin: the inspirational storyteller is **Don Q**, the actual liar/braggart/Quixote-like adventurer figure.
- Clarified the inversion: Don Q performs or exaggerates the myth, while Alonso Quijano becomes the real deal by living the ideal sincerely and competently.

## 2026-05-18 — Adjusted Ciro class background and Don Q truth level

- Updated `characters/ciro-salvatierra.md`: Ciro is no longer from minor nobility/old-name status. His money-as-freedom drive now comes from lower-status precarity, debt, patronage, and the belief that necessity lets other people own your choices.
- Clarified Don Q in Alonso's origin: Don Q should stay morally textured, but literarily he is an actual liar/heavy exaggerator. The point is that Alonso makes a false or unstable story real through sincere action.

## 2026-05-18 — Simplified Ciro into dirt-poor scrounger background

- Updated `characters/ciro-salvatierra.md`: Ciro grew up dirt poor and scrounged for scraps. Preferred version is dysfunctional-family poverty, with adults wasting scarce money on frivolous things and leaving the household in debt; orphan-adjacent remains possible but secondary.
- Updated `themes/drive-spectrum.md` so Ciro's money-as-freedom drive comes from material scarcity, hunger, debt, and lack of safety rather than noble/status pressure.
## 2026-05-20 — Removed obsolete Charcadet ore handoff

- Removed the pre-4Ever beat where Charcadet hands Amber the Mew-adjacent ore. That idea belonged to the older pre-Alonso Charcadet premise.
- Preserved the Viridian cave ore as a Rocket/Mewtwo/Mewtwonite Y seed, but left the custody chain open.
- Reaffirmed that Charcadet bonds with Amber through observed protective choices and promise-keeping, not ore custody.
## 2026-05-20 — Alonso adventurer-vs-knight framing

- Clarified Alonso as a minor noble whose parents want him to become a proper knight.
- Reframed Alonso as rejecting the knight role-label in favor of becoming the Greatest Adventurer, while ironically embodying knightly virtues through action.
- Reduced "knight personality" language: Alonso should not perform archaic/knightly diction; his ideals show through plainspoken courage and worthiness-over-possession conduct.
## 2026-05-20 — Don Q locked as bookstore storyteller

- Locked Don Quixote / Don Q as a shabby Paldean bookstore owner, not a real adventurer or secret mentor.
- Don Q is well-read and tells beautiful lies stitched from travelogues, expedition journals, adventure romances, knight stories, and dubious maps.
- Alonso's dream to become the Greatest Adventurer comes from hearing those false stories and deciding to make them real through action.
- This preserves the anti-legacy structure: Alonso inherits no destiny from Don Q; he transforms a false story into lived conduct.

## 2026-05-20 — Captured Kanto duo structure, Kitakami split, and late-saga bridge direction

- Updated `arcs/arc1-kanto-year1.md` and `arcs/saga-overview.md` so early Kanto's durable travel engine is Amber + Kyle as a duo, with rotating local third forces instead of a fixed large party; guest characters should usually stay single-function and selective rather than spawning full cast ecosystems.
- Clarified the Kanto vision: Amber tries to run a normal badge journey, but gets pulled sideways by promises, quests, Gym politics, Rocket pressure, local Pokemon suffering, environmental hazards, and other weird incidents because of her choices and conduct, not because she is a chosen one.
- Updated `arcs/saga-overview.md` with the current preferred post-Hoenn planning skeleton: Kitakami I -> Sinnoh -> Paldea -> Kalos -> Kitakami II -> brief real-world displacement / Alola-Ultra Space bridge -> later escalation/endgame. Paldea-before-Kitakami-II and Kalos-before-Kitakami-II are planning-direction preferences, not hard scene locks.
- Updated `arcs/arc-kitakami.md` to distinguish Kitakami I from Kitakami II: Kitakami I remains the discovery / seal-reinforcement / Gardevoir-stays arc; Kitakami II is Amber's first deliberate legendary-class raid with a small 4-6 person trusted team, likely including Alonso.
- Kept the seal history conservative: Mew making the original sacrifice is locked; Cresselia as later maintenance / dream-suppression support and Darkrai subconsciously warding people away are open options, not canon lock.
- Updated `lore/mystery-dungeons.md`, `characters/alonso-quijano.md`, and `lore/trainer-systems/adventurer-system.md` so Mystery Dungeon-scale phenomena are primarily Alonso's genre/lane, while Amber intersects with them when they become obligations or promises. Route 1 remains dungeon-adjacent only.
- Updated `plot-threads/rainbow-rocket-endgame.md` so late-saga power is framed as Mega-era strategic force: strong trainers, legendary-class combatants, and Mega-capable elites become political actors, and Rainbow Rocket should read as the first global war of the Mega era.
- Added `plot-threads/dimensional-displacement-bridge.md` for the post-Kitakami II fallout direction: brief displacement into the actual mundane real world, hollow/painful Pokemon-media beat, minimal bureaucracy subplot, and Aether/Lusamine extraction into the Alola / Ultra Space bridge.
- Updated `wiki/index.md` to catalog the new dimensional bridge page.
