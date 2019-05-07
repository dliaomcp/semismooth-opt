## Semismooth and Suboptimal Methods for Real-time Optimization
This is a summary page for our research on a variety of methods for real-time optimization, primarily using suboptimal and semismooth techniques with a focus on applications to Model Predictive Control (MPC). It includes several methods for quadratic programming (FBRS, FBstab), suboptimal parametric nonlinear programming (TD-SQP, SSPC) and Optimal Control Problems (Sens) as well as tools for applying suboptimal (MPC) directly in continuous time (DE-MPC).

## Methods
### (FBRS) Fischer-Burmeister Regularized and Smoothed
This method applies the semismooth Newton's method to derive a quadratic programming solver which is useful for embedded optimization and parameterized problems.

Publications:

* A Regularized and Smoothed Fischer-Burmeister Method for Quadratic Programming with Applications to Model Predictive Control
[[Preprint](https://arxiv.org/abs/1807.03214)] [[Article](10.1109/TAC.2018.2872201)]

### (FBstab) Proximally Stabilized Fischer-Burmeister 
An extension of FBRS that adds proximal regularization to improve its theoretical properties and practical performance.

Publications:

* FBstab: A proximally stabilized semismooth algorithm for convex quadratic programming [[Preprint](https://arxiv.org/pdf/1901.04046.pdf)]
* The FBstab Quadratic Programming Method Applied to Model Predictive Control: An Implicit Condensing Approach

Implementations:

* [MATLAB](https://github.com/dliaomcp/fbstab-matlab)
* [C++](https://github.com/dliaomcp/fbstab-cpp) (Coming soon)

### (TD-SQP) Time Distributed Sequential Quadratic Programming

TD-SQP is a hybrid optimization/systems thoretic method for implementing nonlinear model predictive control. It extends the popular real-time iteration scheme [[RTI1](10.1049/ip-cta:20040008)] [[RTI2](https://doi.org/10.1137/S0363012902400713)].

Publications:

* Time Distributed Sequential Quadratic Programming for Model Predictive Control: Stability and Robustness [[Preprint](https://arxiv.org/pdf/1903.02605.pdf)]


### (SSPC) Semismooth Predictor Corrector
The SSPC method solves parametric nonlinear programs by transforming their necessary conditions into a parameterized semismooth rootfinding problem and applying an Euler-Newton predictor/corrector method.

Publications:

* A Semismooth Predictor Corrector Method for Real-Time Constrained Parametric Optimization with Applications in Model Predictive Control [[Preprint](https://arxiv.org/pdf/1812.01634.pdf)] [[Article](10.1109/CDC.2018.8619823)]
* A Semismooth Predictor Corrector Method for Suboptimal Model Predictive Control 

### (DE-MPC) Dynamically Embedded Model Predictive Control
DE-MPC is a continous time suboptimal MPC technique; it embeds a an MPC feedback law in a continous time feedback that runs in parallel with the plant. Notably it can be implemented as a dynamic system, i.e., without explicitly calling and optimization routine.

Publications:

* Embedding Constrained Model Predictive Control in a Continuous-Time Dynamic Feedback [[Preprint](https://arxiv.org/abs/1709.06499)] [[Article](10.1109/TAC.2018.2867359)]
* Dynamically Embedded Model Predictive Control, American Control Conference (ACC) 2018 [[Article](10.23919/ACC.2018.8431770)]

### (Sens) Sensitivity based-warmstarting
Sensitivity based-warmstarting uses semi-derivaties to predict the change in the solutions of optimal control problems in response to a parameter change and can be used to accelerate MPC algorithms.

* Sensitivity-based Warmstarting for Constrained
Model Predictive Control

## Applications

* Spacecraft Attitude Control with Nonconvex Constraints:
An Explicit Reference Governor Approach [[Preprint](https://arxiv.org/pdf/1905.00387.pdf)]

### Contributors 
* [Dominic Liao-McPherson](https://vodca.engin.umich.edu/profile/dominic-liao-mcpherson/)
* Mike Huang
* [Ilya Kolmanovsky](https://aero.engin.umich.edu/people/ilya-kolmanovsky/)
* [Marco Nicotra](https://www.colorado.edu/faculty/nicotra/)
* [Asen Dontchev](https://sites.google.com/site/adontchev/)
* [Vladimir Veliov](https://orcos.tuwien.ac.at/people/veliov/)
* [Laurent Burlion](https://mae.rutgers.edu/laurent-burlion)

### Funding
* [National Science Foundation](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1562209) (CMMI 1562209)
* [Toyota Research Instituite](https://bec.umich.edu/um-tri/semi-smooth-and-variational-methods-for-real-time-dynamic-optimization/)
* [Toyota Motors North America](https://www.toyota.com/usa/operations/map.html#!/ttc_ann_arbor_and_saline)

### Useful (external) toolboxes
* [ERGToolbox](https://github.com/acotorruelo/ERGToolbox): Software for implementing Explicit Reference Governors (ERGs)
* [ACADO](https://acado.github.io/): Software for real-time optimization
* [CASADI](https://web.casadi.org/): Automatic differentiation

