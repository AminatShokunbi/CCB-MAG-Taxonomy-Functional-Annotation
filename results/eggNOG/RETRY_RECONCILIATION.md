# Reconciliation of GTDB-Tk MAGs and eggNOG retry outputs

## Scope

The GTDB-Tk summaries reported **379 MAG identifiers**. The original eggNOG collection archive contained **364 MAG-named files**. The investigator reported that the other **15 initial eggNOG jobs failed and were rerun separately**. Fifteen retry annotation files and 15 seed-ortholog files were supplied.

The 15 GTDB-Tk MAG identifiers absent from the *original* eggNOG collection were:

| MAG identifier | Retry Galaxy dataset ID | Verification status |
|---|---|---|
| `GO1CC4SS01_bin.102` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS01_bin.119` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS01_bin.16` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS01_bin.80` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS01_bin.82` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS05_bin.112` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS05_bin.121` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS06_bin.119` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS06_bin.145` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS06_bin.17` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS06_bin.22` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS06_bin.73` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS08_bin.13` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS10_bin.10` | Not established | Pending Galaxy history mapping |
| `GO1CC4SS10_bin.25` | Not established | Pending Galaxy history mapping |

The retry annotation files were exported using Galaxy numeric dataset identifiers rather than the MAG names. Their one-to-one association with these 15 MAGs **cannot be established from filenames alone**.

## Reanalysis of initially unsuccessful jobs

The investigator clarified that **15 MAGs were rerun through eggNOG-mapper to ensure they received functional annotation after their initial jobs failed**. These were repeat processing attempts for the same MAGs, not additional genomes, duplicate biological samples, or a separate experimental dataset. The original collection export contained 364 MAG annotation files, and 15 supplementary annotation files were subsequently provided from the reruns.

Protein query identifiers appearing in multiple processing outputs were expected in the context of rerunning the same input sequences and **must not be described as evidence of biological duplication**. The appropriate reporting unit was the MAG, with successful functional annotations attributed to their source genomes.

## Required provenance check

The investigator confirmed that 15 MAGs were rerun solely to ensure their functional annotation was completed. The 15 Galaxy retry dataset IDs can be linked to their original MAG names for a reproducible audit trail, but the reruns do not represent extra MAGs or a duplication problem.

**Status:** 379 GTDB-Tk MAG IDs and 15 supplementary retry outputs were identified; a validated 379-MAG functional-annotation join has **not** yet been established.

The full annotation outputs were not committed to GitHub due to size and CCB data-sharing constraints.
