# kb/AGENTS.md

The author's knowledge base for the fanfiction Pokemon: Ambertwo. It holds what
the story is and what the author has chosen it will be, with the reasons. It is
an author wiki, not a reader wiki: spoilers, character intent and unrevealed
canon belong here.

The manuscript lives in the story repository (`story/chN/`). Chapter prose is
the authority on what has happened; this KB serves it and never outranks it.

## What a page may say

Two things reach the KB: what the written chapters establish, and what the
author chose. An idea he floated ("maybe X?"), a question he asked, or a list
of options he gave without picking stays out, in the work directory or the
conversation, until he chooses. A choice he made with a hedge is written "for
now" or "trying".

Every creative choice is the author's to change. Write it as the story's
current direction, with its reason, not as a ruling. When the author asks for
something a page says against, follow the author and update the page; the page
was never a reason to refuse him. A rule whose reason nobody can state gets
deleted.

Keep a rejected idea only with the fact that ruled it out ("Arceus bringing
them would make Amber chosen by a god, and she isn't a chosen protagonist").
Without the reason it reads as a ban nobody can re-examine. No decision IDs, no
lists of rejected options, no `decisions/` pages: a choice lives on its topic
page.

Pages state current truth and never narrate their own history: no changelogs,
"previously", "was changed to" or dated update notes. Delete what a revision or
a new choice made wrong. Git history is the archive.

## Layout

- `wiki/reference/`: who, where, and how the world works. May hold spoilers and
  settled unrevealed facts; never alternatives presented as equal possibilities.
- `wiki/planning/`: unwritten story the author has chosen: `saga-overview.md`
  (the structural map), `saga-threads/`, numbered `arcs/`, `themes/`,
  `rosters/`, `team-arcs/`. The nested `AGENTS.md` files in `saga-threads/`
  and `arcs/` say what belongs there.
- `wiki/continuity/`: what has happened and when: timeline, established
  events, contradictions between chapters. No future planning; chapter
  summaries stay in the story repository.
- `wiki/vocab.md`: canonical story terms.
- `wiki/index.md` and each folder's `index.md` (`overview.md` in numbered arc
  folders): navigation.
- `styles/`: voice and scene guidance for writer agents; start at
  `styles/index.md`.
- `issues/`: writing problems that span chapters.

## Page conventions

- One subject per page, named for its subject.
- Cite the manuscript as `[chN]` or `[chN §X]` for any claim grounded in prose.
- Mark each page or section's status: `canon` (shown in the chapters; cite
  them) or `drafting` (the author chose it; not yet on the page). Unwritten
  material on a reference page is marked as not yet on the page, so a
  reader-facing export could filter it.
- Link related pages with relative Markdown links. One page owns each fact;
  others link to it.

## Operations

**Ingest** a new or revised chapter: read it, update the reference and
continuity pages it changes, delete what it contradicts, and touch planning
only where the chapter changes future direction. Update `wiki/index.md` when a
page is added or moved.

**Capture** an author decision: find the topic page, write the choice and its
reason, and delete what it replaces. Change a claim only on evidence from the
manuscript or the author's own words.

**Query**: start at `wiki/index.md` and follow links before re-reading
chapters.

**Lint**: look for claims a chapter contradicts, unmarked unwritten material on
reference pages, planning with no author choice behind it, orphan pages and
broken links. Flag what the evidence can't settle inline:

```markdown
> [!FLAG] **Needs human review**: this page says X; chapter N shows Y.
> Flagged YYYY-MM-DD.
```

## Not here

- Chapter prose, summaries, chapter notes and plans: the story repository.
- Generic writing craft: the creative-writing-skills package.

This KB syncs to its own repository through Meridian autosync. Pages cite
chapters as `[chN]`, never by filesystem path.
