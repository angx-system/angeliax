# WALKTHROUGH-commons.md

*how an ordinary space enters angeliaX*

---

ANGX does not require operational nodes to participate. Anyone holding up
something real and consistent enters through the commons log alone.

---

## The people and the space

**Fatima** lives outside Tunis. She runs a small market garden with her
sister. Most weeks there is more than the family needs.

**Youssef** lives nearby. He runs a seasonal olive press. A base in Sfax
added his olive press node four months ago. Commons witnessing is unlocked
for him.

---

## Part 1 — Fatima

### Initializing the client

First run. One question:

*Are you logging work and surplus for a fixed location or for your own work?*

Fatima selects **[ A fixed location ]**. Her keypair is generated. The
answer is signed into the first record.

### Registering a commons node

**Commons tab → Register Node**

- **Node Type:** `food`
- **Description:** `Surplus vegetables from a market garden, given freely. Running for over a year.`
- **Location:** Mornag region, Tunisia

The entry states what is true and how long it has been true. It's simply
a log of her standing provision, not an offer.

### Logging

She logs every Saturday after the gate closes.

**Signal — operational:** `Gate open. Tomatoes and courgettes. Six people came. All taken.`

**Signal — operational:** `Gate open. Smaller harvest. Tomatoes only. Three people came.`

**Signal — failure:** `No surplus this Saturday. Heat damage to courgette crop. Back next week.`

**Signal — operational:** `Gate open. Tomatoes, peppers, herbs. Eight people came.`

Twelve months. Forty-eight Saturdays. Failures logged alongside the good
weeks.

---

## Part 2 — Witnesses

Witnessing a commons node requires a verified node of one's own — work or
provision, already logged and standing. Commons witnessing is
presence-gated: it requires no node of the same type, only sustained,
direct presence.

Youssef holds a verified olive press node. He has known Fatima's garden for
two months, present often enough to know its pattern.

**Commons tab → Fatima's food node → Post Witness Signal**

**Witness signal — operational:** `Garden running as described. Good quantity. Steward present. Consistent over two months.`

A second local steward, running her own verified commons node nearby,
witnesses the following month. A base steward from Sfax, in the region for
her own work, witnesses the month after — using her personal steward
keypair, separate from the base she operates.

Three witness signals. Each from someone already accountable in the
network. Each present long enough to know a real pattern from a single good
week.

---

## Part 3 — The farm becomes a base

Twelve months of honest logging. Three witness signals from verified
stewards across two regions.

The Sfax base steward has read the signal history directly. A household
base outside Bizerte, holding the feed of a steward who knows Fatima's
work, reads the same history independently. Both add her food node to
their collections.

Two distinct verified bases have added a node from this keypair. **Initialize Base activates.**

Fatima clicks **Initialize Base**. A base keypair is generated on the
farm's device, independent of her own. The base is announced.

**Base identity:**

- **Name:** farm-mornag
- **Description:** `Small market garden outside Tunis. Standing surplus provision, witnessed locally.`
- **Location:** Mornag region, Tunisia

### Partnering with Sfax

The Sfax base steward has read twelve months of Fatima's record and judged
it sound. Both stewards exchange base addresses.

One base proposes. The other accepts. Both sides log the event
independently. Both keypairs sign the handshake.

farm-mornag is now a verified base, its collection reachable through the
partner chain.

### Curating

Fatima has watched what happens around her for a year.

Youssef runs an olive press two kilometres away, September to December,
for anyone who brings olives. No charge. She has seen it operating
directly.

**Client → Add to Base** — Youssef's olive press commons node.

A woman from the next village runs a free health consultation from her
home on Wednesday mornings, three years running. Fatima has attended
twice, enough to know it is real.

**Client → Add to Base** — her informational commons node.

Both provisions, observed directly, now stand in farm-mornag's collection,
reachable through every base partnered with it. Fatima did not build
either. She watched them long enough to put her own name behind them.

---

## Part 4 — Fatima queries the network

farm-mornag is now partnered with Sfax. Through Sfax, the partner chain
reaches bases across the region and beyond.

Fatima has been losing courgette plants to a soil fungus for two seasons.
Nothing she has tried has worked. She could search the open internet, but
the results would be generic — chemical treatments unavailable locally,
advice from different climates, unverified claims.

**Operational tab → query: food nodes → learning signals → "pythium"**

She reads through learning signals logged by food nodes across the
partner chain. A farm base in Santa Fe, Argentina logged one eight months
ago, with an attachment — a method for treating the same fungus using
composted organic material available in any market garden. The method was
logged by a verified steward running an identical market garden in the
same climate, witnessed and replicated by three other bases before it
reached Fatima's query.

She fetches the attachment, reads it, tries the method.

It works.

---

## What remained

Fatima started with surplus vegetables and a gate.

Over twelve months: she logged forty-eight Saturdays, failures included.
Three stewards, each already accountable in the network, witnessed her
provision directly. Two independent bases judged her record real and added
her node. Her farm became a verified base, partnered with Sfax. She
curated two more local provisions she had watched long enough to trust.

And through the same partner chain, a method logged on a different
continent reached her, in time to save a crop. Her own twelve months of
signals now stand in the record — a rhythm, a failure, a method —
available to anyone running a similar garden in a similar climate who
reads the partner chain or wants to start one of their own.

Nothing here required a stranger to find her gate and act on it. Every
connection — Youssef's node, the consultation, the fungus treatment — moved
through someone who was there long enough to know it was real.

---

*ANGX — Operational Log + Commons Log*
