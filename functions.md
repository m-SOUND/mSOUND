---         
title: Functions     
---   
 
# Functions
***    
***      

<h3 style="color: #c64949;"> set_grid </h3>             
***      

Define the computational domain      

```
mgrid = set_grid(dt, t_length, dx, x_length);                         
mgrid = set_grid(dt, t_length, dx, x_length, dy, y_length);     
mgrid = set_grid(dt, t_length, dx, x_length, dy, y_length, dz, z_length);     

```

#### Inputs     

INPUT | PROPERTIES               
------------ | -------------                              
dx   | spatial step size in the x direction [m]          
dy   | spatial step size in the y direction [m]            
dz   | spatial step size in the z direction [m]           
dt   | temporal step size in the time domain [s]       
x_length |  total domain size in the x direction [m]        
y_length |  total domain size in the y direction [m]              
z_length |  total domain size in the z direction [m]                  
t_length | total temporal domain size [s]               

#### Outputs          

OPTPUT | PROPERTIES                     
------------ | -------------                                
mgrid.x  | coordinates in the x direction [m]          
mgrid.y  | coordinates in the y direction [m]          
mgrid.z  | coordinates in the z direction [m]           
mgrid.t  | time array [s]              
mgrid.kx |  wavevector in the x direction            
mgrid.ky |  wavevector in the y direction                          
mgrid.w  | angular freuqency              
mgrid.num_x | number of grid points in the x direction                  
mgrid.num_y | number of grid points in the y direction     
mgrid.num_z | number of grid points in the z direction    
mgrid.num_t | number of time steps           

<br>
<h3 style="color: #c64949;"> Forward1D   </h3>           
***      
Simulation of 1D wave propagation and it is based on the transient mixed domain method.              
```
p = Forward1D(mgrid, medium, source_p);      
```

#### Inputs                  

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain            
medium   |input strucutre defined the media properties             
source_p |excitation signal [Pa]      

#### Output    

Time-domain results      

<h3 style="color: #c64949;">Forward2D  </h3>      
***      

Simulation of the 2D wave propagation and it is based on the transient mixed domain method.       

```
p = Forward2D(mgrid, medium, source_p); 
```

#### Inputs            

INPUT | PROPERTIES                        
------------ | -------------      
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties              
source_p |excitation signal [Pa]                       
 
#### Output                          
Time-domain results  

<h3 style="color: #c64949;">Forward3D</h3>      
***      

Simulation of 3D wave propagation and it is based on the transient mixed domain method.               
```
p = Forward3D(mgrid, medium,source_p);           
```
#### Inputs            

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties             
source_p |excitation signal [Pa]                        

#### Output                   
Time-domain results          

<h3 style="color: #c64949;">Forward2D_fund</h3>      
***      

Simulation of the 2D wave propagation at the fundamental freqeuncy and it is based on the frequency-specific mixed domain method.                       
```     
p = Forward2D_fund(mgrid, medium, source_p, omega_c);        
```     
#### Inputs     

INPUT | PROPERTIES               
------------ | -------------    
mgrid     |input strucutre defined the computational domain     
medium    |input strucutre defined the media properties               
source_p  |excitation signal [Pa]                      
omega_c   |fundamental frequency     

#### Output               
Pressure dirtribution through the domain at the fundamental frequecncy        

<h3 style="color: #c64949;">Forward2D_sec</h3>      
***      

Simulation of the 2D wave propagation at the second-harmonic freqeuncy and it is based on the frequency-specific mixed domain method.     
```       
p = Forward2D_sec(mgrid, medium, P_fundamental, omega_c);    
```     

#### Inputs          

INPUT | PROPERTIES               
------------ | -------------    
mgrid          |input strucutre defined the computational domain     
medium         |input strucutre defined the media properties               
P_fundamental  |pressure at the fundamental frequency  [Pa] /the output pressure of ```Forward2D_fun```        
omega_c        |fundamental frequency      

#### Output   
Pressure distribution throughout the spatial domain at the second-harmonic frequecncy    

<h3 style="color: #c64949;">Forward3D_fund</h3>     
***      

Simulation of the 3D wave propagation at the fundamental freqeuncy and it is based on the frequency-specific mixed domain method.            
```
p = Forward3D_fund(mgrid, medium,  source_p, omega_c);           
``` 
#### Inputs       

INPUT | PROPERTIES               
------------ | -------------    
mgrid     |input strucutre defined the computational domain     
medium    |input strucutre defined the media properties               
source_p  |excitation signal [Pa]               
omega_c   |fundamental frequency       

#### Output   
Pressure dirtribution throughout the domain at the fundamental frequecncy      

<h3 style="color: #c64949;">Forward3D_sec</h3>     
***      

Simulation of the 3D wave propagation at the second-harmonic freqeuncy, based on the frequency-specific mixed domain method.               
``` 
p = Forward3D_sec(mgrid, medium, P_fundamental, omega_c);     
``` 
#### Inputs      

INPUT | PROPERTIES               
------------ | -------------    
mgrid          |input strucutre defined the computational domain     
medium         |input strucutre defined the media properties               
P_fundamental  |pressure at the fundamental frequency  [Pa] /the output pressure of ```Forward3D_fun```           
omega_c        |fundamental frequency      

#### Output             
Pressure dirtribution throught the spatial domain at the second-harmonic frequecncy.      
