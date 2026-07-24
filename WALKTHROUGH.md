# WALKTHROUGH.md

*how ANGX works*

---

ANGX is two logs. One records what is being built, tested, learned, and
failed. The other records what is freely and consistently given. Both are
append-only, signed, and permanent. Each entry is a record that something
is true, written by the steward whose work or surplus it describes.

---

## Part 1 — Amara

Amara lives in Nairobi. Eight months developing a low-cost ceramic water
filter for high-sediment river water.

### Registering her work

**Operational tab → Register Node**

- **Node Type:** `water`
- **Description:** `Developing low-cost ceramic water filter for high-sediment river water.`
- **Location:** Nairobi, Kenya

The client generates a Node ID from her keypair.

### Logging

**Signal 1 — operational:** `Ceramic filter prototype four assembled. Testing flow rate in high-sediment water this week.`

**Signal 2 — failure:** `Local ceramic supplier inconsistent porosity. Flow rate 40% below minimum viable. Switching to composite material.`

**Signal 3 — learning:** `Composite ceramic blend confirmed. Filters high-sediment water 8hrs continuous.`

She attaches the full method to the learning signal. The signal is the
pointer; the method is the attachment, fetched on demand.

Eight months. Several failures. One method, documented in full, including
what failed before it worked. The record stands on its own, signed by her
keypair, the moment she writes it.

---

## Part 2 — A Nairobi base

A community kitchen in Mathare. The steward who runs it has cooked and
shared meals from this kitchen for six years. She runs the dedicated device
that will become the base.

### Logging the kitchen's standing commitment

**Commons tab → Register Node**

- **Node Type:** `food`
- **Description:** `Community kitchen. Free meals shared with the neighborhood. Operating for six years.`
- **Location:** Mathare, Nairobi

**Signal — operational:** `Kitchen running this week. Regular turnout.`

**Signal — failure:** `No cooking this week. Repairs needed on the stove.`

The entry states what is true and how long it has been true. The record
carries no schedule and no instruction — only the fact of an ongoing
commitment, confirmed over time by the people positioned to know.

### Witnessing

A health worker who runs her own clinic two streets away has eaten at the
kitchen for over a year, often enough to know its rhythm. A steward from a
base in Kisumu, in Mathare for her own work, has visited twice and seen the
same.

**Commons tab → kitchen's food node → Post Witness Signal**

**Witness signal — operational:** `Eaten here regularly for over a year. Running exactly as described. Steward present every time.`

Witnessing requires a verified node of one's own — work or commons provision,
logged and standing. The signal is written by someone already accountable
within the network, present often enough to know a real pattern from a
single good week.

Over months, signals like these accumulate from local stewards and from
visiting ones — each a record of direct, sustained observation.

### Becoming a base

Two verified bases, each independently informed by a steward who observed
the kitchen's record over time, add the food node to their own
collections.

The steward's client detects this. **Initialize Base activates.**

A base keypair is generated, independent of her own. The base is
announced. The device now holds an identity that outlives whoever happens
to be running it.

**Base identity:**

- **Name:** mathare-kitchen
- **Description:** `Community kitchen and local base, Mathare, Nairobi.`
- **Location:** Mathare, Nairobi

### Partnering

A base steward in Java, running a similar community kitchen base, has
observed mathare-kitchen's collection over time and judged it sound —
additions that hold up, contradictions left visible, nothing inflated. The
two stewards exchange base addresses.

One proposes. The other accepts. Both keypairs sign the handshake,
recorded independently on each side.

mathare-kitchen is now a verified base — its collection reachable
through Java's partner chain, and through every base partnered with Java
beyond that.

### Curating

The mathare-kitchen base steward has followed Amara's work for months —
visited her lab, watched the filter run, read the failure-to-learning arc
in full.

**Client → Add to Base** — Amara's water node.

Amara's node enters mathare-kitchen's collection. Logged, signed,
permanent. Because mathare-kitchen is now a verified base, her client
detects the addition and her keypair gains verified status. She can now
witness other operational and commons nodes.

---

## Part 3 — David

David lives in Kampala. Four months developing rainwater harvesting
systems for informal settlements. A base in Kampala, already partnered
elsewhere, added his operational water node to its collection two months
ago — his own work, already verified, before he ever left home.

He travels to Nairobi for several weeks, work of his own, and connects
his client on arrival. A steward he knows from Kampala, who visited
mathare-kitchen the previous year, gave him the base address before he
left.

### Querying the base

**Operational tab → query: water nodes**

Several water nodes are reachable through mathare-kitchen's collection and
its partner chain. Amara's stands out — four operational signals, two
failures, one learning signal with the full method attached.

He reads the arc before meeting her: what she built, what failed, what she
confirmed.

### Working alongside her

David is in Nairobi for three weeks. He brings ceramic material from
Kampala to Amara's lab and runs her method himself, under her supervision,
over several days.

It works. However, after 72 hours of continuous use without cleaning,
output drops 60% — a degradation rate her documentation never flagged.

He has done what witnessing asks: observed the work directly, closely
enough and long enough to find something her own record missed. His own
node's verified status — earned in Kampala, before this trip — is what
makes his signal admissible here.

**Operational tab → Amara's water node → Post Witness Signal**

**Witness signal — operational:** `Filter running as described. Setup replicable. Steward present throughout.`

**Witness signal — learning** *(referenced to her learning signal):* `Replicated composite blend using Kampala materials. Flow rate within 5% of Nairobi result.`

**Witness signal — failure** *(referenced to her learning signal):* `Output degrades 60% after 72hr continuous use. Not flagged in original docs. Critical for field deployment.`

The failure signal contradicts her learning signal directly. Amara reads
it and answers on her own node:

**Steward signal — learning:** `Cleaning interval critical. 72hr max before significant output degradation. Updated method attached.`

Original claim. Independent replication. Honest contradiction. Steward
response. All permanent, all signed, none of it mediated.

### David, witnessed in turn

David has logged his own water node for four months — operational
signals, failures, no commons node yet.

Amara has worked beside him for three weeks, watched how he operates,
read his record in full. She tells the kitchen steward what she has seen.
The steward reviews the log herself before deciding.

**Client → Add to Base** — David's operational water node.

His node — already held by a base in Kampala — now enters
mathare-kitchen's collection as well. Two verified bases, on two
continents, hold the same record. Neither needed the other's permission
to add it, because David's node was set to `open` at registration and
required no consent for being added to a particular base.

---

## Part 4 — Two bases, apart

Elsewhere, a small settlement runs its own base from a single device,
solar-powered, connectivity thin and intermittent. The first settlement's
steward has spent a year logging the settlement's own work — water
storage, energy systems — and, in time, partnered with a base two regions
over. The second settlement's base is verified. The first settlement's
own energy node, curated into the second settlement's base, is verified
too.

One evening, with a connection window open, the first settlement's
steward queries energy nodes across the partner chain.

**Operational tab → query: energy nodes → learning signals → "wiring fault"**

A signal surfaces, logged months earlier by someone she has never heard
of, in a settlement she has never visited: a battery-bank wiring fault,
the failure that caused it, and a method — documented in full — that
fixed it.

She fetches the attachment. She replicates the method herself, on her own
hardware, the same week.

It works on the first attempt.

**Operational tab → the original node → Post Witness Signal**

**Witness signal — learning:** `Replicated wiring fix locally. Fault resolved, same configuration. First corroboration of this method.`

She logs her own adaptation as a new signal on her own node — crediting
the method, not claiming it as her own.

Neither steward has spoken to the other. Nothing was arranged.

### Months later

The second settlement's steward — the one whose wiring fix was replicated
— is dealing with a water problem of his own: a storage tank losing
volume faster than it should, cause unclear.

He queries water nodes across his own partner chain. Nothing local fits.

**Operational tab → query: water nodes → learning signals → "tank volume"**

He widens the query and finds it: a signal logged by the first
settlement that replicated his wiring fix months earlier, describing an
identical tank fault, and a repair, documented and attached.

He hadn't gone looking for that settlement specifically. He didn't know
its name until he read the signal.

**Operational tab → the water node → Post Witness Signal**

**Witness signal — learning:** `Repair applied. Tank holding at expected volume after two weeks.`

Neither steward arranged any of this. No agreement was made, no
relationship declared. Two bases, unrelated, simply began appearing in
each other's queries often enough that each had learned, without deciding
to, that the other's log was worth checking first.

---

## Part 5 — A design with no steward

Somewhere, months earlier, someone posts a schematic to a public repo: a
gravity-fed chlorine doser, built from a valve and a length of pipe, no
electricity required. No name attached beyond a username. No further
commits after the first. Whoever posted it never runs one, never logs
anything, may never know what happens next.

A clinic steward outside Blantyre finds the repo while searching for a
way to treat a contaminated tank.

### Registering

**Operational tab → Register Node**

- **Node Type:** `water`
- **Description:** `Gravity-fed chlorine doser for community tank, built from public design.`
- **Location:** Blantyre region, Malawi
- **Built From:** `[link to the repo]`

### Logging

**Signal — operational:** `Doser installed. Tank serving forty households. Dosing steady first two weeks.`

**Signal — failure:** `Valve corroding at eight weeks. Dosing rate dropping. Investigating replacement material.`

**Signal — learning:** `Brass fitting resolves corrosion. Stable at fourteen weeks. Method documented and attached.`

The repo is credited once, at registration, and never again. Everything
after that is the steward's own signal, own keypair, and own record of what
actually happened when the design met a real tank.

---

A base steward in the southern Philippines, querying water nodes across
the partner chain for anything on chlorine dosing, finds the node — the
learning signal, the corrosion fix, the fourteen weeks holding steady.

He builds one.

### Registering

**Operational tab → Register Node**

- **Node Type:** `water`
- **Description:** `Gravity-fed chlorine doser, adapted for barangay water system.`
- **Location:** Zamboanga del Sur, Philippines
- **Built From:** `[Node ID of the Blantyre doser]`

He has never seen the original repo. He doesn't know the username behind
it, and doesn't need to. What he found, and what he cited, was a
steward's own witnessed record — a real tank, a real failure, a real fix.

---

## What remained

David arrived in Nairobi carrying four months of logged work, on business
of his own. He left having read eight months of another builder's
documented method, replicated it under her direct supervision, and
surfaced something her own record had missed. His own work, already
verified once, now stood verified twice — reachable through two partner
chains that had never met each other.

Somewhere else, a wiring fix crossed a distance neither steward had
planned for. Months later, a tank fault crossed back the other way. Two
settlements that had never spoken had each, twice now, been the answer to
a problem the other hadn't solved yet.

The network grew by exactly one mechanism, over and over: someone who was
there long enough to know put their name behind what they saw, and left it
where the next person could find it. Sometimes that person built what they
saw themselves, from nothing. Sometimes they picked up a design that had
no steward at all, and became its first real witness — building only for
those who came after, one honest hop back.

---

*ANGX — Operational Log + Commons Log*
