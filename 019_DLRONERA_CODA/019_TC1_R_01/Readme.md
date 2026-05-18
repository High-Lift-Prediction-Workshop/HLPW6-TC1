# High Lift Prediction Workshop 6 - Template Submission Files

This folder contains four files participants are expected to modify and submit for Test Case 1:

1. **FM.dat** = Converged or time-averaged Force and Moment data vs. angle of attack, multiple grid levels may be included
   - N.B.: append grid descriptor if providing results for multiple grids
3. **gridconvergence\_FM.dat** =  Converged or time-averaged Force and Moment data vs. grid level, multiple angles of attack may be included (this is a transpose of #1)
4. **nominalgrid\_cpcf.dat** = Surface pressure and skin friction distributions at locations corresponding to experimental pressure belts. These are defined here: <insert link to distribution definition>
   - N.B.: remove nominal grid, add grid descriptor if providing results for multiple grids
6. **nominalgrid\_iterative.dat** = Solver iterative convergence with respect to iteration, or if time-dependent, with respect to convective time
   - N.B.: remove nominal grid, add grid descriptor if providing results for multiple grids

Additionally, participants should revise the Readme.md (this file) within their submission directory to include the following data:

# PARTICIPANT INFO:

# Name(s) and Organization(s):
Malte Wegener, Axel Schwoeppe - DLR
Thomas Renaud, Camille Fournais - ONERA

## Primary Email:  
malte.wegener@dlr.de

# SOLVER INFORMATION:

## Solver Name and Version:
CFD Software by ONERA, DLR and Airbus (CODA)

## Basic Algorithm:  
Cell-Centred Finite Volume Method
Strong implicit Non-linear solver

## Turbulence Model:  
Spalart-Allamaras Turbulence model

## Convergence Criteria:
8 orders of residual reduction in Density and Turbulence residual compared to the free-stream residual

All reported resdiual convergence histories are normalized by the free-stream residual

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):
Fixed HeldenMesh family

# "TYPICAL" SOLUTION PERFORMANCE INFORMATION 
## Grid size:
2661338

## Computer Platform:  
AMD EPYC 9005 Turin Zen 5

## Number of Processors:  
2 Nodes x 32 Processes x 4 Threads
= 256 cores

## Compiler:  
GCC 12.3

## Run Time CPU:  
N/A

## Run Time Wall-Clock:  
35 minutes

## Memory Requirements:  
N/A

## Convergence Details
Converged 8 orders of magnitude in both density and turbulence residual compared to free-stream

