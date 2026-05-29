# High Lift Prediction Workshop 6 - LAVA Cartesian Participant ID-013

This folder contains four files participants are expected to modify and submit for Test Case 1:

1. **FM.dat** = Converged or time-averaged Force and Moment data vs. angle of attack

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
Launch, Ascent, and Vehicle Aerodynamics (LAVA) Framework, Version 1.0.1

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

## Convergence Criteria:
N/A

## Miscellaneous:  
Convective Flux Discretization: 4th-order HWCNS / KEEPG-HLLE, with upwind blending
Viscous Flux Discretization: 2nd-order
Phyiscal Time Discretization: SSPRK33 (dt is cfl controlled, where for L11 dt ~ 2.3e-7 )
AMR: Small-scale energy error metric based, regrid every 10000 steps

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):
Insert name of committee-supplied grid here

For non-committee grids...
## Grid-Generator Name and Version:  
ANSA (v22.1) for closed surface triangulation

## Type (str, overset, unstr, etc):  
Block-structured Octree AMR

## Number of Total Nodes:  

## Number of Total Cells:
742million, but time-varying

## Miscellaneous:  
Insert any other information about the grids or solution procedure(s) used for Case 2.1 here

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
