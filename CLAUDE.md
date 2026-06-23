# CLAUDE.md — Deep Specialized Translation (biomedical/engineering/legal) (Skill #148)

**Slug:** `deep-specialized-translation`  •  **Cluster:** `design-creative-media`  •  **Source idea:** 148  •  **Phase:** Built (v1)

## Tagline
Performs and evaluates deep specialized translation preserving context and exact terminology, scored with MQM/DQF quality metrics.

## Problem This Skill Solves
Specialized translation fails when terminology, register, and context are not preserved, causing safety, legal, or technical errors. This skill produces and scores domain translation with rigorous quality metrics.

## Harness Flow Summary
1. **Intake** (`sub-intake`) — gather structured inputs, scope, goals.
2. **Framework selection** (`sub-framework-selector`) — choose named world-renowned framework(s).
3. **Research** (WebSearch/WebFetch + SECOND-KNOWLEDGE-BRAIN) — gather highest-tier evidence.
4. **Scoring** (`sub-scoring-engine`) — multi-dimensional weighted scores with citations.
5. **Challenge** — devil's-advocate review of assumptions and weak evidence.
6. **Roadmap** (`sub-improvement-roadmap`) — prioritized effort/impact recommendations.
7. **Synthesize** — assemble the professional deliverable; pass Quality Gates.

## Gates
- No mandatory safety/compliance gate for this cluster, but the standard Quality Gates below still apply.

## Sub-skills
- `skills/sub-intake.md` — Intake & Context Gathering: Collect the structured inputs, scope, and goals needed to run the analysis; ask clarifying questions when key facts are missing.
- `skills/sub-framework-selector.md` — Evaluation Framework Selector: Pick the most appropriate named world-renowned framework(s) for the case and justify the choice.
- `skills/sub-scoring-engine.md` — Scoring Engine: Apply the multi-dimensional rubric to produce weighted scores with evidence citations for each dimension.
- `skills/sub-improvement-roadmap.md` — Improvement Roadmap: Generate a prioritized, effort/impact-ranked set of recommendations traceable to the scored findings.

## Tools Required
- `WebSearch`, `WebFetch` — live evidence and standards updates
- `Read`, `Write` — load knowledge base, emit deliverables
- `Bash` — run `tools/knowledge_updater.py`
- Skill tool — invoke sub-skills in sequence

## Knowledge Sources
- ArXiv: cs.CL
- Authoritative domain sources:
  - https://themqm.org
  - https://www.taus.net
  - https://www.iso.org
  - https://iate.europa.eu
- Crawl queries: translation quality MQM error typology; domain terminology management legal medical; LLM machine translation post-editing quality; COMET metric evaluation update

## Supporting Tools
- `tools/knowledge_updater.py` — crawl4ai pipeline that grows `SECOND-KNOWLEDGE-BRAIN.md` (weekly cron recommended).

## Active Development Tasks
- [x] Scaffold full deliverable set
- [x] Define 4 sub-skills
- [x] Expand SECOND-KNOWLEDGE-BRAIN with authoritative content
- [x] Implement production-grade knowledge pipeline
- [x] Complete all phases (0-5)
- [ ] Add regression cases from real user runs (ongoing)

## Related Root Docs
- `PROJECT-detail.md` — full technical spec
- `PROJECT-DEVELOPMENT-PHASE-TRACKING.md` — phase roadmap
- `SECOND-KNOWLEDGE-BRAIN.md` — self-improving knowledge base
