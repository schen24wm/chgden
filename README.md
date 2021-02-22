# AFQMC Charge Density

All densities are finite-size (FS) corrected AFQMC densities. FS corrections use formula (31) in the paper; an average of 12 quasi-random K-points is used for Cu.

Due to the pseudopotential core effect, all direct comparisons with QMC densites should use the same pseudopotential as (in Appendix A of) the paper.

## Naming convention of the files

> {SYSTEM}\_P{plottingCell}\_F{dataFromSupercell}\_{FFTGridSize}\_{Unit}

{SYSTEM} is the name of the system. "-NeCore" for Cu indicates this density is calculated using the Ne-core pseudopotential.

## Data format

The first three columns of each file are the (x,y,z) Cartesian coordinates in {Unit}. In our case, the unit for all systems is Bohr.

The fourth and last column is the electron charge density, in {Unit}^(-3) -- in our case Bohr^(-3).

1 empty line after each xy-block (within which the x and y coordinates are the same), and 2 extra empty lines after each x-block.
