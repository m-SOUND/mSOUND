---
layout: page
title: About
---
## Introduction ##
***   
mSOUND is an open-source toolbox written in [MATLAB](https://www.mathworks.com/products/matlab.html). This toolbox is intended for modeling linear/nonlinear acoustic wave propagation in media (primarily biological tissues) with arbitrary heterogeneities, in which, the speed of sound, density, attenuation coefficient, power law exponent and nonlinear coefficient are all spatially varying functions. This toolbox is developed based on the generalized Westervelt equation. Unlike the conventional time-domain methods, the method employed by mSOUND computes the acoustic field by marching in the spatial domain (along the axis normal to the source plane) and can be viewed as an extended version of the angular spectrum approach (also known as the wave-vector frequency-domain method). The algorithm, when used to model wave propagation in heterogeneous media, toggles between the wave-vector domain and the real physical domain. This method is therefore called the mixed-domain method. While this mixed-domain method intrinsically considers one-way propagation, we have made the wave solver flexible so that reflections up to a desired order can be modeled in an ad hoc manner. In the current version, mSOUND encompasses two computationally efficient methods for modeling acoustic wave propagation and they are the transient mixed domain method (TMDM) and the frequency-specific mixed domain method (FSMDM). The TMDM generates the waveform at any point in space, while the FSMDM computes the steady-state pressure distribution directly at the frequencies of interest, which are the fundamental frequency and the second harmonics, assuming sinusoidal excitation. The latter should only be used if linear or weakly nonlinear wave propagation is considered. While the TMDM is advantageous for modeling pulsed-waves and arbitrary nonlinearity (from weakly nonlinear to strongly nonlinear wave propagation), FSMDM is more suited for modeling continuous waves which are used in conventional HIFU. Backward propagation is also included in mSOUND and it operates with both the TMDM and FSMDM.  With forward projection, the acoustic waveform or the steady-state pressure could be recorded at a given distance from the source plane, or more generally, any point in space. With backward projection, the recorded signals can be back-projected to reconstruct the source in space and time. 
   

## Download
[Download beta-version 0.1](https://github.com/m-SOUND/mSOUND/blob/master/download/mSOUND.zip)               


## Installation
1. Download and unpack the mSOUND.zip file to a suitable folder.
2. Add this file folder path to the MATLAB path. This can be done using the "Set Path" dialog box which is accessed by typing `pathtool` at the MATLAB command prompt. Once the dialog box is open, the toolbox is installed by clicking "Add Folder", selecting the mSOUND Toolbox folder, and clicking "save". Alternatively, the toolbox can be installed by adding the line: `addpath('...full pathname used above...\mSOUND')`;

## Acknowledgment
This project is supported by the [National Institute of Health (NIH)](https://www.nih.gov/) under the Grant R01EB025205. From 2015 to 2018, Juanjuan Gu was also supported by a fellowship award from China Scholarship Council (CSC).

## References
<p>[ 1 ] Juanjuan Gu and Yun Jing, "A modified mixed domain method for modeling acoustic wave propagation in strongly heterogeneous media," The Journal of the Acoustical Society of America, 147, 4055-4068, 2020. <a href="https://github.com/MDM-series/MDM/tree/master/download/MMDM.pdf" download="MMDM.pdf">Download pdf</a></p> 

<p>[ 2 ] Juanjuan Gu and Yun Jing, "Simulation of the second harmonic ultrasound field in heterogeneous soft tissue using a mixed domain method," IEEE Ultrasonics, Ferroelectrics, and Frequency Control Society, 66, 669-675, 2019. <a href="https://github.com/m-SOUND/mSOUND/tree/master/download/FSMDM.pdf" download="FSMDM.pdf">Download pdf</a></p>   

<p>[ 3 ] Juanjuan Gu and Yun Jing, "Numerical Modeling of Ultrasound Propagation in Weakly Heterogeneous Media Using a Mixed Domain Method," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 65, 1258-1267, 2018. <a href="https://github.com/m-SOUND/mSOUND/tree/master/download/MDM.pdf" download="MDM.pdf">Download pdf</a></p>       
   
<p>[ 4 ] Juanjuan Gu and Yun Jing, "Modeling of wave propagation for medical ultrasound: a review," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 62, 1979-1992, 2015. <a href="https://github.com/m-SOUND/mSOUND/tree/master/download/review.pdf" download="review.pdf">Download pdf</a></p>       

<p>[ 5 ] Yun Jing, "An improved wave-vector frequency-domain method for nonlinear wave modeling," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 61, 515-524, 2014. <a href="https://github.com/m-SOUND/mSOUND/blob/master/download/improved_WVFD.pdf" download="improved_WVFD.pdf">Download pdf</a></p> 

<p>[ 6 ] Yun Jing, "On the use of an absorption layer for the angular spectrum approach (L)," The Journal of the Acoustical Society of America, 131, 999-1002, 2012. <a href="https://github.com/m-SOUND/mSOUND/tree/master/download/Absorption_layer.pdf" download="Absorption_layer.pdf">Download pdf</a></p> 

<p>[ 7 ] Yun Jing, Molei Tao, and Greg T. Clement, "Verification of the westervelt equation for focused transducers," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 58, 1097-1101, 2011. <a href="https://github.com/m-SOUND/mSOUND/blob/master/download/Verification.pdf" download="Verification.pdf">Download pdf</a></p>  

<p>[ 8 ] Yun Jing, Molei Tao, and Greg T. Clement, "Evaluation of a wave-vector-frequency-domain method for nonlinear wave propagation," The Journal of the Acoustical Society of America,129, 32-46, 2011. <a href="https://github.com/m-SOUND/mSOUND/tree/master/download/WVFD.pdf" download="WVFD.pdf">Download pdf</a></p>   

## License
This project is licensed under the [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.txt).  

