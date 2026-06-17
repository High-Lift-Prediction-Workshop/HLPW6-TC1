# High Lift Prediction Workshop 6 - LAVA Cartesian Participant ID-013

This folder contains the following files submitted for Test Case 1:

1. **FM.dat** = Time-averaged Force and Moment data vs. angle of attack (multiple grid levels included).
2. **gridconvergence_FM.dat** = Time-averaged Force and Moment data vs. grid level (transpose of #1).
3. **nominalgrid_cpcf.dat** = Surface pressure and skin-friction distributions along the experimental pressure rows (Tecplot ASCII; 24 rows x 11 angles of attack). Row locations are defined [here](https://aiaa-hlpw.org/assets/HLPW6/tc1/TC1_Pressure_Rows.xlsx).
4. **FlowVis/** = Upper-surface skin-friction (Cf) contours and surface skin-friction streamlines for the requested views and angles of attack.
5. **HLPW6_LAVA_CART_ALPHA35_1080p.mp4** = Solution animation for the alpha = 35 deg case.

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
No transition model is used. A turbulence-sensor-based wall model switches between laminar (no-slip) and a blended-log wall-stress model based on the resolved turbulence kinetic energy at the first cell center off the wall (Sozer et al. 2025, SciTech).

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
N/A (cell-centered finite-volume formulation; see total cell count below)

## Number of Total Cells:
Approximately 495-742 million at Level 11. The mesh is time-varying due to on-the-fly adaptive mesh refinement (the cell count grows with angle of attack); the per-angle-of-attack cell count is reported in the N column of FM.dat.

## Miscellaneous:  
The initial mesh is generated automatically from user-defined surface zones with target cell sizes, then adapted on the fly using a small-scale energy error metric (regridding every 10000 steps). Solution coordinates are in meters; the submitted surface distributions (nominalgrid_cpcf.dat) are converted to inches.

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
