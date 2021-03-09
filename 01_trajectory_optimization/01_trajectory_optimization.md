[toc]

# Trajectory optimization

Trajectory optimization can be categorized into **direct collocation method** and **shooting method**.

* **Direct collocation method** eliminates the system dynamics constraints, the control inputs are calculated using inverse dynamics.
* **Shooting method** considers the control inputs as the decision variables and the trajectory can be obtained by forward simulation using system dynamic equation. Originally, shooting method is used to solved ODE problems, a concise tutorials on shooting method can be found [here](https://www.youtube.com/watch?v=ZMgikZ-lcS8). 
* A good course on optimal control is [here](https://github.com/Optimal-Control-16-745),  hope Zac will make this repo always public.

## Minimum Snap Trajectory Generation and Control for Quadrotors
[PDF](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5980409)    [code]()    [code by me](https://github.com/Garyandtang/ELEC5660-2021/tree/main/project1/proj1phase2)                                                By Daniel Mellinger and Vijay Kumar  

Classic trajectory generation paper with high citation. Major contributions on a **nonlinear controller** for quadrotor and a minimum snap **trajectory generation** method.

The trajectory generation is direct collocation method, it does the time allocation for all waypoints and uses polynomial curves to fit a smooth trajectory  between all watchpoints. The  problem is formulated as a **quadratic programming** with equality constraints, hence it can be easily solved with convex toolbox. The reason why this method works is the quadrotor is differentially flat $[x,y,z,\psi]^{T}$, which is proved in this paper.

The nonlinear controller: to be done once I am working on this

Some drawbacks:

* **Time allocation** should be done at the very beginning, how to allocate the time efficiently deserve to study. One paper by Gao Fei study optimal time allocation is here.

* **Dynamic infeasible.** Even through they proved that the quadrotor is differentially flat, the pitch and roll are not considered here. One method to solve this problem is that  using **inverse dynamics** to transfer pitch to force to acceleration and add it to constraint during optimization. I am not pretty sure about the singularity issue, deserve to study.

