# Deep Specialized Translation Agent Skill

<div align="center">

**🌍 Preserving Context & Exact Terminology Across Biomedical, Engineering & Legal Domains**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-green.svg)](https://www.python.org/downloads/)
[![Production Ready](https://img.shields.io/badge/status-production--ready-success.svg)](https://github.com/dungnotnull/deep-specialized-translation-agent-skill)
[![Open Source](https://img.shields.io/badge/open--source-brightgreen.svg)](https://github.com/dungnotnull/deep-specialized-translation-agent-skill)

*A research-grounded translation quality evaluation framework using MQM, TAUS DQF, ISO standards*

</div>

---

## 📋 Table of Contents

- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Key Features](#key-features)
- [Supported Frameworks](#supported-frameworks)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Scoring Model](#scoring-model)
- [Quality Gates](#quality-gates)
- [Knowledge Base](#knowledge-base)
- [Development](#development)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

**Deep Specialized Translation** is a production-grade AI agent skill that performs and evaluates domain-specific translation with rigorous quality metrics. Designed for biomedical, engineering, and legal domains where terminology fidelity is critical, this skill combines world-renowned evaluation frameworks with automated quality assessment.

### What Makes It Different?

Unlike generic translation tools, this skill:
- ✅ **Enforces terminology fidelity** using authoritative domain termbases
- ✅ **Scores quality** using MQM (Multidimensional Quality Metrics)
- ✅ **Applies ISO standards** (17100, 18587) for professional workflows
- ✅ **Preserves legal/medical register** and domain conventions
- ✅ **Flags ambiguities** that could cause safety/legal issues
- ✅ **Generates improvement roadmaps** with effort/impact prioritization

### Target Users

- **Medical translators** ensuring drug leaflet accuracy
- **Legal professionals** maintaining contract meaning across languages
- **Engineering teams** verifying technical manual consistency
- **Translation QA teams** implementing MT post-editing workflows
- **Regulatory compliance officers** validating translated documentation

---

## Problem Statement

Specialized translation fails when terminology, register, and context are not preserved, causing:

| Domain | Risk Level | Example Consequence |
|--------|------------|---------------------|
| **Medical** | 🔴 Critical | Incorrect dosage information in drug leaflets → patient harm |
| **Legal** | 🔴 Critical | Misinterpreted contract clauses → litigation losses |
| **Engineering** | 🟠 High | Inconsistent technical terms → equipment failure |
| **Regulatory** | 🟠 High | Non-compliant documentation → approval delays |

Existing tools lack:
1. Domain-specific terminology enforcement
2. Rigorous quality metrics with citable frameworks
3. Register preservation for specialized texts
4. Standardized error typology for reliable assessment

This skill addresses these gaps with research-backed, standards-grounded evaluation.

---

## Key Features

### 🔍 Comprehensive Translation Evaluation

- **Multi-dimensional scoring** across 5 quality dimensions
- **Cited evidence** for every assessment point
- **Framework-grounded** evaluation using MQM, TAUS DQF, ISO standards
- **Terminology consistency** checking against authoritative sources

### 🌐 Authoritative Knowledge Integration

- **IATE** (EU InterActive Terminology) for legal/medical terms
- **MQM framework** for standardized error typology
- **TAUS DQF** for dynamic quality assessment
- **ISO 17100/18587** compliance verification
- **Automatic metrics** (BLEU, COMET, chrF) for MT evaluation

### 🛡️ Safety & Compliance

- **Ambiguity flagging** for potentially mistranslated critical terms
- **Legal register preservation** for contracts and regulations
- **Medical terminology enforcement** using pharma standards
- **Unit/citation formatting** for locale compliance

### 📊 Professional Deliverables

- **Executive summary** with overall quality grade
- **Dimension-by-dimension scores** with evidence citations
- **Improvement roadmap** prioritized by effort/impact
- **Limitations disclosure** with certainty assessment

---

## Supported Frameworks

### MQM (Multidimensional Quality Metrics)

> **Standard:** ISO DIS 5060:2024, ASTM WK46396
> 
> **Source:** [themqm.org](https://themqm.org/)

A framework for analytic Translation Quality Evaluation (TQE) generating structured data to reduce subjectivity. MQM provides:
- 100+ translation issue types with varying granularity
- Standardized error typology and scoring models
- Root cause analysis and quality improvement capabilities

### TAUS DQF (Dynamic Quality Framework)

> **Developer:** TAUS (Translation Automation User Society)
> 
> **Source:** [taus.net](https://www.taus.net/)

A comprehensive suite for both human and machine translation quality evaluation:
- Content profiling and evaluation tools
- Rich knowledge base of quality evaluation resources
- Harmonization potential with MQM frameworks

### ISO Standards

| Standard | Focus | Requirements |
|----------|-------|--------------|
| **ISO 17100:2015** | Translation services | Qualified translators, independent revision, quality control |
| **ISO 18587:2017** | MT post-editing | Professional control standards for MT output processing |

### Automatic MT Metrics

| Metric | Type | Use Case |
|--------|------|----------|
| **BLEU** | N-gram overlap | Historical standard for MT evaluation |
| **COMET** | Neural-based | State-of-the-art for LLM-based MT |
| **chrF++** | Character-level | Better correlation for morphologically rich languages |
| **TER** | Edit distance | Complementary error counting |

---

## Architecture

### Harness Flow

```
┌─────────────────────────────────────────────────────────────────┐
│                  Deep Specialized Translation                  │
│                     (skills/main.md)                            │
└─────────────────────────────────────────────────────────────────┘
                              │
         ┌────────────────────┼────────────────────┐
         │                    │                    │
         ▼                    ▼                    ▼
┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐
│  sub-intake     │  │  sub-framework  │  │   Research      │
│  & Context      │→ │  Selector       │→ │   (WebSearch)   │
│  Gathering      │  │                 │  │   + Knowledge   │
└─────────────────┘  └─────────────────┘  │   Base          │
                                         └─────────────────┘
                                                    │
         ┌──────────────────────────────────────────┘
         │
         ▼
┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐
│  sub-scoring    │→ │   Challenge     │→ │  sub-improve-   │
│  Engine         │  │   (Devil's      │  │  ment-roadmap   │
│                 │  │    Advocate)    │  │                 │
└─────────────────┘  └─────────────────┘  └─────────────────┘
         │                    │                    │
         └────────────────────┼────────────────────┘
                              │
                              ▼
                    ┌─────────────────┐
                    │   Synthesize    │
                    │   + Quality     │
                    │   Gates         │
                    └─────────────────┘
```

### Sub-Skills

| Sub-Skill | Purpose | Output |
|-----------|---------|--------|
| **sub-intake** | Gather inputs, scope, goals | Structured context for downstream stages |
| **sub-framework-selector** | Choose appropriate evaluation framework(s) | Justified framework selection with rationale |
| **sub-scoring-engine** | Apply multi-dimensional rubric with citations | Weighted scores per dimension with evidence |
| **sub-improvement-roadmap** | Generate prioritized recommendations | Effort/impact-ranked action items |

### Knowledge Pipeline

```
┌─────────────────────────────────────────────────────────────────┐
│            SECOND-KNOWLEDGE-BRAIN.md (Self-Improving)           │
│                                                                 │
│  • MQM framework definitions                                    │
│  • TAUS DQF specifications                                     │
│  • ISO standard requirements                                   │
│  • IATE terminology database references                        │
│  • Automatic metrics explanations                              │
│  • Research papers with citations                              │
│                                                                 │
│  Updated weekly via: tools/knowledge_updater.py               │
└─────────────────────────────────────────────────────────────────┘
```

---

## Installation

### Prerequisites

- Python 3.8 or higher
- Claude Code with Skill support
- (Optional) crawl4ai for automatic knowledge base updates

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/dungnotnull/deep-specialized-translation-agent-skill.git
   cd deep-specialized-translation-agent-skill
   ```

2. **Install dependencies (for knowledge pipeline):**
   ```bash
   pip install -r requirements.txt
   ```

3. **Verify installation:**
   ```bash
   python -c "import skills.main; print('✅ Skill loaded successfully')"
   ```

### Optional: Automatic Knowledge Updates

To enable weekly knowledge base updates:

```bash
# Install crawl4ai
pip install crawl4ai

# Test the pipeline
python tools/knowledge_updater.py --dry-run

# Add to cron (weekly)
0 2 * * 0 cd /path/to/skill && python tools/knowledge_updater.py >> logs/knowledge.log 2>&1
```

---

## Usage

### Basic Translation Evaluation

```
User: "Translate this drug leaflet EN→VI accurately"

Skill Response:
✅ Translation complete with quality assessment

## Executive Summary
Overall Grade: B (82/100)
✅ Terminology fidelity: 95% - Pharmaceutical terms consistent with IATE
⚠️  Accuracy preservation: 78% - 3 potential mistranslations flagged
✅ Register fit: 88% - Medical tone appropriately preserved
...

## Improvement Roadmap
| Priority | Recommendation | Effort | Impact |
|----------|---------------|--------|--------|
| 1 | Verify "contraindication" rendering | Low | High |
| 2 | Standardize dosage abbreviations | Medium | High |
```

### Terminology Consistency Check

```
User: "Is this engineering manual translation consistent?"

Skill Response:
🔍 Terminology Audit Complete

## Context & Scope
Framework: MQM (Multidimensional Quality Metrics) + ISO 30042 TBX
Source: Technical Manual Section 4.2-4.5
Target Language: German (DE)

## Dimension Scores
| Dimension | Score | Evidence |
|-----------|-------|----------|
| Terminology fidelity | 71% | 4 inconsistent renderings detected |
| Accuracy preservation | 92% | No mistranslations found |
...

## Inconsistent Terms
- "bearing housing": → Lagergehäuse (3), → Lagergehäuse (2)
- "seal": → Dichtung (4), → Dichtring (1)
```

### MT Post-Editing (ISO 18587)

```
User: "Post-edit this machine translation to ISO 18587"

Skill Response:
📝 MT Post-Edit Applied (ISO 18587:2017 Framework)

## Post-Edit Summary
Input: Machine Translation Output (DeepL)
Standard: ISO 18587 Full Post-Editing
Changes: 47 corrections applied

## Quality Before/After
| Metric | Before | After | Improvement |
|--------|--------|-------|-------------|
| Terminology | 68% | 94% | +26% |
| Accuracy | 74% | 96% | +22% |
| Fluency | 82% | 98% | +16% |
```

### Degraded Mode (Offline)

```
User: "Translate offline"

Skill Response:
⚠️  DEGRADED MODE: Working from local knowledge base only

Limitations:
- Cannot fetch latest term databases from IATE
- MQM definitions from cached version (2026-06-18)
- No real-time framework updates available

Translation proceeding with SECOND-KNOWLEDGE-BRAIN content...
```

---

## Scoring Model

### Dimensions & Weights

| Dimension | Weight | What It Assesses | Scoring Criteria |
|-----------|--------|------------------|-----------------|
| **Terminology fidelity** | 30% | Correct, consistent domain terms vs termbase | Percentage of terms matching authoritative sources |
| **Accuracy / meaning preservation** | 25% | No mistranslation/omission/addition | Semantic equivalence score with flagged discrepancies |
| **Register & style fit** | 15% | Domain register, tone, conventions | Appropriateness to domain (medical/legal/engineering) |
| **Fluency & grammar** | 15% | Target-language naturalness | Grammatical correctness and readability |
| **Locale & compliance conventions** | 15% | Units, citations, legal/medical formatting | Adherence to locale-specific standards |

### Grade Calculation

| Grade | Score Range | Description |
|-------|-------------|-------------|
| **A** | 90-100 | Professional quality, ready for delivery |
| **B** | 75-89 | Good quality with minor improvements needed |
| **C** | 60-74 | Fair quality requiring significant revision |
| **D** | 0-59 | Poor quality, major rework required |

### Example Calculation

```
Overall Score = (0.30 × Terminology) + (0.25 × Accuracy) + 
                (0.15 × Register) + (0.15 × Fluency) + 
                (0.15 × Locale)

Sample:
(0.30 × 95) + (0.25 × 78) + (0.15 × 88) + (0.15 × 92) + (0.15 × 85)
= 28.5 + 19.5 + 13.2 + 13.8 + 12.75
= 87.75 → Grade B
```

---

## Quality Gates

Every deliverable must pass these gates before final output:

| Gate | Requirement | Purpose |
|------|-------------|---------|
| **Evidence Citation** | Every score cites a source or framework | Ensures assessments are grounded, not subjective |
| **Challenge Completion** | Devil's advocate stage completed | Tests assumptions and grades certainty |
| **Roadmap Traceability** | All recommendations link to findings | Ensures actionable, justified improvements |
| **Limitations Disclosure** | Certainty and constraints stated | Transparent about evidence quality and scope |

---

## Knowledge Base

### Sources

The `SECOND-KNOWLEDGE-BRAIN.md` file aggregates knowledge from:

| Source | Type | Content | Update Frequency |
|--------|------|---------|------------------|
| **IATE** | Terminology | EU multilingual terminology database | Weekly |
| **MQM** | Framework | Error typology and scoring models | Weekly |
| **TAUS DQF** | Framework | Dynamic quality evaluation methods | Weekly |
| **ISO Standards** | Standards | 17100, 18587 requirements | Monthly |
| **ArXiv (cs.CL)** | Research | Latest computational linguistics papers | Weekly |
| **Domain sources** | Best practices | Medical, legal, engineering translation | Weekly |

### Auto-Update Pipeline

The `tools/knowledge_updater.py` script:
- Crawls authoritative sources for latest content
- Extracts papers, standards, and best practices
- Scores relevance to specialized translation domains
- Deduplicates by URL/DOI hash
- Appends timestamped entries to knowledge base

```bash
# Manual update
python tools/knowledge_updater.py

# Dry run to preview
python tools/knowledge_updater.py --dry-run

# Verbose mode
python tools/knowledge_updater.py --verbose
```

---

## Development

### Project Structure

```
deep-specialized-translation-agent-skill/
├── README.md                          # This file
├── CLAUDE.md                          # Project-level instructions
├── PROJECT-detail.md                  # Full technical specification
├── PROJECT-DEVELOPMENT-PHASE-TRACKING.md  # Phase completion status
├── SECOND-KNOWLEDGE-BRAIN.md          # Self-improving knowledge base
├── requirements.txt                    # Python dependencies
├── skills/
│   ├── main.md                        # Main harness
│   ├── sub-intake.md                  # Intake & Context Gathering
│   ├── sub-framework-selector.md      # Framework Selector
│   ├── sub-scoring-engine.md          # Scoring Engine
│   └── sub-improvement-roadmap.md     # Improvement Roadmap
├── tools/
│   └── knowledge_updater.py           # Knowledge base update pipeline
└── tests/
    └── test-scenarios.md              # Test scenarios (5 scenarios)
```

### Adding New Frameworks

To add a new evaluation framework:

1. **Add to `sub-framework-selector.md`:**
   ```markdown
   | New Framework | Role description |
   ```

2. **Document in `SECOND-KNOWLEDGE-BRAIN.md`:**
   ```markdown
   ### New Framework
   - **Source**: URL
   - **Purpose**: Description
   - **Key components**: Details
   ```

3. **Add test scenario in `tests/test-scenarios.md`**

### Extending the Knowledge Base

Manually add entries to `SECOND-KNOWLEDGE-BRAIN.md`:

```markdown
### Manual Entry YYYY-MM-DD
- YYYY-MM-DD — **Paper Title** (Venue, Year) [URL] relevance=0.XX <!--hash:XXXXXXXX-->
```

---

## Testing

### Test Scenarios

The `tests/test-scenarios.md` file includes 5 comprehensive scenarios:

1. **Medical Translation** — Drug leaflet EN→VI with terminology enforcement
2. **Terminology Audit** — Engineering manual consistency check
3. **Legal Register** — Contract clause meaning preservation
4. **MT Post-Edit** — ISO 18587 compliance verification
5. **Degraded Mode** — Offline fallback with local knowledge

### Running Tests

```bash
# Verify all files are present
find . -name "*.md" -o -name "*.py" | sort

# Test knowledge pipeline
python tools/knowledge_updater.py --dry-run --verbose

# Verify skill loading (in Claude Code)
/load skills/main.md
```

---

## Contributing

We welcome contributions! Areas of interest:

- **Additional frameworks** (e.g., DQF-MQM, LICS)
- **Domain expansions** (e.g., financial, scientific)
- **Language-specific optimizations**
- **Metric enhancements** (e.g., COMET variants)
- **Knowledge base expansions**

### Contribution Guidelines

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make changes with clear documentation
4. Ensure all quality gates pass
5. Submit a pull request with description

### Code Standards

- Follow existing code structure and formatting
- Add type hints for all Python functions
- Include docstrings explaining purpose and behavior
- Update relevant documentation files
- Test all changes against existing scenarios

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

### Attribution

When using this skill in academic or commercial work, please cite:

```bibtex
@software{deep_specialized_translation_2024,
  title={Deep Specialized Translation Agent Skill},
  author={Claude Code and Contributors},
  year={2024},
  url={https://github.com/dungnotull/deep-specialized-translation-agent-skill},
  license={MIT}
}
```

---

## Acknowledgments

Built upon the excellent work of:

- **MQM Community** — [themqm.org](https://themqm.org/) for the Multidimensional Quality Metrics framework
- **TAUS** — [taus.net](https://www.taus.net/) for the Dynamic Quality Framework
- **ISO/TC 37** — For translation service standards (ISO 17100, ISO 18587)
- **IATE Team** — For the EU's multilingual terminology database
- **Research community** — For MT evaluation metrics (BLEU, COMET, chrF)

Special thanks to all contributors improving specialized translation quality worldwide.

---

## Contact

- **Issues**: [GitHub Issues](https://github.com/dungnotnull/deep-specialized-translation-agent-skill/issues)
- **Discussions**: [GitHub Discussions](https://github.com/dungnotnull/deep-specialized-translation-agent-skill/discussions)
- **Email**: [GitHub Contact](https://github.com/dungnotull)

---

<div align="center">

**⭐ Star this repo to help others discover specialized translation quality tools!**

Made with ❤️ by the global translation quality community

</div>
