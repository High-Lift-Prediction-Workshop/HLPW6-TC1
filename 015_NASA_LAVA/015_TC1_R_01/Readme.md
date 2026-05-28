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
Jeffrey A. Housman (NASA Ames Research Center)
Jared C. Duensing (NASA Ames Research Center)

## Primary Email:  
jeffrey.a.housman@nasa.gov
jared.c.duensing@nasa.gov

## Primary Phone:  
707-365-9589

## Address:  
N-258, Rm 150
NASA Ames Research Center
Moffett Field, CA 94035
 
# SOLVER INFORMATION:

## Solver Name and Version:
Launch, Ascent, and Vehicle Aerodynamics (LAVA) Framework

## Basic Algorithm:  
Unsteady Compressible Reynolds Averaged Navier-Stokes
Structured Curvilinear Overset/Multiblock Grids
Node-based Finite-Difference in Strong Conservation Law Form

## Turbulence Model:  
Spalart-Allmaras Turbulence Model, Negative Form (SAneg)

## Transition Method:
Assumed fully turbulent flow

## Convergence Criteria:
Two orders of magnitude residual reduction each pseuod-time step within a dual-time stepping implicit approach

## Miscellaneous:  
Convective Flux Discretization: Modified Roe scheme with 3rd-order upwind/4th-order centered left/right state reconstruction and no limiter
Viscous Flux Discretization: 2nd-order mid-point and node central differencing
Phyiscal Time Discretization: 2nd-order Backward Differencing Formula (BDF2)
Solution Procedure: Dual-time stepping with an approximate Newton-Krylov solver using ILU(1) preconditioned GMRES

# Test Case 1 GRID & SOLUTION INFO (CRM-HLS)

## Name of committee-supplied grid used (if other, supply the info below):
Insert name of committee-supplied grid here


For non-committee grids...
## Grid-Generator Name and Version:  
Combination of ANSA (v22.1), Pointwise (v2025.1), Chimera Grid Tools (CGT3.0 alpha3)

## Type (str, overset, unstr, etc):  
Structured Overset/Multiblock grid

## Number of Total Nodes:  
132160950

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
