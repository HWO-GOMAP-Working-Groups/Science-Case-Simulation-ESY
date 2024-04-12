# **ESYWG Meeting**

## **Exposure time calibration effort**

### 11 Apr 2024

**Context:** This is our fifth meeting. This is a small working session with just Sarah, Armen, and Chris. Our astrophysical fluxes at the telescope agree (except for a 9% difference in stellar flux, which is still being investigated). Most intermediate parameters agree and count rates are close, but we still have disagreement in T_core, I_star, CR_bs, and CR_bstray.

**Progress since last meeting:**

- **Chris, Sarah, & Armen**: have been looking into issues regarding T_core.
- **Chris, Sarah, & Armen**: have been looking into binarity issues

**Reviewing the numbers…**

**Looking at HIP 32439…**

**Intermediate parameter review**

- T_core: AYO has higher core throughput in spite of having the same Omega_core. Why is this?
  - Looked into T_core this past week. Chris manually verified the AYO T_core is roughly correct. Found out the issue was due to a combination of a miscommunication in assumptions as well as a two-step process in ExoSIMS in which Omega_Core can accidentally be inconsistent.
    - To calculate yields using the yield input packages, ExoSIMs uses a two-step process. First, the yield input package must be processed with a given photometric aperture. Then, the yield calculator is called. It is possible to process the yield input package with a different photometric aperture than what is sent to the yield calculator, and due to a miscommunication in the assumptions (the assumptions were to use a photometric aperture radius of 0.7 l/D_inscribed, not 0.7 l/D, which was the only time we referred to using the inscribed diameter and was confusing), this is what was happening. Now that this has been identified T_core is basically in agreement. Chris will reach out to Dmitry.
- I_star: we still don't agree on this. Not sure why.
  - One issue was found regarding how ExoSIMs treats the photon counting efficiency, PCeff. For some reason, this only applies to the planet's count rates and does not affect the star, zodi, or exozodi. Armen and Sarah were using this term as a substitute for dQE, whereas dQE should affect all sources. Instead of updating ExoSIMS, we just got rid of the dQE assumption altogether and updated QE to the product of the two. Chris will reach out to Dmitry to look into this.
  - We have two action items to address continued disagreement (see below)

**Looking at HIP 77052…**

**Count rate review**

- CR_bstray: Armen found he had different separation and dmag for the stellar companion. We reviewed the WDS data and determined those values appear to be erroneous and due to a mishandling of the WDS data. The bogus values are not in to the original ExoCAT, but appear in the ExoCAT update file that is being used in ExoSIMS. This may require an update (see action item below).

**Action items:**

- **Chris:** pick a single slice of the stellar_intens.fits file and calculate Istar manually at a given separation to investigate what the "correct" value is and whether this is an issue of mean vs median vs integration over an aperture, etc.
- **Sarah:** Double-check that changing the photometric aperture in the ExoSIMS coronagraph pre-processor changes CR_bs (roughly proportionately to the area of the aperture)
- **Chris:** will reach out to Eric Mamajek to make sure we understand the proper parsing of the WDS data prior to suggesting a change to the ExoCAT update file.

