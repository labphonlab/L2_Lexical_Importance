# Lexical Importance in L2 English: Derived Datasets and Analysis

This repository contains the datasets and analysis scripts associated with the research article:
**"Lexical Importance in L2 Spoken English: Frequency, Phonological Vulnerability, and Spoken Word Recognition"** 

## 📂 Repository Contents

### 1. Datasets
The datasets provided here are **derived measures** calculated for this study. To comply with licensing restrictions, the original corpora (SUBTLEX-US, Buckeye Corpus) and lexical resources (IPhOD) are not redistributed.

* **`dataset_content_words.csv` (Primary Dataset)**
    * **N = 2,996** (Content words)
    * Contains spoken frequency, log phonotactic probability, lexical competition risk, phonetic instability, and the final cluster labels (0-4) reported in the article.
    * *Columns:* `word`, `pos_tag`, `spoken_frequency_zipf`, `log_phonotactic_probability`, `lexical_competition_risk`, `phonetic_instability`, `cluster_label`.

* **`dataset_function_words_supplementary.csv` (Supplementary Dataset)**
    * Contains probability-weighted mixture measures for function words, accounting for pronunciation variants (strong/weak forms).
    * *Columns:* `word`, `spoken_frequency_zipf`, `mixture_phonotactic_probability`, `mixture_competition_risk`, `mixture_phonetic_instability`, `prob_strong_form`.

### 2. Analysis Scripts
* **`Lexical_Importance_BLC_v2.ipynb`**: The Python (Jupyter) notebook used to generate the clusters, statistics, and figures reported in the paper.

## ⚙️ Methodology & Resources
* **Spoken Frequency**: Calculated using `wordfreq` (SUBTLEX-US).
* **Phonotactic Probability**: Derived from *Irvine Phonotactic Online Dictionary* (IPhOD) and CMU Dict bigram probabilities.
* **Competition Risk**: Frequency-weighted neighborhood density calculated within the provided script.
* **Phonetic Instability**: Computed based on the index defined in the article (Appendix S1), utilizing aggregated variant probabilities.

## 📜 License & Usage
These derived datasets are made available for research and educational purposes. If you use these data or scripts, please cite the original article.
