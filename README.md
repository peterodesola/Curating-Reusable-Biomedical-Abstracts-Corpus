# Curating Reusable-Biomedical-Abstracts-Corpus

**Dataset-Deduplicated · Corpus-Provenance-Verified · Class-Label-Taxonomy-Standardized**

**Dataset DOI:** [10.5281/zenodo.17229456](https://doi.org/10.5281/zenodo.17229456)  
**Code DOI / Repository:** [10.5281/zenodo.17407830](10.5281/zenodo.17407830) · [https://github.com/peterodesola/Curating-Reusable-Biomedical-Abstracts-Corpus](https://github.com/peterodesola/Curating-Reusable-Biomedical-Abstracts-Corpus)  
**License:** CC BY-SA 4.0  
**Contact:** eidreiz01@gmail.com 

---

## Table of Contents

- [Overview](#Overview)
- [Dataset Statistics](#Dataset-Statistics)
- [Label Distribution](#Label-Distribution)
- [File Structure](#File-Structure)
- [Quick Start](#Quick-Start)
- [Provenance](#Provenance)
- [Intended Use](#Intended-Use)
- [Limitations](#Limitations)
- [License](#License)
- [Citation](#Citation)
- [Acknowledgments](#Acknowledgments)
- [Changelog](#Changelog)

---

## Overview

This release provides **metadata**, and **disease labels** for a curated biomedical abstracts corpus derived from a public community dataset.

 **Duplicates and near-duplicates removed** 
 **Provenance tracked via PubMed IDs** 
 **Retired diffusing class label**  

---

## Dataset Statistics

| Stage                                  | Count  |
|----------------------------------------|--------|
| Source Total                           | 14,438 |
| Duplicates Removed                     | 6,140  |
| Ultra-short Removed (< threshold)      | 4      |
| Diffusing class label removed          | 2,593  |
| **Final Records (v1.0)**               | **5,901** |

---

## Final Label Distribution

| Label Category              | Count |
|-----------------------------|------:|
| Neoplasms                   | 2,193 |
| Cardiovascular Diseases     | 1,960 |
| Nervous System Diseases     | 1,049 |
| Digestive System Diseases   | 699   |

---

## File Structure

```

Data collection and exploration codes/
├─ 01_Data_Preparation.ipynb       
└─ 02_Medical_abstract_dedup.ipynb        
└─ requirements.txt        

Dataset and PubMed check/
├─ deduplicated_medical_abstract.csv
├─ pubmed_spotcheck_results.csv
└─ README.md                 

result/
├─ tables/*.csv              
└─ plots/*.png               

```

---

## Quick Start


### 1. Create environment
python3 -m venv venv
source venv/bin/activate

### 2. Clone repository & install dependencies
git clone [https://github.com/peterodesola/Curating-Reusable-Biomedical-Abstracts-Corpus](https://github.com/peterodesola/Curating-Reusable-Biomedical-Abstracts-Corpus)
cd Reusable-Biomedical-Abstracts-Corpus
pip install -r requirements.txt

### 3. Regenerate curated CSV 
download original dataset from [https://github.com/sebischair/Medical-Abstracts-TC-Corpus](https://github.com/sebischair/Medical-Abstracts-TC-Corpus)
merge train and test csv. Read into code environment
run 02_Medical_abstract_dedup.ipynb script


## Provenance

A **random 100-record sample** was checked via **NCBI E-utilities (PubMed API)**. PMIDs were recorded when matches were found.

See: `result/tables/pubmed_spotcheck_summary.csv`


## Intended Use

* **Supervised / Weakly-Supervised Classification Benchmarks**
* **Curriculum Use for Demonstrating Curation & Provenance**
* **Class label Taxonomy Design / Comparisons**

---

## Limitations

* Label taxonomy favours **separability for classification**; domain-specific alternatives may be preferable for clinical use.
* PubMed matching is **sample-based**, not exhaustive.

---

## License

This dataset is released under **CC BY-SA 4.0**.

> You must **attribute both the original creators and this curated release**, and **share derivatives under the same license**.

---

## Citation

```
DATASET
Idris Babalola, Adewale Alex Adegoke, Peter Adebayo Odesola. (2025).
Curated Biomedical Abstracts Metadata & Labels - Provenance-Verified, Deduplicated (v1.0) [Data set].
Zenodo. https://doi.org/10.5281/zenodo.17229456

CODE
Idris Babalola, Adewale Alex Adegoke, Peter Adebayo Odesola. (2025).
Curated Biomedical Abstracts Metadata & Labels - Provenance-Verified, Deduplicated (v1.0) [Data set].
Zenodo. https://doi.org/10.5281/zenodo.17229456
```

---

## Acknowledgments

Derived from the original dataset by **[Original Author/Team]**
Original License: CC BY-SA 3.0
Source: [https://www.kaggle.com/datasets/chaitanyakck/medical-text](https://www.kaggle.com/datasets/chaitanyakck/medical-text) or [https://github.com/sebischair/Medical-Abstracts-TC-Corpus](https://github.com/sebischair/Medical-Abstracts-TC-Corpus)

---

## Changelog

| Version  | Date       | Notes                                                                                                                                       |
| -------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **v1.0** | 2025-10-17 | Initial public release. Dedup = 6,140; ultra-short removed = 4; final records = 5,901; four-class taxonomy; PMIDs recorded where available. |


```
