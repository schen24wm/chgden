# AFQMC Charge Density

All AFQMC densities are finite-size (FS) corrected, using formula (31) in the paper; an average of 12 quasi-random K-points is used for Cu.

All DFT (dense-K-grid) densities are generated with Quantum Espresso and are from self-consistent 6x6x6 K-point-grid LDA runs.

We also provide the pseudopotentials (\*.UPF) for reproducing the pseudopotential core effect.

## Naming convention of the files

Pseudopotential files have the following names, which are the standard UPF formats (for Quantum Espresso use) generated from D. R. Hamann's ONCVPSP code:

> {atomicNumber}\_{element}\_{XC}\_{kineticEnergyCutoff}\_SRL.UPF

Density data files have the following names:

> {system}\_{source}\_P{plottingCell}\_F{dataFromSupercell}\_{plottingGridSize}

Here, {system} is the name of the system. "-NeCore" for Cu indicates this density is calculated using the Ne-core pseudopotential.

{source} is QMC (for AFQMC densities) or DFT (for DFT dense-K-grid densities).

{plottingCell} and {dataFromSupercell} should be self-explanatory. Note that, for example, "fcc2x2x2" means a 2x2x2 supercell from the smallest possible FCC cell.

{plottingGridSize} is the number of grid points we used for plotting, on Cartesian x, y, and z directions, respectively.

## Data format

The first three columns of each file are the (x,y,z) Cartesian coordinates in \[Bohr\].

The fourth and the fifth columns are the electron charge density and corresponding AFQMC error bar, (respectively,) in \[Bohr^(-3)\].

For DFT densities the fifth column is not present.

There is 1 empty line after each xy-block (within which the x and y coordinates are the same), and 2 extra empty lines after each x-block.
