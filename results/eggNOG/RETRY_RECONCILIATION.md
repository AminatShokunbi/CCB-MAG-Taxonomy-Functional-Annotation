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

## Cross-file comparison

The original eggNOG collection and retry annotations were compared by their protein query identifiers. **Some query identifiers occurred in both datasets.** These overlaps do not automatically prove duplicated MAGs: gene identifiers can recur across distinct bins and assemblies. However, the overlap means that naive summation or deduplication by query identifier alone is not defensible.

In particular, the retry output for Galaxy input dataset **2531** shared all 678 of its protein query identifiers with the original file `GO1CC4SS10_bin.6.tabular`; the correspondence requires verification against the original Galaxy input mapping before the files can be combined or treated as independent MAGs.

## Required provenance check

The investigator should supply a Galaxy history or collection element mapping of the 15 retried input **dataset IDs** to their original **MAG names**. Once mapped, each original MAG can be paired with its correct retry annotation file, checked for overlap, and incorporated into a nonduplicated 379-MAG inventory.

**Status:** 379 GTDB-Tk MAG IDs and 15 supplementary retry outputs were identified; a validated 379-MAG functional-annotation join has **not** yet been established.

The full annotation outputs were not committed to GitHub due to size and CCB data-sharing constraints.
