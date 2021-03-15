# Data repository -- charge densities in Si, NaCl, Cu
## From the paper: 
"Ab initio electronic density in solids by many-body plane-wave auxiliary-field quantum Monte Carlo calculations," 

Siyuan Chen, Mario Motta, Fengjie Ma, Shiwei Zhang,

Phys. Rev. B 103, 075138 (2021)

DOI: 10.1103/PhysRevB.103.075138

## Downloading and use of the data should only be in a manner consistent with the use of the paper. See citation above.


## Additional information on the included charge density

See Sec.'s III and IV in the paper for details of the AFQMC densities. 

All DFT (dense-K-grid) densities are generated with Quantum Espresso, using self-consistent LDA with a 6x6x6 K-point-grid.

We also provide the pseudopotentials (\*.UPF) used in these calculations.

## Naming convention of the files

Pseudopotential files have the following names, and are in standard UPF formats, generated from D. R. Hamann's ONCVPSP code:

> {atomicNumber}\_{element}\_{XC}\_{kineticEnergyCutoff}\_SRL.UPF

Density grid data files have the following names:

> {system}\_{source}\_P{plottingCell}\_F{dataFromSupercell}\_{plottingGridSize}

Here, {system} is the name of the system. (In Cu, "-NeCore" is appended to indicate that the density is calculated using a Ne-core pseudopotential, to distinguish from the Ar-core results which are mentioned in the paper but not included here.)

{source} is QMC (for AFQMC densities) or DFT (for DFT dense-K-grid densities).

{plottingCell} gives the cell in which the data is presented, and {dataFromSupercell} indicates the supercell from which the raw AFQMC data is obtained (prior to finite-size correction).

{plottingGridSize} is the number of FFT grid points used to represent the density, in Cartesian x, y, and z space.

1D-route density files (for QMC only) have the following names:

> {system}\_QMC\_1D\_001-110-111

These correspond to the data in Figs. 4, 6, and 9. They can be extracted directly from the AFQMC density data on the full 3D grid, but are included here as separate files for convenience. 

## Density grid data format

The first three columns of each file are the (x,y,z) Cartesian coordinates in \[Bohr\].

The fourth and the fifth columns are the charge density values and the corresponding AFQMC statistical error bars, in \[Bohr^(-3)\].

For DFT densities the fifth column is blank.

There is 1 empty line after each xy-block (within which the x and y coordinates are the same, and z is varied), and 2 extra empty lines after each x-block.

## 1D-route density data format

The first column is the distance along the route.

The 2nd~4th columns are the (x,y,z) Cartesian coordinates in \[Bohr\].

The last two columns are the QMC density and statistical error bar, in \[Bohr^(-3)\].
