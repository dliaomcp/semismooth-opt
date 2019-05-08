## Semismooth and Suboptimal Methods for Real-time Optimization
This is a summary page for our research on a variety of methods for real-time optimization, primarily using suboptimal and semismooth techniques with a focus on applications to Model Predictive Control (MPC). It includes several methods for quadratic programming (FBRS, FBstab), suboptimal parametric nonlinear programming (TD-SQP, SSPC) and Optimal Control Problems (Sens) as well as tools for applying suboptimal (MPC) directly in continuous time (DE-MPC).

## Methods
### (FBRS) Fischer-Burmeister Regularized and Smoothed
This method applies the semismooth Newton's method to derive a quadratic programming solver which is useful for embedded optimization and parameterized problems.

Publications:

* D. Liao-McPherson, M. Huang, and I. Kolmanovsky, “A regularized and smoothed fischer-burmeister method for quadratic programming with applications to model predictive control,” IEEE Transactions on Automatic Control, 2018, [[Preprint](https://arxiv.org/abs/1807.03214)] [[Article](10.1109/TAC.2018.2872201)]

### (FBstab) Proximally Stabilized Fischer-Burmeister 
An extension of FBRS that adds proximal regularization to improve its theoretical properties and practical performance.

Publications:

* D. Liao-McPherson and I. Kolmanovsky, “FBstab: A stabilized semismooth algorithm for quadratic programming with applications in model predictive control,” [[Preprint](https://arxiv.org/pdf/1901.04046.pdf)]
* D. Liao-McPherson and I. Kolmanovsky, “The FBstab algorithm for model predictive control: An implicit condensing approach,

Implementations:

* [MATLAB](https://github.com/dliaomcp/fbstab-matlab)
* [C++](https://github.com/dliaomcp/fbstab-cpp) (Coming soon)

### (TD-SQP) Time Distributed Sequential Quadratic Programming

TD-SQP is a hybrid optimization/systems thoretic method for implementing nonlinear model predictive control. It extends the popular real-time iteration scheme [[RTI1](10.1049/ip-cta:20040008)] [[RTI2](https://doi.org/10.1137/S0363012902400713)].

Publications:

* D. Liao-McPherson, M. Nicotra, and I. Kolmanovsky, “Time distributed sequential quadratic programming for model predictive control: Stability and robustness,” [[Preprint](https://arxiv.org/pdf/1903.02605.pdf)]


### (SSPC) Semismooth Predictor Corrector
The SSPC method solves parametric nonlinear programs by transforming their necessary conditions into a parameterized semismooth rootfinding problem and applying an Euler-Newton predictor/corrector method.

Publications:

* D. Liao-McPherson, M. Nicotra, and I. Kolmanovsky, “A semismooth predictor corrector method for real-time constrained parametric optimization with applications in model predictive control,” in Proceedings of the 2018 IEEE Conference on Decision and Control (CDC), (Miami Beach, Florida), pp. 3600–3607, IEEE, 2018, [[Preprint](https://arxiv.org/pdf/1812.01634.pdf)] [[Article](10.1109/CDC.2018.8619823)]
* D. Liao-McPherson, M. Nicotra, and I. Kolmanovsky, “A semismooth predictor corrector method for suboptimal model predictive control,” in To appear at the European Control Conference (ECC), (Naples Italy), IFAC, 2019, [[Preprint](http://arxiv.org/abs/1905.02684)]

### (DE-MPC) Dynamically Embedded Model Predictive Control
DE-MPC is a continous time suboptimal MPC technique; it embeds a an MPC feedback law in a continous time feedback that runs in parallel with the plant. Notably it can be implemented as a dynamic system, i.e., without explicitly calling and optimization routine.

Publications:

* M. Nicotra, D. Liao-McPherson, and I. Kolmanovsky, “Embedding constrained model predictive control in a continuous-time dynamic feedback,” IEEE Transactions on Automatic Control, 2018, [[Preprint](https://arxiv.org/abs/1709.06499)] [[Article](10.1109/TAC.2018.2867359)]
* M. Nicotra, D. Liao-McPherson, and I. Kolmanovsky, “Dynamically embedded model predictive control,” in Proceedings of the 2018 Annual American Control Conference (ACC), (Milwaukee Wisconsin), pp. 4957–4962, June 2018[[Article](10.23919/ACC.2018.8431770)]

### (Sens) Sensitivity based-warmstarting
Sensitivity based-warmstarting uses semi-derivaties to predict the change in the solutions of optimal control problems in response to a parameter change and can be used to accelerate MPC algorithms.

* A. Dontchev, D. Liao-Mcpherson, I. Kolmanovsky, M. Nicotra, and V. Veliov, “Sensitivity-based warmstarting for constrained model predictive control,”

## Applications

* M. Nicotra, D. Liao-McPherson, L. Burlion, and I. Kolmanovsky, “Spacecraft attitude control with nonconvex constraints: An explicit reference governor approach,” [[Preprint](https://arxiv.org/pdf/1905.00387.pdf)]

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

