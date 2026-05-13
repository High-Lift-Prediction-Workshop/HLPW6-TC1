# High Lift Prediction Workshop 6 - Template Submission Files

This folder contains No.1. and 3. files of the followings:

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
Hidemasa Yasuda (KHI)  
Yuta Sawaki (KHI)  
Hiroyoshi Asano (KHI)

## Primary Email:  
yasuda_hidemasa@global.kawasaki.com

## Primary Phone:  
+81-58-382-5346

## Address:  
1.Kawasaki-Cho, Kakamigahara City, Gifu-Pref. 504-8710 Japan  
 
# SOLVER INFORMATION:

## Solver Name and Version:
Cflow, cflow-solv.5.10.12

## Basic Algorithm:  
Unstructured Navier-Stokes solver, Cell-centered finite volume method  

## Turbulence Model:  
SA-neg  

## Transition Method:
none (fully turbulent)  

## Convergence Criteria:
Eyeball and Cflow method (\*)  

(\*) Based on the gradient of CL and CD convergence history.  
CL does not change 0.01 within 2FT, CD does not change 0.001 within 2 FT.  
FT=2 Flow Through MAC based on averaged time step.  
https://doi.org/10.2322/jjsass.71.181 (In Japanese)  
! Some cases does not satisfy this criteria in this version.

## Miscellaneous:  
Nothing  

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):
R.1.TC1.01 HeldenMesh fixed grid family (Helden Series 03)  

For non-committee grids...
## Grid-Generator Name and Version:  
Insert grid generator name and version here

## Type (str, overset, unstr, etc):  
Insert grid type here

## Number of Total Nodes:  
Insert number of nodes here (multiple lines if grid convergence study was done)

## Number of Total Cells:
B: 5,730,017  
C: 17,156,245  
D: 38,396,609
E: 121,556,748

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
