---
layout: page
title: About
---
## Introduction ##
***   
mSOUND is an open-source toolbox for [MATLAB](https://www.mathworks.com/products/matlab.html) and developed by [Juanjuan Gu](https://www.researchgate.net/profile/Juanjuan_Gu) and [Yun Jing](https://www.mae.ncsu.edu/jing/). This toolbox is intended for modeling one-way linear/nonlinear wave propagation in biological tissue with arbitrary heterogeneities, in which speed of sound, density, attenuation coefficients, power law exponent and nonlinear coefficients are all spatially varying functions. The governing equation used in this software is the Westervelt equation. In the current version, mSOUND contains two methods for modeling wave proapgation and they are transient mixed-domain method (TMDM) and frequency-specific mixed-domain method (FSMDM).TMDM can generate the simulation results in the time domain and FSMDM generates the simulation results directly at the specific frequencies of interest, which are the center frequency and the 2nd harmonics. The latter is only modeled if weakly nonlinear propagation is considered. While TMDM is advantageous for modeling pulses, FSMDM is more suited for modeling continuous waves. In addition, for the cases where nonlinearity is moderate or strong, TMDM should always be used.               
   

## Download
[Download version 1.0](https://github.com/m-SOUND/FileDownloader/MDM_code.zip" download="MDM_code.zip)               


## Acknowledgment
This project is supported by the [National Institute of Health (NIH)](https://www.nih.gov/) under the Grant R01EB025205. Juanjuan Gu was also supported by a fellowship from China Scholarship Council (CSC) during her Ph.D. study in [North Carolina State University](https://www.ncsu.edu/).         

## References
<p>[ 1 ] Juanjuan Gu and Yun Jing, "Simulation of the second harmonic ultrasound field in heterogeneous soft tissue using a mixed domain method," IEEE Ultrasonics, Ferroelectrics, and Frequency Control Society, 2019. <a href="https://github.com/MDM-series/MDM/tree/master/download/FSMDM.pdf" download="FSMDM.pdf">Download pdf</a></p>  

<p>[ 2 ] Juanjuan Gu and Yun Jing, "Numerical Modeling of Ultrasound Propagation in Weakly Heterogeneous Media Using a Mixed Domain Method," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 65, 1258-1267, 2018. <a href="https://github.com/MDM-series/MDM/tree/master/download/MDM.pdf" download="MDM.pdf">Download pdf</a></p>      
   
<p>[ 3 ] Juanjuan Gu and Yun Jing, "Modeling of wave propagation for medical ultrasound: a review," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 62, 1979-1992, 2015. <a href="https://ieeexplore.ieee.org/abstract/document/7321705" download="review.pdf">Download pdf</a></p>         

<p>[ 4 ] Jing Yun, Molei Tao, and Greg T. Clement, "Evaluation of a wave-vector-frequency-domain method for nonlinear wave propagation," The Journal of the Acoustical Society of America,129, 32-46, 2011. <a href="https://asa.scitation.org/doi/abs/10.1121/1.3504705" download="WVFD.pdf">Download pdf</a></p>       


## License
This project is licensed under the [GNU General Public License v3.0](license.md).   
