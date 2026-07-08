# angeliaX (ANGX)

*Trust infrastructure for work and surplus.*

---

Most of what builders learn disappears.

It disappears when projects end, when organisations lose funding, when people move on. A water researcher in Java solves something a builder in Haiti needs. They never find each other. The Haiti builder starts from scratch — or doesn't solve it at all.

The same happens with surplus. A hostel feeds five people every morning. A lawyer sees migrants for free on Tuesday afternoons. A farmer leaves produce at the gate on Fridays. Real, consistent, already happening — invisible to anyone not already there, and unprovable to anyone who wasn't.

ANGX is trust infrastructure for actors who operate outside institutional frameworks — independent builders, small farms, community kitchens, free clinics, individual practitioners, households with surplus to give. People and spaces whose work dissolves when projects end and whose surplus is invisible beyond their immediate location. ANGX makes that work and surplus permanently visible and reachable by other stewards through a partner chain — not as something to claim, but as a record that it is real, ongoing, and witnessed by people who were there.

At sufficient density, ANGX becomes the first permanent and decentralized record of the operational reality of fundamental infrastructure work and surplus provision happening outside institutional frameworks. Witnessed by those present, owned by no one, resilient by design.

---

## What It Is

Two append-only logs. Structurally separate.

**Operational Log** — the operational reality of work. What is being built, tested, failed, learned. The node is the specific project or practice — not the person, team, or space behind it.

**Commons Log** — standing provisions only. What a node regularly and freely gives — food, water, shelter, health, energy, connectivity, informational surplus. Not a one-off, not a passing kindness — a structural pillar of the community it stands in, stated precisely and logged honestly.

Every node has two independent streams: what the steward logs about their own work, and what witnesses log after directly observing or replicating it. Where they align, the work gains credibility. Where they contradict, the contradiction sits permanently visible.

Nothing can be edited or deleted. Every entry is cryptographically signed by its author. Authorship is always traceable. Knowledge that enters this network stops dissolving.

Trust is what this architecture actually builds. Witnessing, curation, and partnering are the three acts that establish it — each one a steward or a base staking their own name on what they've seen.

---

## Status

Schema documented. Target implementation: Hypercore stack.

A relay-based prototype demonstrating the core signal loop — two-log model, Ed25519 signing, steward/witness separation — is available at [codeberg.org/angx-protocol/angx-prototype](https://codeberg.org/angx-protocol/angx-prototype). It predates the current specification and does not implement bases, libraries, or the partner chain. Useful only as a reference for the intended UI and client design.

---

## Docs

- WALKTHROUGH.md — how ANGX works
- WALKTHROUGH-commons.md — how an ordinary space enters angeliaX
- SCHEMA.md — complete technical specification
- CONSTRAINTS.md — ten system constraints

---

*ANGX*
