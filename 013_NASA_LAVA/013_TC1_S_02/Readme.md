# High Lift Prediction Workshop 6 - LAVA Cartesian Participant ID-013

This folder contains the following files submitted for Test Case 1:

1. **FM.dat** = Time-averaged Force and Moment data vs. angle of attack (Levels 11, 10 and 9 included).
2. **gridconvergence_FM.dat** = Time-averaged Force and Moment data vs. grid level (transpose of #1).

This dataset contains forces and moments only, at alpha = 10, 20, 30, 33, 34, 35, 36, 37, 38 and 39 deg (alpha = 15 and 25 deg were not run for this dataset).

## Differences from 013_TC1_S_01
- Improved FP32 precision.
- Improved wall boundary condition.
- Grid-level schedule: the finest level is added at fixed convective times, L9 at 40, L10 at 80 and L11 at 120 CTU. The same schedule and the same Level 11 mesh settings are used at every angle of attack (about 544 million cells at Level 11).
- Time averaging: each grid level is averaged over the last 10 CTU of the time that level was the finest level (TSTART and TAVG columns in FM.dat).

Additionally, participants should revise the Readme.md (this file) within their submission directory to include the following data:

# PARTICIPANT INFO:

# Name(s) and Organization(s):
Michael Barad (NASA Ames Research Center)
Francois Cadieux (NASA Ames Research Center)
Jared C. Duensing (NASA Ames Research Center)

## Primary Email:  
michael.f.barad@nasa.gov
francois.cadieux@nasa.gov
jared.c.duensing@nasa.gov

## Primary Phone:  
N/A

## Address:  
N-258, Rm 150
NASA Ames Research Center
Moffett Field, CA 94035
 
# SOLVER INFORMATION:

## Solver Name and Version:
Launch, Ascent, and Vehicle Aerodynamics (LAVA) Framework, unreleased development version (newer than Version 1.0.1)

## Basic Algorithm:  
The Cartesian solver within LAVA solves the compressible Navier-Stokes equations on blocks of cubic cells with Octree-type refinement. Objects embedded in the mesh are accounted for via a sharp immersed boundary ghost-cell method. The solver supports various numerical schemes and is geared toward performing wall-modeled large-eddy simulations (WMLES). https://www.nas.nasa.gov/LAVA/cart_docs/introduction_cartesian/

Here is an overview of solver capabilities used:
- Automatic initial mesh generation based on user-defined surface zones with target cell sizes
- Automatic and on-the-fly error metric based adaptive mesh refinement
- Sensor-based upwind/central blended low-dissipation interpolation scheme
- Constant coefficient Vreman subgrid scale model for LES closure
- Custom force/moment integration groups
- Solution sampling on cut planes
- Iso-surface generation of primitive and derived flow quantities (e.g. Q-criterion, density gradient magnitude...) output as triangulated surfaces
- Separate output of volume (parallel) and surface (buffered or parallel) solutions
- Turbulence sensor based wall model (based on Larsson 2015) presented by Sozer et al 2025, SciTech (https://arc.aiaa.org/doi/abs/10.2514/6.2025-0887). Switches between laminar no-slip and blended-log wall model.

## Turbulence Model:  
Constant coefficient Vreman subgrid scale model for LES closure

## Transition Method:
No transition model is used. A turbulence-sensor-based wall model switches between laminar (no-slip) and a blended-log wall-stress model based on the resolved turbulence kinetic energy at the first cell center off the wall (Sozer et al. 2025, SciTech).

## Convergence Criteria:
N/A

## Miscellaneous:  
Convective Flux Discretization: 4th-order HWCNS / KEEPG-HLLE, with upwind blending
Viscous Flux Discretization: 2nd-order
Physical Time Discretization: SSPRK33 (dt is cfl controlled, where for L11 dt ~ 2.5e-7 s)
AMR: Solution-based error metric, regrid every 10000 steps

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):
Insert name of committee-supplied grid here

For non-committee grids...
## Grid-Generator Name and Version:  
ANSA (v22.1) for closed surface triangulation

## Type (str, overset, unstr, etc):  
Block-structured Octree AMR

## Number of Total Nodes:  
N/A (cell-centered finite-volume formulation; see total cell count below)

## Number of Total Cells:
Approximately 544 million at Level 11, 230 million at Level 10 and 60 million at Level 9. The mesh is time-varying due to on-the-fly adaptive mesh refinement; the time-averaged cell count for each angle of attack and grid level is reported in the N column of FM.dat.

## Miscellaneous:  
The initial mesh is generated automatically from user-defined surface zones with target cell sizes, then adapted on the fly using a solution-based error metric (regridding every 10000 steps). Solution coordinates are in meters.

# "TYPICAL" SOLUTION PERFORMANCE INFORMATION 
## Grid size:
Insert the grid size here that was used for providing the subsequent statistics

## Computer Platform:  
Insert computer platform here

## Number of Processors:  
Insert number of processors here

## Operating System:  
Insert operating system here

## Compiler:  
Insert compiler here

## Run Time CPU:  
Insert CPU run time here

## Run Time Wall-Clock:  
Insert wall-clock time here

## Memory Requirements:  
Insert memory requirements here

## Convergence Details
Insert convergence information here (if applicable)

## Miscellaneous:
Insert miscellaneous information here regarding solution performance

# OTHER
Provide any other information desired here
