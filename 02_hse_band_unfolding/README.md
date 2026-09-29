# HSE effective band structure

This section contains the SQS01 HSE SCF calculation and the subsequent
zero-weight band-path calculation unfolded onto the primitive WZ Brillouin
zone. `TRANSMAT.in`, `KPATH.in`, `KPOINTS_MAPPING_TABLE.in`, and `KLABELS`
record the transformation and path used by the unfolding procedure.

`unfold/EBS.dat` is the raw unfolded output. Plot broadening and other derived
figure data are intentionally not duplicated in this raw-data archive.

The SQS01 gap is indirect Gamma-to-K and is approximately `2.612 eV`. The
reported five-SQS HSE mean and sample standard deviation (`2.614 +/- 0.039
eV`) are obtained from the five compressed `EIGENVAL` files in
`01_bulk_properties/wz_alloy_hse`.
