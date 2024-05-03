# ESYWG Meeting
## Exposure Time Calibration Effort
### 29 Apr 2024

**Context:** This is our 8th meeting. Most aspects of detection times agree. Outstanding issues include:
1. Less than 10% differences in stellar fluxes likely stemming from how we’re calculating flux.
2. Differences in how we’re calculating exozodi as a function of wavelength.
3. Large differences in how we’re calculating stray light from binary stars.

**Progress since last meeting:**
- **Chris:**
  - Determined ExoSIMS is likely calculating exozodi’s color based off of zodi’s color instead of the target star. Still need to verify this is the case.
  - Has been looking into issues regarding CR_bstray. No consensus on this yet.
  - Created spreadsheet for comparison of spectral characterization times.

**At this meeting we’ll be comparing characterization times to detect O2 at 800 nm looking exclusively at HIP 32439…**

### Basic Parameters Review
- These all look good.

### Astrophysical Fluxes Review
- These all look good except maybe exozodi. Chris needs to verify differences are actually due to scaling with zodi color instead of target star.

### Intermediate Parameters Review
- Sp Omega Tcore and skytrans all look good.
- Istar is not in agreement. Need to figure out why. Likely due to either differences in how we’re treating the stellar diameter or differences in Dinsc vs Dcirc when defining units.
- det_npix disagrees by factor of 1.5. This is because AYO is adopting 6 pix per lenslet whereas ExoSIMS is adopting 4. Chris to follow up with Neil Z and Mike M to get current best estimate.

### Count Rate Comparison
- This needs to be followed up after taking care of items above but overall looks good.
- For some reason AYO is listing a value for CR_bstray even though zero is expected. Chris needs to look into this.

**Action items:**
- Chris, Sarah & Armen: manually look into Istar value.
- Chris: Get best estimate of lenslet pixel multiplier.
- Chris: Manually check if ExoSIMS and AYO exozodi values at lambda > 550 nm would agree if scaled by stellar flux instead of zodi color.
- Chris: Figure out why AYO reports stray light for HIP 32439 at 800 nm.

