---
title: Setup
permalink: /docs/Setup/
---

## Prerequisite
### Compiler
Either **gfortran** or **Intel compiler** should be installed
### MPI
FEST3D is distributed-memory based multiblock code. It uses [**MPICH**](https://www.mpich.org/) for message passing interface.
### Tools
* [**GNU MAKE**](https://www.gnu.org/software/make/) for generation of executable.
* [**CMAKE**](https://cmake.org/) for platform independent comilation.

## Compilation
For Linux system:
```bash
  $mkdir build
  $cd build
  $FC='mpif90 -f90=ifort' cmake ../ -DCMAKE_BUILD_TYPE=RELEASE
```
  

