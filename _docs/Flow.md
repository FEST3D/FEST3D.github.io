---
title: Flow File
permalink: /docs/Flow/
---

## Path
**$RUN**/system/flow.md
## Content
##### Number of variables
This is a redundant input and will be removed in future release.
##### Free stream denstiy
##### Free stream x-component of velocity
##### Free stream y-component of velocity
##### Free stream z-component of velocity
##### Free stream pressure
##### Free stream turbulent kinetic energy
##### Free stream dissiapation rate
##### Reference viscosity
##### Viscosity variation law
 _Sutherland Law_ or _Constant_
##### Reference temperature
##### Sutherland temperature
##### prandtl number (laminar and turbulent)
Both laminar and turbulent prandtl number are defined here.
##### Gamma (specific heat capacity ratio)
##### Gas constant


## Template
```markdown
# FLOW CONTROL FILE

## FREE STREAM PROPERTIES

### Number of variables
5

### Free Stream Density
1.17682

### Free Stream X Speed
69.4377

### Free Stream Y Speed
0.

### Free Stream Z Speed
0.

### Free Stream Pressure
101325.0

### Free TKE Pressure
0.

### Free omega Pressure
0.

### Viscous effects
### Give mu reference = 0 for inviscid
### Using Sutherlands law for coefficient of viscosity
### mu reference or mu0 (in kg/ms)
0.0

# viscoisty variation(sutherland_law/constant)
sutherland_law

### T reference or T0 (in K)
300

### Sutherland Temparature (K)
110.5

### Prandtl Number and Turbulent Prandtl Number
0.7 0.9

### gamma (ratio of specific heats)
1.4

### R_gas (specific gas constant)
287.
```
