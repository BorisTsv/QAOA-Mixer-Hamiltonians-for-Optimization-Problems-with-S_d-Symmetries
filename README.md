We present codes for simulations of two QAOA algorithms utilizing different mixer Hamiltonians: the classical one, represented by B=∑X_i, 
and the mixer H_M equivariant with resoect to the action of symmetric group S_d, introduced in the paper 'Equivariant QAOA and the Duel of the Mixers' 
for the edge coloring and graph partitioning problems. We employ the following iterative implementation of the algorithms:

the algorithms begin by establishing the initial state, where the initial pair of parameters beta_1,gamma_1 are randomly selected from a uniform distribution. 
Subsequently, the algorithm iterates through runs: after completing the p=1 run, optimal values beta*_1,\gamma*_1 are determined with the aid of a classical optimizer.
The subsequent QAOA run is then executed with starting parameters (\beta^*_1,gamma^*_1,0,0) for p=2, and this process continues iteratively. The objective of the classical 
optimizer is to minimize the energy, which is defined as the average value of the objective function on the states output by the algorithm over multiple runs.
