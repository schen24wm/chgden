# chgden
AFQMC Charge Density

All densities are finite-size (FS) corrected AFQMC densities (FS corrections use formula (31) in the paper; an average of 12 quasi-random K-points is used for Cu).

Due to the pseudopotential core effect, all direct comparisons with QMC densites should use the same pseudopotential as in Appendix A of the paper.

Naming convention of the files are {SYSTEM}_P{plotting_cell}_C{data_from_supercell}_{FFT_grid_size}_{Unit}

The first three columns of each file are the (x,y,z) Cartesian coordinates in {Unit}. In our case, the unit for all systems is Bohr.

The fourth and last column is the electron charge density, in {Unit}^(-3) -- in our case Bohr^(-3).
