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
Yoimi Kojima, Yasushi Ito, Mitsuhiro Murayama, Takashi Ishida, Kentaro Tanaka, Tohru Hirai
Japan Aerospace Exploration Agency (JAXA)

## Primary Email:  
kojima.yoimi@jaxa.jp

## Primary Phone:  
+81-70-1170-3159

## Address:  
6-13-1 Osawa, Mitaka-shi, Tokyo
181-0015, Japan

# SOLVER INFORMATION:

## Solver Name and Version:
TAS

## Basic Algorithm:  
unstructured, node-centered

## Turbulence Model:  
SA-noft2-R(Crot=1)

## Transition Method:
N/A

## Convergence Criteria:
Insert convergence criteria here (if applicable)

## Miscellaneous:  
Insert any other information about the code/solver here

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):
R.1.TC1.03 (Pointwise HexVoxel F1)

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
75726976

## Computer Platform:  
JAXA Supercomputer System Generation 3 (JSS3)
TOKI-SORA (HPC System; Fujitsu PRIMEHPC FX1000)

## Number of Processors:  
108 CPUs (=5184 cores)

## Operating System:  
Red Hat Enterprise Linux release 8.6

## Compiler:  
Fujitsu frtpx (FRT) 4.12.1 20250529

## Run Time CPU:  
Insert CPU run time here

## Run Time Wall-Clock:  
12.3 H

## Memory Requirements:  
1362.59 GiB

## Convergence Details
Insert convergence information here (if applicable)

## Miscellaneous:
Timestep CFL was reduced around 110k steps.

# OTHER
Provide any other information desired here
