# Retained SQS02 fixed-cell NEB states

Only the two requested calculation states are retained here.

## `spring0_converged_job_58491611`

This is the validated, non-climbing `SPRING=0` band. VASP stopped with the
required-accuracy marker in all three active images. The final maximum atomic
forces for images 01--03 were 0.000921, 0.006365, and 0.009907 eV/angstrom.

For each image, `after/XX/CONTCAR` is the final converged geometry. These files
are byte-identical to the active root `XX/POSCAR` files through the subsequent
`SPRING=-1` checkpoint's `before/XX/POSCAR` copies.

## `springminus1_progress_job_58492688`

This contains the complete before/after checkpoint for the attempted
non-climbing `SPRING=-1` continuation. It was deliberately cancelled after 20
force evaluations because the band was becoming less stable; the driver did
not promote its `CONTCAR` files.

At the last completed evaluation, maximum atomic forces for images 01--03 were
0.007633, 0.026433, and 0.018824 eV/angstrom. The adjacent image distances were
1.830635, 1.849657, 1.906415, and 1.961892 angstrom. The full trajectory remains
in the retained OUTCAR files.

## Active root convention

- `01/POSCAR`--`03/POSCAR`: preserved converged `SPRING=0` geometries.
- `01/CONTCAR`--`03/CONTCAR`, OUTCAR, OSZICAR, and `output`: retained
  `SPRING=-1` progress from the cancelled run.
- `INCAR`: the `SPRING=-1`, `LCLIMB=.FALSE.` input used for that continuation.

No SQS02 job was active when this cleanup was performed on 2026-09-18.

