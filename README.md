# Replication Package: AI in Customs Compliance — A Bibliometric-Systematic Literature Review

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Overview

This repository contains the replication dataset and supplementary materials for:

> **N. L. Ha, T. H. Tran, S. H. Do, and V. P. Le**, "Artificial Intelligence for Customs Compliance Management and Trade Facilitation: A Bibliometric-Systematic Literature Review," *Future Business Journal*, 2026.

The study presents a dual-stage bibliometric-systematic literature review (B-SLR) of 872 peer-reviewed publications (1996–2026) on AI applications in customs compliance and international trade facilitation. A focused PRISMA-guided systematic review of 71 papers in the "Intelligent Customs Compliance" cluster provides thematic synthesis across four domains: HS code classification, fraud detection, cargo inspection, and regulatory compliance.

## Citation

```bibtex
@article{ha2026ai_customs_bslr,
  author  = {Ha, N. Long and Tran, Thi Huong and Do, S. Huong and Le, Van Phuc},
  title   = {Artificial Intelligence for Customs Compliance Management and Trade Facilitation: A Bibliometric-Systematic Literature Review},
  journal = {Future Business Journal},
  year    = {2026},
  note    = {Under review}
}
```

## Repository Structure

```
├── data/
│   ├── corpus/          # Full 872-paper bibliometric dataset
│   ├── clusters/        # Leiden cluster assignments (L1/L2/L3)
│   ├── analysis/        # Bibliometric coupling, gap detection, keyword bursts
│   ├── networks/        # GEXF network files (VOSviewer-compatible)
│   └── paper-ready/     # Aggregated tables directly backing manuscript claims
├── appendix/            # Tables A-I and A-II as machine-readable CSVs
├── figures/             # All 11 manuscript figures (PNG)
├── search/              # Scopus search string and keyword thesaurus
├── DATA_DICTIONARY.md   # Column definitions for all CSV files
└── LICENSE              # CC-BY-4.0
```

## Key Files

| Manuscript Section | File | Records |
|---|---|---|
| §3.2 Search | `data/corpus/dataset_a.csv` | 872 papers |
| §4.2 Geography | `data/paper-ready/country_analysis.csv` | 10 countries |
| §4.3 Venues | `data/paper-ready/source_analysis.csv` | Top sources |
| §4.5 Authors | `data/paper-ready/author_stats.csv` | Top authors |
| §4.8 Clusters | `data/clusters/clusters.csv` | 5 clusters |
| §4.8.3 Keywords | `data/analysis/keyword_bursts.csv` | Burst keywords |
| §6.2 Gaps | `data/analysis/gap_detection.csv` | 6 gaps |
| Appendix A-I | `appendix/table_a1_study_characteristics.csv` | 71 papers |
| Appendix A-II | `appendix/table_a2_data_limitations.csv` | 71 papers |

## Network Visualization

The VOSviewer-native files (`map.txt` + `network.txt`) are located under `data/figures/`:

| Network | Path | Manuscript |
|---------|------|------------|
| Keyword co-occurrence | `data/figures/4-clustering/vosviewer/cooccurrence/` | Fig 11 |
| Bibliographic coupling | `data/figures/5-impact/vosviewer/bibcoupling/` | Fig 7 |
| Co-citation | `data/figures/5-impact/vosviewer/cocitation/` | Fig 6 |
| Direct citation | `data/figures/5-impact/vosviewer/citation/` | §4.6 |
| Co-authorship | `data/figures/9-laws/vosviewer/coauthorship/` | Fig 5 |

To visualize: open [VOSviewer](https://www.vosviewer.com/) → *File → Open* → select the `map.txt` and `network.txt` pair.

GEXF network files are also available in `data/networks/` for use with Gephi or other graph tools.

## Data Collection

- **Database:** Scopus
- **Search date:** January 2026
- **Search string:** See `search/scopus_search_string.txt`
- **Keyword normalization:** See `search/thesaurus_auto.tsv`
- **Author disambiguation:** OpenAlex API

## Reproduction

1. The `data/corpus/dataset_a.csv` contains the full bibliometric corpus enriched with OpenAlex metadata
2. Cluster assignments in `data/clusters/` were generated using the Leiden algorithm
3. All figures in `figures/` were generated from the corresponding CSV files in `data/`
4. Network files in `data/networks/` can be opened directly in VOSviewer for interactive exploration

## License

This dataset is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

## Contact

- **Corresponding Author:** N. Long Ha — hnlong@hueuni.edu.vn
- **Institution:** University of Economics, Hue University, Vietnam
