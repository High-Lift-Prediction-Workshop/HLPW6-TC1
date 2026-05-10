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
Insert name(s) and corresponding organization(s) here
Hidemasa Yasuda (KHI)
Yuta Sawaki (KHI)
Hiroyoshi Asano (KHI)

## Primary Email:  
Insert point of contact (POC) email here
yasuda_hidemasa@global.kawasaki.com

## Primary Phone:  
Insert POC phone here
+81-58-382-5346

## Address:  
Insert POC address here
 
# SOLVER INFORMATION:

## Solver Name and Version:
Insert solver name and version here
cflow-solv.5.10.12

## Basic Algorithm:  
Insert relevant details about algorithm here

## Turbulence Model:  
Insert details about turbulence model here (if applicable)

## Transition Method:
Insert details about transition model or method (if applicable)

## Convergence Criteria:
Insert convergence criteria here (if applicable)

## Miscellaneous:  
Insert any other information about the code/solver here

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):
Insert name of committee-supplied grid here


For non-committee grids...
## Grid-Generator Name and Version:  
Insert grid generator name and version here

## Type (str, overset, unstr, etc):  
Insert grid type here

## Number of Total Nodes:  
Insert number of nodes here (multiple lines if grid convergence study was done)

## Number of Total Cells:
Insert number of cells here (multiple lines if grid convergence study was done)

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
