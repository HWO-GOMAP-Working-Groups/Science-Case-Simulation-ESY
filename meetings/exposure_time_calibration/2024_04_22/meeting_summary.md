# ESYWG Meeting
## Exposure Time Calibration Effort
**Date:** 22 Apr 2024

### Context
This is our 7th meeting. All fluxes and count rates seem to agree for HIP 32439. All count rates agree for HIP 77052, except for CR_bstray.

### Progress Since Last Meeting
- Chris, Sarah, & Armen have been looking into issues regarding CR_bstray.

### Looking at HIP 77052…
#### Count Rate Review
- **CR_bstray:** AYO’s count rates are ~100x higher than EBS. EXOSIMS is many orders of magnitude higher.
  - Discussion of the formulas used to calculate stray light from a binary companion. Formulas are fairly similar. Chris shows formulas used by AYO (see PPT slides).
  - One source of difference is that EXOSIMS applies the core throughput of the coronagraph whereas AYO applies “skytrans” assuming it’s a diffuse source. At the last meeting, we said this could account for a factor of ~2, but it may be much larger.
    - **T_core** is the fraction of the PSF inside of the photometric aperture evaluated for a single point source.
    - **Skytrans** must be evaluated over the same photometric aperture. Since it is convolved with a uniform background, the value of skytrans evaluated over the photometric aperture is more than multiplied by the number of pixels in the skytrans map within the photometric aperture.
    - One thing that will help resolve this issue is by putting skytrans in units of per solid angle in the google spreadsheet. Chris updated this.
    - General discussion about the validity of these equations and the proper treatment of stray light from a binary companion.
    - Chris will follow up with Dmitry and John Krist offline to make sure we’re implementing the correct formulas.
    - Chris will manually verify that the difference between using T_core and skytrans can result in the large difference we observe.

### Looking at All Targets…
#### Review of 1000 nm Detection Numbers
- Most of the count rates still check out when calculating detections at 1000 nm.
- One area of disagreement is in the exozodi flux. The EXOSIMS and AYO exozodi fluxes change differently on a per-target and wavelength basis. This may relate to exozodi spectral type dependence and color dependence included in the calculations. Need to figure this out.

## Action Items
- Chris: manually verify that using skytrans vs T_core can produce the large difference in stray light count rates observed.
- Chris: follow up offline with Dmitry & John K (& Bijan?) to settle on the correct implementation of stray light from binary companion.
- Chris, Sarah, Armen: Look into color and spectral type dependence of exozodi and create some basic tests to understand spectral type, color, and distance dependence.

