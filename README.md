# NADPH lipid-interface research materials

Private review deposit of the curated lipid-interface code and structural audit
package supporting manuscript Fig. 2b and Supplementary Fig. S4.

## Download and inspect

Download [`lipid_code_release.zip`](lipid_code_release.zip) and extract it locally.
The archive preserves the directory structure required by the scripts. The full
technical README, source snapshots, input structures, result tables and file
integrity manifest are inside the archive.

This is a release candidate, **not** a complete from-scratch reproduction package
for the entire paper. No DOI or public-use licence has been assigned.

## Contents

- Three original lipid construction, relaxation and classification scripts.
- A separate read-only offline audit script (`audit_release.py`).
- 54 reported lipid-interface structures, three slabs and two gas-phase references.
- Six additional MGDG/TiO2 verification structures.
- Five original CSV tables, a SHA-256 manifest, and a scoped Code availability draft.

## Offline check

With Python and NumPy available, run `audit_release.py` from the extracted package.
This checks the supplied geometry and stored classification records; it does not
recalculate PFP energies or forces and does not require Matlantis or VASP.

The check performed before this upload covered 54 main and six verification
structures. It reproduced 26 intact PC configurations and one rearranged PC
configuration; the stored-force MGDG classifications were 20 rearranged, six
insufficient-contact and one borderline configuration.

The illustrative composition-weighted Fig. 2b totals are 104.8, 103.6 and
92.0 mN/m for Cu, Cu2O and TiO2. These include diagnostic MGDG model values;
they are not quantitative predictions of native membrane tension or rupture.

## Limitations and outstanding material

- The original tables retain a superseded `quant_valid=True` flag for dry
  TiO2/MGDG. The package README and independent audit identify it as borderline.
- PC per-structure final-force records and the actual dry orientation-selection
  logs/configurations still need to be supplied.
- Separated relaxed reference structures/energies and exact runtime dependency
  records remain necessary for complete from-scratch energy reproduction.
- The original simulation scripts retain their original workspace paths and
  can launch licensed/paid Matlantis calculations. Inspect them before execution.
- The NADPH electronic-structure, NEB, Bader, CDD and PDOS workflows are outside
  this deposit; example templates are not presented as actual execution records.
- Confirm author/institution approval, licensing and provenance before public
  release or DOI registration. No proprietary model weights or credentials are
  included.

The included source scripts were syntax checked; the offline audit was run.
No new PFP/VASP simulations were run as part of this upload.
