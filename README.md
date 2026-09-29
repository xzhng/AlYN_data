# Publication data for Y-rich AlYN

This archive contains the VASP inputs, key outputs, and relaxed structures
underlying the computational results in the YAlN manuscript. 

## Contents

- `01_bulk_properties`: PBE WZ and RS alloy relaxations, all five HSE WZ
  alloy calculations used for the reported mean and standard deviation, and
  the AlN/YN end-member calculations used for mixing enthalpies.
- `02_hse_band_unfolding`: the HSE SCF and unfolded SQS01 band calculation,
  including the unfolding transformation and raw `EBS.dat` output.
- `03_berry_polarization`: the 33-point fixed-structure Berry-phase paths for
  all five SQS cells.
- `04_fixed_cell_neb`: the five three-intermediate-image fixed-cell NEB paths.
  The main-text average uses SQS01, SQS03, SQS04, and SQS05; SQS02 is retained
  for the individual-path discussion in the SI.
- `05_slab_models`: the ordered alloy films at `a = 3.50 Angstrom`, with and
  without four GaN bilayers, plus the reported sensitivity calculations.

## File policy

For standard calculations, the archive retains `INCAR`, `KPOINTS`, `POSCAR`,
`CONTCAR`, `OSZICAR`, and a gzip-compressed `OUTCAR` when those files exist in
the production directory. Specialized raw unfolding files are also included.
`OUTCAR.gz` can be read directly with tools such as `zgrep` or expanded with
`gunzip`.

VASP `POTCAR` files are not redistributed. Each calculation instead contains
`POTCAR.spec`, extracted from its `OUTCAR`, which records the PAW dataset names
and valence counts in the required order. Large restart and redundant files
(`WAVECAR`, `CHGCAR`, `vasprun.xml`, `vaspout.h5`, and scheduler logs) are
intentionally omitted.

`SOURCE_MAP.csv` maps each archived data family to its original working
directory.
