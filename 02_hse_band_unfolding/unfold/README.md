# HSE wurtzite-reference effective band structure

The parent HSE relaxation is converged. `POSCAR` is an internal link to its
own `CONTCAR`; it does not link to PBE data.

VASPKIT task `281` has generated `KPOINTS` and
`KPOINTS_MAPPING_TABLE.in` from `KPATH.in` and `TRANSMAT.in`. The generated
file has an 8-point weighted 2x2x3 Gamma-centered SCF mesh followed by 67
zero-weight points along Gamma--M--K--Gamma--A--L--H--A.

The converged HSE SCF `WAVECAR` and `CHGCAR` are copied into this directory
as restart inputs. The supplied `INCAR` uses `ISTART = 1`, `ICHARG = 1`, and
`NELMIN = 10`, so the 67 new zero-weight path states receive at least ten
electronic iterations. Do not use `ICHARG = 11` for this hybrid-functional
calculation. After VASP completes, run VASPKIT task `282` here to write
`EBS.dat` and `KLABELS`.
