# Orbit
A python automation script for optimizing ligands with ORCA and testing their binding affinity in multiple receptors using AutoDock Vina

This script has the following dependencies:
 - Orca 6.0.0.0
 - OpenBabel
 - AutoDock Vina
 - Python

In order to properly run the script
1) Place all ligands in the "ligands" folder with extension .xyz. For ligands already optimized there must be a version in this folder with another copy placed in the "orca_optimized" folder. Optimized files must have the same name with "_optimized" following. Note: the location of the ligands folder can be modified in the config.ini file.
2) Place all receptors in the folder "receptors", with extension .pdbqt. Each receptor must have its own section in the config.ini file with name "receptor_name". Note: the location of the receptors folder can be modified in the config.ini file.
3) Point to the directory of the Orca and AutoDock Vina programs in the configuration file.
4) Modify any other settings you desire in the config.ini file.
5) Run the script using "python Orbit_1.0.0.py"

Results will be saved in .csv files found in the results folder. Optimized ligands will be found in the orca_optimized folder.

If you use this software for publication, please cite the relevant papers for ORCA and AutoDock Vina, as well as those for the functionals and basis you used
:
(1) Neese,F.; Wennmohs,F.; Becker,U.; Riplinger,C. “The ORCA quantum chemistry program package” J. Chem. Phys., 2020 152 Art. No. L224108
(2) Neese, F. “Software update: The ORCA program system—Version 5.0” Wiley Interdisciplinary Reviews: Computational Molecular Science, 2022, Vol. 12, Issue 5, p. e1606.
(3) J. Eberhardt, D. Santos-Martins, A. F. Tillack, and S. Forli. (2021). AutoDock Vina 1.2.0: New Docking Methods, Expanded Force Field, and Python Bindings. Journal of Chemical Information and Modeling.
(4) O. Trott, A. J. Olson, AutoDock Vina: improving the speed and accuracy of docking with a new scoring function, efficient optimization and multithreading, Journal of Computational Chemistry 31 (2010) 455-461

For any comments or suggestions, please contact me on GitHub, "kin6dom", or via email: jtk.void@gmail.com. Thanks for using the program.

Version 1.0.0 features:
 - Will optimize ligands and analyze their binding affinity for multiple receptors.
 - Allows for the selection of functional and basis set.
 - Allows for the selection of number of processors.
 - Allows for the determination of receptor active site grid.
 - Allows for the selection of binding exhaustiveness and number of modes.
 - Will skip optimization of already optimized ligands and determine their binding affinity.
 - Saves binding affinity results to a .csv file.
 - Saves results of ligand optimization.
