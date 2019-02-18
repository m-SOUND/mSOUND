---
title: wave propagation in 2D heterogeneous media
---

## generate the grid structure in the compputational domain       
***
For 2D time domain simulation, we need six inputs to define the mgrid structure with funciton [mgrid](\functions.md). Coordinates defined with the mgrid functiions are all in Cartesian coordinates.

```         
dx = lambda/4;                 %  step size in the x direction   [m]
dy = lambda/4;                 %  step size in the y direction   [m]  
dt = 1/fc/16;                  %  time step    

ylen = lambda*18;              % total computatoinal domain size in x direction    [m]
xlen = lambda*40;              % total computatoinal domain size in y direction    [m]
tlen = num_cycles/fc*11.0;     % total computatoinal domain size in the temporal domain    [s]

mgrid = set_grid(dt, tlen, dx, xlen, dy, ylen);              
``` 
## Define a phased array transducer      
***
In this example, phased array transducer is used to generate the foucsed ultrasound beam. Here shows the details of defining the phased array transducer. 
          
```
TR_focus  = 14*lambda;                                      % transducer focus length   [m]
TR_radius = 4.5*lambda;                                     % Transducer diameter       [m]
num_el    = round(TR_radius*2/mgrid.dx);                    % [grid points]

el_x  = -floor(num_el/2):floor(num_el/2);                    % [grid points]

% calculate the time delay for each transducer element[s]
delay = sqrt((el_x*mgrid.dx).^2 + (TR_focus)^2)/medium.c0;   
delay = delay - min(delay);
```

## Excitation signal
*** 
A 4-cycles gaussian-modulated pulse is used for the excitation signal.            
```
ts    = [-num_cycles/fc:dt:num_cycles/fc].';           % define the pulse length
delay = repmat(delay, length(ts),1);
ts    = repmat(ts, 1,length(el_x));       

excit_ps = p0*sin(2*pi*fc*(ts+delay)).*exp(-(ts+delay).^2*fc^2/2);     % define the pulse    
```
 
## define the heterogeneous media        
***       
```
medium.c    = c;                 % speed of sound   [m/s]
medium.rho  = rho;               % density  [kg/m^3]
medium.beta = beta;              % nonlinear coefficient
medium.ca   = ca;                % attenuation coefficient  [dB/(MHz^y cm)]
medium.cb   =cb;                 % power law exponent    
```

## 2D forward Simulation
***
Transient pressure field results are calculated with the 2D forward simulation function [Forward2D](\functions.md).    
```
p_total = Forward2D(mgrid, medium, excit_p);
```

## Results
***     


