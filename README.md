# Single N2 Bubble Rise in Liquid Mercury (N2/Hg) – OpenFOAM Case

## Description
This repository contains an OpenFOAM case for the simulation of a **single nitrogen bubble rising in stagnant liquid mercury (N2/Hg)**. This case corresponds to one of the validation cases used in the manuscript:

**Single-Bubble Rise in Liquid Metals: CFD Modeling, Validation and Correlation Assessment**

submitted to *Progress in Nuclear Energy* (under review).

The repository is intended to provide a reproducible reference case for CFD simulations of gas bubbles in liquid metals.

## Case overview
- **System:** N2 bubble in liquid Hg
- **Application:** Experimental validation case
- **Solver:** `interIsoFoam`
- **Method:** Geometric Volume-of-Fluid (VOF)
- **OpenFOAM version:** `v2012`

## Requirements
To run this case correctly, you need:

- A working installation of **OpenFOAM v2012**
- The **dynamic adaptive mesh refinement library** described in:

**Rettenmaier, D., Deising, D., Ouedraogo, Y., Gjonaj, E., De Gersem, H., Bothe, D., Tropea, C., Marschall, H., 2019.**  
*Load balanced 2D and 3D adaptive mesh refinement in OpenFOAM.*  
**SoftwareX, 10, 100317.**  
https://doi.org/10.1016/j.softx.2019.100317

Please make sure that this library is properly compiled and available in your OpenFOAM environment before running the case.

## Repository contents
Typical repository structure:

- `0/` → initial and boundary conditions
- `constant/` → physical properties, mesh, and model parameters
- `system/` → numerical settings and solver controls
- `Allclean` → removes generated files and resets the case
- `Allrun` → executes the complete simulation workflow

## How to run
From the case directory, execute:

```bash
./Allclean
./Allrun
