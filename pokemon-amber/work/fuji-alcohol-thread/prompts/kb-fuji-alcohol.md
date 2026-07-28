# Task: Correct Dr. Fuji's alcohol timeline in the KB wiki

Update two wiki pages so they encode a newly settled canon decision about Dr. Fuji's
drinking. The current pages contradict each other and both contradict the author's
decision. Prose chapters are NOT in scope — do not touch `story/`.

## Files to edit

- `$MERIDIAN_CONTEXT_KB_DIR/wiki/characters/dr-fuji.md`
- `$MERIDIAN_CONTEXT_KB_DIR/wiki/characters/giovanni.md`

## The settled canon (author-confirmed this session)

Fuji's drinking is **cyclical, not continuous**. It tracks whether he has a purpose.
Giovanni is the supplier of purpose. Five phases:

1. **Basement years (~12 years before story).** Rock bottom after Amber's death.
   Obsessive research by day, alcohol by night. Escalating violence toward Delia ---
   he wasn't a violent man who drank, he was a drunk who became violent. Delia leaves
   and divorces him. This phase is already correct on the page; keep it.

2. **Giovanni recruits him (~12 years before story) --- HE GETS SOBER.**
   This is the correction. Giovanni offers funding, facilities, and the promise of
   bringing Amber back. Purpose displaces the bottle entirely. Fuji is genuinely
   sober for roughly twelve years, and that is *why* he can rebuild himself into
   someone composed and competent.

3. **Ch 6 --- the relapse begins.** Domino hands him surveillance photos of Delia
   with Stephen Ketchum. He had declined a drink minutes earlier (asked for water).
   After the photos, he asks for whiskey. This is his first drink in ~12 years.
   Whiskey is his coping drink.

4. **Ch 6 through Ch 17 --- escalating collapse.** Ch 11 he buys wine (framed to
   himself as a reunion gift). Ch 13 he drinks that bottle alone on a log and then
   murders Stephen. Ch 14-15 arson. He is never *sloppy* drunk in these chapters ---
   impaired at the edges, judgment blurred, not enough to be an excuse.

5. **After Ch 17 --- the raging phase.** Amber escapes him. Losing the daughter he
   resurrected is the failure that breaks him for good. This is the "drunk scientist"
   period: openly, visibly drinking; known by everyone around him; snapping at and
   physically lashing out at his research scientists. Unpredictable --- sometimes
   producing brilliant work while drunk, sometimes purely destructive. Nobody is
   hiding it and neither is he.

6. **Clone-family era (+5-10 years) --- SOBER AGAIN.** Giovanni runs the exact same
   transaction a second time: offers him another daughter (new Ambertwo) and with it
   a purpose. Fuji gets sober again and is genuinely competent, present, and a good
   father to new Ambertwo.

## What each page currently gets wrong

**`dr-fuji.md` line ~50** currently reads: "Giovanni didn't cure the alcoholism ---
he redirected it... The drinking became functional, managed, part of the routine
rather than the whole of it... but the bottle never left. It just became invisible."

This is wrong. He stopped. Rewrite this passage for phase 2, and extend the page so
phases 3-6 are represented in the backstory/timeline structure the page already uses.

**`giovanni.md` line ~184** currently reads: "...without the alcohol and grief-madness
(Giovanni sobered him up, gave him purpose), he might actually be good at it."

The *conclusion* is correct and must be preserved --- Fuji is sober and good at
fathering new Ambertwo, and that is devastating for our Amber. But "Giovanni sobered
him up" needs to be clearly the **second** sobering, with the post-Ch-17 raging phase
in between. Make the repetition legible.

## The thematic point to encode

Giovanni never cures Fuji --- he *supplies* him. Purpose is the actual dependency;
alcohol is what fills the gap when the supply is cut. Giovanni has now run the
identical transaction twice (promise of a daughter, in exchange for total compliance),
which means he is manufacturing the dependency he then relieves. This sharpens
Giovanni's "loyalty is familial, not coerced" doctrine into something darker, and it
is worth a sentence or two where the pages discuss his leverage over Fuji.

Do not overstate it or moralize in the wiki voice. State the mechanism; let it sit.

## Constraints

- Match each page's existing voice, heading structure, and formatting conventions.
- `dr-fuji.md` opens with a spoiler warning; content below it can be explicit.
  `giovanni.md` --- follow whatever spoiler convention that page already uses.
- Punctuation: em dash is `---` (three hyphens), ellipsis is `...`, ASCII quotes only.
- Links out of the repo use GitHub URLs, not local paths. Reference-style preferred.
  Base: `https://github.com/haowjy/writing-kb/blob/main/pokemon-amber/kb/`
- Do not invent new plot events. Everything you need is above. If something seems to
  require a fact you don't have, leave it out and report it as a gap.
- Do not create a Domino page. Explicitly declined by the author.
- Check whether any *other* KB page asserts Fuji drinks during the Giovanni years or
  in the clone-family era. If so, fix it the same way. Report what you found.

## Report back

- Which files changed and the substance of each change
- Any other page that contradicted the new timeline
- Any gap or contradiction you could not resolve without asking the author

Commit the KB repo when done. Do not push.
