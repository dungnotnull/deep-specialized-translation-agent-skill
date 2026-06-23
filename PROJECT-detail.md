# PROJECT-detail.md — Deep Specialized Translation (biomedical/engineering/legal) (Skill #148)

## Executive Summary
Performs and evaluates deep specialized translation preserving context and exact terminology, scored with MQM/DQF quality metrics. This skill is a full Claude harness in the **design-creative-media** cluster. It runs a research-first, framework-grounded workflow that scores the subject against named world-renowned methodologies and returns a prioritized improvement roadmap, while continuously updating its knowledge base.

## Problem Statement
Specialized translation fails when terminology, register, and context are not preserved, causing safety, legal, or technical errors. This skill produces and scores domain translation with rigorous quality metrics.

## Target Users & Use Cases
Practitioners, reviewers, and decision-makers who need an expert-grade, evidence-based assessment in this domain. Trigger examples:
1. **Medical translation** — User: "Translate this drug leaflet EN->VI accurately" → Skill translates, enforces pharma terminology, scores with MQM, flags risky ambiguities.
2. **Terminology audit** — User: "Is this engineering manual translation consistent?" → Skill checks termbase consistency, flags inconsistent renderings, MQM score.
3. **Legal register** — User: "Translate this contract clause keeping legal meaning" → Skill preserves legal register/terms, flags untranslatable concepts, notes.
4. **MT post-edit** — User: "Post-edit this machine translation to ISO 18587" → Skill applies post-editing levels, fixes errors, scores residual quality.
5. **Degraded mode** — User: "Translate offline" → Falls back to SECOND-KNOWLEDGE-BRAIN glossaries, signals it can't fetch latest term databases.

## Harness Architecture
```
/deep-specialized-translation (main.md)
   ├── sub-intake .................... gather inputs & scope
   ├── sub-framework-selector ........ choose world-renowned framework(s)
   ├── [research] WebSearch/WebFetch + SECOND-KNOWLEDGE-BRAIN
   ├── sub-scoring-engine ............ multi-dimensional weighted scoring
   ├── [challenge] devil's-advocate assumption review
   ├── sub-improvement-roadmap ....... prioritized effort/impact actions
   └── synthesize ................... professional deliverable + quality gates
```

## Full Sub-Skill Catalog
### sub-intake — Intake & Context Gathering
- **Purpose:** Collect the structured inputs, scope, and goals needed to run the analysis; ask clarifying questions when key facts are missing.
- **Inputs:** case context from prior stage.
- **Outputs:** structured result passed to the next stage.
- **Tools:** Read, WebSearch/WebFetch (as needed).
- **Quality gate:** output is complete, evidence-cited, and consistent with frameworks before proceeding.

### sub-framework-selector — Evaluation Framework Selector
- **Purpose:** Pick the most appropriate named world-renowned framework(s) for the case and justify the choice.
- **Inputs:** case context from prior stage.
- **Outputs:** structured result passed to the next stage.
- **Tools:** Read, WebSearch/WebFetch (as needed).
- **Quality gate:** output is complete, evidence-cited, and consistent with frameworks before proceeding.

### sub-scoring-engine — Scoring Engine
- **Purpose:** Apply the multi-dimensional rubric to produce weighted scores with evidence citations for each dimension.
- **Inputs:** case context from prior stage.
- **Outputs:** structured result passed to the next stage.
- **Tools:** Read, WebSearch/WebFetch (as needed).
- **Quality gate:** output is complete, evidence-cited, and consistent with frameworks before proceeding.

### sub-improvement-roadmap — Improvement Roadmap
- **Purpose:** Generate a prioritized, effort/impact-ranked set of recommendations traceable to the scored findings.
- **Inputs:** case context from prior stage.
- **Outputs:** structured result passed to the next stage.
- **Tools:** Read, WebSearch/WebFetch (as needed).
- **Quality gate:** output is complete, evidence-cited, and consistent with frameworks before proceeding.


## Evaluation Frameworks (World-Renowned, Citable)
| Framework / Standard | Role in this skill |
|---|---|
| MQM (Multidimensional Quality Metrics) | Standardized translation error typology and scoring. |
| TAUS DQF | Dynamic Quality Framework for translation evaluation. |
| ISO 17100 & ISO 18587 | Translation-service and MT post-editing requirements. |
| Terminology management (ISO 30042 TBX) | Termbase consistency and glossary control. |
| Automatic metrics (BLEU/COMET/chrF) | Reference- and model-based MT quality signals. |

## Scoring Model
| Dimension | Weight | What is assessed |
|---|---|---|
| Terminology fidelity | 30% | correct, consistent domain terms vs termbase |
| Accuracy / meaning preservation | 25% | no mistranslation/omission/addition |
| Register & style fit | 15% | domain register, tone, conventions |
| Fluency & grammar | 15% | target-language naturalness |
| Locale & compliance conventions | 15% | units, citations, legal/medical formatting |
Each dimension is scored 0-100 with cited evidence; the weighted total yields an overall grade (A: 90+, B: 75-89, C: 60-74, D: <60).

## Skill File Format Specification
- Frontmatter: `name`, `description`.
- Required sections: Role & Persona, Workflow (Harness Flow), Sub-skills Available, Tools, Output Format, Quality Gates.

## E2E Execution Flow
1. Parse user request; if inputs are insufficient, `sub-intake` asks targeted questions.
2. `sub-framework-selector` picks framework(s) and justifies the choice.
3. Research stage gathers highest-tier evidence (see evidence hierarchy); degrade gracefully to SECOND-KNOWLEDGE-BRAIN if offline.
4. `sub-scoring-engine` scores each dimension with citations.
5. Challenge stage stress-tests conclusions.
6. `sub-improvement-roadmap` produces ranked actions.
7. Synthesize deliverable; run Quality Gates; present.

**Error handling:** missing inputs → ask; conflicting evidence → present both and grade certainty; tool failure → fallback + explicit limitation notice.

## SECOND-KNOWLEDGE-BRAIN Integration
- Sources: https://themqm.org, https://www.taus.net, https://www.iso.org, https://iate.europa.eu
- ArXiv categories: cs.CL
- Crawl queries: translation quality MQM error typology; domain terminology management legal medical; LLM machine translation post-editing quality; COMET metric evaluation update
- Append format: dated entries with Title, Authors, Year, Venue, DOI/URL, key finding, relevance.

## Supporting Tools Spec
`tools/knowledge_updater.py`: inputs = source list + queries; outputs = appended SECOND-KNOWLEDGE-BRAIN entries; schedule = weekly cron; dedup by URL/DOI hash.

## Quality Gates (must all pass before final output)
- Every score cites at least one source or the chosen framework.
- Challenge stage completed; key assumptions tested.
- Roadmap items are prioritized by effort and impact and traceable to findings.
- Limitations and evidence certainty are stated explicitly.

## Test Scenarios
1. **Medical translation** — User: "Translate this drug leaflet EN->VI accurately" → Skill translates, enforces pharma terminology, scores with MQM, flags risky ambiguities.
2. **Terminology audit** — User: "Is this engineering manual translation consistent?" → Skill checks termbase consistency, flags inconsistent renderings, MQM score.
3. **Legal register** — User: "Translate this contract clause keeping legal meaning" → Skill preserves legal register/terms, flags untranslatable concepts, notes.
4. **MT post-edit** — User: "Post-edit this machine translation to ISO 18587" → Skill applies post-editing levels, fixes errors, scores residual quality.
5. **Degraded mode** — User: "Translate offline" → Falls back to SECOND-KNOWLEDGE-BRAIN glossaries, signals it can't fetch latest term databases.

## Key Design Decisions
1. Framework-grounded scoring (no ad-hoc criteria).
2. Research-first with graceful degradation to the local knowledge brain.
3. Mandatory challenge stage to counter confirmation bias.
4. Standard quality gates enforced before delivery.
5. Self-improving knowledge base via weekly crawl.
