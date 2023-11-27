## MC_HEA
* This is the data analysis (data+code) for the paper [Monte Carlo simulation of order-disorder transition in refractory high entropy alloys: A data-driven approach](https://www.sciencedirect.com/science/article/abs/pii/S0927025620306261?via%3Dihub)
* The data of random generated configurations, using suercells of different sizes, are store at Random_<HEA> (e.g. Random_MoNbTaW). The configurations generated from MC simulation at different temperatures, are stored at MC_<HEA> (e.g. MC_MoNbTaW)。
* The energy unit is Ryderbergy, i.e, about 13.6 eV
* In Random_<HEA>, there are a few <n>Atom directories, which are the data for n-atom supercells. In <n>Atom, there are different random configurations, where the file name is just the index. For example, in Random_MoNbTaW/128Atom/1/ there are three files: 
    * position.dat: The position files, including lattice constant, unit vectors, elements info, and positions. This is the format for the MuST/MST code: See https://github.com/mstsuite/MuST/tree/master/MST
    * MadelungShiftTable: this is a table generated by MST. It contains information of the local information, such as local charge, and energy, for each atom, obtained from integrate the Green's function at real space with the local polyhedron. This file is not used, but can be tested for fun for machine learning models using local information (the dataset size would be much larger since it scales with the number of atoms)
    * k_n0000_<HEA>: this is the self-consistent calculation output of the MuST/MST code. Only the last energy is used for the data analysis since that is the converged value.
    * The jupyter notebook: MC_HEA.ipynb contains the data analysis codes. It should be self-explanatory.
    * If you have question, feel free to contact me at xianglinliu01@gmail.com

To be finishd
