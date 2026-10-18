# Complete reconciliation of GTDB-Tk and eggNOG MAGs

## Verified result

The original eggNOG collection contained **364 distinct MAG-named annotation files**. Fifteen initial eggNOG jobs had failed, so the investigator reran those 15 MAGs individually to ensure they received functional annotation. The investigator supplied the original MAG identities for each Galaxy input dataset ID, which were checked against the original collection and both GTDB-Tk summary tables.

**The union of the 364 original MAG names and the 15 rerun MAG names exactly matched all 379 distinct GTDB-Tk MAG identifiers.** There were **zero overlapping MAG identifiers** between the 364-file collection and the 15 rerun MAGs, **zero GTDB-Tk MAGs absent from the union**, and **zero additional MAG identifiers outside the GTDB-Tk inventory**.

These reruns were technical recovery of initially unsuccessful annotation jobs, not additional genomes or biological replicates.

## Manually reconciled and independently cross-checked input mapping

| Galaxy input dataset ID | Original MAG identifier | Annotation records | KEGG KO records |
|---|---|---:|---:|
| 1195 | `GO1CC4SS01_bin.16` | 2,446 | 1,415 |
| 1347 | `GO1CC4SS01_bin.80` | 2,889 | 1,424 |
| 1351 | `GO1CC4SS01_bin.82` | 3,073 | 1,681 |
| 1415 | `GO1CC4SS01_bin.102` | 1,129 | 736 |
| 1471 | `GO1CC4SS01_bin.119` | 2,871 | 1,572 |
| 2255 | `GO1CC4SS05_bin.112` | 2,278 | 1,495 |
| 2267 | `GO1CC4SS05_bin.121` | 520 | 400 |
| 2339 | `GO1CC4SS06_bin.17` | 1,373 | 933 |
| 2343 | `GO1CC4SS06_bin.22` | 463 | 309 |
| 2415 | `GO1CC4SS06_bin.73` | 562 | 349 |
| 2503 | `GO1CC4SS06_bin.119` | 449 | 296 |
| 2531 | `GO1CC4SS06_bin.145` | 678 | 456 |
| 2611 | `GO1CC4SS08_bin.13` | 3,740 | 1,864 |
| 2647 | `GO1CC4SS10_bin.10` | 3,181 | 1,798 |
| 2675 | `GO1CC4SS10_bin.25` | 2,642 | 1,544 |
| **Total** | **15 MAGs** | **28,294** | **16,272** |

Machine-readable mapping: [retry_MAG_mapping.csv](retry_MAG_mapping.csv).

The input-to-MAG mapping was supplied by the investigator after manual inspection of the Galaxy history. Independent validation established that these 15 MAG names were exactly the 15 identifiers absent from the original eggNOG collection and that their union matched the GTDB-Tk inventory.

## Functional annotation coverage

The 15 rerun annotation files contained 28,294 protein annotation records. The initial 364-file collection contained 626,123 records. The combined files therefore contained **654,417 protein annotation records across 379 MAGs**. These were predicted-protein annotation records, not a claim that every record had an assigned function.

| Field | Original 364 MAGs | Rerun 15 MAGs | Combined |
|---|---:|---:|---:|
| Protein annotation records | 626,123 | 28,294 | 654,417 |
| Functional descriptions | 590,024 | 26,675 | 616,699 |
| KEGG KO assignments | 370,563 | 16,272 | 386,835 |
| Pfam assignments | 574,349 | 25,893 | 600,242 |
| EC numbers | 189,928 | 8,428 | 198,356 |
| KEGG pathways | 223,337 | 9,505 | 232,842 |
| KEGG modules | 149,447 | 6,134 | 155,581 |
| Gene Ontology | 52,220 | 2,027 | 54,247 |
| CAZy | 8,784 | 407 | 9,191 |

Field counts indicate populated annotations and should not be interpreted as experimentally validated enzyme functions or complete metabolic pathways.

## File naming and provenance

The raw Galaxy exports retained their original Galaxy-generated filenames outside GitHub. The CSV mapping provided clear MAG identifiers for all 15 rerun files without modifying the original raw files. Full eggNOG and Prodigal outputs were not uploaded because of their size and applicable data-sharing permissions.
