---
title: Boundary Conditions File
permalink: /docs/BoundaryConditions/
---

## Details of Boundary conditions
#### Supersonic Inlet
- *FIX_DENSITY*
- *FIX_X_SPEED*
- *FIX_Y_SPEED*
- *FIX_Z_SPEED*
- *FIX_PRESSURE*
#### Supersonic Outlet
- *COPY_DENSITY*
- *COPY_X_SPEED*
- *COPY_Y_SPEED*
- *COPY_Z_SPEED*
- *COPY_PRESSURE*
#### Subsonic Inlet
- *FIX_DENSITY*
- *FIX_X_SPEED*
- *FIX_Y_SPEED*
- *FIX_Z_SPEED*
- *COPY_PRESSURE*
#### Subsonic Outlet
- *COPY_DENSITY*
- *COPY_X_SPEED*
- *COPY_Y_SPEED*
- *COPY_Z_SPEED*
- *FIX_PRESSURE*
#### Symmetry
- *COPY_DENSITY*
- *COPY_PRESSURE*
- *FLOW_TANGENCY*


## Format of file
![Domain](/img/bc_xx.png)

## Template
```
BOUNDARY CONDITIONS CONFIGURATION
=================================

# imn
- COPY_DENSITY
- COPY_X_SPEED
- COPY_Y_SPEED
- COPY_Z_SPEED
- COPY_PRESSURE

# imx
- INTERFACE

# jmn
- COPY_DENSITY
- COPY_PRESSURE
- FLOW_TANGENCY

# jmx
- COPY_DENSITY
- COPY_PRESSURE
- FLOW_TANGENCY

# kmn
- COPY_DENSITY
- COPY_PRESSURE
- FLOW_TANGENCY

# kmx
- COPY_DENSITY
- COPY_PRESSURE
- FLOW_TANGENCY

FIN
```
