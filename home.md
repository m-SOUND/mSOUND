---
layout: page
title: About
---
## Introduction ##
***   
mSOUND is an open-source toolbox written in [MATLAB](https://www.mathworks.com/products/matlab.html). This toolbox is intended for modeling linear/nonlinear acoustic wave propagation in media (primarily biological tissues) with arbitrary heterogeneities, in which, the speed of sound, density, attenuation coefficient, power law exponent and nonlinear coefficient are all spatially varying functions. This toolbox is developed based on the generalized Westervelt equation. Unlike the conventional time-domain methods, the method employed by mSOUND computes the acoustic field by marching in the spatial domain (along the axis normal to the source plane) and can be viewed as an extended version of the angular spectrum approach (also known as the wave-vector frequency-domain method). The algorithm, when used to model wave propagation in heterogeneous media, toggles between the wave-vector domain and the real physical domain. This method is therefore called the mixed-domain method. While this mixed-domain method intrinsically considers one-way propagation, we have made the wave solver flexible so that reflections up to a desired order can be modeled in an ad hoc manner. In the current version, mSOUND encompasses two computationally efficient methods for modeling acoustic wave propagation and they are the transient mixed domain method (TMDM) and the frequency-specific mixed domain method (FSMDM). The TMDM generates the waveform at any point in space, while the FSMDM computes the steady-state pressure distribution directly at the frequencies of interest, which are the fundamental frequency and the second harmonics, assuming sinusoidal excitation. The latter should only be used if linear or weakly nonlinear wave propagation is considered. While the TMDM is advantageous for modeling pulsed-waves and arbitrary nonlinearity (from weakly nonlinear to strongly nonlinear wave propagation), FSMDM is more suited for modeling continuous waves which are used in conventional HIFU. Backward propagation is also included in mSOUND and it operates with both the TMDM and FSMDM.  With forward projection, the acoustic waveform or the steady-state pressure could be recorded at a given distance from the source plane, or more generally, any point in space. With backward projection, the recorded signals can be back-projected to reconstruct the source in space and time. 

Please include a reference to our paper "mSOUND: An Open Source Toolbox for Modeling Acoustic Wave Propagation in Heterogeneous Media" on IEEE UFFC, if you write a paper that uses mSOUND. 
   

## Download
[Download beta-version 0.1](https://github.com/m-SOUND/mSOUND/blob/master/download/mSOUND v01.zip)      

[Download beta-version 0.2](https://drive.google.com/file/d/160gWslZgdyqTtsIOD2XYEBJuhaXd_32b/view?usp=sharing)   


## Installation
1. Download and unpack the mSOUND.zip file to a suitable folder.
2. Add this file folder path to the MATLAB path. This can be done using the "Set Path" dialog box which is accessed by typing `pathtool` at the MATLAB command prompt. Once the dialog box is open, the toolbox is installed by clicking "Add Folder", selecting the mSOUND Toolbox folder, and clicking "save". Alternatively, the toolbox can be installed by adding the line: `addpath('...full pathname used above...\mSOUND')`;

## Release note
(6/27/2022 by YJ) We are pleased to release the beta-version 0.2 of mSOUND. The most important change is that mSOUND is now signifcantly more accurate in modeling strongly inhomogeneous media, such as the skull. The comparison of mSOUND against other wave solvers (including k-wave) for modeling transcrnial ultrasound can be found in https://arxiv.org/abs/2202.04552. Please note that we have only modified and included Forward3D_fund and Forward3D_sec in this new version of mSOUND, as they are the most relevant codes for modeling therapeutic ultrasound. We are going to also modify the 2D (Forward2D, Forward2D_fund, Forward2D_sec, Backward2D, Backward2D_fund), and the rest of the 3D codes (Forward3D, Backward3D, Backward3D_fund) in the future. Other changes include: 
(1) for Forward3D_fund, there are now three solvers included: one is for weakly heterogeneous media (default one), one is for strongly heterogeneous one (like skull), and one is for layered media with arbitrary heterogeneities. When using the 2nd solver, you will need to enter a range of speed of sound of the medium under study.
For example, you can use [1500 2800] where 1500 is the minimum speed of sound in the problem (from the water, for example) while 2800 is the maximum speed of sound (from the maximum speed of sound in the skull, for example). You can enter more numbers in between such as [1500 2200 2800], but this is not guaranteed to give you more accurate results and the more numbers entered, the slower the computation. 
(2) In the beta-version 0.1 of mSOUND, for 3D simulations, the medium properties should be given as matrices with a size (mgrid.num_x, mgrid.num_y, mgrid.num_z+1).
Now you should just use a matrix of the size (mgrid.num_x, mgrid.num_y, mgrid.num_z), because that "+1" is now already considered in "set_grid". 
(3) We have updated the following examples "Simulation of a 3D homogeneous medium using the frequency-specific mixed domain method", "Simulation of a 3D heterogeneous medium using the frequency-specific mixed domain method", and added the following new examples "Integrating mSOUND with FOCUS for transducers of curved shape", "Comparison between the rigid boundary condition and pressure release boundary condition".

(4/9/2022 by YJ) version 0.1: this version was updated to fix some bugs. We are currently working on the next version of mSOUND to improve the modeling for strongly heterogeneous media. 


## References
<p>[ 1 ] Juanjuan Gu and Yun Jing, "mSOUND: An Open Source Toolbox for Modeling Acoustic Wave Propagation in Heterogeneous Media," IEEE Ultrasonics, Ferroelectrics, and Frequency Control Society, 2021. <a href="https://github.com/MDM-series/MDM/tree/master/download/MSOUND.pdf" download="MSOUND.pdf">Download pdf</a></p> 

<p>[ 2 ] Juanjuan Gu and Yun Jing, "A modified mixed domain method for modeling acoustic wave propagation in strongly heterogeneous media," The Journal of the Acoustical Society of America, 147, 4055-4068, 2020. <a href="https://github.com/MDM-series/MDM/tree/master/download/MMDM.pdf" download="MMDM.pdf">Download pdf</a></p> 

<p>[ 3 ] Juanjuan Gu and Yun Jing, "Simulation of the second harmonic ultrasound field in heterogeneous soft tissue using a mixed domain method," IEEE Ultrasonics, Ferroelectrics, and Frequency Control Society, 66, 669-675, 2019. <a href="https://github.com/m-SOUND/mSOUND/tree/master/download/FSMDM.pdf" download="FSMDM.pdf">Download pdf</a></p>   

<p>[ 4 ] Juanjuan Gu and Yun Jing, "Numerical Modeling of Ultrasound Propagation in Weakly Heterogeneous Media Using a Mixed Domain Method," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 65, 1258-1267, 2018. <a href="https://github.com/m-SOUND/mSOUND/tree/master/download/MDM.pdf" download="MDM.pdf">Download pdf</a></p>       
   
<p>[ 5 ] Juanjuan Gu and Yun Jing, "Modeling of wave propagation for medical ultrasound: a review," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 62, 1979-1992, 2015. <a href="https://github.com/m-SOUND/mSOUND/tree/master/download/review.pdf" download="review.pdf">Download pdf</a></p>       

<p>[ 6 ] Yun Jing, "An improved wave-vector frequency-domain method for nonlinear wave modeling," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 61, 515-524, 2014. <a href="https://github.com/m-SOUND/mSOUND/blob/master/download/improved_WVFD.pdf" download="improved_WVFD.pdf">Download pdf</a></p> 

<p>[ 7 ] Yun Jing, "On the use of an absorption layer for the angular spectrum approach (L)," The Journal of the Acoustical Society of America, 131, 999-1002, 2012. <a href="https://github.com/m-SOUND/mSOUND/tree/master/download/Absorption_layer.pdf" download="Absorption_layer.pdf">Download pdf</a></p> 

<p>[ 8 ] Yun Jing, Molei Tao, and Greg T. Clement, "Verification of the westervelt equation for focused transducers," IEEE Transactions on Ultrasonics, Ferroelectrics and Frequency Control, 58, 1097-1101, 2011. <a href="https://github.com/m-SOUND/mSOUND/blob/master/download/Verification.pdf" download="Verification.pdf">Download pdf</a></p>  

<p>[ 9 ] Yun Jing, Molei Tao, and Greg T. Clement, "Evaluation of a wave-vector-frequency-domain method for nonlinear wave propagation," The Journal of the Acoustical Society of America,129, 32-46, 2011. <a href="https://github.com/m-SOUND/mSOUND/tree/master/download/WVFD.pdf" download="WVFD.pdf">Download pdf</a></p>   

## License
This project is licensed under the [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.txt).  

## Acknowledgment
This project is supported by the [National Institute of Health (NIH)](https://www.nih.gov/) under the Grant R01EB025205. From 2015 to 2018, Juanjuan Gu was also supported by a fellowship award from China Scholarship Council (CSC).

