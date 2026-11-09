# High Lift Prediction Workshop 6 \- Template Submission Files

This folder contains four files participants are expected to modify and submit for Test Case 1:

1. **FM.dat** \= Converged or time-averaged Force and Moment data vs. angle of attack, multiple grid levels may be included  
   - N.B.: append grid descriptor if providing results for multiple grids  
2. **gridconvergence\_FM.dat** \=  Converged or time-averaged Force and Moment data vs. grid level, multiple angles of attack may be included (this is a transpose of \#1)  
3. **nominalgrid\_cpcf.dat** \= Surface pressure and skin friction distributions at locations corresponding to experimental pressure belts. These are defined [here](https://aiaa-hlpw.org/assets/HLPW6/tc1/TC1_Pressure_Rows.xlsx)  
   - N.B.: remove nominal grid, add grid descriptor if providing results for multiple grids  
4. **nominalgrid\_iterative.dat** \= Solver iterative convergence with respect to iteration, or if time-dependent, with respect to convective time  
   - N.B.: remove nominal grid, add grid descriptor if providing results for multiple grids

Additionally, participants should revise the Readme.md (this file) within their submission directory to include the following data:

# PARTICIPANT INFO:

# Name(s) and Organization(s):

Mehmet Sahin, Hulya Sukas, İbrahim Asar — Istanbul Technical University

## Primary Email:

[msahin@itu.edu.tr](mailto:msahin@itu.edu.tr), [hulyaistifsukas@gmail.com](mailto:hulyaistifsukas@gmail.com), [asar17@itu.edu.tr](mailto:asar17@itu.edu.tr)

## Primary Phone:

## Address:

# SOLVER INFORMATION:

## Solver Name and Version:

HEMLAB

## Basic Algorithm:

Vertex-based finite volume method with the AUSMpM flux scheme.

## Turbulence Model:

Spalart–Allmaras negative model (SA-neg).

## Transition Method:

## Convergence Criteria:

$1{0}^{-5}$, $1{0}^{-6}$ (RHS L2 Norm)

## Miscellaneous:

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):

For non-committee grids...

## Grid-Generator Name and Version:

NASA refine

## Type (str, overset, unstr, etc):

Unstructured, tetrahedral.

## Number of Total Nodes:

Final mesh node counts from gridconvergence\_FM.dat:

- AoA \= 20 deg: 40325446 nodes.  
- AoA \= 25 deg: 40293125 nodes.  
- AoA \= 30 deg: 40253765 nodes.  
- AoA \= 35 deg: 40185775 nodes.

## Number of Total Cells:

## Miscellaneous:

Anisotropic mesh adaptation using a Mach-number Hessian sensor.

# "TYPICAL" SOLUTION PERFORMANCE INFORMATION

## Grid size:

## Computer Platform:

## Number of Processors:

## Operating System:

## Compiler:

## Run Time CPU:

## Run Time Wall-Clock:

## Memory Requirements:

## Convergence Details

The AUSMpM solutions did not fully converge.

## Miscellaneous:

# OTHER