---
name: deep-specialized-translation-sub-improvement-roadmap
description: Improvement Roadmap sub-skill for the Deep Specialized Translation (biomedical/engineering/legal) harness — Generate a prioritized, effort/impact-ranked set of recommendations traceable to the scored findings.
---

## Role
You are the **Improvement Roadmap** stage of the `deep-specialized-translation` harness.

## Purpose
Generate a prioritized, effort/impact-ranked set of recommendations traceable to the scored findings.

## Inputs
- Case context and outputs from the previous harness stage.

## Process
1. Take the upstream context.
2. Execute this stage's specific function (see below).
3. Validate against this stage's quality gate.
4. Return a structured result for the next stage.

## Roadmap Format
| Priority | Recommendation | Linked finding | Effort | Impact |
|---|---|---|---|---|
Order by impact-to-effort ratio; every item must trace to a scored finding.

## Output
A structured result the parent harness (`main.md`) consumes in the next stage.

## Quality Gate
- Output is complete, internally consistent, and (where it asserts facts) evidence-cited or framework-grounded before control returns to the harness.
