# Prompt Review: character circumstances with style

**Verdict: request changes**

The pairing is right, the loading split is right, and voice-only surfaces were left alone. The author-facing half of write-and-flag is not. `agents/muse.md` uses "the page" for prose and then for the wiki in the same body, which can reverse the mismatch default.

## Findings

### 1. High — "the page" means prose, then wiki, in one muse body

`agents/muse.md`:

> If you put character prose **on the page** yourself, load `/creative-writing-modes` and read style files and character files first

then:

> If prose or author direction contradicted character files, say so in that report and ask whether to **update the page**.

then:

> Do not patch character files from a draft contradiction until the author confirms **the page** is wrong.

Same file, same leading word, two referents. "On the page" is the manuscript. "Update the page" is supposed to mean the character file. A muse will ask whether to rewrite the draft, or treat write-to-request as provisional until the wiki wins.

That breaks the split: writer flags, muse reports, kb waits. The muse report is the only author-facing step. If it asks the wrong question, wiki-wait never happens and write-to-request gets undone.

Same collision, lower stakes, in `skills/story-review/resources/prose-critique/character.md`: "the author decides whether the page or the draft is wrong."

**Fix:** say "character file" wherever the wiki is meant. Keep "the page" only for prose. Muse report line should read: flag the contradiction and ask whether to update the character file.

### 2. Medium — in-session muse still may not *find* character files

The c98 line in `agents/muse.md` is the right trigger and the right files. It does not say what to do when those files were not attached. Writer gets "find them before writing; do not invent circumstances" only after loading `resources/prose-modes.md`. Muse is told to load `/creative-writing-modes` and "read style files and character files first, same as `@writer`."

c98 was style-without-wiki, not "forgot the skill name." "Read character files" with no find-them rule fails the same way: style files are already in habit; wiki pages are not.

"same as `@writer`" does not change behavior. The previous clause already named the files.

**Fix:** "If you put character prose on the page yourself, load `/creative-writing-modes`, then load style files and character files. If character files were not attached, find them. Do not invent circumstances." Drop "same as `@writer`."

### 3. Medium — skill-only muse got a checklist, not a load

`skills/creative-writing-muse/SKILL.md` changed one self-prompt bullet:

> Which constraints, style files, character files, canon, and vocabulary matter now?

Answering "character files matter" is not loading them. This path has no subagents and no `agents/muse.md` paragraph. Informal samples skip "Choose the Stance," never load `/creative-writing-modes`, and recreate c98.

Drafting stance does load the modes skill, so a formal draft pass is covered. The failure is the sample that never becomes a stance.

**Fix:** one action, not a question: "Before putting character prose on the page, load style files and character files. If they contradict the request, write to the request and flag it; do not update character files."

### 4. Low — modes SKILL restates the resource opening, and weaker

`skills/creative-writing-modes/SKILL.md` now routes to the opening of `resources/prose-modes.md`. Then it restates pairing + contradiction in four lines that omit "find them," omit "current knowledge," and end on "do not update **the files**" (style, character, or both).

If the agent follows the new routing, the SKILL restatement is duplicate. If it does not, it gets the weaker copy.

**Fix:** keep one load-bearing line in the skill body ("Load style files and character files before writing a character. The opening of `resources/prose-modes.md` has the pairing rule and the contradiction protocol.") Put the protocol only in the opening.

### 5. Low — anti-freeze is in a handoff resource planners may not load

`skills/story-memory/resources/story-context.md` brainstormer bullet:

> During story-planning, treat unsettled backstory as open, not frozen.

That is the right rule in the wrong place. Muse loads `story-planning` and `writing-staffing`, not `story-memory`, when exploring. `creative-direction.md` only adds character files to the post-confirmation handoff, so this change does not freeze planning by itself. The guard does not fire unless someone already opened story-context.

Not a revert. Do not also add it to brainstorming method unless you see freeze behavior.

## What holds — do not undo

- Two artifacts, not three. "Character state" as a file type is gone. Style = how they sound; character files = history, circumstances, current knowledge.
- Not a new always-loaded skill. `creative-writing-modes` stays `available` on muse.
- Writer description now names character files, so callers pass them.
- Writer output: note the contradiction; do not update character files.
- KB wait lives in muse "After Work Settles" and in story-context knowledge maintenance.
- `writing-staffing` attaches character files for writer, character/continuity critic, continuity-checker, and character-sim — not for voice-only critique, style-creator, or style-analysis.
- `character-sim` "Load both. If missing, find them or state that you are inventing history" is the right sim-shaped escape hatch (stricter "do not invent" belongs on the writer).
- Opening-plus-section routing is the right way to cover bridge / alternate take / polish without repeating the rule in every mode.
- "Voice without circumstances is a costume" is a leading phrase that earns its line.

## Checks

1. **Every added line?** Mostly. Dead weight: "same as `@writer`"; the SKILL.md protocol duplicate; "update the page" actively misleads.
2. **Write-and-flag split?** Writer flags and kb waits. Muse report question is ambiguous. Skill-only muse never got the wiki-wait line.
3. **c98 muse sample?** Partially. Agent muse will load named files if they are obvious. It still will not hunt wiki pages. Skill-only muse will not load them for a sample.
4. **Third concept?** No. Pairing is style files + character files.
5. **Over-attached to voice extract/analyze?** No.

## Mechanics

- `creative-writing-modes` remains `available` / `model-invocable: true` on muse. Correct.
- Writer already `load`s that skill. Correct.
- `cw/` copies of generated skills will drift until `sync_cw_skills.py --apply`. Out of band for this review; CI will catch it.
