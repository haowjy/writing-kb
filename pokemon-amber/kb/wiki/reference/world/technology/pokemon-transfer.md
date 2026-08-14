---
status: drafting
---

# Pokemon Transfer & Storage

How Pokemon move between trainers and facilities beyond physically carrying
them. The system's defining constraint: **transfer moves custody and location
between physical facilities; it is not indefinite digital storage.** A
transferred Pokemon lives at an approved receiving facility --- a ranch,
stable, laboratory, or Center care --- not in a server.

## Current Era: Limited Beta (Amber's first journey year)

- Instantaneous Pokemon transfer exists as a **limited beta at select Pokemon
  Centers**. Participating Centers have trial terminals.
- The service is not advertised. Trainers generally have to know it exists and
  ask staff to use it.
- Transfers go only to **approved physical receiving facilities**, such as
  Professor Oak's ranch.
- Amber knows about the beta through Oak and can transfer Pokemon to his
  ranch.

Everything else still moves physically: stabling, surrender, release, and
hand-carry remain the ordinary ways to open a carry slot. See
[Licensing System & Trainer Tiers](../systems/trainers/licensing.md).

## Next Year: Broad Public Rollout

The following year --- when Ash's cohort begins --- the Center-to-ranch
instantaneous transfer network is broadly available to the public. This is the
familiar Center-to-ranch transfer system of the early games era.

## Later: Registry Integration (direction settled, details open)

Roughly two to three years after Amber's departure, Pokedex, Pokeball, and
license-registry integration matures enough to relax the rule that a trainer
at capacity must open a slot **before** registering another capture. Planned
functions include automatic capture registration, license/capacity checks,
protected-status checks where supported, designated receiving facilities, and
inactive/deployment locks for Pokemon beyond the active carry limit.

Two invariants hold across every phase:

- **The six-Pokemon active limit remains.** Technology relaxes the handling of
  excess captures, never the active-team safety ceiling.
- **No Pokemon is dangerously trapped without recourse.** Inactive balls
  cannot ordinarily be deployed, traded, or re-registered without
  authorization, but Pokemon Centers retain emergency and welfare overrides.

The exact timing (two vs. three years), vendor attribution (Silph Co. or
another technology provider), offline behavior, and engineering mechanism
remain open. The settled direction and its boundaries are recorded in
[Capture registration and transfer automation](../../../planning/decisions/capture-registration-automation.md).

## Attribution

Oak's Pokedex work contributes identification and field-registration
architecture to the later system. Oak is not the sole inventor of the transfer
or registry network; ball-lock and transfer protocols may come from Silph Co.
or another provider. See [Professor Oak](../../characters/humans/professor-oak.md).

## Cross-Refs

- [Licensing System & Trainer Tiers](../systems/trainers/licensing.md) --- carry limits, slot-opening, capture legality
- [Pokeball Technology](pokeball-technology.md) --- ball mechanics and limitations
- [Communications](communications.md) --- network coverage the transfer system depends on
- [Identity & Security](identity-security.md) --- ball serialization and registries
- [Joy Network](../../organizations/joy-network.md) --- the Pokemon Centers that operate the terminals
