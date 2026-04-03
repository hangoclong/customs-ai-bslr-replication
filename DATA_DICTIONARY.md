# Data Dictionary

## data/corpus/dataset_a.csv
The full 872-paper bibliometric corpus enriched with OpenAlex metadata.

| Column | Description |
|--------|-------------|
| `doi` | Digital Object Identifier |
| `title` | Paper title |
| `year` | Publication year |
| `source` | Journal or conference name |
| `authors` | Author names (semicolon-separated) |
| `abstract` | Paper abstract |
| `citations` | Total citation count (Scopus) |
| `document_type` | Article, Conference Paper, or Review |
| `keywords` | Author-provided keywords |
| `affiliations` | Author affiliations |
| `country` | First author country |
| `cluster_id` | Leiden cluster assignment (0–4) |

## data/clusters/

| File | Description |
|------|-------------|
| `clusters.csv` | 5 macro-cluster labels and paper counts |
| `clusters_L1.csv` | Level-1 sub-cluster assignments |
| `clusters_L2.csv` | Level-2 sub-cluster assignments |
| `themes_L3.csv` | Level-3 thematic labels |
| `topic_distribution.csv` | Topic distribution across clusters |

## data/analysis/

| File | Description | Manuscript Section |
|------|-------------|-------------------|
| `keyword_bursts.csv` | Keyword burst detection results | Table 5 (§4.8.3) |
| `gap_detection.csv` | Co-occurrence gap scores | Table 7 (§6.2) |
| `thematic_map.csv` | Strategic diagram coordinates (density × centrality) | §4.8 |
| `thematic_evolution.csv` | Keyword flow across time periods | Fig 9 |
| `bradford_zones.csv` | Bradford's Law journal zone assignments | §4.3 |
| `lotka_law.csv` | Author productivity distribution | §4.5 |
| `bibcoupling.csv` | Bibliographic coupling pairs and shared references | Fig 7 |
| `cocitation.csv` | Co-citation pairs | Fig 6 |
| `direct_citation.csv` | Direct citation network edges | §4.6 |
| `cluster_timeline.csv` | Publication counts per cluster per year | §4.8.2 |
| `topic_trends_clustering.csv` | Mann-Kendall trend analysis per cluster | Fig 10 |
| `topic_trends_kw.csv` | Mann-Kendall trend analysis per keyword | §4.8.3 |

## data/networks/

| File | Format | Description |
|------|--------|-------------|
| `author_network.gexf` | GEXF (VOSviewer) | Co-authorship network (2,526 nodes) |
| `network.gexf` | GEXF (VOSviewer) | Keyword co-occurrence network |

## data/paper-ready/

Pre-aggregated tables directly backing manuscript claims.

| File | Manuscript Reference |
|------|---------------------|
| `publication_trends.csv` | Fig 2 — Annual publication count |
| `country_analysis.csv` | Table 1 — Top 10 countries |
| `source_analysis.csv` | Table 2 — Top 10 venues |
| `citation_analysis.csv` | Table 3 — Top 10 cited papers |
| `author_stats.csv` | Table 4 — Top 10 authors |
| `keyword_cooccurrence.csv` | Fig 11 — Keyword network edges |
| `coauthorship.csv` | §4.6 — Co-authorship metrics |
| `author_network_edges.csv` | Fig 5 — Author network edge list |

## appendix/

| File | Description | Rows |
|------|-------------|------|
| `table_a1_study_characteristics.csv` | Table A-I: 71 included SLR papers with AI techniques, customs tasks, and datasets | 71 |
| `table_a2_data_limitations.csv` | Table A-II: Data characteristics, explainability gaps, and limitations for all 71 papers | 71 |

## search/

| File | Description |
|------|-------------|
| `scopus_search_string.txt` | Exact Boolean search string used in Scopus (SPICE framework) |
| `thesaurus_auto.tsv` | Keyword normalization thesaurus (TSV: original → canonical) |
