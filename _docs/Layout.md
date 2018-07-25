---
title: Layout File
permalink: /docs/Layout/
---

## Purpose
Define boundary condition in simplified manner.


- -1 **SUPERSONIC INFLOW**
- -2 **SUPERSONIC OUTFLOW**
- -3 **SUBSONIC INFLOW**
- -4 **SUBSONIC OUTFLOW**
- -5 **WALL**
- -6 **SLIP PLANE**
- -7 **Pole**
- -8 **Far-field**
- -9 **Total inlet**
- +1 **INTERFACE**



## Format of file
![Layout.md](/img/Layout.png)

### Template
```
 ## BLOCK LAYOUT FILE
 ## ==========================
 ## NUMBER OF PROCESSES
 4
 ## NUMBER OF ENTRIES PER PROCESS
 9
 ## PROCESS_NO GRID BC_FILE IMIN IMAX JMIN JMAX KMIN KMAX
 ## ===================================
 ## PROCESS 0
 00  grid_00.txt  bc_00.md  -006  0001  -006  -006  -006  -006
 ## PROCESS 1
 01  grid_01.txt  bc_01.md  0000  0002  -006  -006  -006  -006
 ## PROCESS 2
 02  grid_02.txt  bc_02.md  0001  0003  -006  -006  -006  -006
 ## PROCESS 3
 03  grid_03.txt  bc_03.md  0002  -006  -006  -006  -006  -006
~                                                                  
```
