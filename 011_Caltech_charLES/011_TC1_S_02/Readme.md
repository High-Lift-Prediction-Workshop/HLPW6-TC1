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
Adrian Lozano-Duran (Caltech)

Imran Hayat (Caltech)

Hugh Cairney (MIT)

Yuenong Ling (MIT)

## Primary Email:  
adrianld@caltech.edu

ihayat@caltech.edu

## Primary Phone:  
626-395-2374

## Address:  
California Institute of Technology
Mail Code MC 105-50
Pasadena, CA 91125
 
# SOLVER INFORMATION:

## Solver Name and Version:
Fidelity CharLES

## Basic Algorithm:  
Compressible, unstructured grid, cell-centered finite volume LES

## Turbulence Model:  
WMLES: Vreman SGS + EQWM

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
Stitch (Fidelity CharLES)

## Type (str, overset, unstr, etc):  
Unstructured

## Number of Total Nodes:  
Insert number of nodes here (multiple lines if grid convergence study was done)

## Number of Total Cells:
307027209

## Miscellaneous:  
Grid was provided by SRS-TFG lead (Konrad) - L11 grid

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
