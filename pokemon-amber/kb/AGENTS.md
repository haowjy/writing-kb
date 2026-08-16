# kb/AGENTS.md

The kb is an LLM-maintained author wiki: a persistent, compounding artifact
of everything known about Pokemon: Ambertwo, with the LLM doing the
cross-referencing and bookkeeping. Inspired by the Karpathy LLM-wiki
pattern, adapted for an author's working knowledge --- includes spoilers,
intent, and unrevealed canon.

## Layout

- wiki/reference/ --- established entity and world reference
- wiki/planning/ --- unwritten story architecture, arcs, saga threads, themes, and decisions
- wiki/continuity/ --- timeline, established events, and contradictions
- wiki/index.md --- curated navigation
- Each major branch and reusable collection has a local `index.md`; numbered
  arc folders use `overview.md` instead
- wiki/vocab.md --- stable project vocabulary
- wiki/log.md --- append-only maintenance history
- research/ --- raw external sources cited by wiki pages
- styles/ --- voice and tone references
- issues/ --- craft backlog

## Knowledge Boundaries

### Reference

Reference pages answer **who, where, and how the world works**. They may contain
spoilers and unrevealed settled facts, but speculative alternatives belong in
planning rather than being mixed into reference prose as equal possibilities.

### Planning

- planning/saga-overview.md owns the full structural map.
- planning/saga-threads/ contains only story-level throughlines whose removal
  would restructure several major arcs.
- planning/arcs/<number-name>/overview.md owns one arc or adjacent arc range.
  Smaller plot threads and scene plans live beside that overview.
- planning/themes/ holds thematic architecture.
- planning/decisions/ records settled choices when the reasoning remains
  useful; rejected plans should not remain on live entity pages.
- planning/rosters/ holds future team construction.
- planning/team-arcs/ holds Pokemon character and relationship progression by
  trainer; stable identity belongs in reference and membership logistics stay
  in rosters.

### Continuity

Continuity pages answer **what has happened and when**. They do not hold future
brainstorming. Chapter summaries remain in the story repository.

## Page conventions

Every wiki page should:

- Have a clear subject (the page name = the subject)
- Cite chapters by `[chN]` or `[chN §X]` for any claim grounded in
  published prose
- Cite `research/<file>` for any claim grounded in external research
- Cross-link other wiki pages with `[[page-name]]` style references
- Include status as a property: `canon` | `drafting` | `speculation`
  - `canon` --- locked in by published chapters, cite which
  - `drafting` --- author has decided, not yet shown in prose
  - `speculation` --- under consideration, not committed

Author notes / spoilers / intent are welcome on any page --- this is an
author wiki, not a reader wiki. Mark unrevealed material clearly so a
reader-mode export could filter it later if ever needed.

## Operations

The three things agents do with the kb. Each operation has an entry-point
agent in the creative-writing-skills package.

### Ingest

When a new chapter publishes or a research source is added, integrate it:

1. Read the source
2. Read the chapter's `story/chX/summary.md` when applicable
3. Update the relevant reference and continuity pages
4. Update planning only when the new material changes future direction
5. Update `wiki/index.md` for new navigation entry points
6. Append a line to `wiki/log.md`

Entry point: `chronicler` agent. For chapter ingest, pass the chapter
file. For research ingest, pass the research file.

### Query

When asked something about the project, prefer the wiki over re-reading
chapters:

1. Read `wiki/index.md` to locate relevant pages
2. Read those pages, follow cross-references
3. If the answer is worth keeping, file it as a new concept page or
   update an existing one

Entry point: `explorer` agent for fast lookup.

### Lint

Periodic health check:

- Orphan pages (no incoming links from index or other pages)
- Stale claims (entity page contradicts latest chapter summary)
- Missing cross-references (entity mentioned in summary but no page exists)
- Broken `[[wiki-link]]` references
- Canon contradictions --- file to `wiki/continuity/contradictions/`
- Craft issues --- file to `kb/issues/`

Entry point: `chronicler` or `continuity-checker`.

## What does NOT belong in the wiki

- Raw chapter prose --- stays in `story/` (main repo)
- Author voice rules --- `kb/styles/`
- Recurring prose problems --- `kb/issues/`
- Generic writing craft --- `.agents/skills/` (creative-writing-skills package)

## Sync

This kb is synced to a separate repo via meridian's autosync feature. Tool
state (sessions, work-items, locks) stays in the main repo's `.meridian/`
and is NOT part of the kb sync.

Chapters live in the main repo at `story/chX/`. Wiki pages reference
them by canonical `[chN]` notation without filesystem paths.
