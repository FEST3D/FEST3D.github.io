---
title: Run
permalink: /docs/Run/
---

## Prerequisite
**C++11 compiler**, **Python 2.7** and **bash**

## Directory Structure
Python script, provided at [**github**](https://github.com/FEST3D/run.git), automate the process of generating a correct directory sturcture and input files for FEST3D. [**Download**](https://github.com/FEST3D/run.git) this script and edit the top matter according to requirements.

## Setup
```bash
python automaton.py
```
Make sure to provide the absolute path of the FEST3D binary in the script before executing.

## Execute
```bash
$mpiexec.hydra -np 16 bin/FEST3D 
```
