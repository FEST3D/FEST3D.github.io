---
title: Output Control File
permalink: /docs/Output/
---

## Path 
**$RUN**/sytem/output_control.md
## content
##### List of variables to write in output files.
- *Velcoity* => {u, v, w}
- *Density*
- *Pressure*
- *Mu* => Laminar Viscosity
- *Mu_t* => Eddy Viscosity
- *TKE* => Turbulence Kinetic Energy
- *Omega* => Turbulence dissiapation frequency
- *kL* => Second variable of k-kL turbulence model
- *tv* => Variable for SA turbulence model
- *Wall_distance* => Local distance from nearest wall
- *TKE_residue* => Local residue for turbulence kinetic energy equation
- *Mass_residue* => Local residue for continuity equation
- *X_mom_residue* => Local residue for X-momentum equation
- *Y_mom_residue* => Local residue for Y-momentum equation
- *Z_mom_residue* => Local residue for Z-momentum equation
- *energy_residue* => Local residue for Energy equation
- *DuDx* => Partial derivative of X-speed with respect to X-direction
- *Dudy* => Partial derivative of X-speed with respect to Y-direction
- *DuDz* => Partial derivative of X-speed with respect to Z-direction
- *DvDx* => Partial derivative of Y-speed with respect to X-direction
- *DvDy* => Partial derivative of Y-speed with respect to Y-direction
- *DvDz* => Partial derivative of Y-speed with respect to Z-direction
- *DwDx* => Partial derivative of Z-speed with respect to X-direction
- *DWDy* => Partial derivative of Z-speed with respect to Y-direction
- *DwDz* => Partial derivative of Z-speed with respect to Z-direction
- *DTDx* => Partial derivative of temperature with respect to X-direction
- *DTDy* => Partial derivative of temperature with respect to Y-direction
- *DTDz* => Partial derivative of temperature with respect to Z-direction
- *DtkDx* => Partial derivative of turbulent kinetic energy with respect to X-direction
- *DtkDy* => Partial derivative of turbulent kinetic energy with respect to Y-direction
- *DtkDz* => Partial derivative of turbulent kinetic energy with respect to Z-direction
- *DtwDx* => Partial derivative of Omega to X-direction
- *DtwDy* => Partial derivative of Omega to Y-direction
- *DtwDz* => Partial derivative of Omega to Z-direction
- *DtvDx* => Partial derivative of nu_t(SA model) with respect to X-direction
- *DtvDy* => Partial derivative of nu_t(SA model) with respect to Y-direction
- *DtvDz* => Partial derivative of nu_t(SA model) with respect to Z-direction
- *DtkLDx* => Partial derivative of kL(k-kL model) with respect to X-direction
- *DtkLDy* => Partial derivative of kL(k-kL model) with respect to Y-direction
- *DtkLDz* => Partial derivative of kL(k-kL model) with respect to Z-direction

##### List of variables to read from input files.
- *Velcoity* => {u, v, w}
- *Density*
- *Pressure*
- *TKE* => Turbulence Kinetic Energy
- *Omega* => Turbulence dissiapation frequency
- *kL* => Second variable of k-kL turbulence model
- *tv* => Variable for SA turbulence model

## Template
```c++
# variable to write
{
  Velocity
  Density
  Pressure
}
# variable to read
{
  Velocity
  Density
  Pressure
}
```

