# Data for: Real space simulation for state-resolved high-resolution atomic force microscopy of defects in monolayer h-BN

## Citation
This repository contains the input files and calculated data used to generate the results and figures for the manuscript:  
Zhao Tang, Dingxin Fan, and James R. Chelikowsky, *Real space simulation for state-resolved high-resolution atomic force microscopy of defects in monolayer h-BN*, submitted to Physical Review Materials (2025).  

## Repository contents
The repository is organized by the system simulated. Each top-level directory contains the data for a specific sample (or tip) structure and electronic state.  

```
.
├── cbvn_s1_up/
├── cbvn_s1_down/
├── cbvn_s2/
├── hbn_co/
├── hbn_cu/
└── README.md
```

* `cbvn_s1_up/`: Data for the <sup>1</sup>*A*<sub>1</sub> state of the C<sub>B</sub>V<sub>N</sub> defect with the carbon atom displaced upward.
* `cbvn_s1_down/`: Data for the <sup>1</sup>*A*<sub>1</sub> state of the C<sub>B</sub>V<sub>N</sub> defect with the carbon atom displaced downward.
* `cbvn_s2/`: Data for the <sup>3</sup>*B*<sub>2</sub> state of the C<sub>B</sub>V<sub>N</sub> defect with a planar structure.
* `hbn_co/`: Data for the pristine h-BN monolayer with a CO tip.
* `hbn_cu/`: Data for the pristine h-BN monolayer with a Cu tip.

We utilized the frozen density embedding theory (FDET) to accelerate AFM simulations, where the sample is treated as a frozen external field.
Within each main system directory (e.g., `cbvn_s1_up/`), there are multiple subdirectories named `seq_i_j` and one subdirectory named `spot`. The `spot` directories contains input files for the sample potential field calculation. Input files for the tip sampling calculations are in the `seq_i_j` subdirectories, where `i` represents the vertical (*z*) index and `j` represents an index for parallel performed jobs.

The output data are stored in the `toten.dat` files for each system, which contain the total energies on the tip sampling grid.
