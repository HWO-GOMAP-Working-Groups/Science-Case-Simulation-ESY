# Meeting to work on ESYWG/CTR/CDS Exposure Time Calibration
18 March 2024

## Introduction
- Reviewed all values for HIP 32439 through Row 30 (“Basic Parameters” and “Astrophysical Fluxes”).
- AYO and EBS generally agreed on most values. Astrophysical fluxes are all similar. Most differences appear to be minor or likely related to detailed treatments of exozodi model, pointing, etc. See list of action items below to follow up on these differences
- Primary mirror collecting areas were notably different between all codes–need to follow up on this
- Difference in flux zero points. ExoSIMS doesn’t really use this internally–all fluxes are calculated by integrating a spectral model over the bandpass, whereas AYO relies on interpolations of empirical photometry. However, we should agree on these values and for some reason AYO’s source of flux zero points are ~10% larger than ExoSIMS’.

### Notes
Pin: Angular separation of the target planet is different for EBS & ExoSIMS–this should be exactly the same
Dmitry: we should consider extending this detection study to a different wavelength prior to looking into spectral characterization

## Action Items
Chris & Dmitry: look into why the AYO V band flux zero point disagrees with the ExoSIMS/EBS flux zero point.
Chris: Look into the correct values for Row 11
Armen: Figure out why E27 and F27 disagree.
Armen: Same for E and F 28-30
Chris: Look into why D29 and E29 disagree. Maybe due to treatment of telescope pointing/RA/Dec?
Sarah: check if E30 includes the nzodis factor or not. It should include the nzodis=3 factor.
To do for next week: complete all remaining rows of the existing tabs. We will review the intermediate parameters, count rates, and exposure times for all 5 fiducial targets at next week's meeting.



