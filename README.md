# angeliaX (ANGX)

*Trust infrastructure for work and surplus.*

---

Most of what builders learn disappears.

It disappears when projects end, when organisations lose funding, when people move on. A water researcher in Java solves something a builder in Haiti needs. They never find each other. The Haiti builder starts from scratch — or doesn't solve it at all.

The same happens with surplus. A hostel feeds five people every morning. A lawyer sees migrants for free on Tuesday afternoons. A farmer leaves produce at the gate on Fridays. Real, consistent, already happening — invisible to anyone not already there, and unprovable to anyone who wasn't.

ANGX is trust infrastructure for actors with no institution already vouching for them — no network, registry, or parent organization a stranger could check instead that vouches for the operational reality of the work or provision itself. Independent builders, unaffiliated community kitchens, free clinics, individual practitioners, households with surplus to give — real and sustained, but verifiable only by going there and asking someone who already knows. ANGX makes that work and surplus permanently visible and reachable by other stewards through a partner chain — not as something to claim, but as a record that it is real, ongoing, and witnessed by people who were there.

At sufficient density, ANGX becomes the first permanent and decentralized record of the operational reality of work and surplus that no institution was already vouching for. Witnessed by those present, owned by no one, resilient by design.

---

## What It Is

Two append-only logs. Structurally separate.

**Operational Log** — the operational reality of work. What is being built, tested, failed, learned. The node is the specific project or practice — not the person, team, or space behind it.

**Commons Log** — standing provisions only. What a node regularly and freely gives — food, water, shelter, health, energy, connectivity, informational surplus. Not a one-off, not a passing kindness — a structural pillar of the community it stands in, stated precisely and logged honestly.

Every node has two independent streams: what the steward logs about their own work, and what witnesses log after directly observing or replicating it. Where they align, the work gains credibility. Where they contradict, the contradiction sits permanently visible.

ANGX does not move resources. It records that work is happening and that surplus stands — not what is needed, not what is available to take. What crosses the network is trust and method: proof that something is real, and a fix for a problem someone else has already solved. Exchange of goods, where it happens, happens the way it always has — locally, between people who are already there.

Nothing can be edited or deleted. Every entry is cryptographically signed by its author. Authorship is always traceable. Knowledge that enters this network stops dissolving.

Trust is what this architecture actually builds. Witnessing, curation, and partnering are the three acts that establish it — each one a steward or a base staking their own name on what they've seen.

ANGX sits in the lineage of an old idea, extended in a new direction. Git gave code a permanent, distributed history — every change, every branch, traceable without a central server. Dat, and later Hypercore, extended that same idea to datasets and general files. ANGX extends it once more: not to the artifact's history, but to what happens after the artifact leaves the repository — where it got deployed, what failed, what was learned, who replicated it and where. Git shows how code changed. ANGX shows what the code, the design, or the practice actually did once they met the world.

---

## Status

Schema documented. Target implementation: Hypercore stack.

The schema itself — two logs, signals, witnessing — doesn't depend on 
any one transport. Hypercore is the current, concrete choice: an 
existing, working, append-only signed feed protocol with exactly the 
properties ANGX needs.

A relay-based prototype demonstrating the core signal loop — two-log model, Ed25519 signing, steward/witness separation — is available at [codeberg.org/angx-protocol/angx-prototype](https://codeberg.org/angx-protocol/angx-prototype). It predates the current specification and does not implement bases, libraries, or the partner chain. Useful only as a reference for the intended UI and client design.

---

## Docs

- WALKTHROUGH.md — how ANGX works
- WALKTHROUGH-commons.md — how an ordinary space enters angeliaX
- SCHEMA.md — complete technical specification
- CONSTRAINTS.md — ten system constraints

Two optional companion tools extend ANGX without being required to run
it: [angx-reader](https://github.com/angx-system/angx-reader) surfaces
failure↔learning matches across replicated feeds; [angx-bridge](https://github.com/angx-system/angx-bridge)
carries feed updates over Reticulum when the internet is absent. Neither
is a dependency — a steward or base can register, log, and witness with
only this client.

---

*ANGX*
