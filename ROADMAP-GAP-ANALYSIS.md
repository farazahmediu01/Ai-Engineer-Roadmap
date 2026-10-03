# AI Engineer Roadmap — 3-Way Gap Analysis

**Prepared:** 2026-10-03 · **For:** Faraz Ahmed — Digital FTE Builder track / AI Educator, Aptech Institute

> ### ⚠️ Read this box before anything else
>
> `My-Current-Roadmap.md` **Standing Rule 6** says: *"No new strategy documents. This file is the last one. Amend it in place; never fork it."*
> **Benchmark P8** says: *"One new strategy document is a failure of this plan regardless of what else shipped."*
>
> **This file is not a strategy document and must not become one.** It is a transient review artifact. The correct end state is: fold §4 into `My-Current-Roadmap.md` in place, then **delete this file in the same session**. If `ROADMAP-GAP-ANALYSIS.md` is still in this repo at Week 26, P8 has failed and I helped it fail.

---

## 0. Sources

| # | Source | Status |
|---|--------|--------|
| **1** | `My-Current-Roadmap.md` — *Digital FTE Builder — Execution Guide v2*, 2026-08-27, 26 weeks (2026-08-31 → 2027-02-28) | ✅ Read in full (333 lines) |
| **2** | `images/*.webp` — "AI Engineer Learning Roadmap: 0 → Job Ready", 9 slides, watermarked **"Jean Lee"** | ✅ All 9 read |
| **3** | Agent Factory Roadmap — live curriculum tree via the Agent Factory System of Record | ✅ Full tree walked |

**Note on Source 2:** third-party LinkedIn carousel content. Fine as a benchmark. Not yours to ship — see §5.

---

## 1. Source 2 transcribed (the image roadmap)

| Slide | Stage | Content |
|-------|-------|---------|
| 00 | Cover | "AI Engineer Learning Roadmap — 0 → Job Ready" |
| 01 | **Build the Foundation** · Level 1 | Python fundamentals · Functions & OOP · File handling · APIs & JSON · Git & GitHub · SQL basics — *Tools:* Python, VS Code, Git, PostgreSQL |
| 02 | **Understand AI Fundamentals** | *Models:* neural networks · transformers · foundation models — *LLM concepts:* tokens · embeddings · context windows · temperature — *Limitations:* hallucinations · context limits · non-deterministic outputs |
| 03 | **Build with LLM APIs** | *APIs:* OpenAI · Anthropic · Gemini — *Prompting:* system prompts · few-shot — *Outputs:* JSON · structured outputs · Pydantic — *Advanced:* tool calling · streaming · multimodal |
| 04 | **Master RAG** | documents → chunking → embeddings → vector DB → retrieval → reranking → LLM response — *Learn:* vector search · metadata filtering · hybrid retrieval · RAG evaluation |
| 05 | **Build AI Agents** | *Anatomy:* model · tools · state · routing · guardrails — *Learn:* tool calling · agent loops · memory & state · human approval · MCP |
| 06 | **AI Backend Engineering** | FastAPI · PostgreSQL · Redis · asyncio · Docker — *Skills:* authentication · streaming · background jobs · rate limiting · error handling |
| 07 | **Evaluate Your AI System** | Output→accuracy+relevance · RAG→retrieval+faithfulness · Agents→tool+task success · Performance→latency+cost · Safety→injection+permissions — *Tools:* LangSmith · Ragas · Arize Phoenix · Promptfoo |
| 08 | **Ship to Production** | *Code:* testing · validation · error handling — *Deploy:* Docker · CI/CD · cloud hosting — *Reliability:* retries · fallbacks · rate limits — *Monitor:* logs · latency · token cost |

---

## 2. The 3-Way Comparison Matrix

✅ first-class · 🟡 present but thin, buried, deferred or Tier-2 · ❌ absent · ⬛ **deliberately and defensibly skipped** (S1 §7 only)

| # | Capability | **S1 — Execution Guide v2** | **S2 — Images** | **S3 — Agent Factory** |
|---|-----------|------------------------------|------------------|------------------------|
| 1 | Python & software basics | 🟡 assumed for self; Ch0 for students | ✅ Level 1 | ✅ *Python in the AI Era* |
| 2 | **Git mastery** | ✅ 20 min/day Phase 0–1 + **P2 timed, no-AI** | 🟡 one tile | ❌ assumed |
| 3 | **SQL / schema design** | ✅ 20 min/day Phase 2 + **P3 `EXPLAIN` benchmark** | 🟡 "SQL basics" | 🟡 inside pgvector |
| 4 | LLM internals (tokens, embeddings, context, temperature) | ❌ | ✅ Slide 02 | ✅ *What AI Actually Is* |
| 5 | LLM limitations (hallucination, non-determinism) | 🟡 implicit in eval design | ✅ Slide 02 | ✅ Foundations + *Governance* |
| 6 | Prompting as a discipline | ❌ | ✅ Slide 03 | ✅ *AI Prompting in 2026* · *AI Fluency* |
| 7 | Raw model API / loop by hand | 🟡 Tier 2 `claude-api-agentic-loops`; Ch1 teaching | ✅ Slide 03 | ✅ *The Loop by Hand* |
| 8 | Structured outputs / Pydantic | ✅ Ch3 + SDK | ✅ Slide 03 | ✅ *Structured Extraction Pipelines* |
| 9 | Streaming / multimodal | 🟡 SSE in FastAPI depth; multimodal ❌ | ✅ Slide 03 | 🟡 inside SDK courses |
| 10 | RAG pipeline | ✅ C28 pgvector, Phase 2 + L9 FileSearchTool | ✅ whole stage | ✅ *RAG on Postgres with pgvector* |
| 11 | Hybrid retrieval · reranking · metadata filtering | ❌ | ✅ Slide 04 | ✅ Phase 1 |
| 12 | Context engineering beyond RAG | 🟡 Ch5 + run compaction + Tier-2 `augmented-memory` | ❌ | ✅ *Building the Context Layer* |
| 13 | Agent anatomy (model/tools/state/routing/guardrails) | ✅ Phase 1, 4 weeks | ✅ Slide 05 | ✅ *Build AI Agents* |
| 14 | OpenAI Agents SDK | ✅ L4–L10 + capstone | 🟡 unnamed | ✅ Phase 2 |
| 15 | Claude Agent SDK / Agents Kit | 🟡 Tier 2, gated behind Phase 1 capstone | ❌ | ✅ *Claude Agent SDK* · *Managed Agents* |
| 16 | Memory / sessions / state | ✅ `SQLiteSession` + Ch4 | ✅ Slide 05 | ✅ Phase 2 |
| 17 | **MCP — consuming** | ✅ L8 + `mcp-fundamentals` | 🟡 one tile | ✅ *Skills & Connectors* |
| 18 | **MCP — authoring a server** | ✅ `custom-mcp-servers` + **P4** + published server | ❌ | ✅ *Connector-Native Apps* |
| 19 | Skills / plugins / reusable bundles | 🟡 Tier 2 `agent-skills-mcp-code-execution` | ❌ | ✅ *Plugins for AI Agents* |
| 20 | **Identity & agent access** (OAuth, scoped agent perms) | 🟡 JWT human auth only | 🟡 "Authentication" | ✅ *AI Identity* |
| 21 | Backend serving (FastAPI, async) | ✅ 14-section archive depth | ✅ Slide 06 | 🟡 inside deployment |
| 22 | Postgres / SQLModel / migrations | ✅ Phase 2 | ✅ Slide 06 | ✅ Phase 1 |
| 23 | Redis / caching | ⬛ **cut, reasoned** (§7.3) | ✅ Slide 06 | 🟡 |
| 24 | Background jobs / durable execution | ⬛ **deferred, reasoned** (Inngest, §7.2) | ✅ Slide 06 | ✅ *Nervous System* |
| 25 | **Evals & eval-driven development** | ✅✅ **Phase 0 *and* Phase 3** · 9-layer pyramid · golden dataset ≥50 · **P5 CI gate** | ✅ full stage | ✅ *Eval-Driven Development* |
| 26 | Eval tooling | ✅ DeepEval · Ragas · OpenAI Agent Evals · Phoenix | ✅ LangSmith · Ragas · Phoenix · Promptfoo | 🟡 multi-track |
| 27 | TDD / pytest | ✅ Phase 0 + `tdd-for-agents` | ✅ Slide 08 | ✅ inside EDD |
| 28 | Safety: injection · permissions · blast radius | 🟡 3 guardrail types ✅ · `needs_approval` ✅ · `production-security` Phase 4 — but **no injection module** | ✅ Slide 07 "Safety" | ✅ *Governance, Risk & Responsible Use* |
| 29 | Docker / CI-CD / cloud hosting | ✅ Phase 4, real stack | ✅ Slide 08 | ✅ *Deploy Your Agent Harness* |
| 30 | **Observability & cost** | ✅ OTel + App Insights + Phoenix on shared `run_id` | ✅ Slide 08 "Monitor" | ✅ inside deployment |
| 31 | Reliability (retries · fallbacks · rate limits) | 🟡 `multi-agent-reliability.md` only | ✅ Slide 08 | 🟡 |
| 32 | Spec-Driven Development | 🟡 spec-before-code in Phase 0 playbook; **not a module** | ❌ | ✅ the book's spine |
| 33 | Multi-agent orchestration & **architecture choice** | ✅ Phase 3 + **C42 decision tree**, Phase 5 | ❌ | ✅ *Choosing Agentic Architectures* |
| 34 | Human-agent teaming / HITL / agent UX | 🟡 `needs_approval` mechanism ✅ · ⬛ C35/C36 skipped | 🟡 "Human approval" | ✅ **2 courses** |
| 35 | Monetisation / payments | ⬛ **deferred, reasoned** (C43, §7.2) | ❌ | ✅ *Payment-Enabled Agents* |
| 36 | Positioning / selling / getting paid | 🟡 Phase 5 resume + LinkedIn + roles page | ❌ | ✅ *How to Get Paid* · *How to Sell* |
| 37 | Certification | ✅ **CCA-F**, Phase 5, named and scheduled | ❌ | ✅ Certifications track |
| 38 | **Proof-of-mastery benchmarks** | ✅✅ **P1–P8, binary, dated, no partial credit** | ❌ | 🟡 certifications |
| 39 | **Teaching / cohort delivery model** | ✅✅ **PRIMM template, 78 sessions, S1–S4 benchmarks** | ❌ | ❌ |

**Tally** — S1: ✅ 19 · 🟡 12 · ⬛ 4 · ❌ 4 — S2: ✅ 19 · 🟡 6 · ❌ 14 — S3: ✅ 27 · 🟡 8 · ❌ 4

---

## 3. Gap Analysis

### 3.1 Alignment verdict

| Pair | Alignment | Read |
|------|-----------|------|
| S1 ↔ S2 | **~70%** | S1 covers almost everything S2 covers, and goes deeper on every shared item. S2 is ahead on exactly three things: LLM fundamentals, prompting, and retrieval technique depth. |
| S1 ↔ S3 | **~80%** | Same book, same lifecycle, same primary role. S1's divergences are documented decisions in §7, not oversights. |
| S2 ↔ S3 | **~60%** | S2 is a 2025-era "AI engineer" ladder; S3 is a 2026 "agent manufacturer" ladder. Same stack, different destination. |

**Headline: your roadmap is stronger than the benchmark you are measuring it against.** On evals, MCP authoring, proof benchmarks, teaching model and cost engineering, S1 beats S2 outright. The gaps that remain are narrow and specific — which is why they are worth naming precisely.

### 3.2 The one structural contradiction that matters

**`CLAUDE.md §3` is a second roadmap, and your own rule says one of them is wrong.**

`My-Current-Roadmap.md` opens with: *"This is the only roadmap file. If a second one appears, one of them is wrong."* Then `CLAUDE.md §3` contains **"My Current Roadmap (Part 6 Execution Plan)"** — a six-step table running **Jun 15 2026 → Jan 2027**, indexed by **Ch61–Ch90 chapter numbers that §3.1 of your own v2 declares dead**, and ending:

> *"Current position: Step 1 — Ch62 L4 (Handoffs & Message Filtering), started 2026-06-13."*

Every session you open loads that file. So every session you are told you are in a plan that was superseded on 2026-08-27, positioned at a lesson your real plan schedules for Phase 1, and dated to the exact day v2 §5 flags as *"an open loop since 2026-06-13."* It also still carries the old Standing Rule 5 wording (*"Tests start now, not Step 4"*) against a Step 4 that no longer exists, and a skills table that pre-dates Phase 0.

This is not a cosmetic duplication — it is the failure mode v1 died of, reproduced inside the file that boots every session. **Ten-minute fix, highest leverage item in this document.** See U1.

### 3.3 Genuine gaps (present in ≥2 sources, absent or thin in S1 — *excluding* reasoned skips)

| # | Gap | Evidence | Severity |
|---|-----|----------|----------|
| **G1** | **LLM internals** — tokens, embeddings, context windows, temperature, non-determinism | S2 slide 02 (whole stage) · S3 *What AI Actually Is* · S1 ❌ | **High — teaching-critical** |
| **G2** | **Prompting as engineering** — system prompts, few-shot, structure | S2 slide 03 · S3 *AI Prompting in 2026* + *AI Fluency* · S1 ❌ | **High — teaching-critical** |
| **G3** | **Retrieval technique depth** — hybrid retrieval, reranking, metadata filtering | S2 slide 04 · S3 Phase 1 · S1 has pgvector plumbing but not retrieval *quality* | Medium |
| **G4** | **Prompt injection as its own topic** — you teach three guardrail types and `needs_approval`, which is the *mechanism*; you never teach the *threat model* | S2 slide 07 "Safety: Injection + Permissions" · S3 *Governance, Risk* · S1 🟡 | **High — you are teaching students to give LLMs tools** |
| **G5** | **Agent identity & scoped access** — JWT authenticates a *human*; nothing covers what an agent is permitted to do on that human's behalf | S3 *AI Identity* (full course) · S2 "Authentication" · S1 🟡 | Medium-High — a Digital FTE acting for an employee is an identity problem first |
| **G6** | **Reliability patterns** — retries, fallbacks, timeouts, rate-limit handling | S2 slide 08 · S1 has only `multi-agent-reliability.md`; the durable-execution answer (Inngest) is deliberately deferred, leaving nothing in the interim | Medium |
| **G7** | **SDD as a taught module** — it is your stated differentiator and your `CLAUDE.md` mandates it, but in v2 it appears only as "write Ch6's spec before any code" in Phase 0 | S3's spine · S1 🟡 · S2 ❌ | Medium |
| **G8** | **The student curriculum past Ch6 is a reading list, not a curriculum** | §7 rule 7: *"Students past Ch6 read archive slugs through the PRIMM template."* Benchmark S3 expects ≥70% cohort cold-build at W16 | **High — see §5** |

### 3.4 Reasoned skips I am *not* calling gaps

§7 is the best-argued section of your document and I am not going to relitigate most of it. Redis (Postgres + indexes handle your load), K8s/Helm/Dapr (*the live book declines to teach them too*), Google ADK (a third framework fragments a consolidating base), GraphRAG, payment gateways, mobile — all correctly cut with stated reasons and re-entry conditions. Inngest is **deferred with a named trigger**, which is the right shape.

**One I want to push back on — C35 Human-Agent Teams.** You dismiss it as *"eight governance documents, no code."* That is accurate and it is the point. You already ship `needs_approval=True` in Phase 1 — the mechanism. What C35 supplies is the operating model around it: escalation paths, authority boundaries, what a human reviewer is actually accountable for. Two reasons to promote it from "skip" to "Phase 5 Reader track, 2 hours":

1. **It is your secondary target role.** `CLAUDE.md` lists Outcome Architect as Secondary — *"decides what a Worker should achieve, authors the spec"* — and flags your teaching background as the fit. C35 is that role's core text. Skipping it skips the role.
2. **It is what makes a Digital FTE sellable.** Phase 3 already requires *"confidence thresholds + escalation paths."* C35 is where escalation paths come from. You have scheduled the deliverable and skipped its source.

Cost: 2 hours in the Phase 5 Reader block, next to C42. Not a phase, not a build.

---

## 4. Recommendations

### 4.1 PRESERVE — do not touch

| Keep | Why |
|------|-----|
| **Slug indexing over chapter numbers** (§3, §4.3 #1) | The single best architectural decision in the document. It is why v2 will survive the next renumber. |
| **Archive = depth · Live = currency · Ch0–6 = teaching** (§4) | A clean, defensible source-of-truth rule. Most curricula have none. |
| **Evals in Phase 0, Weeks 1–2** | Resolves v1's contradiction completely. Ahead of S2 (stage 7 of 8) and S3 (Phase 3). **This is now the strongest part of your plan.** |
| **P1–P8 binary benchmarks** | Neither S2 nor S3 has anything equivalent. "A deliberately degraded prompt gets caught by CI, not by you" is a better mastery gate than any certification. |
| **The PRIMM 2-hour template** | Reusable across 78 sessions, ~20 min prep, and *Predict* doubles as a free comprehension metric. Genuinely excellent. |
| **MCP authoring as a first-class outcome + P4** | S2 reduces MCP to one tile. You publish a server a stranger can connect to. |
| **Explicit skip list with re-entry conditions** | Rarer and more valuable than the inclusion list. |
| **Git & SQL remediation, 20 min/day, no AI** | Honest about a real gap, and the no-AI constraint is correct. |
| **Standing Rule 6 + P8** | Keep enforcing them. Including against this file. |

### 4.2 UPDATE — in place, in `My-Current-Roadmap.md`

| # | Change | Where | Cost |
|---|--------|-------|------|
| **U1** | **Delete the roadmap table from `CLAUDE.md §3`** and replace it with a single pointer: *"Roadmap: see `My-Current-Roadmap.md`. Current phase: Phase 1 (Weeks 3–6)."* Also drop the dead skills table and the stale Standing Rule 5 wording. | `CLAUDE.md` | **10 min — do this first** |
| **U2** | **Add a dated position line** to `My-Current-Roadmap.md` §11, updated weekly: *"As of YYYY-MM-DD: Phase N, Week W."* One line, one source of truth, no second file. | §11 | 2 min/week |
| **U3** | Fold **G3 (hybrid retrieval, reranking, metadata filtering)** into Phase 2's C28 block as named sub-topics. Pure addition to an existing phase. | §5 Phase 2 | +2 h |
| **U4** | Promote **G4 (prompt injection threat model)** into Phase 1 next to the guardrail work — you are already writing three guardrail types; teach *what they defend against* in the same sitting. | §5 Phase 1 | +1.5 h |
| **U5** | Add **G5 (agent identity / scoped access)** to Phase 2 alongside JWT. S3's `ai-identity-crash-course` is the source. | §5 Phase 2 | +2 h |
| **U6** | Add **G6 (retries, fallbacks, timeouts, rate limits)** as an explicit Phase 4 line item under `production-security`. | §5 Phase 4 | +1.5 h |
| **U7** | Move **C35 Human-Agent Teams** from §7.2 skip → Phase 5 Reader track, next to C42. See §3.4. | §5 Phase 5, §7.2 | +2 h |
| **U8** | Name **SDD** as a standing practice in §9, not just a Phase 0 playbook step: *"Rule 9 — spec before code, every phase."* Zero hours; it formalises what you already do. | §9 | 0 h |
| **U9** | Resolve the **Ch7–12 vs Ch0–6 contradiction** flagged inside your own Rule 7. Pick 6. Fix `README.md` and the counselling notes in one edit. | external | 20 min |

**Net: ~+9 hours across 26 weeks**, all inside existing phases, no phase boundary or date moves. §5's shape is unchanged.

### 4.3 INSERT — one new module, student track only

Everything above is an amendment. This is the only genuine insertion, and it is for the **cohort**, not for you:

> **Ch-0.5 · "How the Model Actually Works"** — 2 class sessions, slotted between Ch0 (Python for Agents) and Ch1 (The Agent Loop).
> **Covers:** tokens · embeddings · context windows · temperature · why the same prompt returns different JSON twice · hallucination as a property, not a bug · system prompts and few-shot as structure, not magic words.
> **Closes:** G1 + G2.
> **Why it must exist:** this is the only capability where *both* benchmarks beat you, and it is the one students cannot derive by building. Everything else in your curriculum is learnable from an artifact. This is not — and without it, "Predict" in the PRIMM loop degrades from a comprehension score into a guessing game, because students have no model of the machine to predict *from*. It is load-bearing for your own teaching instrument.
> **Cost:** 2 sessions of the 78. Prep fits the existing ~20-min template.

### 4.4 Student sequence after the amendment

```
Ch0    Python for Agents
Ch0.5  How the Model Actually Works ........... NEW — tokens · embeddings · context · temperature · prompting
Ch1    The Agent Loop
Ch2    Typed Tools
Ch3    Structured Outputs
Ch4    Sessions & State
Ch5    The Context Window
Ch6    Evals ................................... Core track graduates ~W16
───────────────────────────────────────────────  authoring stops here (Rule 7)
Specialist extension: archive slugs via PRIMM — handoffs · guardrails · MCP · observability
```

---

## 5. Honest Mentor Advice

First, the correction I owe you: I drafted this review against the roadmap table in `CLAUDE.md §3` before you pushed the real file, and half of what I had written was wrong. v2 is a genuinely strong document — better than the carousel you are benchmarking against on evals, MCP authoring, cost engineering, proof benchmarks and teaching model, and close to the Agent Factory's own structure without being a copy of it. The slug-indexing decision and the §7 skip list with re-entry conditions are the work of someone who has learned from a plan that died. **Your structure is not your problem.** Which means most of §4 above is small amendments, and you should treat it that way rather than as an invitation to re-plan.

So here is the thing I actually want you to act on. `My-Current-Roadmap.md` says *"This is the only roadmap file. If a second one appears, one of them is wrong."* The second one already exists — it is `CLAUDE.md §3`, it is indexed by the dead chapter numbers your own §3.1 buried, it runs to a January 2027 calendar you have replaced, and it ends with *"Current position: Step 1 — Ch62 L4, started 2026-06-13."* That file loads into **every single session**. So every session, your coaching system is briefed on the superseded plan and told you are standing exactly where v2 §5 says you have had an open loop since June. You wrote the rule and left the violation in the boot file. Ten minutes, highest leverage item on this page, do it before you do anything in §4.

Now the arithmetic, which is the part that should worry you. The plan runs 2026-08-31 → 2027-02-28 and you wrote **"There is no slack."** Today is **2026-10-03** — Week 5, Phase 1, Week 3 of 4. Phase 1's proof is a capstone passing its own validation checklist with handoffs, three guardrail types, sessions, hooks and `needs_approval` visible in Spendly, and Phase 1 is the loop that has been open since 2026-06-13 — now **sixteen weeks**. Phase 2 starts Oct 12 whether or not Phase 1 closed. Your plan has no mechanism for a late phase except §5's *"miss two sessions in a week → cut a Tier 2 item, never re-plan"* — which handles missing hours, not missing a phase. If Phase 1 is not closed by Oct 11, cut Tier 2 and start Phase 2 anyway; a four-week slip at Week 6 compounds into a missed Feb 2027, and the dates are the only thing holding this plan honest.

On the teaching side, one blind spot with your name on it. Your own `CLAUDE.md` calls 6+ years of teaching experience *"encoded domain expertise — the scarcest input in the agent era,"* and then Rule 7 stops authoring at Ch6 and sends students past it to *"read archive slugs through the PRIMM template."* That is a reading list with a worksheet stapled to it, and benchmark S3 asks ≥70% of that cohort to cold-build a working tool-using agent in a new domain, unaided, by Week 16. Those two things cannot both hold. Rule 7 is the right *economic* call — you cannot author twelve chapters and ship Spendly in 26 weeks — but then S3 is the wrong benchmark, or the cohort needs Ch7–12 in a cheaper form than full authored chapters. Pick one and write it down. And while you are in there: the one place both benchmarks genuinely beat you is the bottom rung — tokens, embeddings, context windows, temperature, prompting. You skip it because *you* do not need it, and your students will spend a year debugging by superstition without it. Ch0.5, two sessions, closes it.

Last thing, and I mean this literally. This file you are reading is a planning `.md`. Benchmark P8 counts them and says *"one new strategy document is a failure of this plan regardless of what else shipped."* Fold §4.2 into `My-Current-Roadmap.md`, make the ten-minute `CLAUDE.md` edit, and **delete this file in the same sitting**. The thing that killed v1 was not a bad plan. It was that planning feels like progress, and reviewing a roadmap feels like working on the roadmap. Your entry ticket from v1 is still unanswered — *why is Spendly's Intent Classifier → Expense Extractor currently orchestration, and what would change for the user if it became a true `handoff()`* — and answering it in code is worth more than everything above.

---

## Appendix — Verification notes

- `My-Current-Roadmap.md` read in full at commit `97c8113` ("Addd current Roadmap"), pulled mid-review.
- Agent Factory structure walked live: front matter → Getting Started (Foundations ×10, General Agents ×16, Personal Agent Harnesses, Mode 1, Mode 2) → Mode 2 Phases 1–3 (8 + 5 + 9 crash courses) → Certifications → Glossary. Course slugs cited in S1 §3.2 were confirmed present.
- Not verifiable from this repo: `resources/agent-factory/archived-wayback/` contents, `MANIFEST.tsv`, `CHAPTER_PLAYBOOK.md`, `RUNS.md`, `agentic-ai-from-scratch/`, and all `C:\` / `D:\` paths. Archive-side claims in §3.1 and §4 are taken as stated.
- Phase/week positions computed from the stated start date 2026-08-31 against today, 2026-10-03.
