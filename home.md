---
layout: page
title: About
---
## Introduction ##
***   
mSOUND is an open-source toolbox written in [MATLAB](https://www.mathworks.com/products/matlab.html). This toolbox is intended for modeling linear/nonlinear wave propagation in biological tissue with arbitrary heterogeneities, in which speed of sound, density, attenuation coefficient, power law exponent, and nonlinear coefficient are all spatially varying functions. The governing equation used in this software is the generalized Westervelt equation. While the algorithm is developed based on the one-way propagation approximation, users have the option to include reflections. In the current version, mSOUND contains two methods for modeling wave proapgation and they are the transient mixed-domain method (TMDM) and frequency-specific mixed-domain method (FSMDM). The TMDM generates the results in the time domain while FSMDM generates the simulation results directly at the specific frequencies of interest, which are the center frequency and the second harmonics. The latter should only be used if linear or weakly nonlinear wave propagation is considered. While the TMDM is advantageous for modeling pulsed-waves and arbitrary nonlinearity, FSMDM is more suited for modeling continuous waves. 
   

## Download
[Download version 1.0](https://github.com/m-SOUND/FileDownloader/MDM_code.zip" download="MDM_code.zip)               


## Acknowledgment
This project is supported by the [National Institute of Health (NIH)](https://www.nih.gov/) under the Grant R01EB025205. Juanjuan Gu was also supported by a fellowship from China Scholarship Council (CSC) during her Ph.D. study in [North Carolina State University](https://www.ncsu.edu/).         

## References
<p>[ 1 ] Juanjuan Gu and Yun Jing, "Simulation of the second harmonic ultrasound field in heterogeneous soft tissue using a mixed domain method," IEEE Ultrasonics, Ferroelectrics, and Frequency Control Society, 66, 669-675, 2019. <a href="https://github.com/MDM-series/MDM/tree/master/download/FSMDM.pdf" download="FSMDM.pdf">Download pdf</a></p>  

<p>[ 2 ] Juanjuan Gu and Yun Jing, "Numerical Modeling of Ultrasound Propagation in Weakly Heterogeneous Media Using a Mixed Domain Method," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 65, 1258-1267, 2018. <a href="https://github.com/MDM-series/MDM/tree/master/download/MDM.pdf" download="MDM.pdf">Download pdf</a></p>      
   
<p>[ 3 ] Juanjuan Gu and Yun Jing, "Modeling of wave propagation for medical ultrasound: a review," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 62, 1979-1992, 2015. <a href="https://ieeexplore.ieee.org/abstract/document/7321705" download="review.pdf">Download pdf</a></p>        

<p>[ 4 ] Yun Jing, "On the use of an absorption layer for the angular spectrum approach (L)," The Journal of the Acoustical Society of America, 131, 999-1002, 2012. <a href="https://asa.scitation.org/doi/10.1121/1.3675967" download="review.pdf">Download pdf</a></p> 

<p>[ 5 ] Yun Jing, Molei Tao, and Greg T. Clement, "Evaluation of a wave-vector-frequency-domain method for nonlinear wave propagation," The Journal of the Acoustical Society of America,129, 32-46, 2011. <a href="https://asa.scitation.org/doi/abs/10.1121/1.3504705" download="WVFD.pdf">Download pdf</a></p>       


## License
This project is licensed under the [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.txt).  

