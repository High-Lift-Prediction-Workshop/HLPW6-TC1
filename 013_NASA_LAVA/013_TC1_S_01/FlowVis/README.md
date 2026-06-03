# Flow Visualization — 013_NASA_LAVA (LAVA Cartesian, Level 11)

Upper-surface skin-friction (C<sub>f</sub>) contours and surface skin-friction
streamlines for HLPW6 Test Case 1, following the views and variables defined at
<https://aiaa-hlpw.org/HLPW6/TC1_Post>.

- **C<sub>f</sub>** = |τ<sub>w</sub>| / q<sub>∞</sub> (freestream dynamic pressure),
  banded **0 to 0.02 in 0.002 increments** with the `CfMap_HLPW5` colormap.
- Time-averaged (running exponential moving average) surface solution on the
  **Level 11 (finest)** adaptively refined mesh.
- **Two images per view, per angle of attack:**
  - `aoaYYY_tauw_view_0N_<name>.png`  — skin-friction magnitude only
  - `aoaYYY_stream_view_0N_<name>.png` — skin-friction magnitude with surface streamlines
- **Views:** `view_01_wing`, `view_02_slat`, `view_03_flap`, `view_04_B2_top`, `view_05_B2_bottom`.
- **Angles of attack (deg):** 10, 15, 20, 25, 30, 33, 34, 35, 36, 37, 38.

View 6 (slat-bracket wake vorticity) is not included — it requires off-body
volumetric vorticity fields and cutting planes, which are outside this
surface-solution submission.
