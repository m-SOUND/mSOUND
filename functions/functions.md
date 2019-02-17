---
layout: page
title: Functions
---

## Functions             
***        
### set_grid 

Define the computational domain   

mgrid = set_grid(dt, tlen, dx, xlen)     
mgrid = set_grid(dt, tlen, dx, xlen, dy, ylen)     
mgrid = set_grid(dt, tlen, dx, xlen, dy, ylen, dz, zlen)     

dt dx dy dz           temporal and spatial step size     
tlen xlen ylen zlen   total domain size in the temproal and spatial domain              

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

### Forward2D     

2D mixed-domain simulation of wave propagation, can give transient results directly                     

Forward2D(mgrid, medium,excit_p)              

INPUT | PROPERTIES                
------------ | -------------     
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties              
excit_p  |excitation signal          

OUTPUTS    
Time-domain pressure dirtribution through the whole domain   

### Forward3D 

3D mixed-domain simulation of wave propagation, can give transient results directly        

Forward1D(mgrid, medium,excit_p)           

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties             
excit_p  |excitation signal               

OUTPUTS     
Time-domain pressure dirtribution through the whole domain                

### Forward2D_fund 

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

### Forward2D_secd 

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

### Forward3D_fund 

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

### Forward3D_secd 

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
