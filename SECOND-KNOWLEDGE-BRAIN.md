# SECOND-KNOWLEDGE-BRAIN.md — Deep Specialized Translation (biomedical/engineering/legal) (Skill #148)

> Self-improving domain knowledge base. Grown by `tools/knowledge_updater.py` (weekly cron). Newest evidence is preferred per the evidence hierarchy (Systematic Review > Meta-Analysis > RCT > Cohort > Expert Opinion > Blog).

## Core Concepts & Frameworks
- **MQM (Multidimensional Quality Metrics)** — Standardized translation error typology and scoring.
- **TAUS DQF** — Dynamic Quality Framework for translation evaluation.
- **ISO 17100 & ISO 18587** — Translation-service and MT post-editing requirements.
- **Terminology management (ISO 30042 TBX)** — Termbase consistency and glossary control.
- **Automatic metrics (BLEU/COMET/chrF)** — Reference- and model-based MT quality signals.

## Key Research Papers
| Title | Authors | Year | Venue | DOI/Link | Relevance |
|---|---|---|---|---|---|
| Multidimensional Quality Metrics (MQM): A Framework for Declaring and Describing Translation Quality Metrics | Lommel, A.; Melby, A.; et al. | 2013 | TC-2013 | [ACL Anthology](https://aclanthology.org/2013.tc-1.6.pdf) | foundational MQM framework defining shared vocabulary of issue types |
| Dynamic Quality Framework: quantifying and benchmarking quality | Görög, A. | 2017 | Tradumàtica | [UAB](https://revistes.uab.cat/tradumatica/article/download/n12-gorog2/pdf/370) | TAUS DQF methodology for standardizing translation quality evaluation |
| ISO 17100:2015 Translation services — Requirements for translation services | ISO/TC 37 | 2015 | ISO Standard | [ISO](https://www.iso.org/standard/59352.html) | International requirements for translation service providers |
| ISO 18587:2017 Translation services — Post-editing of machine translation output | ISO/TC 37 | 2017 | ISO Standard | [ISO](https://www.iso.org/standard/62970.html) | Requirements for full post-editing of MT output |
| COMET: A Neural Framework for Translation Evaluation | Rei, A.; et al. | 2020 | ACL | [arXiv:2010.12344](https://arxiv.org/abs/2010.12344) | State-of-the-art metric for MT evaluation using neural networks |
| chrF: character n-gram F-score for automatic MT evaluation | Popović, M. | 2015 | WMT | [ACL Anthology](https://aclanthology.org/W15-3049.pdf) | Character-level metric showing better correlation with human judgment |

## Framework Deep Dives

### MQM (Multidimensional Quality Metrics)
- **Standard**: ISO DIS 5060:2024, ASTM WK46396
- **Source**: https://themqm.org/
- **Core principle**: Framework for analytic Translation Quality Evaluation (TQE) generating structured data to reduce subjectivity
- **Application**: Human translation, machine translation, and AI-generated translation
- **Key components**: 
  - Master listing of 100+ translation issue types with varying granularity
  - Standardized error typology and scoring models
  - Enables root cause analysis and quality improvement
- **Benefits**: Enhanced comparability, improved stakeholder communication, data-driven process improvement

### TAUS DQF (Dynamic Quality Framework)
- **Developer**: TAUS (Translation Automation User Society)
- **Since**: 2011
- **Source**: https://www.taus.net/
- **Purpose**: Standardize translation quality evaluation through dynamic evaluation model
- **Features**:
  - Comprehensive suite for both human and machine translation
  - Content profiling and evaluation tools
  - Rich knowledge base of quality evaluation resources
  - Harmonization potential with MQM frameworks
  - Best practices error typology guidelines

### ISO Standards for Translation

#### ISO 17100:2015
- **Scope**: Requirements for translation service providers
- **Requirements**:
  - Qualified translators with proven competence
  - Independent revision process
  - Project management standards
  - Quality control procedures
  - Core processes, resources, and aspects for quality translation delivery
- **Target**: Language Service Providers (LSPs) and translation organizations

#### ISO 18587:2017
- **Scope**: Post-editing of machine translation output
- **Requirements**:
  - Framework for full post-editing when MT output must be accurate and usable
  - Professional control standards for MT post-editing
  - Process requirements distinct from human translation (ISO 17100)
- **Target**: Organizations incorporating MT into their workflows

### IATE (InterActive Terminology for Europe)
- **Operator**: European Union institutions
- **Since**: 2004 (project launched 1999)
- **Source**: https://iate.europa.eu/
- **Purpose**: EU's multilingual terminology management system
- **Coverage**: Law, environment, human rights, social questions, medicine, transport, agriculture, chemistry, intellectual property, data processing
- **Function**:
  - Collection, dissemination, and shared management of EU-specific terminology
  - Ensures quality of written communication across EU languages
  - Primary users: translators and linguists
- **Scale**: Web-based infrastructure harmonizing all EU terminology resources

### Automatic MT Evaluation Metrics

#### BLEU (Bilingual Evaluation Understudy)
- **Type**: N-gram-based string overlap metric
- **Function**: Compares MT output to single reference translation
- **Status**: Historical standard for MT evaluation
- **Limitations**: Weak correlation with human judgment on morphologically rich languages

#### COMET (Crosslingual Optimized Metric for Evaluation of Translation)
- **Type**: Neural network-based metric
- **Function**: Crosslingual evaluation using pretrained language models
- **Status**: State-of-the-art for LLM-based MT evaluation
- **Advantage**: Superior correlation with human judgments across language pairs

#### chrF / chrF++ (CHaRacter-level F-score)
- **Type**: Character n-gram F-score metric
- **Function**: Character-level precision and recall combined into F-score
- **Status**: Second most popular metric; better human correlation than BLEU
- **Advantage**: Particularly useful for morphologically complex languages

#### TER (Translation Error Rate)
- **Type**: Edit distance-based metric
- **Function**: Measures number of edits required to match reference
- **Use case**: Complementary to BLEU/chrF for error counting

## State-of-the-Art Methods & Tools
- Apply the frameworks above as the scoring backbone.
- Prefer primary standards documents and peer-reviewed sources over secondary blogs.
- Combine quantitative scoring with a qualitative challenge stage.

## Authoritative Data Sources
- https://themqm.org
- https://www.taus.net
- https://www.iso.org
- https://iate.europa.eu
- ArXiv: cs.CL

## Analytical Frameworks (Scoring Backbone)
| Framework / Standard | Role in this skill |
|---|---|
| MQM (Multidimensional Quality Metrics) | Standardized translation error typology and scoring. |
| TAUS DQF | Dynamic Quality Framework for translation evaluation. |
| ISO 17100 & ISO 18587 | Translation-service and MT post-editing requirements. |
| Terminology management (ISO 30042 TBX) | Termbase consistency and glossary control. |
| Automatic metrics (BLEU/COMET/chrF) | Reference- and model-based MT quality signals. |

## Self-Update Protocol (crawl4ai config)
- **Sources:** the authoritative URLs above + ArXiv categories.
- **Search queries:**
- `translation quality MQM error typology`
- `domain terminology management legal medical`
- `LLM machine translation post-editing quality`
- `COMET metric evaluation update`
- **Frequency:** weekly.
- **Append format:** dated section with Title, Authors, Year, Venue, DOI/URL, key finding, relevance note.
- **Dedup:** skip entries whose URL/DOI hash already exists.

## Knowledge Update Log
- 2026-06-18 — Knowledge base seeded at skill creation (frameworks + sources). First live crawl pending.
