O number is O4772  
# PPGN: Physics-Preserved Graph Networks for Real-Time Fault Location in Distribution Systems with Limited Observation and Labels
=============================

* PPGN is a two-stage graph neural network architecture to locate the fault on the node level in power grids. Refer to our paper [1] for details. 
* This demo is implemented in the Western Electricity Coordinating Council (WECC) 179-bus [2].  Only 55 buses with more than two connection degrees are measured for the detection and location algorithms.  At each measured bus, we have magnitudes & angles of voltages and reactive and active powers. 
* Total 1899 faults occur at all possible buses at 1 second and are cleared after 0.03 second. There are random 70% of the datasets for training and the remaining for testing. 
* To monitor the power system with the streaming data automatically, we include a subspace-based fault detection algorithm [3] that is executed before PPGN locating the faults.  


## A Pytorch-based implementation of PPGN on Jupyter Notebook includes the main following files:
 
* trained (folder): saves the saved or pre-trained models     
* Training_123nodes: trains the datasets offline with two stages
* Testing_123nodes: tests the location accuracy rates online with the trained models 
* load_data.py, PPGN.py, util_final: these files include some useful functions for training. 

# Reference
------------------------------

[1] Wenting Li, Deepjyoti Deka, “PPGN: Physics-Preserved Graph Networks for Fault Location with Limited Observation and Labels”, accepted by Hawaii International Conference on System Sciences (HICSS). IEEE, 2022.  

© 2024. Triad National Security, LLC. All rights reserved.

This program was produced under U.S. Government contract 89233218CNA000001 for Los Alamos National Laboratory (LANL), which is operated by Triad National Security, LLC for the U.S. Department of Energy/National Nuclear Security Administration. All rights in the program are reserved by Triad National Security, LLC, and the U.S. Department of Energy/National Nuclear Security Administration. The Government is granted for itself and others acting on its behalf a nonexclusive, paid-up, irrevocable worldwide license in this material to reproduce, prepare. derivative works, distribute copies to the public, perform publicly and display publicly, and to permit others to do so.
 
