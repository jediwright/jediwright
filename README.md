# Jedi Wright

I build governance architecture for the boundary between personal data and institutional systems — the place where local-first software hands off to the network, where a worker's record crosses into a platform, where a patient's data reaches a health system, where a person's social graph touches a relay, and where financial transactions clear through payment infrastructure. That boundary has never had a principled design. This work is an attempt to build one.

The core argument, developed in the [Full Personhood essay](https://systemsofthought.com) at Systems of Thought: the gap between what institutions know about people and what people can know, control, or demonstrate about themselves is architectural before it is political. The architecture can now be built on the person's side. These repos are the build.

---

## The Architecture

**[seam-stack](https://github.com/jediwright/seam-stack)** — The foundational framework. A four-layer pattern (Substrate, Governance, Boundary, Evidence) for systems where the seam — the governed crossing point between a person's data and an institutional system — is the primary design surface, not the server.

**[local-first-series](https://github.com/jediwright/local-first-series)** — Specifications and Pattern Commons entries for governed boundary crossings across employment, commerce, healthcare, and social domains. The Pattern Commons is a reusable library of architectural patterns for seam design; entries currently include PC#0 (The Governed Crossing), PC#7 (Employment Seam), and PC#8 (Substrate-Crossing Seam — governing how a local-first record crosses into a public protocol like AT Protocol / Bluesky).

**[employment-seam](https://github.com/jediwright/employment-seam)** — The reference implementation. Pattern Commons #7: the worker owns the knowledge graph; the platform facilitates the handoff and exits. Built on Automerge + Keyhive for cryptographic local-first document storage, with a live AT Protocol crossing demonstration. This is where the architecture runs.

**[governed-pr-framework](https://github.com/jediwright/governed-pr-framework)** — A lightweight PR review framework that scales rigor by blast radius rather than line count. The governance discipline developed for this work, extracted for general use.

---

## The Argument

The seam-stack architecture rests on a diagnosis about why personal data governance fails: institutions have always had sophisticated data architectures; individuals have not. Telling individuals to negotiate better terms or choose better platforms doesn't address the structural asymmetry. Building a governed architecture on the person's side does.

A person's employment history, health record, or financial data doesn't need to live on a server someone else controls. Local-first software — document stores that sync via conflict-free data structures, with cryptographic access control — makes it technically feasible for the person to hold the authoritative copy. What's been missing is the governance layer: explicit rules for when data crosses out of that personal store, under what terms, with what evidence left behind.

The Seam Stack is that governance layer. The Pattern Commons is the reusable expression of it. The employment-seam prototype is the first demonstrated instance.

For the full theoretical argument, including the five structural requirements and their derivation: [Full Personhood — The Governance Model AI Requires and Capitalism Never Built](https://systemsofthought.com)

---

## Earlier Prototypes

These explored the problem space and directly informed the architecture above. They're functional demonstrations, not governed to the same standard as the current work.

**[checkout-seam](https://github.com/jediwright/checkout-seam)** / **[local-first-ecommerce](https://github.com/jediwright/local-first-ecommerce)** — A local-first e-commerce prototype. Y.js + IndexedDB for all state; the server is required only for payment processing. Demonstrates deliberate boundary design: the network is the seam, not the default.

**[fhir-seam](https://github.com/jediwright/fhir-seam)** — Local-first patient intake with a FHIR mock endpoint as the seam. The healthcare boundary crossing case.

**[local-first-social-network](https://github.com/jediwright/local-first-social-network)** — A local-first social architecture. The user owns the graph; the relay facilitates connection and exits.

**[governance-tracker](https://github.com/jediwright/governance-tracker)** — Local-first prototype for tracking the AI governance window. Companion to the governance writing at Systems of Thought.

---

## Where to Start

**If you want the conceptual frame first:** Read [THEORY.md](https://github.com/jediwright/seam-stack/blob/main/THEORY.md) in the seam-stack repo (~650 words, no assumed domain knowledge), then the [Full Personhood essay](https://systemsofthought.com) for the full argument.

**If you want to see the architecture run:** Start with [PC#7 in local-first-series](https://github.com/jediwright/local-first-series/blob/main/pattern-commons/pattern-commons-07-employment-seam-v0-5.md) for the spec, then the [employment-seam repo](https://github.com/jediwright/employment-seam) for the implementation.

**If you're interested in the governance methodology:** [governed-pr-framework](https://github.com/jediwright/governed-pr-framework) is the most portable piece — usable independently of the rest of this work.

---

## Stack

TypeScript · Automerge · Keyhive · AT Protocol · Vitest · MIT licensed throughout

Active research. Work in progress.

---

*Systems of Thought is the writing and research practice behind this work: [systemsofthought.com](https://systemsofthought.com) | UX Minds, LLC*
