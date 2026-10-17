# CCB MAG Taxonomy and Functional Annotation Using Galaxy

This repository documented the downstream taxonomic and functional characterization of quality-screened metagenome-assembled genomes (MAGs) recovered from the **Cuatro Ciénegas Basin, Coahuila, Mexico**.

The CCB MAGs had been assessed with **CheckM2 in a separate Galaxy history**. MAGs selected after quality assessment were processed in the downstream Galaxy workflow using **GTDB-Tk** for genome taxonomy, **Prodigal** for protein-coding gene prediction, and **eggNOG-mapper** for orthology-based functional annotation.

## Workflow

```text
CCB MAGs → CheckM2 quality screening (separate Galaxy history)
                     ↓
             Selected MAG collection
                     ├── GTDB-Tk → taxonomic classifications
                     └── Prodigal → predicted proteins → eggNOG-mapper → functional annotations
```

## Results from supplied outputs

GTDB-Tk summaries contained **379 classified MAG entries** (268 bacterial and 111 archaeal). The eggNOG-mapper export contained **364 MAG-level files** and **626,123 protein annotation records**. Of these, **590,024** had populated descriptions, **370,563** had KEGG KO assignments, **574,349** had Pfam assignments, and **189,928** had EC numbers. Fifteen initial eggNOG jobs had failed and were retried separately; therefore, they were not missing MAGs. Ten retry annotation tables have been examined (19,895 protein records), but the original MAG identifiers and remaining retry outputs must be reconciled before combined totals are reported.

See [eggNOG results](results/eggNOG/RESULTS.md) for detailed annotation coverage and sample-level counts, [Prodigal documentation](results/Prodigal/README.md), and [methods](docs/METHODS.md).

## Data availability

The full Prodigal and eggNOG output collections were too large for ordinary GitHub commits and **were not uploaded**. Compact analytical summaries were provided instead. Access to original CCB-derived files is subject to dataset-owner authorization. See [data availability](docs/DATA_AVAILABILITY.md).

These genome annotations represented **predicted functional potential**, not experimentally verified biochemical activity. A complete independently rerun workflow has not been demonstrated by the workflow export alone.

## Relationship to the preceding project

The [MAG reconstruction and quality assessment project](https://github.com/AminatShokunbi/Metagenomic-MAG-Reconstruction-Galaxy) documented a related **methodological** stage using a different source dataset. The CCB MAGs in this repository were not the six MAGs reconstructed in that demonstration.

## Publication status

This repository remains under development. **No GitHub release or Zenodo DOI has been created for this project.** When authorized and finalized, the repository will be archived via **GitHub release → Zenodo integration**, rather than manual Zenodo release upload.

**Author:** Aminat Olamide Shokunbi.
