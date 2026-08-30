# ANGX — Prototype Scope

---

This document defines what falls inside the ANGX prototype and what
doesn't. It carries no estimate of effort, timeline, staffing, or cost —
those are for whichever team builds this to determine on their own terms.
What follows is scope only: the boundary of what gets built, and the
order it depends on.

---

## Source

Everything a build team needs is already resolved and documented across
the repos:

- **README.md** — what ANGX is and why it exists
- **CONSTRAINTS.md** — the ten invariants every decision runs through
- **SCHEMA.md** — the complete technical specification: registration,
  signals, witnessing, verification, ordering, querying, bases,
  curation, and partnering
- **WALKTHROUGH.md** / **WALKTHROUGH-commons.md** — worked scenarios
  showing the mechanics in use, including the case of a steward who
  never touches the operational log at all

Two companion tools extend the core without being required by it: **angx-reader** (failure↔learning matching) and **angx-bridge** (Reticulum transport when the internet is absent). Both are fully specified in their own repos and are out of core scope — see below.

---

## Already resolved

A prior technical feasibility review identified six protocol-level
decisions that would normally need resolving before implementation
could start. All six are now closed and written into SCHEMA.md as
settled specification, not open design questions a build team inherits:

- The space↔base relationship is proven by attestation, not key
  derivation (Base Keypair Linkage).
- Verified status is a three-state, deterministic resolver —
  verified / unverified / unknown — evaluated at read time
  (Verification).
- Witness signals reach curating bases through a topic-announcement
  mechanism (Verification).
- Nothing in the protocol depends on wall-clock time; order across
  feeds is proven by citation (Ordering).
- Partner-chain queries work by enumerating reachable bases and
  querying each one's index, not by live recursive search (Querying)
  — though traversal depth, loop prevention, and result merging
  remain open; see below.

What remains genuinely open is listed as such in SCHEMA.md's own Open
Questions sections — bootstrap rules for the first bases in a network,
the Reviewed Entries minimum, multiple base stewards, Custody Log,
partner replication strategy, Initialize Base trigger synchronization
across devices, partner-chain traversal depth and result merging, the
proposed node/base summary view, and a handful of UX decisions. These
are flagged, not hidden, and a build team resolves them against the
running client as they're reached.

Five of these are load-bearing for this build and require written
sign-off before a resolution becomes permanent: first-base and
second-base bootstrap rules, the Reviewed Entries minimum, partner
replication strategy, Initialize Base trigger synchronization, and
partner-chain query mechanics. If the node/base summary view is built
in this phase, the same applies to it. Custody Log and multiple base
stewards are out of scope for this build (see below) and require no
sign-off yet.

No separate design-resolution phase is needed before implementation
begins. A team builds directly from SCHEMA.md, proposing a resolution
for each of these as it's reached and confirming it in writing before
building on top of it.

---

## In scope — Foundation

The groundwork every later stage depends on.

- Wire schema and canonical encoding for all signed entries
- Keypair and identity layout, Corestore structure
- Client Type Declaration — the first-run question establishing a
  space or mobile keypair, signed into its first record
- Space keypair ↔ base keypair attestation mechanism
- Validation on reference hardware (Raspberry Pi 4 or 5, 64-bit OS,
  4GB+ RAM, USB SSD or high-endurance storage, UPS — per SCHEMA.md's
  Technical Stack)

---

## In scope — Core Loop

The full protocol, CLI/daemon-grade: operable by commands and
background processes, no graphical client. Every item below is fully
functional this way — node registration, witnessing, base
initialization, curation, and partnering all included. Nothing is
withheld pending a GUI; the walkthroughs' tabbed interface is a later,
separate presentation layer over these same operations, not a
precondition for them.

- Node registration, both logs — operational and commons
- Steward signals and attachments (Hyperdrive, fetched on demand)
- Citation-based ordering — entry order proven by sequence position
  and reference, never by wall-clock timestamp
- Library, replication, local indexes and queries
- Witness signals, the discovery mechanism, the verification resolver
- Base initialization, including the bootstrap cases for the first
  bases in a network
- Collection Log, including the consent co-signature path for
  consent-required nodes
- Partner Log: handshake, dual signing, dissolution
- Base Retirement, including Successor Base ID handling
- Partner-chain querying (enumerate reachable bases, query each index,
  combine locally)
- Two physical bases, partnered and soak-tested on target hardware

---

## Out of scope — deferred

Not part of this build. Each is a distinct, later engagement, scoped
and priced on its own terms once the core proves out.

- **Graphical client.** The walkthroughs describe a tabbed UI; the
  prototype itself is CLI/daemon-grade only.
- **Selective Contact disclosure.** Structural consent (co-signed
  curation) is in scope. Field-level encryption of the Contact field
  for consent-required nodes — so only approved readers can read it —
  is not.
- **Live, recursive partner-chain search.** The enumerate-and-query
  model is in scope. A live recursive search protocol across the whole
  chain is a larger, separate feature.
- **Multiple stewards on one base.** A base is a single keypair in
  this build. Multi-writer coordination (Autobase) is deliberately
  excluded — nothing in the core forecloses adding it later.
- **angx-reader and angx-bridge integration.** Both tools are fully
  specified and independently buildable, but sit outside the core
  loop. Neither is a dependency of it.
- **Custody Log.** Accountability for a keypair changing hands without
  ending the base — not yet designed, per SCHEMA.md's own Open
  Questions.

---

*ANGX — Prototype Scope*
