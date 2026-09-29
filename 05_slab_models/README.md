# Ordered alloy slab calculations

The production slabs contain 2, 3, 4, or 6 ordered
Y0.8Al0.2N bilayers at a fixed in-plane lattice parameter of 3.50 Angstrom.
The supported models contain four GaN bilayers and about 20 Angstrom of
vacuum. The upper two GaN bilayers and alloy film were relaxed; the lower two
GaN bilayers were fixed to strained-bulk GaN optimized at the same in-plane
lattice parameter. The artificial bottom N surface was passivated with five
fractional-valence H atoms (`H.75`).

The alloy-only models were made from the corresponding relaxed supported
structures by removing GaN and replacing the removed N-Ga bonds with `H.75`,
then relaxing the alloy atoms at the same fixed lattice vectors. Their
original `INCAR` and `KPOINTS` files are retained with each calculation.

The VASP outputs retain the total energies used to calculate WZ-minus-RS
differences. Negative WZ-minus-RS values favor WZ. Extracted plotting tables
are not duplicated in this archive.

These constrained ordered slabs are proof-of-principle models for possible
epitaxial, interface, and surface contributions. They are not atomistic models
of the exact experimental interface and do not establish that coherent
clamping to bulk GaN alone stabilizes WZ.
