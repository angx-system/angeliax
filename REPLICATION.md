# REPLICATION.md

*how replication works in ANGX*

---

## The problem with a blueprint

A free school model, developed and refined over years in Belgrade,
Serbia, teaches teenagers design, programming, and device repair —
running on donated, recycled hardware, self-sustaining, no institution
behind it. It works. Someone writes it up: a PDF, a wiki, a masterdoc.
Curriculum, space requirements, a rough budget, lessons learned.

Someone in another country reads it and tries to build the same thing.

The PDF cannot know what it doesn't know. It was written by people for
whom the model worked, in the specific conditions of Belgrade — a
particular bureaucratic environment, a particular device-donation
pipeline, a particular climate, a particular pool of volunteers. Every
one of those conditions is invisible in the document, because none of
them were a problem worth writing down at the time.

The moment a new attempt meets a condition the document never had to
solve, the document goes silent. The person trying to replicate it
reads that silence as their own failure — not as new information
worth logging, because there is nowhere to log it *to*. A franchise
model fixes accountability but not this — deviation from the source
still reads as failure against the brand, routed through a head office
with no operational stake in the local reality. A case study fixes
neither — it is written after the fact, by the survivors, about the
version that worked.

None of these carry the thing that actually determines whether a
replication succeeds: what breaks, specifically, when the model meets
a context it wasn't built for, and what the people on the ground did
about it.

---

## The source node

The Belgrade steward registers a commons node.

**Commons tab → Register Node**

- **Node Type:** `informational`
- **Description:** `Independent free design, programming, and device-repair school for ages 13-17, self-sustaining.`
- **Location:** Belgrade, Serbia
- **Curation:** open

The steward publishes the external write-up — the masterdoc — as a **Built From** reference: a URL, cited once, at registration. The
document is credited as the first touch with physical reality. Nothing
about what happens next depends on that document staying current, or
even staying online.

The Belgrade node's own signal history is not a finished recipe
either:

**Signal — operational:** `Twelve students enrolled. Repair bench running three afternoons a week.`

**Signal — failure:** `Donated laptop batteries swelling within four months. Storage conditions inadequate.`

**Signal — learning:** `Battery drawer with passive ventilation and monthly voltage check resolves swelling. Method documented and attached.`

Even the origin is logged as an arc, not a result. This matters for
what follows: nobody replicating Belgrade is replicating a finished
object. They are replicating a node's *position* — its most recent
honest state — with its own failures already part of the record they
inherit.

---

## Three attempts

Three stewards, on three continents, independently find the write-up
and decide to try. None of them know the others exist.

Each registers a node citing **Belgrade's Node ID** as `Built From` —
not the PDF. From the moment of registration, each is a **sibling** of
Belgrade, not a copy of a file. Three separate keypairs. Three
separate append-only histories. Nothing about any of them can be
edited by Belgrade, or by each other.

---

### Manila — urban, high-bureaucracy

**Commons tab → Register Node**

- **Node Type:** `informational`
- **Description:** `Free design, programming, and device-repair school for ages 13-17, adapted from Belgrade model.`
- **Location:** Manila, Philippines
- **Built From:** `[Belgrade Node ID]`

Space here is expensive and every used space triggers a different
permitting question than a purpose-built one. Donated devices arrive
faster than Belgrade's ever did — but a meaningful share are held at
customs pending an e-waste import classification nobody anticipated.

**Signal — operational:** `Space secured, shared with a print shop after hours. Eight students enrolled first month.`

**Signal — failure:** `Eleven donated laptops held at customs six weeks under e-waste import classification. Repair bench idle.`

**Signal — learning:** `Registering as an educational equipment donation, not e-waste, clears customs in under a week. Template letter attached.`

A local repair collective, already running its own verified node, has
watched the space operate for two months.

**Witness signal — operational:** `Sessions running as described. Bench active, students present, steward consistent.`

---

### Rural highlands — low-connectivity

**Commons tab → Register Node**

- **Node Type:** `informational`
- **Description:** `Free design, programming, and device-repair school for ages 13-17, adapted from Belgrade model.`
- **Location:** [rural highland region]
- **Built From:** `[Belgrade Node ID]`

The nearest reliable internet is a two-hour walk. Power is
intermittent. The device pool is small enough that every unit failing
is a real setback, not a rounding error.

**Signal — operational:** `Six students. Two donated desktops, one functioning laptop. Sessions twice weekly, daylight hours only.`

**Signal — failure:** `Second desktop failed. No local replacement part. Nearest repair shop four hours by bus.`

**Signal — learning:** `Cannibalizing failed units for parts across the small device pool keeps a working core running. One functioning machine per two students, rotated, sustains the program below the scale Belgrade assumed.`

Signals move over Reticulum via angx-bridge on the weeks the steward
cannot reach a connection point — carried hop by hop until they reach
a device online, then replicated normally through Hyperswarm.

A steward from a base two regions over, in the area for unrelated
work, spends a week observing.

**Witness signal — operational:** `Sessions held as described despite device scarcity. Rotation method observed directly, functioning.`

---

### Humid lowland town — tropical, material

**Commons tab → Register Node**

- **Node Type:** `informational`
- **Description:** `Free design, programming, and device-repair school for ages 13-17, adapted from Belgrade model.`
- **Location:** [humid lowland town]
- **Built From:** `[Belgrade Node ID]`

Heat and humidity are the defining condition here, not bureaucracy or
scarcity. Devices that ran for years in Belgrade's dry climate fail in
months.

**Signal — operational:** `Ten students enrolled. Repair bench running, donated devices mostly functional on arrival.`

**Signal — failure:** `Three motherboards corroded within ten weeks. Humidity well above manufacturer tolerance, no climate control available.`

A local steward, running her own verified node nearby, witnesses the
program directly — and logs something the steward's own record does
not yet show:

**Witness signal — operational:** `Sessions running, students present, steward engaged.`

**Witness signal — failure** *(referenced to the steward's own operational signal)*: `Two additional units showing early corrosion not yet logged by the steward. Same cause likely.`

The contradiction — steward reporting steady operation, witness
flagging failure the steward hasn't caught yet — sits permanently
next to both signals. Neither is deleted. Neither is resolved by
authority. It is simply visible to whoever reads this node next.

---

## The cross-pollination moment

Months pass. None of the three stewards have contacted each other.

The rural highland node, working from necessity, already solved a
version of the corrosion problem — not for humidity, but for
generalized component stress under conditions Belgrade never faced:
a silica-gel and passive-airflow storage method, developed to protect
the small device pool from dust and temperature swings, logged as a
learning signal months before the lowland town's corrosion failure was
ever posted.

The lowland steward never searches for it. angx-reader, running
continuously on the base that curates both nodes, has already embedded
every `failure` and `learning` signal in its collection. The
corrosion failure lands near the rural highland's storage method in
vector space — climate and geography apart, mechanism close enough to
surface as a match.

The lowland steward queries the base by their own Node ID, reads the
match, adapts the method — passive airflow plus a drying agent, built
from what's locally available — and logs the outcome.

**Signal — learning:** `Passive-airflow storage with local drying agent, adapted from a method logged in the highlands, cuts corrosion rate substantially over eight weeks. Method documented and attached.`

**Witness signal — learning** *(on the highland node's original signal)*: `Adapted for tropical humidity rather than dust/temperature stress. Substantial improvement, different failure mode than originally addressed.`

Neither steward had heard of the other's context. Neither was looking
for a match to their specific climate. The failure met a method that
already existed, for a different reason, somewhere neither of them
had been.

---

## The graph

A file distributed by download produces a tree: one origin, N
identical copies, each copy's fate invisible to the others.

What exists here is a graph:

```
                    Belgrade
                   /    |    \
              Manila  Highland  Lowland
                            \    ↗
                          (cross-cited via
                           reader match)
```

Four independent, signed, permanent histories. Three siblings citing
one root, once, immutably. One edge between two siblings that no one
planned and no central index arranged — surfaced because both signals
existed in a shared collection and a failure genuinely resembled a
learning signal, regardless of who wrote either one or why.

Belgrade's node did not need to update. The PDF did not need a second
edition. Nothing was pushed downstream. Everything that mattered
propagated because it was logged where it could be found, by people
with no prior relationship to each other, structurally unable to hide
the parts that didn't go as planned.

---

## What the graph reveals

A single document is one data point — it can't tell you what's
essential versus what's just how Belgrade happened to do it, because
nothing has ever been tried differently under its own name.

Four siblings can. Schedule, device ratio, storage method, paperwork —
all four differ. What every steward kept anyway, unplanned and
unenforced, is the actual definition of the thing: free, ages 13 to
17, design and programming taught alongside device repair, on donated
hardware, with no owning institution. Nobody declared that a rule.
Divergence under real pressure revealed it — the network doesn't
converge because a standard was enforced; reality only ever pressures
the packaging, never the principle underneath it.

This isn't specific to free schools. The same separation — principle
from packaging — would surface for a free clinic, a hackerspace, a
makerspace, a food bank: whatever the local siblings keep in common
once bureaucracy, climate, and scarcity have each had their say at
what could be discarded.

---

## Why the separateness is the point

Three attempts at "the same" free school produced three different
crises: an import-classification problem, a device-scarcity problem, a
materials-science problem. None of them was a failure to replicate
Belgrade correctly. Each was Belgrade's model meeting a reality
Belgrade never had to survive.

A system that treats these as deviations to minimize would have
pressured every steward to under-report exactly the information the
next replicator needed most. ANGX treats them as the actual content of
the replication — logged, signed, witnessed, contradicted where
contradiction is honest, and left permanently discoverable by anyone
whose own attempt is about to hit the same wall.

The Belgrade model didn't get copied three times. It got tested three
times, in conditions it was never designed for, by people who owed it
nothing but a citation — and the record of all three tests is now
worth more to the next replicator than the original document ever
was.

---

*ANGX — Replication*
