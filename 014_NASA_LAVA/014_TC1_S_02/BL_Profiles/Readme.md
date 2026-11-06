# Boundary-layer probes: 014_TC1_S_02 (LAVA Unstructured, Level 11)

Time-averaged profiles at the seven stations requested by the SRS TFG, at spanwise location B. The request is for alpha = 25 deg; the other ten angles are included because the data already exist.

**These are not extractions along the requested rakes.** They come from wall-normal line probes recorded during the runs. They start at the requested points but run in a different direction, and two are shorter. See [Differences from the request](#differences-from-the-request) before overlaying them on other datasets.

## Files

    AoA<alpha>_L11/014_TC1_S_02_BLP_<rake>.csv

There are 11 angles (10, 15, 20, 25, 30, 33, 34, 35, 36, 37, 38 deg) and 7 rakes per angle: SB1, SB2 (slat), WB1, WB2, WB3 (wing), FB1, FB2 (flap). Rake names follow the file names of `extract_BL_v2p2.mcr`. Each CSV has one header row, then one row per point, from the wall outward.

## Differences from the request

| Item | Requested | This dataset |
|---|---|---|
| Rake direction | In the plane y = 16.848 in, along the spreadsheet's normal vector | True 3-D wall normal, which leaves that plane |
| Rake length | 3 in; 5 in for WB3 and FB2 | 3 in for all rakes |
| Points | 1000, uniform | 411, uniform, 0.0073 in apart (410 for SB1 and FB2, see below) |
| Variables | T, ux, uy, uz, \|u\|, urms, p, rho, x, y, z | All present. Density is derived, urms is given per component, and more columns are added (see [Columns](#columns)) |
| Extraction | Tecplot, from a volume solution | LAVA line probes, written during the run |
| Angles | 25 deg | 11 angles, including 25 deg |

Rake by rake:

| Rake | Requested start point (x, y, z) [in] | Requested length [in] | Length here [in] | Angle between requested rake and this rake [deg] | y offset from 16.848 in at the tip [in] |
|---|---|---|---|---|---|
| SB1 | 10.651, 16.848, -1.941 | 3 | 3 | 26.5 | +1.34 |
| SB2 | 13.253, 16.848, -0.142 | 3 | 3 | 21.5 | +1.10 |
| WB1 | 14.740, 16.848, 0.297 | 3 | 3 | 22.8 | +1.17 |
| WB2 | 18.478, 16.848, 1.350 | 3 | 3 | 3.7 | +0.19 |
| WB3 | 35.389, 16.848, 1.252 | **5** | 3 | 4.5 | -0.24 |
| FB1 | 41.174, 16.848, -0.391 | 3 | 3 | 23.8 | -1.21 |
| FB2 | 43.470, 16.848, -2.702 | **5** | 3 | 30.7 | -1.53 |

What this means when comparing:

- **Distance from the wall:** `h_in` is distance along the true wall normal. For a locally flat wall, the same point lies h / cos(angle) along the requested rake, which is 7 to 16% further at SB1, SB2, WB1, FB1 and FB2, and under 1% at WB2 and WB3. Compare against wall distance rather than distance along the rake.
- **FB2 stops inside the wake.** At the 3 in tip, the time-averaged total pressure is still below the value at the WB1 tip by 0.12 q_inf at alpha = 25 deg, rising to 0.89 q_inf at alpha = 38 deg. The outer part of the requested FB2 rake is not covered.
- **WB3 stops outside the wake.** Its 3 in tip shows no total-pressure deficit at any angle, so little is lost by the shorter rake.
- **First points:** each rake starts within 0.003 in of the requested Point 1. The first point of SB1 and FB2 was flagged as outside the fluid at every angle and is left out, so those two rakes start 0.0073 in from the wall.

## Columns

Only time-averaged quantities are included. Coordinates are in inches, everything else is SI.

| Column | Units | Meaning |
|---|---|---|
| `x_in`, `y_in`, `z_in` | in | Point coordinates, in the model axes |
| `h_in` | in | Distance from the rake's first point along the wall normal |
| `T_K` | K | Temperature |
| `ux_ms`, `uy_ms`, `uz_ms` | m/s | Velocity components, in the model axes |
| `umag_over_Uinf` | - | Magnitude of the mean velocity, over U_inf |
| `urms_ms`, `vrms_ms`, `wrms_ms` | m/s | Rms of the velocity components. The request does not say which urms is meant, so all three are given |
| `p_Pa` | Pa | Static pressure |
| `rho_kgm3` | kg/m^3 | Density, derived from p and T as p / (R T). It is not a separately time-averaged quantity |
| `p0_Pa` | Pa | Total pressure |
| `prms_Pa`, `Trms_K` | Pa, K | Rms of pressure and temperature |
| `uv_m2s2`, `uw_m2s2`, `vw_m2s2` | m^2/s^2 | Reynolds shear stresses u'v', u'w', v'w' |
| `tauw_Pa`, `rhow_kgm3`, `muw_Pas` | Pa, kg/m^3, Pa s | Wall shear stress, density and viscosity at the foot of the rake, repeated on every row. Together with `h_in` these give wall units |

Columns up to `rho_kgm3` are the requested variables, plus `h_in`. The rest are extra.

Reference values:

| Quantity | Value |
|---|---|
| Mach number | 0.2 |
| Speed of sound, a_inf | 340.264 m/s |
| Velocity, U_inf | 68.053 m/s |
| Temperature, T_inf | 288.15 K |
| Pressure, p_inf | 100851.1 Pa |
| Density, rho_inf | 1.21948 kg/m^3 |
| Dynamic pressure, q_inf | 2823.83 Pa |
| Gas constant, R | 287.0 J/(kg K) |
| 1 CTU = MAC / U_inf | 0.0112 s |

## Time averaging

The solver's averages are exponential moving averages, not cumulative means. Averaging starts at CTU 30, with a window of 20 CTU. So each profile mainly reflects the last 20 CTU before its sample, not the whole run. Every sample is at least 24 CTU past the start of averaging. `FM.dat` uses its own averaging windows (TSTART, TAVG), so the profiles and the forces do not cover the same span of time.

## Other notes

- **Near the wall:** this is a wall-modeled simulation, so the profile is not resolved down to the wall, and the velocity does not go to zero at `h_in` = 0.
