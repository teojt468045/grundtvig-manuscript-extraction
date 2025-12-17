# Grundtvig Manuscript Metadata Extraction

This repository documents the computational workflow used in the article  
“Reconstituting the Literary Archive: Digitization, Metadata, and Computational Approaches in the Grundtvig Archive”  
(under review in *Variants*).

The purpose of the repository is to ensure transparency, reproducibility, and methodological accountability for the XML-based analyses presented in the article.

---

## Overview

The workflow processes XML catalogue records from the *Registranten* of the Grundtvig Archive and extracts:

- dating information (years of composition),
- physical extent (pages and leaves),
- bibliographic identifiers,
- fascicle numbers mapped to fourteen archival categories.

The extracted metadata is aggregated into a structured dataset and used to generate the visualisations discussed in the article.

---

## Repository Structure

- `notebooks/`  
  Contains the complete, executable Python notebook implementing the metadata-extraction pipeline.

- `data/sample_xml/`  
  Provides a representative XML example illustrating the structure and content of the source material.  
  The complete *Registranten* corpus, consisting of approximately 5,000 XML files, is not redistributed here for practical reasons related to size and repository manageability; however, it may be made available upon request: [tafdrup@cas.au.dk](mailto:tafdrup@cas.au.dk)


- `data/grundtvig_datering_alle_biblio_WITH_FASC_INTERVAL.xlsx`  
  The structured dataset produced by the notebook and used for analysis and visualisation.

- `figures/`  
  All figures generated from the extracted data and reproduced in the article.

- `docs/`  
  Supplementary documentation, including:
  - a methodological description of the workflow,
  - a reproducibility statement,
  - a flowchart visualising the extraction logic,
  - documentation of how user prompts and AI assistance contributed to script development.

---

## Methodological Principles

The extraction pipeline is rule-based and deterministic.
It does not rely on machine learning or stochastic processes.

Generative AI (ChatGPT, GPT-4o) was used selectively as a coding assistant during script development.
All AI-generated suggestions were reviewed, adapted, and validated by the authors of the study.
The workflow therefore follows a **Human-in-the-Loop (HITL)** model, with full scholarly responsibility retained by the researchers.

---

## Reproducibility

All analytical results presented in the article can be reproduced by running the notebook in a standard Python environment using the same XML source files.

The repository provides a representative XML example and the full extraction logic; researchers with access to the complete *Registranten* archive may therefore replicate or extend the analyses by applying the notebook to the full corpus.

---

## Requirements

The notebook relies on commonly used Python libraries for XML parsing, data handling, and visualisation:

```text
pandas
lxml
numpy
openpyxl
matplotlib
```

---

## Execution

```bash
pip install -r requirements.txt
jupyter notebook notebooks/datering_registranten_sidetal_FINAL.ipynb
```

---

## Citation

If you refer to this repository, please cite the associated article.
A persistent identifier will be added upon publication.

---



