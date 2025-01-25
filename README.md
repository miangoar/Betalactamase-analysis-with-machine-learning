# Large-scale analysis of the β-lactamase sequence space with protein language models
<img src="https://github.com/miangoar/protein_language_models_for_betalactamases_analysis/blob/main/images/blas.png" alt="Texto alternativo">
This repository contains the main dataset and Jupyter notebooks used to analyze sequences from the BetaLactamase DataBase (BLDB) using protein language models

# Content list
- [Datasets description](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning?tab=readme-ov-file#datasets-description)
- [Notebooks](https://github.com/miangoar/Betalactamase-analysis-with-machine-learning?tab=readme-ov-file#notebooks)

# Datasets description 

The main dataset contains 29,445 rows and 82 columns. The rows represent all sequences retrieved from the BLDB. The columns contain information processed from the BLDB, including their taxonomy annotated against the Genome Taxonomy Database (GTDB RS207), the per-protein embeddings derived from five protein language models (ESM-1b, ESM2-650, ESM2-3b, CARP-640M, ProtTrans-t5-xl-u50), functional annotations estimated with Biopython, sequence quality filters applied to select sequences for the analysis, annotations from the AlphaFold Database (AFDB) for the available structures, and the secondary structure annotations generated from the predicted structures by AlphaFold2 using pyDSSP

| Column name | Description | 
|-----------|-----------| 
| **BLDB info** | ——————————————————————————————— |
| #name |  |
| seq |  |
| length |  |
| filename |  |
| bla_class |  |
| protein_name |  |
| protein_family_filename |  |
| superfamily |  |
| protein_family |  |
| top_fam |  |
| seq_id |  |
| ambler_class |  |
| alternative_protein_name |  |
| subfamily |  |
| genpept_id |  |
| genbank_id |  |
| pubmed_id |  |
| seq_url |  |
| pdb_structures |  |
| mutants |  |
| phenotype |  |
| functional_info |  |
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
| uniprotStart |  |
| uniprotEnd |  |
| modelCreatedDate |  |
| latestVersion |  |
| allVersions |  |
| isReviewed  |  |
| isReferenceProteome |  |
| cifUrl |  |
| bcifUrl |  |
| pdbUrl |  |
| paeImageUrl |  |
| paeDocUrl |  |
| dup_entry |  |
| **pyDSSP annotations** |  ——————————————————————————————— |
| secondary_structure |  |
| frec_turn, frec_helix, frec_beta  |  |
| simple_secondary_structure |  |
|  |  |



# Notebooks 

| Name | Description | 
|-----------|-----------| 
| [bldb_01_create_dataset]() | Parse |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
| []() |  |
