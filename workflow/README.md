# Galaxy workflow: quality-filtered MAG taxonomy and functional annotation

The exported Galaxy workflow [Galaxy-Workflow-CCB_Quality_Filtered_MAGs_GTDBTk.ga](Galaxy-Workflow-CCB_Quality_Filtered_MAGs_GTDBTk.ga) was deposited as a **workflow definition**, not as a copy of the underlying Cuatro Ciénegas Basin (CCB) metagenomic dataset.

## Intended reproducibility

The workflow documented the downstream analysis of quality-screened MAGs, with **GTDB-Tk** for taxonomy and **Prodigal → eggNOG-mapper** for functional annotation. **CheckM2 quality screening occurred separately in another Galaxy history and is not part of this exported workflow**. A new user must first quality-screen their own MAGs and prepare inputs compatible with the exported workflow.

The export included many individually wired dataset inputs and Galaxy collection inputs. Reuse on another dataset may require reassigning inputs and adapting the workflow in Galaxy. The presence of a workflow definition does not establish that an independent user has successfully rerun it.

## Data availability

The original CCB MAG assemblies, full Prodigal protein FASTAs and complete eggNOG annotation files **were not deposited** in this repository. The repository documents analytical methods and aggregate findings only. It is intended for methodological transparency and reuse on authorized datasets, not public distribution of the original CCB research data.

## Suggested reuse

1. Import the `.ga` file into a compatible Galaxy server.
2. Run quality assessment on your own MAGs separately (for example, with CheckM2) and select MAGs using a clearly documented quality criterion.
3. Inspect and reconnect the workflow's dataset and collection inputs.
4. Confirm database availability and compatible versions of GTDB-Tk, Prodigal and eggNOG-mapper before execution.
5. Execute the workflow and evaluate each tool's output and execution logs.

This repository does not guarantee byte-identical reproduction of the CCB results without the original inputs, environment and database snapshots.
