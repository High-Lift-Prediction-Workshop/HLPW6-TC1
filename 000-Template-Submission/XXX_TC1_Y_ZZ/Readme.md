# High Lift Prediction Workshop 6 - Template Submission Files

This folder contains four files participants are expected to modify and submit for Test Case 1:

1. **FM.dat** = Converged or time-averaged Force and Moment data vs. angle of attack, multiple grid levels may be included
   - N.B.: append grid descriptor if providing results for multiple grids
3. **gridconvergence\_FM.dat** =  Converged or time-averaged Force and Moment data vs. grid level, multiple angles of attack may be included (this is a transpose of #1)
4.nominalgrid\_cpcf.dat** = Surface pressure and skin friction distributions at locations corresponding to experimental pressure belts. These are defined [here](https://aiaa-hlpw.org/assets/HLPW6/tc1/TC1_Pressure_Rows.xlsx)
   - N.B.: remove nominal grid, add grid descriptor if providing results for multiple grids
6. **nominalgrid\_iterative.dat** = Solver iterative convergence with respect to iteration, or if time-dependent, with respect to convective time
   - N.B.: remove nominal grid, add grid descriptor if providing results for multiple grids

Additionally, participants should revise the Readme.md (this file) within their submission directory to include the following data:

# PARTICIPANT INFO:

# Name(s) and Organization(s):
Alaa Elmiligui 	NASA , 
Boris Diskin  	NASA
Craig A. Hunter   NASA
Mohagna J. Pandya NASA
Sally Viken 	NASA
tausif jamal 	NASA
Andrew Wick 	HeldenAero 
John R. Hooker HeldenAero

## Primary Email:  
alaa.a.elmiligui@nasa.gov

## Primary Phone:  
757-864-5004

## Address:  
Alaa ELmiligui
Configuration Aerodynamics Branch
Research Directorate
NASA Langley Research Center
Mail Stop 499
Hampton, VA 23681-2199
 
# SOLVER INFORMATION:
USM3D-ME	 1.0.1 ( https://software.nasa.gov/software/LAR-19841-1 )
## Solver Name and Version:
USM3D-ME         1.0.1 
## Basic Algorithm:  
2nd-order, cell-centered, finite-volume, mixed-element  
Insert details about turbulence model here (if applicable)
SA-neg
## Transition Method:
N/A 

## Convergence Criteria:
meanflow and turbulence-model residuals reach machine zero or F&M averages over last 2000 iterations remain within prescribed tolerance

## Miscellaneous:  
Initialization method:  Free stream conditions
Time integration or iteration method: Steady state with Hierarchical Adaptive Nonlinear Iteration Method (HANIM)

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):
R.1.TC1.02 HeldenMesh Adaptive grid family (Helden Series 04)


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
NASA Advanced Supercomputing (NAS) Electra Skylake Nodes
k-cluster at NASA Langley

## Number of Processors:  
2000

## Operating System:  
Insert operating system here

## Compiler:  
intel

## Run Time CPU:  
Insert CPU run time here

## Run Time Wall-Clock:  
Insert wall-clock time here

## Memory Requirements:  
Insert memory requirements here

## Convergence Details
meanflow and turbulence-model residuals reach machine zero or F&M averages over last 2000 iterations remain within prescribed tolerance

## Miscellaneous:
Insert miscellaneous information here regarding solution performance

# OTHER
Provide any other information desired here
