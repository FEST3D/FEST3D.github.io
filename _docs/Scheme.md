---
title: Scheme Files
permalink: /docs/Scheme/
---

## Path
**$RUN**/system/fvscheme.md

## Content
##### Inviscid flux reconstruction scheme
 _AUSM_ or _LDFSS_ or _SLAU_
##### Face state reconstruction scheme
 _First Order_ or _MUSCL_ or _PPM_ or _WENO_
##### Limiter switch for first five variables
Switch to turn on or off the limiter when using MUSCL scheme for higher order face-state reconsturction of first five variables{rho, u, v, w, P}. **1** stands for _on_ and **0** stands for _off_.
##### Limiter switch for turbulent variables
Switch to turn on or off the limiter when using MUSCL scheme for higher order face-state reconsturction of turbulent variables. **1** stands for _on_ and **0** stands for _off_.
##### Turbulence model
 _SA_ or _SST_ or _k-kL_
##### Time stepping method and value
 Either global or local time-steppig method can be used. When using global time step, particular step can be specified. For example: "_g 1.e-3_"
##### Time integration method
 _Euler Explicit_ or _RK4_ or _TVDRK3_
##### Switch for higher order boundary conditions
 Switch for higher order boundary conditions. **1** stands for _on_ and **0** stands for _off_.


## Template
```markdown
SCHEME CONTROL FILE
===================

# SOLVER SPECIFIC

## Scheme: van_leer / ldfss0 / hlle / ausm / slau
slau

## Higher order extension: none or ppm or muscl or weno
none

## Higher order extension  switch:
### 0 -> off
### 1 -> on
### limiter /&/  pressure based switch (x,y,z)
     1 1 1            0 0 0

### limiters for turbulent variables
1 1 1

### Tubulence: none / sst / kkl / sa
none

## Time-stepping method: global (g) or local (l)
g  1.0e-4

## Higher Order Time Integration: none or RK4 or TVDRK2, or TVDRK3
RK4

## Higher order boundary condition (accur: 0 or 1)
0
```
