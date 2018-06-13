---
title: Input Files
permalink: /docs/InputFiles/
---

## Control File
### Name 
system/control.md
### content
```markdown
CONTROL FILE
============

# TIME SPECIFIC

## CFL
1.0

## State Load File ('0' for no load file)
0

## stop at (Max Iterations)
1000

## write interval(Checkpoint iter-dump data after how many iterations)
### (Enter 0 to turn checkpointing off)
50

## write file format (tecplot/vtk)
vtk

## write data format (ascii/binary)
ASCII

## read file format (tecplot/vtk)
vtk

## read data format (ascii/binary)
ASCII

## write percision (no of digit after decimal; for resnorm)
6

## purge write (no. of recent solution dump folder to keep)
0

## resnorm write inteval (resnorm dump interval)
100

## tolerance(value [Resnorm strings ] )
### eg 0.0001 Resnorm_abs
### Resnorm strings: Mass_abs, Resnorm_abs, Viscous_abs, Turbulent_abs, Continuity_abs, X-mom_abs, Y-mom_abs, Z-mom_abs, Energy_abs, Mass_rel, Resnorm_rel, Viscous_rel, Turublent_rel, Continuity_abs, X-mom_rel, Y-mom_rel, Z-mom_rel, Energy_rel, TKE_abs,Tv_abs, Dissipation_abs, Omega_abs, Kl_abs, TKE_rel, Tv_rel, Dissipation_rel, Omega_rel, Kl_rel
1e-9  Viscous_abs

## Debug level: Most detail (1) to least detail (5)
5
```

## Finite volume scheme File
### Name
system/fvscheme.md
### Content
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

## Flow condition file
### Name
system/flow.md
### content
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

## Output control file
### Name 
sytem/output_control.md
### content
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

## Resnorm-to-file control file
### Name
system/res_control.md
### Content
```c++
{
  Mass_abs
  Viscous_abs
  Mass_abs
  Resnorm_abs
  Viscous_abs
  Turbulent_abs
  Continuity_abs
  X-mom_abs
  Y-mom_abs
  Z-mom_abs
  Energy_abs
  Mass_rel
  Resnorm_rel
  Viscous_rel
  Turublent_rel
  Continuity_abs
  X-mom_rel
  Y-mom_rel
  Z-mom_rel
  Energy_rel
  TKE_abs
  Tv_abs
  Dissipation_abs
  Omega_abs
  Kl_abs
  TKE_rel
  Tv_rel
  Dissipation_rel
  Omega_rel
  Kl_rel
}
```
Remove lines which are not required.

## Stop File
### Name
system/stopfile
### content
```
0
```
Change 0 to 1 if want the solver to stop.

