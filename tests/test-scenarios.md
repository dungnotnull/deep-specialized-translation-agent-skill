# Test Scenarios — Deep Specialized Translation (biomedical/engineering/legal) (Skill #148)

These scenarios validate the harness end-to-end: stage order, framework grounding, scoring with citations, gates, roadmap, and graceful degradation. Minimum 5 scenarios.

### Scenario 1: Medical translation
- **User input:** "Translate this drug leaflet EN->VI accurately"
- **Expected behavior:** Skill translates, enforces pharma terminology, scores with MQM, flags risky ambiguities.
- **Pass criteria:** correct stage order; framework named; scores cited; roadmap prioritized; limitations stated.
### Scenario 2: Terminology audit
- **User input:** "Is this engineering manual translation consistent?"
- **Expected behavior:** Skill checks termbase consistency, flags inconsistent renderings, MQM score.
- **Pass criteria:** correct stage order; framework named; scores cited; roadmap prioritized; limitations stated.
### Scenario 3: Legal register
- **User input:** "Translate this contract clause keeping legal meaning"
- **Expected behavior:** Skill preserves legal register/terms, flags untranslatable concepts, notes.
- **Pass criteria:** correct stage order; framework named; scores cited; roadmap prioritized; limitations stated.
### Scenario 4: MT post-edit
- **User input:** "Post-edit this machine translation to ISO 18587"
- **Expected behavior:** Skill applies post-editing levels, fixes errors, scores residual quality.
- **Pass criteria:** correct stage order; framework named; scores cited; roadmap prioritized; limitations stated.
### Scenario 5: Degraded mode
- **User input:** "Translate offline"
- **Expected behavior:** Falls back to SECOND-KNOWLEDGE-BRAIN glossaries, signals it can't fetch latest term databases.
- **Pass criteria:** correct stage order; framework named; scores cited; roadmap prioritized; limitations stated.

## Regression Notes
- Add real user runs here as regression cases.
- Verify `tools/knowledge_updater.py` dry-run appends well-formed entries and dedups by URL/DOI hash.
