## Semismooth and Suboptimal Methods for Real-time Optimization
This is a summary page for our research on a variety of methods for real-time optimization, primarily using suboptimal and semismooth techniques with a focus on applications to Model Predictive Control (MPC). It includes several methods for quadratic programming (FBRS, FBstab), suboptimal parametric nonlinear programming (TDO, SSPC) and Optimal Control Problems (Sens) as well as tools for applying suboptimal (MPC) directly in continuous time (DE-MPC).

## Methods
### (FBRS) Fischer-Burmeister Regularized and Smoothed
This method applies the semismooth Newton's method to derive a quadratic programming solver which is useful for embedded optimization and parameterized problems.

Publications:

* D. Liao-McPherson, M. Huang, and I. Kolmanovsky, “A regularized and smoothed fischer-burmeister method for quadratic programming with applications to model predictive control,” IEEE Transactions on Automatic Control, 2018, [[Preprint](https://arxiv.org/abs/1807.03214)] [[Article](10.1109/TAC.2018.2872201)]

### (FBstab) Proximally Stabilized Fischer-Burmeister 
An extension of FBRS that adds proximal regularization to improve its theoretical properties and practical performance.

Publications:

* D. Liao-McPherson and I. Kolmanovsky, “FBstab: A proximally stabilized semismooth algorithm for convex quadratic programming,” Automatica, vol. 113, p. 108801, 2020 [[Preprint](https://arxiv.org/pdf/1901.04046.pdf)] [[Article](https://doi.org/10.1016/j.automatica.2019.108801)]
* D. Liao-McPherson* and I. Kolmanovsky, “The FBstab algorithm for model predictive control: An implicit condensing approach,” in 2019 IEEE 58th Conference on Decision and Control (CDC), (Nice, France), pp. 3370–3376, IEEE [[Article](https://ieeexplore.ieee.org/abstract/document/9029950)]

Implementations:

* [MATLAB](https://github.com/dliaomcp/fbstab-matlab)
* [C++](https://github.com/dliaomcp/fbstab)

### (SSPC) Semismooth Predictor Corrector
The SSPC method solves parametric nonlinear programs by transforming their necessary conditions into a parameterized semismooth rootfinding problem and applying an Euler-Newton predictor/corrector method.

Publications:

* D. Liao-McPherson, M. Nicotra, and I. Kolmanovsky, “A semismooth predictor corrector method for real-time constrained parametric optimization with applications in model predictive control,” in Proceedings of the 2018 IEEE Conference on Decision and Control (CDC), (Miami Beach, Florida), pp. 3600–3607, IEEE, 2018, [[Preprint](https://arxiv.org/pdf/1812.01634.pdf)] [[Article](10.1109/CDC.2018.8619823)]

### (TDO) Time Distributed Optimization

TDO is a hybrid optimization/systems thoretic method for implementing nonlinear model predictive control. It extends the popular real-time iteration scheme (which is a instance of time-distributed sequential quadratic programming) [[RTI1](10.1049/ip-cta:20040008)] [[RTI2](https://doi.org/10.1137/S0363012902400713)].

Publications:

* D. Liao-McPherson, M. Nicotra, and I. Kolmanovsky, “Time-distributed optimization for real-time model predictive control: Stability, robustness, and constraint satisfaction,” Automatica, vol. 117, p. 108973, 2020 [[Preprint](https://arxiv.org/pdf/1903.02605.pdf)] [[Article](https://doi.org/10.1016/j.automatica.2020.108973)]

* D. Liao-McPherson*, M. M. Nicotra, and I. V. Kolmanovsky, “A semismooth predictor corrector method for suboptimal model predictive control,” in 2019 18th European Control Conference (ECC), (Naples, Italy), pp. 2749–2755, June 2019 [[Preprint](http://arxiv.org/abs/1905.02684)] [[Article](https://ieeexplore.ieee.org/document/8796089)] \(Best student paper finalist (Top 5)\)




### (DE-MPC) Dynamically Embedded Model Predictive Control
DE-MPC is a continous time suboptimal MPC technique; it embeds a an MPC feedback law in a continous time feedback that runs in parallel with the plant. Notably it can be implemented as a dynamic system, i.e., without explicitly calling and optimization routine.

Publications:

* M. Nicotra, D. Liao-McPherson, and I. Kolmanovsky, “Embedding constrained model predictive control in a continuous-time dynamic feedback,” IEEE Transactions on Automatic Control, 2018, [[Preprint](https://arxiv.org/abs/1709.06499)] [[Article](10.1109/TAC.2018.2867359)]
* M. Nicotra, D. Liao-McPherson, and I. Kolmanovsky, “Dynamically embedded model predictive control,” in Proceedings of the 2018 Annual American Control Conference (ACC), (Milwaukee Wisconsin), pp. 4957–4962, June 2018[[Article](10.23919/ACC.2018.8431770)]

### (Sens) Sensitivity based-warmstarting
Sensitivity based-warmstarting uses semi-derivaties to predict the change in the solutions of optimal control problems in response to a parameter change and can be used to accelerate MPC algorithms.

Publications:

* D. Liao-Mcpherson, M. Nicotra, A. Dontchev, I. Kolmanovsky, and V. Veliov, “Sensitivity-based warmstarting for nonlinear model predictive control with polyhedral state and control constraints,” IEEE Transactions on Automatic Control, pp. 1–7, August 2020 [[Article](https://ieeexplore.ieee.org/document/8906134)]

## Applications

### Aerospace
* M. M. Nicotra, D. Liao-McPherson, L. Burlion, and I. V. Kolmanovsky, “Spacecraft attitude control with nonconvex constraints: An explicit reference governor approach,” IEEE Transactions on Automatic Control, vol. 65, no. 8,
pp. 3677–3684, 2020, [[Preprint](https://arxiv.org/pdf/1905.00387.pdf)] [[Article](https://doi.org/10.1109/TAC.2019.2951303)]
* A. Berning Jr., D. Liao-McPherson, A. Girard, and I. Kolmanovsky, “Suboptimal nonlinear model predictive control strategies for tracking near rectilinear halo orbits,” in 2020 AAS/AIAA Astrodynamics Specialist Conference, (Lake Tahoe, California), American Astronautical Society (AAS), August 2020

### Automotive
* D. Liao-McPherson, K. Shinhoon, M. Huang, M. Shimada, K. Butts, and I. Kolmanovsky, “Model predictive emissions control of a diesel engine airpath: Design and experimental evaluation,” To appear in the International Journal of Robust and Nonlinear Control, 2020
* M. R. Amini, H. Wang, X. Gong, D. Liao-McPherson, I. Kolmanovsky, and J. Sun, “Cabin and battery thermal management of connected and automated HEVs for improved energy efficiency using hierarchical model predictive control,” IEEE Transactions on Control Systems Technology, vol. 28, no. 5, pp. 1711–1726, 2020 [[Article](https://doi.org/10.1109/TCST.2019.2923792)]

### Contributors 
* [Dominic Liao-McPherson](https://scholar.google.ca/citations?user=llSJCuUAAAAJ&hl=en&oi=ao)
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

