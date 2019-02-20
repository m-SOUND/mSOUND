---
layout: page
title: Functions
---
 
# Functions
***    
***      

## set_grid            
***      

Define the computational domain      

```
mgrid = set_grid(dt, tlen, dx, xlen);                         
mgrid = set_grid(dt, tlen, dx, xlen, dy, ylen);     
mgrid = set_grid(dt, tlen, dx, xlen, dy, ylen, dz, zlen);     

```

### Inputs     

INPUT | PROPERTIES               
------------ | -------------                              
dx   | spatial step size in the x direction          
dy   | spatial step size in the y direction           
dz   | spatial step size in the z direction             
dt   | temporal step size in the time domain       
xlen |  total domain size in the x direction        
ylen |  total domain size in the y direction                
zlen |  total domain size in the z direction                  
tlen | total temporal domain size             

### Outputs          

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
mgrid.num_x | number of grid points in the x direction                  
mgrid.num_y | number of grid points in the x direction     
mgrid.num_z | number of grid points in the x direction    
mgrid.num_t | number of time steps          

## Forward1D         
***      
1D mixed-domain simulation of wave propagation, can give transient results directly                   
```
p = Forward1D(mgrid, medium,excit_p);
```

### Inputs                  

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain            
medium   |input strucutre defined the media properties             
excit_p  |excitation signal         

### Output    

Time-domain pressure dirtribution through the whole domain         

## Forward2D   
***      

2D mixed-domain simulation of wave propagation, can give transient results directly                     
```
p = Forward2D(mgrid, medium,excit_p); 
```

### Inputs            

INPUT | PROPERTIES                        
------------ | -------------      
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties              
excit_p  |excitation signal              
 
### Output                          
Time-domain pressure dirtribution through the whole domain   

## Forward3D 
***      

3D mixed-domain simulation of wave propagation, can give transient results directly        
```
p = Forward1D(mgrid, medium,excit_p);           
```
### Inputs            

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties             
excit_p  |excitation signal               

### Output                   
Time-domain pressure dirtribution through the whole domain                

## Forward2D_fund 
***      

2D frequency-domain simulation of wave propagation at the fundamental frequency                 
```     
p = Forward2D_fund(mgrid, medium, excit_p, omegac);        
```     
### Inputs     

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties               
excit_p  |excitation signal               
omegac   |fundamental frequency     

### Output               
Pressure dirtribution through the domain at the fundamental frequecncy        

## Forward2D_secd 
***      

2D frequency-domain simulation of wave propagation at the second-harmonic frequency           
```       
p = Forward2D_secd(mgrid, medium, P_fundamental,omegac);    
```     

### Inputs          

INPUT | PROPERTIES               
------------ | -------------    
mgrid          |input strucutre defined the computational domain     
medium         |input strucutre defined the media properties               
P_fundamental  |excitation signal               
omegac         |fundamental frequency      

### Output   
Pressure dirtribution through the domain at the second-harmonic frequecncy    

## Forward3D_fund 
***      

3D frequency-domain simulation of wave propagation at the fundamental frequency                  
```
p = Forward3D_fund(mgrid, medium, excit_p, omegac);           
``` 
### Inputs       

INPUT | PROPERTIES               
------------ | -------------    
mgrid    |input strucutre defined the computational domain     
medium   |input strucutre defined the media properties               
excit_p  |excitation signal               
omegac   |fundamental frequency     

### Output   
Pressure dirtribution through the domain at the fundamental frequecncy      

## Forward3D_secd        
***      

3D frequency-domain simulation of wave propagation at the second-harmonic frequency                   
``` 
p = Forward3D_secd(mgrid, medium, P_fundamental,omegac);     
``` 
### Inputs      

INPUT | PROPERTIES               
------------ | -------------    
mgrid          |input strucutre defined the computational domain     
medium         |input strucutre defined the media properties               
P_fundamental  |excitation signal               
omegac         |fundamental frequency      

### Output             
Pressure dirtribution through the domain at the second-harmonic frequecncy         
