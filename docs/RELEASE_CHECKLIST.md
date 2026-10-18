# v1.0.0 release readiness checklist

**Objective:** Archive the CCB MAG taxonomy and functional-annotation **reproducibility repository**, not the original CCB dataset.

- [x] Galaxy `.ga` workflow present under `workflow/`
- [x] Separate CheckM2 quality screening documented
- [x] GTDB-Tk and eggNOG MAG inventories reconciled (379 MAGs)
- [x] Galaxy rerun-to-MAG mapping documented
- [x] Original CCB sequence data and full annotation files excluded
- [x] MIT `LICENSE` committed for reusable software and associated documentation
- [x] `CITATION.cff` updated without a premature DOI
- [ ] Review the workflow import and tool/input compatibility on a fresh Galaxy history
- [ ] Verify all links, versions, parameters and results descriptions for v1.0.0
- [ ] **Confirm Zenodo GitHub integration is enabled for `AminatShokunbi/CCB-MAG-Taxonomy-Functional-Annotation`**
- [ ] After confirming integration, create a GitHub tagged release (not before)
- [ ] Confirm Zenodo automatically archived that GitHub release and issued the correct DOI
- [ ] Update `CITATION.cff` and README with the verified DOI in a later commit

## Zenodo integration verification

In Zenodo, sign in to the account connected to GitHub and open the **GitHub** integration settings. Confirm the repository appears and its archive toggle is **enabled**. If it does not appear, refresh/synchronize the repository list or review the GitHub authorization. Do **not** manually upload a Zenodo record as a substitute for the requested GitHub-triggered archive.

The connected GitHub repository interface can confirm repository files and commits but does not independently establish the user's Zenodo account connection or archive toggle state.

## Release boundary

The MIT license covers the repository's reusable workflow and associated documentation. It does not authorize access to or redistribution of the underlying CCB research data. The public repository's aggregate numerical results are not a substitute for restricted input data, and exact result replication would require authorized access to those inputs.
