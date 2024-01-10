# Output files of "Microbiome modeling: A beginner's guide"

The used queries and corresponding output files are listed in the tables below. The parameter for the initial number of papers was always set to 100. Afterwards, the most cited papers were extracted from the references of these initial 100 and ordered by node degree of the reference network. Starting with the highest-ranked articles, the best-fitting articles were selected for the respective sections.

| section     | Script query                                                                             | date             | Number of hits | Topics                                                                  | File numbers |
| ----------- | ---------------------------------------------------------------------------------------- | ---------------- | -------------- | ----------------------------------------------------------------------- | ------------ |
| 4           | (microbiome) AND (microbial community)                                                   | November 7, 2023 | 4465           | Role and properties of microbiomes                                      | 1, 2         |
| 5           | (metaproteomics) OR (metagenomics) OR (metaomics)                                        | November 7, 2023 | 4200           | Metaomics methods, metaproteomics, bioinformatic challenges             | 3, 4         |
| 6           | (computational model) AND ((metabolism) OR (regulation) OR (signaling))                  | November 7, 2023 | 3163           | model types, modeling approaches applicable to metabolism and signaling | 5, 6         |
| 7.1         | (biological network reconstruction) AND ((microbiome) OR (microbial community))          | November 7, 2023 | 6531           | Reconstruction of metabolic and signaling networks                      | 7, 8         |
| 7.2         | (computational model) AND ((parameter estimation) OR (contextualization) OR (reduction)) | November 7, 2023 | 1035           | parameter estimation, context-specific models, reduction of model size  | 9, 10        |
| 8.1 and 8.2 | (computational modeling) AND ((microbiome) OR (microbial community))                     | November 7, 2023 | 1035           | examples of prediction, optimization                                    | 11, 12       |
| 8.3         | (control algorithm) AND ((microbiome) OR (microbial community))                          | November 7, 2023 | 4313           | microbiome control                                                      | 13, 14       |
| 9           | (network modeling) AND (guidelines OR software OR repository)                            | November 7, 2023 | 1671           | FAIR, initiatives, standards, languages,                                | 15, 16       |

The following table lists generated xlsx files listing all references and html files containing the interactive visualization for the corresponding reference list.

| file number | file name                                                                                                   |
| ----------- | ----------------------------------------------------------------------------------------------------------- |
| 1           | 07_11_23_microbiome_or_microbial_community_100_list.xlsx                                                    |
| 2           | 07_11_23_microbiome_or_microbial_community_100_graph.html                                                   |
| 3           | 07_11_23_meta_proteomics_or_meta_genomics_or_meta_omics_100_list.xlsx                                       |
| 4           | 07_11_23_meta_proteomics_or_meta_genomics_or_meta_omics_100_graph.html                                      |
| 5           | 07_11_23_computational_modeling_and_metabolism_or_regulation\_ or_signaling_100_list.xlsx                   |
| 6           | 07_11_23_computational_modeling_and_metabolism_or_regulation\_ or_signaling_100_graph.html                  |
| 7           | 07_11_23_biological_network_reconstruction_and_microbiome_or\_ microbial_community_100_list.xlsx            |
| 8           | 07_11_23_biological_network_reconstruction_and_microbiome_or\_ microbial_community_100_graph.html           |
| 9           | 07_11_23_computational_modeling_and_parameter \_estimation_or_contextualization_or_reduction_100_list.xlsx  |
| 10          | 07_11_23_computational_modeling_and_parameter \_estimation_or_contextualization_or_reduction_100_graph.html |
| 11          | 07_11_23_computational_modeling_and_microbiome \_or_microbial_community_100_list.xlsx                       |
| 12          | 07_11_23_computational_modeling_and_microbiome \_or_microbial_community_100_graph.html                      |
| 13          | 07_11_23_control_algorithm_and_microbiome_or_microbial_community\_ 100_list.xlsx                            |
| 14          | 07_11_23_control_algorithm_and_microbiome_or_microbial_community\_ 100_graph.html                           |
| 15          | 07_11_23_network_modeling_and_guidelines_or_software_or_repository\_ 100_list.xlsx                          |
| 16          | 07_11_23_network_modeling_and_guidelines_or_software_or_repository\_ 100_graph.html                         |
