---
title: Residue Control File
permalink: /docs/Residue/
---

## Path
**$Run**/system/res_control.md

## Content
##### List of residue
Either scaled or just normalized, to write in **$RUN**/time_directories/aux/resnorm
- *Mass_abs* => Mass balance between inlet and outlet boundaries.
- *Resnorm_abs* => L2 norm of scaled residue of all equations
- *Viscous_abs* => L2 norm of scaled residue of continuity, momentum and energy equation
- *Turbulent_abs* => L2 norm of scaled residue of turbulence equations
- *Continuity_abs* => Scaled residue of continuity equation
- *X-mom_abs* => Scaled residue of x-momentum equation
- *Y-mom_abs* => Scaled residue of y-momentum equation
- *Z-mom_abs* => Scaled residue of z-momentum equation
- *Energy_abs* => Scaled residue of energy equation
- *Mass_rel*
- *Resnorm_rel*
- *Viscous_rel*
- *Turublent_rel*
- *Continuity_abs*
- *X-mom_rel*
- *Y-mom_rel*
- *Z-mom_rel*
- *Energy_rel*
- *TKE_abs*
- *Tv_abs*
- *Dissipation_abs*
- *Omega_abs*
- *Kl_abs*
- *TKE_rel*
- *Tv_rel*
- *Dissipation_rel*
- *Omega_rel*
- *Kl_rel*


## Template
```c++
{
  Mass_abs
  Viscous_abs
  Turbulent_abs
  Continuity_abs
}
```
Remove lines which are not required.

