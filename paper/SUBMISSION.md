# arXiv submission — copy-paste sheet

Upload **`paper/main.tex` only**. Do not upload the PDF or any `.aux`/`.log`
files. arXiv compiles the source itself.

---

## Title

```
Carve, Then Compose: Training-Free Domain Pruning and Recombination of Experts in Mixture-of-Experts LLMs
```

## Authors

```
Yash Sarwaiya
```

Affiliation field: `University of Florida`

## Abstract (plain text — paste as-is)

```
Expert pruning of Mixture-of-Experts (MoE) language models is believed to be safe only up to roughly 25% without retraining. We show that this ceiling is an artifact of demanding general capability, and that when only one domain must survive, an off-the-shelf fine-grained MoE tolerates far deeper cuts. On Qwen3-30B-A3B (128 experts/layer, top-8), a norm-aware contribution score computed from a teacher-forced prefill over only ~30 domain demonstrations retains 97% of baseline HumanEval pass@1 with 50% of routed experts removed, and 90% with 65% removed - while GSM8K collapses from 99.3% to 33.3%, confirming genuinely domain-targeted compression. A size-matched random control scores 26.8% HumanEval at the 50% ratio, an advantage of 62 points for informed selection. We further show that domain-pruned variants compose: the per-layer union of independently derived coding and math expert sets (52% of experts) scores within 1-2 points of the full model on both HumanEval (90.9%) and GSM8K (97.3%), while dropping 34 points on a non-STEM MMLU probe - a two-skill specialist assembled post hoc with no retraining. Composition holds for distant domain pairs (code-union-humanities: 84.1% HumanEval, 74.3% MMLU-humanities), whose keep-sets overlap less than sibling pairs. Finally, we observe a sharp asymmetry: procedural domains (coding, math) prune cleanly, but a knowledge domain (humanities) does not - the humanities-only specialist collapses even on its own domain (28.7% vs 84.7% baseline), yet unions restore it to 74.3%. Our results suggest fine-grained MoE models are post-hoc composable at the expert level, and motivate applying the recipe to the most fine-grained public MoE, Kimi K3 (896 experts/layer).
```

## Comments field

```
7 pages, 3 tables. Code, calibration sets, and raw results: https://github.com/YashSarwaiya/carve-then-compose
```

## Categories

- **Primary:** `cs.LG` (Machine Learning)
- **Cross-list:** `cs.CL` (Computation and Language)

## License

Recommended: **CC BY 4.0** — maximum reuse, requires attribution. The
minimal alternative is arXiv's default perpetual non-exclusive license,
which is more restrictive for readers but keeps more rights with you.

---

## Step by step

1. Log in at arxiv.org → **START NEW SUBMISSION**
2. Accept the submission agreement; pick the license (above)
3. **Files:** upload `paper/main.tex` — nothing else
4. **Process:** arXiv compiles it. Wait for success, then **view the generated
   PDF** and confirm it matches `paper/main.pdf`
5. **Metadata:** paste title, authors, abstract, comments from above
6. **Categories:** cs.LG primary, add cs.CL as cross-list
7. Review everything, then **Submit**

## After submitting

- You get an identifier like `arXiv:2607.XXXXX`
- Submissions made before 14:00 US Eastern on a weekday are announced around
  20:00 Eastern the next business day; it is public and citable then
- Add the arXiv link to the GitHub README once it is live
- Announce it: a short post naming the headline number (65% of experts
  removed, 90% of coding retained) plus the two links
