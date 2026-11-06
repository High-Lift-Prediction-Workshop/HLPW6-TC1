# High Lift Prediction Workshop 6 - LAVA Unstructured Participant ID-014

This folder contains the following files submitted for Test Case 1:

1. **FM.dat** = Time-averaged Force and Moment data vs. angle of attack.
2. **nominal\_cpcf.dat.gz** = Time-averaged surface pressure and skin friction at the experimental pressure belts on the nominal (Level 11) grid. Rows are defined [here](https://aiaa-hlpw.org/assets/HLPW6/tc1/TC1_Pressure_Rows.xlsx).
3. **FlowVis/** = Time-averaged surface flow visualization on the Level 11 grid, in the standard workshop views.
4. **BL\_Profiles/** = Time-averaged boundary-layer probe profiles at all angles. Its Readme.md explains the columns and how these rakes differ from the SRS TFG's request.

This dataset is a fresh Level 11 alpha sweep at alpha = 10, 15, 20, 25, 30, 33, 34, 35, 36, 37 and 38 deg, with no grid sensitivity set. 014_TC1_S_01 is unchanged.

## Differences from 014_TC1_S_01
- Single-precision (FP32) build of the solver; 014_TC1_S_01 ran in double precision.
- Upwind blending sensor: strain-based sensor, replacing the modified Ducros sensor used in 014_TC1_S_01.
- Reduced dissipation in the upwind component of the convective flux, now 3rd order in regular mesh regions.
- Improved gradient accuracy and MUSCL reconstruction limiter.
- Regenerated Level 11 Voronoi mesh: 229,513,185 cells and 1,407,147,194 nodes (260,094,313 and 1,608,010,550 in 014_TC1_S_01). S_01 mesh was finer than intended at the wall. The new LAVA Voronoi mesher version used in S_02 addresses this.
- Time averaging: FM.dat uses the windows in its TSTART and TAVG columns. The surface data and BL profiles use the solver's exponential moving average from CTU 30, with a 20 CTU window.

# PARTICIPANT INFO:

# Name(s) and Organization(s):
Emre Sozer (NASA Ames Research Center)
Jared C. Duensing (NASA Ames Research Center)

## Primary Email:  
emre.sozer@nasa.gov
jared.c.duensing@nasa.gov

## Primary Phone:  
N/A

## Address:  
N/A

# SOLVER INFORMATION:

## Solver Name and Version:
Launch, Ascent, and Vehicle Aerodynamics (LAVA) Framework, Version 1.1.0

## Basic Algorithm:  
LAVA Unstructured uses arbitrary polyhedral unstructured meshes with a cell-centered finite-volume formulation.
In this test, a WMLES approach is used with low dissipation, kinetic energy preserving convective flux paired with sensor-based application of localized upwinding. Time integration is explicit with the 3rd order accurate SSPRK33 scheme. A constant coefficient Vreman SGS model is used with directional filter size. An equilibrium wall model is used in conjunction with a turbulence sensor that switches between no-slip and wall model wall stress based on resolved turbulence kinetic energy level. The wall model uses the first cell center off the wall as the sampling location. Details about the scheme are documented in Sozer et al 2025, SciTech (https://arc.aiaa.org/doi/abs/10.2514/6.2025-0887). 

## Turbulence Model:  
- Constant coefficient Vreman subgrid scale model with directional filter size.
- Equilibrium wall model.

## Transition Method:
- Wall model switches between no-slip (laminar) and wall function (turbulent) wall stresses based on detected resolved turbulence kinetic energy at the first cell center off the wall.
- No true transition model is used.

## Convergence Criteria:
N/A

## Miscellaneous:  
- Convective flux: 2nd-order kinetic-energy-preserving flux, blended with an AUSMPW+ upwind flux using the rminmod limiter.
- Time step: CFL-controlled at CFL = 2.5. The nondimensional time step is the DT column of FM.dat.
- Vreman SGS constant: 0.08.
- Wall model: blended log law, with a transition threshold of 0.05.

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):
N/A (non-committee grid, see below)

For non-committee grids...
## Grid-Generator Name and Version:  
LAVA Voronoi Mesher, development build of 2026-07-21

## Type (str, overset, unstr, etc):  
Unstructured Voronoi 

## Number of Total Nodes:  
(L11) 1407147194

## Number of Total Cells:
(L11) 229513185

## Miscellaneous:  
N/A

# "TYPICAL" SOLUTION PERFORMANCE INFORMATION 
Not provided.

# OTHER
N/A
