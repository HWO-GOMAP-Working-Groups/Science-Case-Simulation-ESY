# ESYWG Meeting
> **Exposure time calibration effort**
>*25 Mar 2024*

## Context This is our third meeting. Our astrophysical fluxes at the telescope
should agree by this point and we are comparing count rates in the detector
plane.

Looking at HIP 32439…

Astrophysical flux review

F_star: AYO is 9% brighter b/c F0 is 9% larger. Need to understand which F0 to
use.

F_p: AYO is 9% brighter b/c F0 is 9% larger. Need to understand which F0 to
use.

F_zodi: There are differences here that are understood. AYO and ExoSIMS use
pointing dependent zodi fluxes and they are in agreement based on differences
in pointing. EBS uses the canonical 23 mag arcsec^-2 and does not calculate a
pointing-dependent zodi. So we are all in agreement to w/in assumptions.

F_exozodi: 7% variation here. Given differences in exozodi models, this is very
good agreement. Will look for trends with wavelength or spectral type later.

Astrophysical fluxes mostly agree. Some small issues to take care of, but we
understand the reasons for disagreement.

Basic parameter review

F_0: still need to follow up on this. C. Stark working with Noah Tuchow to
understand better. For now this results in 9% higher stellar and planet fluxes
for AYO.

Intermediate parameter review

sp: ExoSIMS has a larger sp b/c the stellar luminosity and distance are
different. This all checks out.

Omega_core: AYO tuned the PSF ratio to get the same value as EBS & ExoSIMS.

T_core: AYO has higher core throughput in spite of having the same Omega_core.
Why is this? Is it possible EBS & ExoSIMS are using units of l/D_insc instead
of l/D when getting coronagraph performance?

Det_npix: we disagree on this number, likely due to a pixel scale issue. EBS
was just forcing the # of detector pixels as described in the assumptions
document. Need to update this document to just state the pixel scale. Probably
assume Nyquist sampling at 500 nm.

t_photon_count: this value is missing for EBS & ExoSIMS. Not sure how CIC is
being converted into a count rate. Chris, Sarah, and Armen need to tag up
offline about this.

CR_NF: this varies by an order of magnitude among the group. This is b/c AYO is
using a NF that is fixed in delta_mag, while EBS & ExoSIMS are using something
proportionate to contrast. Will need to work this out offline.

Dmitry: When will we be looking at other wavelengths?

Chris: We should try to do that by next week. Let’s see if we can get count
rates in agreement for the first star by next week, then move on to multiple
stars and multiple wavelengths. Will need to reformat the google sheet to
account for another wavelength.
