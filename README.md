# Scottish Gaelic Machine Translation Evaluation

Evaluation of Scottish Gaelic → English machine translation using BLEU, chrF, COMET, LLM-based post-editing, and fine-tuning.

---

## Author

Danya Leyva  
California State University, Dominguez Hills

## Advisor

Benyamin Ahmadnia  
California State University, Dominguez Hills

---

## Overview

This project investigates how to improve translation quality for a **low-resource language (Scottish Gaelic)**.

Three approaches are compared:

- Baseline NLLB model
- LLM-based post-editing
- Fine-tuning on cleaned parallel data

All models are evaluated on the **same fixed test subset** to ensure a fair and reproducible comparison.

---

## Research Question

Can translation quality for Scottish Gaelic be improved more effectively through:

- LLM post-editing, or
- Fine-tuning on cleaned data?

---

## Methodology

- Built baseline translations using **NLLB**
- Cleaned and filtered parallel dataset (LaBSE-based filtering)
- Applied **LLM post-editing** to baseline outputs
- Fine-tuned the model on cleaned data
- Evaluated all approaches using:
  - BLEU
  - chrF
  - COMET

---

## Results

| Model            | BLEU  | chrF  | COMET |
| ---------------- | ----- | ----- | ----- |
| Baseline (NLLB)  | 13.90 | 28.98 | 0.632 |
| LLM Post-Edited  | 14.39 | 29.05 | 0.631 |
| Fine-Tuned Model | 64.93 | 72.58 | 0.887 |

---

## Key Findings

- LLM post-editing produced **only small improvements** over the baseline
- Fine-tuning on cleaned data resulted in **significant gains across all metrics**
- Data quality had a larger impact than post-processing methods

---

## Visualizations

The repository includes:

- Baseline vs LLM post-editing comparison
- Baseline vs fine-tuned model (15 epochs)

See notebook outputs or poster for figures.

---

## Repository Structure

```text
scottish-gaelic-translation-evaluation/
├── _ScottishGaelic_to_English_.ipynb
├── Poster/
├── Danya Leyva _ GMIS Poster .pptx.pdf
└── README.md
```

---

## Reproducibility

- Fixed test subset used across all experiments
- Same evaluation metrics applied consistently
- Controlled pipeline for direct comparison

---

## Limitations

- Limited high-quality Gaelic data
- Overfitting observed in extended fine-tuning
- Evaluation performed on a subset due to compute constraints

---

## Future Work

- Expand dataset size and diversity
- Improve filtering methods
- Evaluate additional LLMs for post-editing
- Reduce overfitting in fine-tuning

---

## References

- Costa-jussà et al. (2022). _No Language Left Behind_
- Papineni et al. (2002). _BLEU_
- Rei et al. (2020). _COMET_
- Wolf et al. (2020). _Transformers_

---

## Acknowledgments

This work was supported by the **CAHSI LREU Program** and the **National Science Foundation (NSF)**.
