# LMCRep — Language Model Corpus Research Replaceability

> A multi-model evaluation framework assessing the degree to which state-of-the-art language models can replace human researchers in corpus linguistics tasks.

---

## Overview

**LMCRep** provides a structured, fine-grained dataset that scores the *replaceability* of human corpus linguists by large language models (LLMs) across a comprehensive taxonomy of corpus research tasks. Each task is evaluated along multiple dimensions — from how deterministic the task is to how much interpretive judgement it demands — producing a rich profile of where AI can already substitute human effort and where fundamental barriers remain.

The dataset covers **50+ corpus linguistics tasks** drawn from well-established sub-fields and is scored independently by multiple frontier LLMs, enabling cross-model comparison and ensemble aggregation.

---

## Repository Structure

```
LMCRep/
├── data/
│   ├── Claude Opus 4.7 Thinking.csv     # Scores from Claude Opus 4.7 (extended thinking)
│   ├── GPT-5.4 Thinking.csv             # Scores from GPT-5.4 (extended thinking)
│   ├── GPT-5.5 Thinking.csv             # Scores from GPT-5.5 (extended thinking)
│   ├── Gemini 3.1 Pro Thinking.csv      # Scores from Gemini 3.1 Pro (extended thinking)
│   ├── Kimi K2.6 Thinking.csv           # Scores from Kimi K2.6 (extended thinking)
│   ├── Nemotron 3 Super.csv             # Scores from NVIDIA Nemotron 3 Super
│   ├── Sonar-Pro.csv                    # Scores from Perplexity Sonar-Pro
│   └── Model Council.csv                # Ensemble / aggregated scores across all models
└── ai_replaceability_full.html          # Interactive visualisation of replaceability results
```

---

## Task Coverage

Tasks are organised into the following research areas:

| Research Area | Example Tasks |
|---|---|
| Keyword Analysis | Log-likelihood keyword extraction, BIC-based keyword ranking, diachronic keyword comparison |
| Collocation Analysis | MI-based collocation, Log-Dice ranking, asymmetric window collocation |
| Dispersion & Distribution | DP-based dispersion (Gries), Juilland's D, frequency–dispersion trade-off mapping |
| Corpus-Based Grammar / Pattern | CQL/CQP concordance search, SVO dependency parsing, constructional frequency profiling |
| Corpus-Assisted Discourse Studies | Semantic prosody assessment, discourse preference profiling |
| Learner Corpus | Overuse/underuse analysis, error-tagged frequency profiling |
| Corpus Stylistics | Burrows's Delta authorship attribution, foregrounding frequency profiling |
| Diachronic / Historical Corpus | COHA/COCA frequency trajectories, semantic change detection |
| Multi-Dimensional Analysis | Biber-style factor scores, register comparison via MD dimensions |
| Corpus Phonology / Spoken Corpus | Filled pause profiling, turn-taking pattern analysis |
| Sentiment / Stance Corpus | LIWC-based sentiment, epistemic stance marker comparison |
| Phraseology | Lexical bundle extraction (Biber-style), phraseological frame profiling |
| Collostructional Analysis | Collexeme analysis, distinctive collexeme analysis |
| Corpus-Based Cognitive Linguistics | Behavioural profile analysis |
| Forensic Linguistics | Idiolectal style marker profiling |
| Corpus Pragmatics | Speech-act frequency profiling |
| Corpus-Based Sociolinguistics | Variationist analysis with mixed-effects modelling |
| Historical Corpus Linguistics | Spelling-variant normalisation (VARD) |
| Corpus Phonetics | Forced-alignment duration analysis (MFA) |
| Child Language Corpora | MLU and morpheme-emergence profiling (CHILDES) |
| Language Testing / Assessment | CEFR-aligned lexical profiling (TAALES) |
| Terminology Extraction | C-value / NC-value automatic term extraction |
| Corpus-Based Metaphor Studies | MIPVU metaphor identification |
| Computational Corpus Exploration | LDA topic modelling |
| Keyness Meta-Analysis | Log Ratio / %DIFF effect-size analysis |

---

## Scoring Schema

Every task–model pair is rated across **13 dimensions** on a 1–10 scale:

| Dimension | Description |
|---|---|
| **Human Feasibility** | How readily a skilled human researcher can execute the task |
| **Research Significance** | Importance of the task to the broader corpus linguistics field |
| **Current AI Replaceability** | How well current AI can perform or replicate the task |
| **AI Replaceability in 10 Years** | Expected replaceability within a decade |
| **Theoretical Maximum AI Replaceability** | Upper bound given any technological advances |
| **Specification Extractability** | Ease of formalising task parameters from published prose |
| **Parameter Explicitness** | How explicitly parameters are reported in publications |
| **Execution Determinism** | Whether outputs are reproducible given identical inputs |
| **Tool-chain Maturity** | Quality and availability of existing software support |
| **Interpretive Judgement Load** | Amount of qualitative human judgement required |
| **Evaluation / Ground-Truth Availability** | Availability of objective benchmarks or published comparators |
| **Robustness Tractability** | Feasibility of systematic sensitivity analysis |
| **Verification Cost** | Effort required to audit or validate outputs |

Each score is accompanied by a plain-language explanation column (e.g., `Current AI Replaceability — Explanation`).

---

## Models Evaluated

| Model | File |
|---|---|
| Claude Opus 4.7 (Thinking) | `Claude Opus 4.7 Thinking.csv` |
| GPT-5.4 (Thinking) | `GPT-5.4 Thinking.csv` |
| GPT-5.5 (Thinking) | `GPT-5.5 Thinking.csv` |
| Gemini 3.1 Pro (Thinking) | `Gemini 3.1 Pro Thinking.csv` |
| Kimi K2.6 (Thinking) | `Kimi K2.6 Thinking.csv` |
| Nemotron 3 Super | `Nemotron 3 Super.csv` |
| Sonar-Pro | `Sonar-Pro.csv` |
| **Model Council** (ensemble) | `Model Council.csv` |

---

## Interactive Visualisation

The file [`ai_replaceability_full.html`](./ai_replaceability_full.html) provides an interactive browser-based dashboard for exploring replaceability scores across tasks, models, and research areas. Open it locally in any modern web browser — no server or installation required.

---

## Key Findings (Highlights)

- **Highest replaceability**: Purely algorithmic tasks such as CQL concordance search, MI-based collocation, lexical bundle extraction, TTR/MTLD computation, and LIWC-based sentiment analysis score at or near **10/10** for current AI replaceability across all models.
- **Lowest replaceability**: Tasks requiring deep interpretive or qualitative judgement — including MIPVU metaphor identification, semantic prosody assessment, and speech-act frequency profiling — cluster at **4–5/10** for current AI, with theoretical maximums capped by inherent subjectivity.
- **10-year horizon**: Nearly all tasks converge toward **9–10/10** replaceability within a decade, with the notable exception of tasks involving unresolvable human interpretive judgement (e.g., prosody, pragmatics, metaphor).
- **Model Council consensus**: The ensemble file (`Model Council.csv`) aggregates scores across all seven models, providing more stable and representative estimates than any single model alone.

---

## Citation

If you use this dataset or the associated visualisation in your research, please cite:

```
@misc{LMCRep2025,
  author    = {Huang, Weihang},
  title     = {LMCRep: Language Model Corpus Research Replaceability},
  year      = {2025},
  url       = {https://github.com/Weihang-Huang/LMCRep}
}
```

---

## Licence

Please refer to the repository owner for licensing terms.

---

## Contact

For questions, suggestions, or collaboration enquiries, please open a [GitHub Issue](https://github.com/Weihang-Huang/LMCRep/issues) or contact the repository maintainer directly via GitHub.
