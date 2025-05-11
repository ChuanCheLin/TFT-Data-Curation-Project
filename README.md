# TFT Dataset Curation Project

This repository contains scripts and cleaned data from a personal data curation workflow using the Riot Games API for **Teamfight Tactics (TFT)**.

The goal is to demonstrate a complete data lifecycle:
- Acquire a small number of matches from my own game history
- Clean and assess data quality
- Document metadata and variable definitions
- Enable reproducibility via version-controlled code

## 📁 Folder Structure
- `raw/` – Raw match JSONs, organized by date and patch
- `curated/` – Cleaned player-level CSV
- `docs/` – Project documentation
  - `README.md`
  - `data_dictionary.md`
  - `retrieval_log.csv`
- `notebooks/` – Interactive EDA and analysis notebooks



## 📌 Current Dataset

| Item                | Value                                  |
|---------------------|----------------------------------------|
| Source              | Riot Games Developer API               |
| Match Count         | ~50 (personal account only)            |
| Patch Version(s)    | e.g., 15.7                              |
| Region              | Personal / NA                          |
| Date of Collection  | 2025-05-11                             |
| Game Mode           | Ranked (queue_id = 1100)               |

Only records with complete placement and unit data were kept for analysis (`status == "ok"`).

## 🧾 Metadata & QC

The `data_dictionary.md` provides field definitions and types for all cleaned fields.  
Raw data is organized by patch to account for champion/trait changes over time.

## 🔁 Reproducibility & Archiving

This GitHub repository serves as an **ephemeral workspace** for development and version control.  
For long-term preservation and citation, a **Zenodo sandbox deposit** may be created after final cleanup.

The current version does not include sensitive data or identifiers (only Riot PUUIDs), and it complies with Riot’s personal-use API policy.

---

For questions, contact: **Chuan-Che Lin** **diamond16888@gmail.com**
