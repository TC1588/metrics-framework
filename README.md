# metrics-framework

How I design a metrics framework for a product or a marketing function, written as a template you can fill in.

I built this while specifying an internal performance product that four teams now run on. The problem it solves is narrow and common. A team has a dashboard, the dashboard has numbers, and nobody can say where any of them came from or what would have to change for one to move.

## 1. One North Star, written at full length

Write the metric as a sentence, not a label. "Streams" is a label. "Worldwide licensed royalty-bearing consumption at song level, carried with modeled USD value" is a metric, because every word in it rules something out.

Then answer three questions in writing.

**Why this quantity and not a nearby one.** This is a business judgment about what the company runs on, and it should read like one.

**What it reconciles to.** Name the authoritative source and state the tolerance. Mine reconciles to the licensing portal to the exact stream. If you cannot name a source, you do not have a North Star, you have a preference.

**What it deliberately excludes.** The exclusions are where the arguments happen later, so settle them now.

## 2. Input metrics, defined as levers

Every input metric gets four fields. Skip any one of them and the metric will be disputed inside a month.

| Field | What it answers |
|---|---|
| Numerator | What is being counted, exactly |
| Window | Over what period, and whether it is rolling or fixed |
| Source | Which system is authoritative for this field |
| Rationale | Why moving this moves the North Star |

The test for whether something belongs here: can someone on the team change it on purpose this quarter? If not, it is context, not a lever.

## 3. Health guardrails, each tied to a named failure

A guardrail exists to catch one thing going wrong. Write the failure first, then the metric that would show it.

| Failure it guards against | Guardrail |
|---|---|
| A launch spike hiding a collapsing baseline | Decay rate |
| Distribution pulled out from under you | Playlist or channel drop-off |
| One market carrying a number that reads as global | Geographic concentration |
| A stale number that looks flat | Pipeline freshness, per source |

## 4. Business metrics, with modeled kept visibly separate from measured

Modeled revenue, goal pace, and portfolio contribution belong on the same surface as the measured numbers, and they must not look like them. Every modeled figure carries its formula one tap away, and the two categories are styled differently.

This is the rule people skip and regret. A modeled number quoted in a board deck as a measured one is a problem you cannot walk back.

## 5. Alert thresholds, with trip conditions and a cadence

A framework that tells you what to look at is half a framework. Say when to look.

- Per-metric trip conditions, written as a comparison and not a feeling
- A daily, weekly, and monthly review split, so the daily read does not turn into a monthly retro
- One owner per alert

## The rule underneath all of it

Lock one consumption basis in writing before a second data source arrives. When a second vendor's figure shows up later it can appear as a labelled breakout, never as a competing headline. Two authoritative numbers for the same quantity is the fastest way to lose a room.

Blank version in [TEMPLATE.md](TEMPLATE.md).
