---
title: Control File
permalink: /docs/Control/
---

## Path
**$RUN**/system/control.md
## Content
##### CFL number
Float of value greater than 0.0. The actual value of this parameter will depend on the time-integration scheme.
##### Restart folder number
 All the solution files are stored at *__$RUN__/time\_directories/* with number between **0000** (Initial state file) to **9999**.
##### Maximum number of Iterations
Integer greater than or equal to one.
##### Number of iteration after which solution will be saved.
Integer greater than or equal to zero. Incase of zero as input, solution will never be saved.
##### Format of output solution file.
  _TECPLOT_ or _.vtk_
##### Format of data in output file.
  _ASCII_
##### Format of input solution file.
  _TECPLOT_ or _.vtk_
##### Format of data in input file.
  _ASCII_
##### Precision with which resnorm are written in a file.
This precision is not applied to solution file. Solution files are written with double precision to reduce error when restarting solver with previous saved solution file. Precision parameter is used only for writing residue to a file.
##### Purge number
How many latest solution folder to keep. This helps to save memeory for problems with large grid size.
##### Normalized residue write interval
Residue is written in file *__$RUN__/time_directoies/aux/resnorm*. User may skip the update of resnorm file for some iteration to reduce the size of resnorm file. This will help when performing explicit time-integration with millions of iteration.
##### Tolerance value
Two inputs are needed: Tolerance value and Tolerance equation. The code has two stop criteria: Max number of iterations and minimum residual achived.
##### Debug level
  While developming some part of the code, value '1' will help to provide more details information about the run in *__$RUN__/time_directoies/aux/out file*, which might help in catching the error.


### Template
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

## write data format (ASCII)
ASCII

## read file format (tecplot/vtk)
vtk

## read data format (ASCII)
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
