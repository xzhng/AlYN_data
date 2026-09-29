# Bulk property calculations

The alloy folders contain five independent 128-atom SQS cells at
`Y_0.796875 Al_0.203125 N` (51 Y, 13 Al, and 64 N atoms). PBE calculations
are provided for WZ and RS cells; HSE calculations are provided for WZ cells.
Compressed `EIGENVAL` files are retained for all five HSE SQS cells used to
calculate the reported mean and sample standard deviation (`2.614 +/- 0.039
eV`).

Mixing enthalpies use ground-state structural references: WZ AlN and RS YN.
The `endmembers` folders are the calculations at the fitted equilibrium
volumes. `EOS` contains the complete volume grids used to fit
the end-member equilibrium energies. WZ YN is included to document its energy
relative to RS YN; the fitted PBE and HSE differences are 174.8 and
197.8 meV per formula unit, respectively.
