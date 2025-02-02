# Large-scale analysis of the β-lactamase sequence space with protein language models
<img src="https://github.com/miangoar/protein_language_models_for_betalactamases_analysis/blob/main/images/blas.png" alt="Texto alternativo">
This repository contains the main dataset and Jupyter notebooks used to analyze sequences from the BetaLactamase DataBase (BLDB) using protein language models

# Content list
- [Datasets description](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning?tab=readme-ov-file#datasets-description)
- [Notebooks](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning?tab=readme-ov-file#notebooks)

# Datasets description 

The main dataset and 2D representations computed with PCA, tSNE and UMAP are available thought Zenodo:
- <https://zenodo.org/records/14743325>

The main dataset contains 29,445 rows and 82 columns. The rows represent all sequences retrieved from the BLDB. The columns contain information processed from the BLDB, including their taxonomy annotated against the Genome Taxonomy Database (GTDB RS207), the per-protein embeddings derived from five protein language models (ESM-1b, ESM2-650, ESM2-3b, CARP-640M, ProtTrans-t5-xl-u50), functional annotations estimated with Biopython, sequence quality filters applied to select sequences for the analysis, annotations from the AlphaFold Database (AFDB) for the available structures, and the secondary structure annotations generated from the predicted structures by AlphaFold2 using pyDSSP

| Column name | Description | 
|-----------|-----------| 
| **BLDB info** | ——————————————————————————————— |
| #name | information from the raw header |
| seq | aminoacid sequence  |
| length | sequence length |
| filename | name of the raw file from BLDB that contain the sequence |
| bla_class | molecular classification for betalactamases: A, B, C and D |
| protein_name | name of the protein (e.g. TEM-1, SHV-1, etc) |
| protein_family_filename | protein family retived from the raw filename (eg. TEM, SVH, etc) |
| superfamily | SBL for serinbetalactamase and MBL for metalobetalactamase |
| protein_family | Protein family retrieved from the header of each sequence (e.g., TEM, SVH, etc.) and validated using the current list of recognized families by the BLDB |
| top_fam |  |
| seq_id | arbitraty sequence identifier for easy manipulation |
| ambler_class | molecular classification curated by the BLDB |
| alternative_protein_name | alterative names curated by the BLDB |
| subfamily | subfamilies for class D serinbetalactamases curated by the BLDB |
| genpept_id | genpept_id curated by the BLDB |
| genbank_id | genbank_id curated by the BLDB |
| pubmed_id | pubmed_id curated by the BLDB|
| seq_url | url curated by the BLDB for the sequence hosted in NCBI  |
| pdb_structures | number of available structures in the PDB curated by the BLDB |
| mutants | number of mutants available in the PDB curated by the BLDB |
| phenotype | functional classification curated by the BLDB |
| functional_info | functional classification curated by the BLDB |
| **GTDB annotation** | ——————————————————————————————— |
| source |  |
| bitscore |  |
| Domain - Species | 'Domain', 'Phylum', 'Class', 'Order', 'Family', 'Genus', 'Species' |
| phylo_group |  |
| phylo_group_genus |  |
| phylo_group_sp |  |
| bla_subclass |  |
| **Embeddings** |  ——————————————————————————————— |
| esm1b |  |
| esm2_650m |  |
| esm2_3b |  |
| carp |  |
| t5xlu50 |  |
| **Biopython annotaions** | ——————————————————————————————— |
| molecular_weight |  |
| aromaticity |  |
| instability |  |
| gravy |  |
| isoelectric_point |  |
| entropy |  |
| helix, turn, sheet |  |
| **Sequence quality filters** |  ——————————————————————————————— |
| pass_the_filter |  |
| is_clust_rep_30 |  |
| is_clust_rep_60 |  |
| is_clust_rep_90 |  |
| **AFDB annotations** |  ——————————————————————————————— |
| has_af2_model |  |
| model |  |
| mean_plddt |  |
| resid_plddt |  |
| entryId |  |
| gene |  |
| uniprotAccession |  |
| uniprotId |  |
| uniprotDescription |  |
| taxId |  |
| organismScientificName |  |
| uniprotStart, uniprotEnd |  |
| modelCreatedDate, latestVersion, allVersions, allVersions, isReviewed, isReferenceProteome |  |
| cifUrl, bcifUrl, pdbUrl, paeImageUrl, paeDocUrl |  |
| dup_entry |  |
| **pyDSSP annotations** |  ——————————————————————————————— |
| secondary_structure |  |
| frec_turn, frec_helix, frec_beta  |  |
| simple_secondary_structure |  |
|  |  |



# Notebooks 

| Name | Description | 
|-----------|-----------| 
| [bldb_01_create_dataset](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_01_create_dataset.ipynb) | Parse |
| [bldb_02_embeddings](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_02_embeddings.ipynb) |  |
| [bldb_03_af2](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_03_af2.ipynb) |  |
| [bldb_04_PCA](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_04_PCA.ipynb) |  |
| [bldb_04_PCA_rep90](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_04_PCA_rep90.ipynb) |  |
| [bldb_05_tSNE_merge_csv](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_05_tSNE_merge_csv.ipynb) |  |
| [bldb_06_tSNE](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_06_tSNE.ipynb) |  |
| [bldb_umap_create](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_umap_create.ipynb) |  |
| [bldb_umap_map](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_umap_map.ipynb) |  |
| [bldb_07_tax_panel](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_07_tax_panel.ipynb) |  |
| [bldb_08_fams_plots](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_08_fams_plots.ipynb) |  |
| [bldb_09_class_a_foldseek](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_09_class_a_foldseek.ipynb) |  |
| [bldb_10_class_c_foldseek_analysis](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_10_class_c_foldseek_analysis.ipynb) |  |
| [bldb_11_unsupervised](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_11_unsupervised.ipynb) |  |
| [bldb_12_biochem](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning/blob/main/notebooks/bldb_12_biochem.ipynb) |  |
| []() |  |
