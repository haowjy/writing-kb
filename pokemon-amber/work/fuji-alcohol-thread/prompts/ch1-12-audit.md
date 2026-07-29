# Task

Audit published chapters 1 through 12 of Pokemon: Ambertwo for things that do not
make sense. Report defects only. Do not rewrite anything, do not edit any file.

Chapters: `story/ch1/chapter1.md` through `story/ch12/chapter12.md` in the repo at
/Users/jimmyyao/repos/pokemon-amber

## What counts as a defect

1. **Duplicated text.** Paragraphs or sentences written twice, near-identical
   phrasings reused within a chapter. Two are already known and you do not need to
   re-report them: ch12 lines 97 and 105 (Ash's "greatest Pokemon Master" speech
   appears twice), ch13 lines 69/71 (out of scope anyway).
2. **Contradictions between chapters.** A fact stated one way in an early chapter
   and differently later. Physical geography, who was present, what a character
   knows, timing, object locations, names, ages, Pokemon rosters.
3. **POV knowledge violations.** Default POV is Amber, 1st person. Ch 6 is Fuji,
   3rd limited. Amber is an isekai'd adult consciousness in a clone body: her old
   life is **memory only**. She died under a semi-truck. Anything she narrates as
   fact about events after her death on the other side is invention. Flag any place
   she knows something she has no access to.
4. **Internal logic failures.** Actions that could not physically happen, objects
   that appear or vanish without cause, characters reacting to information they
   were not given, time that does not add up within a scene.
5. **Setup with no payoff, or payoff with no setup**, where the gap looks like an
   error rather than deliberate withholding.

## What does NOT count

- Prose quality, wordiness, weak lines, over-description. Out of scope.
- Deliberate ambiguity or withheld information. This story runs an iceberg
  convention: if a first-time reader would not stumble, it is not a defect.
- Anything the chapter's own `notes.md` already documents as intentional. Check
  `story/chN/notes.md` before reporting.

## Method

Read every chapter file in full, plus each `summary.md` and `notes.md`. Build a
timeline of who is where, holding what, knowing what. Check claims against
`$MERIDIAN_CONTEXT_KB_DIR/wiki/` (characters/, events/, timeline.md) but treat
published prose as the authority when the wiki disagrees, and report the
disagreement.

## Output

A flat list, most severe first. For each: chapter and line number, the quoted text,
what is wrong, and how a reader would notice. Say explicitly if you find nothing in
a category. Do not pad the list to look thorough --- a short list of real defects
beats a long list of nitpicks.
