# Data availability and reproducibility scope

This public repository distributed the **Galaxy workflow definition, procedural documentation, software settings, and limited aggregate analysis summaries** for methodological transparency. It **did not distribute the Cuatro Ciénegas Basin (CCB) research dataset**.

The original MAG assemblies, nucleotide and protein sequences, complete Prodigal outputs, complete eggNOG-mapper annotation tables, original sequence reads, and other source data were **not deposited** in this repository. No external dataset archive or unrestricted access to the CCB inputs was implied.

The reported aggregate MAG and annotation counts documented the analysis performed, but they did not enable exact reproduction of the original numerical results without access to the original data. Other researchers could import the Galaxy `.ga` workflow, inspect its parameters, and adapt it to **their own authorized MAG inputs**.

CheckM2 quality screening was executed in a separate Galaxy history and was not included in the exported downstream workflow. Consequently, the workflow file documented the GTDB-Tk and Prodigal-to-eggNOG stages, rather than an end-to-end raw-read-to-annotation pipeline.

A future **GitHub release** could archive only the repository's distributable workflow and documentation through GitHub–Zenodo integration. Such a release must not be interpreted as permission to share the underlying CCB dataset. The GitHub–Zenodo integration and the intended repository license must be confirmed before a tagged release is created.
