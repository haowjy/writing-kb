# Chapter 18 KB audit

Read-only investigation. Do not edit any file.

Audit the Pokemon Amber KB against story repository commit `466ac5d`, focusing on the settled Chapter 18 state in `story/ch18/chapter18.md`, `notes.md`, and `plan.md`. The KB root is resolved by `meridian context kb` / `$MERIDIAN_CONTEXT_KB_DIR`.

Inspect existing KB pages before proposing targets. Search broadly enough to find stale claims about journey age, early departure/evaluation exceptions, Reid and Nora, Oak's sponsorship and training, the prototype Pokedex, travel equipment/spatial bag, the visible Mega Stone and its provenance, and Oak's reasons for trusting Amber. Pay special attention to existing decision pages, Amber/Oak/Pallet references, Arc 1 planning, open questions/current direction, style pages only if they encode facts, and indexes/cross-links.

Return a concise report with:

1. Current-truth findings, each with exact file paths and supporting lines/quotes.
2. Every contradiction or stale claim found, with exact file path and replacement/deletion recommendation.
3. Recommended existing files to update; do not recommend new pages unless no existing page can own the fact.
4. Anything unsettled that must remain explicitly open.
5. Adjacent areas worth exploring only if they could change a concrete doc target.

Honor the human's settled facts in `prompts/ch18-kb-update.md` over inference from older docs. Distinguish intended KB truth from the draft chapter's not-yet-shipped status.
