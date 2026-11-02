# High Lift Prediction Workshop 6 - Template Submission Files

This folder contains four files participants are expected to modify and submit for Test Case 1:

1. **FM.dat** = Converged or time-averaged Force and Moment data vs. angle of attack, multiple grid levels may be included
   - N.B.: append grid descriptor if providing results for multiple grids
3. **gridconvergence\_FM.dat** =  Converged or time-averaged Force and Moment data vs. grid level, multiple angles of attack may be included (this is a transpose of #1)
4. **nominalgrid\_cpcf.dat** = Surface pressure and skin friction distributions at locations corresponding to experimental pressure belts. These are defined [here](https://aiaa-hlpw.org/assets/HLPW6/tc1/TC1_Pressure_Rows.xlsx)
   - N.B.: remove nominal grid, add grid descriptor if providing results for multiple grids
6. **nominalgrid\_iterative.dat** = Solver iterative convergence with respect to iteration, or if time-dependent, with respect to convective time
   - N.B.: remove nominal grid, add grid descriptor if providing results for multiple grids

Additionally, participants should revise the Readme.md (this file) within their submission directory to include the following data:

# PARTICIPANT INFO:

# Name(s) and Organization(s):
Krishna Zore, Cristhian Aliaga, Jeya Selva, Anil Wakale and Synopsys Inc.

## Primary Email:  
krishna.zore@synopsys.com

## Primary Phone:  
+91 7875102200

## Address:  
Synopsys Inc. 34, 1, MIDC, Phase 1, Rajiv Gandhi Infotech Park, Hinjawadi, Pune, Maharashtra 411057
 
# SOLVER INFORMATION:

## Solver Name and Version:
Fluent v261

## Basic Algorithm:  
Fluent Coupled DBNS

## Turbulence Model:  
SA

## Transition Method:
NA

## Convergence Criteria:
2e-5 for CL and CD and 1e-5 for Residuals  

## Miscellaneous:  
FMG Full multi grid initialization (cold start) 

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):
Pointwise – HexVol (F1) – Quad dominant


For non-committee grids...
## Grid-Generator Name and Version:  
Insert grid generator name and version here

## Type (str, overset, unstr, etc):  
unstructure

## Number of Total Nodes:  
15520444
28289287
75726976

## Number of Total Cells:
25435031
43517347
106410939

## Miscellaneous:  
NA

# "TYPICAL" SOLUTION PERFORMANCE INFORMATION 
## Grid size:
NA
## Computer Platform:  
NA
## Number of Processors:  
NA
## Operating System:  
NA
## Compiler:  
NA
## Run Time CPU:  
NA
## Run Time Wall-Clock:  
NA
## Memory Requirements:  
NA
## Convergence Details
2e-5 for CL and CD and 1e-5 for Residuals  
## Miscellaneous:
NA
# OTHER
NA