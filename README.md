# Introduction #
***        
MDM-series is an open-source toolbox for [MATLAB](https://www.mathworks.com/products/matlab.html) and it is developed for modeling one-way linear/nonlinear wave propagation in biological tissue with arbitrary heterogeneities, in which speed of sound, density, attenuation coefficients, power law exponent and nonlinear coefficients are all spatially varying functions. In the current version, MDM-series contains two methods for modeling nonlinear wave proapgation and they are transient mixed-domain method (TMDM) and frequency-specific mixed-domain method (FSMDM). TMDM can generate the simulaiton results in the transient domain and FSMDM generates the simulaiton results directly at the specific frequencies of interest.  
 
<p align="justify">Since FSMDM is dubbed from the TMDM based on the quasilinear approximation (Mach number epsilon << 1), therefore, TMDM should be chosen for strongly nonlinear wave propagation simulation.</p>   

# Download #
***        
- **<a href="https://github.com/MDM-series/FileDownloader/blob/master/MDM_code.zip" download="MDM_code.zip">Download MDM-series</a>**   

# License #   
***          
This project is licensed under the GNU General Public License v3.0  

# References #   
***           
<p align="justify">[ 1 ] J. Gu and Y. Jing, “Numerical Modeling of Ultrasound Propagation in Weakly Heterogeneous Media Using a Mixed Domain Method,” IEEE Trans. Ultrason., Ferroelect., Freq. Control, vol. 65, no. 7, pp. 1258-1267, Jul. 2018. <a href="https://github.com/MDM-series/FileDownloader/blob/master/MDM.pdf" download="MDM.pdf">Download pdf</a></p>
   
<p align="justify">[ 2 ]  J. Gu and Y. Jing, “Simulation of the second harmonic ultrasound field in heterogeneous soft tissue using a mixed domain method,”  IEEE Trans. Ultrason., Ferroelect., Freq. Control, accepted. <a href="https://github.com/MDM-series/FileDownloader/blob/master/FSMDM.pdf" download="FSMDM.pdf">Download pdf</a></p>
 
# Acknowledgment #   
***                    
This project is supported by the [National Institute of Health (NIH)](https://www.nih.gov/) under the Grant R01EB025205. Juanjuan Gu was also supported by a fellowship from China Scholarship Council (CSC) during her Ph.D. study in [North Carolina State University](https://www.ncsu.edu/).

# Functions #            
***        
### set_grid ###

Define the computational domain    

mgrid = set_grid(dt, tlen, dx, xlen)     
mgrid = set_grid(dt, tlen, dx, xlen, dy, ylen)     
mgrid = set_grid(dt, tlen, dx, xlen, dy, ylen, dz, zlen)     

INPUT | PROPERTIES              
------------ | -------------             
dx  | step size in the x direction           
dy  | step size in the y direction           
dz  | step size in the z direction            
dt  | step size in the time domain           
xlen |  total domain size in the x direction         
ylen |  total domain size in the y direction                  
zlen |  total domain size in the z direction                     
tlen |  total domain size in the temporal domain                   
 

OPTPUT | PROPERTIES              
------------ | -------------            
mgrid.x  | coordinates in the x direction          
mgrid.y  | coordinates in the y direction          
mgrid.z  | coordinates in the z direction           
mgrid.t  | time array           
mgrid.kx |  wavevector in the x direction            
mgrid.ky |  wavevector in the y direction              
mgrid.kz |  wavevector in the z direction               
mgrid.w  | angular freuqency              
mgrid.numx | number of grid points in the x direction                
mgrid.numy | number of grid points in the x direction
mgrid.numz | number of grid points in the x direction
mgrid.numt | number of time steps         

### Forward1D ###         

1D mixed-domain simulation of wave propagation, can give transient results directly               

Forward1D(mgrid, medium,excit_p)            

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain            
medium   |input strucutre defined the media properties             
excit_p  |excitation signal        

OUTPUTS                 
Time-domain pressure dirtribution through the whole domain         

### Forward2D ###         

2D mixed-domain simulation of wave propagation, can give transient results directly                     

Forward2D(mgrid, medium,excit_p)              

INPUT | PROPERTIES                
------------ | -------------     
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties              
excit_p  |excitation signal          

OUTPUTS    
Time-domain pressure dirtribution through the whole domain   

### Forward3D ###         

3D mixed-domain simulation of wave propagation, can give transient results directly        

Forward1D(mgrid, medium,excit_p)           

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties             
excit_p  |excitation signal               

OUTPUTS     
Time-domain pressure dirtribution through the whole domain                

### Forward2D_fund ###         

2D frequency-domain simulation of wave propagation at the fundamental frequency                 

Forward2D_fund(mgrid, medium, excit_p, omegac)           

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties               
excit_p  |excitation signal               
omegac   |fundamental frequency     

OUTPUTS     
Pressure dirtribution through the domain at the fundamental frequecncy        

### Forward2D_secd ###         

2D frequency-domain simulation of wave propagation at the second-harmonic frequency           

Forward2D_secd(mgrid, medium, P_fundamental,omegac)     

INPUT | PROPERTIES               
------------ | -------------    
mgrid          |input strucutre defined the computational domain     
medium         |input strucutre defined the media properties               
P_fundamental  |excitation signal               
omegac         |fundamental frequency      

OUTPUTS     
Pressure dirtribution through the domain at the second-harmonic frequecncy    

### Forward3D_fund ###         

3D frequency-domain simulation of wave propagation at the fundamental frequency                  

Forward3D_fund(mgrid, medium, excit_p, omegac)           

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties               
excit_p  |excitation signal               
omegac   |fundamental frequency     

OUTPUTS      
Pressure dirtribution through the domain at the fundamental frequecncy      

### Forward3D_secd ###         

3D frequency-domain simulation of wave propagation at the second-harmonic frequency                   

Forward3D_secd(mgrid, medium, P_fundamental,omegac)     

INPUT | PROPERTIES               
------------ | -------------    
mgrid          |input strucutre defined the computational domain     
medium         |input strucutre defined the media properties               
P_fundamental  |excitation signal               
omegac         |fundamental frequency      

OUTPUTS     
Pressure dirtribution through the domain at the second-harmonic frequecncy         


# Examples #       
***                      
