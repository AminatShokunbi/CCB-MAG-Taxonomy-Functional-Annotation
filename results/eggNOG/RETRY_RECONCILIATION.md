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

The investigator clarified that the overlap between initial and retry records arose because **the initial eggNOG jobs failed and were subsequently rerun**. The retries were recovery attempts for existing MAGs, **not additional MAGs or biological replicates**. Therefore, a failed-run record and its successful retry must not both contribute to final annotation counts. Where failed-run outputs were retained in the Galaxy history, those records should be treated as execution provenance rather than independent functional annotation results.

In particular, the retry output for Galaxy input dataset **2531** shared all 678 of its protein query identifiers with the original file `GO1CC4SS10_bin.6.tabular`; this was consistent with the reported rerun history, but the Galaxy input mapping remains necessary to establish exactly which successful retry belongs to each MAG.

## Required provenance check

The investigator confirmed that the overlapping outputs reflected failed initial jobs followed by retries. To complete an auditable per-MAG inventory, the 15 retried input **dataset IDs** should still be associated with their original **MAG names** using Galaxy history or collection element metadata. For each MAG, only the successful annotation output should be counted. No independent duplicate-MAG hypothesis is warranted solely from the reported overlap.

**Status:** 379 GTDB-Tk MAG IDs and 15 supplementary retry outputs were identified; a validated 379-MAG functional-annotation join has **not** yet been established.

The full annotation outputs were not committed to GitHub due to size and CCB data-sharing constraints.
