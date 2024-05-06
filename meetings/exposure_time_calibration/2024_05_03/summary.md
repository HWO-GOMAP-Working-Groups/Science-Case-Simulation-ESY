# ESYWG Meeting
## Exposure Time Calibration Effort
**03 May 2024**

### Context
This is our 9th meeting. Most aspects of detection and characterization times agree. Known outstanding issues include:

1. **<10% Differences in Stellar Fluxes:**
   - Likely stems from differences in calculating flux.
   - AYO uses flux zero points and interpolates magnitudes.
   - ExoSIMS obtains stellar flux data, fits a high-resolution template spectrum to it, then integrates over the bandpass.
   - Disagreement varies with spectral type. AYO overpredicts flux from early-type stars and underpredicts it for later-type stars compared to ExoSIMS.
   - Later versions of AYO could be updated to adopt the ExoSIMS approach.

2. **Exozodi Calculation Differences:**
   - ExoSIMS currently scales exozodi color based on zodi (the Sun’s color), not the target star’s color.
   - Requires an update to ExoSIMS, but the timeline is unclear.

3. **Stray Light from Binary Stars:**
   - There are significant differences in calculation methods.
   - Still working on resolving this issue.

### Review Topics
1. **HIP 26779 - Astrophysical Fluxes Review:**
   - ExoSIMS and EBS have different stellar flux values for detection times at 1 micron despite agreeing closely at 500 nm.
   - ExoSIMS and AYO largely agree, indicating an EBS issue.
   - Stellar input parameters are very similar (5226 K for EBS vs. 5263 K for ExoSIMS).
   - Follow-up required.

2. **HIP 32439 - Intermediate Parameters Review:**
   - Istar differs between ExoSIMS and EBS for spectral characterization at 800 nm.
   - Codes agree at 500 nm and 1000 nm for this target.
   - ExoSIMS and AYO agree, indicating an EBS issue.
   - Follow-up required.

### Action Items:
1. **Chris:** Look into the timeline for the exozodi issue.
2. **Sarah & Armen:** Investigate why Fstar differs for HIP 26779 at 1 micron.
3. **Sarah & Armen:** Investigate why Istar differs at 800 nm for HIP 32439. Break it down into component factors and identify which factor is responsible.

