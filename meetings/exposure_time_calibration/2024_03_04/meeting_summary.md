# Notes from Meeting to Discuss ESYWG/CDS/CTR Exposure Time Calibration Efforts
> 04 March 2024

## Introduction
- Reviewed goals of CDS, CTR, and ESYWG; all desire an exposure time calibration of some sort, so we're coordinating
ESYWG will end up inheriting the exposure time calibration as CDS and CTR will ramp down
- We want this effort to potentially be long-lived, meaning we can repeat this process one or two years from now
- Files will be kept in ESYWG folder for this reason, but results and discussion can be used by all three groups

## Discussion of approach
- We will adopt the 5 fiducial stars already defined by CTR. There was interest in expanding this to potentially an M-type star that really pushed IWA, as well as a star that did not push IWA (e.g., close F type star). We may expand this list in the future after getting agreement on these 5
- There is a spreadsheet in the google drive folder that lists parameters for comparison
- Our goal isn't to get perfect agreement on exposure times, but to understand why there are differences. As such, we will be tracking inputs, intermediate values, count rates, as well as final exposure times. We should have our code directly report the values it is using as late as possible in the calculation (i.e., don't list the input values in the comparison sheet—list values directly printed from the code).
- We expect to have disagreements and find bugs—this is part of the process

## Discussion of assumptions
- Astrophysical assumptions are all well-defined
- May be differences in treatment of exozodi or local zodi—we will see these when we report astrophysical fluxes
- Are starting with a very simple observing strategy
- Focus on detection at 500 nm only to start with. Will look at characterization later
- The noise floor is potentially a source of complication when comparing calculations. Some noise floor count rates are determined by the contrast, post processing factors, other inputs, etc. We may need to build in the ability to alter this to a given value so that we can easily compare exposure times.
- Example exposure time equations given. We should include planet's count rates as a source of noise as well as a factor of 2 on the backgrounds to account for ADI.

## Mission parameters
- We are going to start with the CDS mission parameters with some alterations. We will simplify to a single coronagraph channel with a single coronagraph design. We will adopt detector noise parameters consistent with EMCCD. Chris to finalize these mission parameters and send around.

## Documentation of efforts
- We should all save a local instance of our code specific to these comparisons. This will make it easier to repeat in the future.
