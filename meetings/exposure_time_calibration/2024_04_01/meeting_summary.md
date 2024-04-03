# ESYWG Meeting
## Exposure Time Calibration Effort
### Date: 01 Apr 2024

**Context:** This is our fourth meeting. Our astrophysical fluxes at the telescope agree (except for a 9% difference in stellar flux, which is still being investigated). We are aiming to have the count rates at the detector plane in agreement and are expanding to additional stars and wavelengths as well.

### Progress since last meeting:

- **Chris:** Followed up with Emiel and verified that yield input packages always reference circumscribed diameter when using units of l/D. 
- **Chris:** Defined a pixel scale and updated assumptions document.
- **Chris, Sarah, & Armen:** Figured out `t_photon_count`.
- **Chris, Sarah, & Armen:** Figured out CR_NF. Chris adopted same approach as EBS/EXOSIMS.
- **Armen:** Included the missing contamination factor.
- **All:** Filled out rest of values for all stars, including the new 1000 nm exposure time columns.

### Reviewing the numbers…

#### Looking at HIP 32439…

##### Basic Parameter Review

- **Armen** is still adopting 6.5 m circumscribed diameter (and the area associated with that) instead of the 7.87 m we’re baselining. This could result in some differences in count rates. Action item to Armen to review this.
- EXOSIMS does not have an equivalent of `t_overhead,dynamic`. Minor issue; will ignore this and simply note that our overheads will not agree in the end.

##### Intermediate Parameter Review

- **T_core:** AYO has higher core throughput in spite of having the same Omega_core. Why is this? Is it possible EBS & EXOSIMS are using units of l/D_insc instead of l/D when getting coronagraph performance? Sarah looked into this and reported that it looked like EXOSIMS/EBS was using the circumscribed diameter. Rhonda disagreed and showed an analysis suggesting that the EXOSIMS coronagraph performance processing utility uses the inscribed diameter in the yield input package header, not the circumscribed diameter that is fed to it. Action to Sarah and Armen to review. Action to Chris to pick a standard separation in units of l/D that is already in the yield input package to calculate core throughput, which would bypass any interpolation issues.
- **I_star:** units on this changed to per unit solid angle. Armen & Sarah need to update these values given the change in units. AYO has different value than EBS/EXOSIMS—this could be related to the same issue as T_core.

##### Count Rate Review

- We added temporary lines in pink that are analytic checks on CR_p and CR_bs using the values reported in the spreadsheet. The pink numbers should agree with the white/gray numbers immediately below them. This helped us find a difference in dQE/PCeff that was corrected. They now agree.
- CR_p numbers between AYO and EXOSIMS differ by a factor equal to the 9% difference in stellar flux multiplied by the 24% difference in T_core. Once we get those fixed, CR_p will agree. Same is expected for CR_bs.
- Other count rates largely agree.
- Looking at the 1 micron results: the EXOSIMS values for F_star and F_p are quite high compared to AYO and EBS. Armen to review.
- Skytrans values don’t agree at 1 micron. Need to investigate once the T_core and I_star issues have been resolved.
- ExoSIMs analytic (pink) count rates don’t agree with white count rates below it. Armen to review.

### Action items:

- **Armen:** Review and correct F12-13.
- **Chris:** Pick a provided offset PSF in the yield input package and report T_core (this avoids any interpolation issues that could be causing differences in T_core).
- **Sarah & Armen:** Look into whether D_circumscribed or D_inscribed is used when retrieving coronagraph performance in units of l/D. Need to print out what D is being used within the processing utility routine.
- **Armen:** Review L32-33.
- **Armen:** Figure out why L47 doesn’t agree with L48, and why L49 doesn’t agree with L50. This probably relates to the issues associated with L32-33.
- **Chris, Sarah, & Armen:** Look into the major disagreement in stray light values for HIP 77052 line 53.
- **Sarah:** Get stray light model from Rhonda & Armen.
- **Chris:** Verify that stray light model is consistent between AYO & EXOSIMS.
- **Chris, Sarah, & Armen:** Report separation and dmag being assumed for the companion star.
- **Chris, Sarah, & Armen:** Once T_core and I_star issues are figured out, review J41-L41
- Chris: review Armen’s zodi value for HIP 113283 and make sure it’s consistent with pointing dependence of model
- Chris: look into exozodi spectral dependence.
