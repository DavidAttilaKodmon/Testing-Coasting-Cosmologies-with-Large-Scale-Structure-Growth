## Repository for "Probing the Growth of Large-Scale Structures in a Coasting Universe"

This repository contains the programs used to perform the curve fitting and Anderson-Darling tests for the article **Probing the Growth of Large-Scale Structures in a Coasting Universe** by Dávid A. Ködmön (Institute of Physics and Astronomy, ELTE Eötvös Loránd University, 1117 Budapest, Hungary) and Péter Raffai (Institute of Physics and Astronomy, ELTE Eötvös Loránd University, 1117 Budapest, Hungary; HUN-REN–ELTE Extragalactic Astrophysics Research Group, 1117 Budapest, Hungary), submitted to the  _The Astrophysical Journal_ on the 14th of October, 2024. 

Corresponding author: Dávid A. Ködmön (davidkodmon@student.elte.hu)

- Dependencies:
   - **Python 3**
   - **`numpy`**
   - **`emcee`**
   - **`scipy`**
   - **`tqdm`**

#### Structure of the Fitting Codes
In order to fit the $f\sigma_8(z)$ values in _fsigma_8_dataset.csv_ to a theoretical $f\sigma_8(z)$, the dataset has to be recalibrated to account for the fact that the data points were obtained under the assumption of a fiducial cosmology which differs from the one for which the theoretical $f\sigma_8(z)$ curve is valid. This recalibration can achieved by multiplying the data points and their correspoding uncertainties with a correction factor, $q(z, \Omega_\rm{m,0}, \Omega_{\rm{m,0}}^{\rm{fid}}) = \frac{H(z)D_\rm{A}(z)}{H^\rm{fid}(z)D^\rm{fid}_{\rm{A}}(z)}$ (<a href="https://journals.aps.org/prd/abstract/10.1103/PhysRevD.97.103503">Kazantzidis and Leandros (2018)</a>). The curve fitting was performed using the **emcee** implementation of the MCMC alogrithm by <a href="https://iopscience.iop.org/article/10.1086/670067">Foreman-Mackey et al. (2013)</a>.  


#### Data Sources
The data in _fsigma_8_dataset.csv_ originate from **Table VI.** in **Tension of the $𝐸_𝐺$ statistic and redshift space distortion data with the Planck-ΛCDM model and implications for weakening gravity** by <a href="https://journals.aps.org/prd/abstract/10.1103/PhysRevD.101.063521">Skara and Perivolaropoulos (2020)</a>.  

The data file _Data_for_AD_test.mat_ was generated using the Jupyter Notebooks found in this repository. One need only uncomment the relevant part of the code where the recalibrated data points are saved to file in order to obtain the data files which were imported into MATLAB to create _Data for AD test.mat_. 

#### General Information
Should the comments and markups in the Jupyter Notebooks, the MATLAB Live Script, as well as the article's text itself, combined with the documentation of **emcee** (available at emcee.readthedocs.io/en/v3.1.6) and of the MATLAB implementation of the Anderson-Darling test (www.mathworks.com/help/stats/adtest.html) prove insufficient to understand and run the programs, feel free to ask questions you may have!



