# eggNOG-mapper functional annotation results

## Dataset and processing

Functional annotations were examined from the Galaxy eggNOG-mapper export `2687_ eggNOG Mapper on collection 1167_ annotations.zip`. The archive contained **364 MAG-level tabular files** from the ten Cuatro Ciénegas Basin samples (`GO1CC4SS01`–`GO1CC4SS10`). Prodigal-predicted proteins had been supplied to eggNOG-mapper for orthology-based functional annotation. The full Prodigal and eggNOG datasets were not committed because of their size.

## Annotation results

A direct count of data rows across all 364 tabular files identified **626,123 protein annotation records**. Among these, **590,024** records contained nonempty functional descriptions and COG-category fields; **370,563** had KEGG Orthology (KO) assignments; **574,349** had Pfam annotations; **189,928** had enzyme commission (EC) annotations; **223,337** had KEGG pathway annotations; **149,447** had KEGG module annotations; **52,220** had Gene Ontology annotations; and **8,784** had CAZy assignments. Fields were counted as populated when their values were neither blank nor the missing-value marker `-`. These counts represented annotation-field coverage, not independent genes, experimentally verified activities, or pathway completeness.

| Annotation field | Records with populated field |
|---|---:|
| Total protein records | 626,123 |
| Functional description | 590,024 |
| COG category | 590,024 |
| KEGG KO | 370,563 |
| Pfam | 574,349 |
| EC number | 189,928 |
| KEGG pathway | 223,337 |
| KEGG module | 149,447 |
| Gene Ontology | 52,220 |
| CAZy | 8,784 |

## Files per sample

| Sample | Habitat | MAG annotation files |
|---|---|---:|
| GO1CC4SS01 | Mat Layer 1 | 89 |
| GO1CC4SS02 | Mat Layer 2 | 73 |
| GO1CC4SS03 | Mat Layer 3 | 3 |
| GO1CC4SS04 | Mat Layer 4 | 49 |
| GO1CC4SS05 | Mat Layer 5 | 69 |
| GO1CC4SS06 | Mat Layer 6 | 49 |
| GO1CC4SS07 | Microbialite Layer 1 | 17 |
| GO1CC4SS08 | Microbialite Layer 2 | 4 |
| GO1CC4SS09 | Microbialite Layer 3 | 1 |
| GO1CC4SS10 | Microbialite Layer 4 | 10 |
| **Total** | | **364** |

## Interpretation and limitations

The annotation results indicated substantial predicted functional diversity among the analyzed MAGs. Pfam domain assignments and COG-category annotations were more broadly represented than KEGG KO, pathway, or module assignments. These differences reflected annotation coverage across reference systems; they did not establish differential biological activity. KEGG pathway annotations represented associations of individual proteins with pathway entries, **not evidence that complete pathways were present**.

The GTDB-Tk classification summaries contained **379 MAG entries**, whereas the eggNOG archive contained **364 MAG-level files**. The remaining 15 genomes were not represented in this export, and the reason for this difference was not established. Joint taxonomy–function analyses must use reconciled MAG identifiers.

The findings were computational predictions. No claim of measured gene expression, enzymatic activity, or confirmed metabolism was made.

## Data availability

The complete Prodigal and eggNOG outputs were retained outside the Git repository because of their size. Public access links and checksums may be added later **subject to authorization from the CCB dataset owners**. This document reports aggregate results derived from the supplied eggNOG export; it is not a substitute for the complete raw annotation files.
