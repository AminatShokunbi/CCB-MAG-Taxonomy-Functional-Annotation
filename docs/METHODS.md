# Methods and provenance

The CCB MAGs were assessed with CheckM2 in a **separate Galaxy history**. MAGs passing that screening were uploaded to a downstream Galaxy history. The exported workflow includes GTDB-Tk (taxonomic classification), Prodigal (gene prediction), and eggNOG-mapper (functional annotation). CheckM2 itself is not an executable step in the supplied downstream workflow.

The GTDB-Tk summary archive contains 268 bacterial and 111 archaeal genome classifications (379 total). The eggNOG archive contains 364 per-MAG annotation files. The user clarified that 15 initial eggNOG jobs failed and were retried separately. All 15 retry annotation outputs and their seed-ortholog tables have now been provided. The 15 annotation tables contained 28,294 protein records. These are not missing MAGs; the retry outputs must be mapped to original MAG identifiers and checked for overlap before joint summaries are finalized.

The exported workflow contains many individual inputs and must not be described as independently rerun and validated. Functional annotations indicate predicted potential, not experimentally demonstrated activity. Tool settings and outputs must be verified against the original Galaxy history before publication.

**Data provenance:** Cuatro Ciénegas Basin MAGs, separate from the public SRA dataset used in the earlier MAG-reconstruction tutorial.
