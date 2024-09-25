# ESYWG Full Membership Meeting Minutes  
**Date:** July 25, 2024  

## Agenda:
1. **Task Group Updates**
2. **Presentation: Photometric and Spectroscopic Characterization for Exo-Earth Survey (Avi Mandell)**

---

### 1. Task Group Updates

- **Visualizations Task Group**:  
  - Presented by **Sarah Steiger**  
  - The group's GitHub repository is up and running, thanks to Corey Spohn's efforts.  
  - The infrastructure has been set up for coding and contributions via virtual environments (Conda).  
  - Future plans include setting up a coding infrastructure and encouraging more contributors to the platform.
  
- **Survey Strategies Task Group**:  
  - Presented by **Natasha Latouf**  
  - The group had their first recurring meeting, where they discussed strategies to evaluate collected survey data in collaboration with tools like AYO and EXOSIMS.  
  - Next meeting will be in two weeks, as meetings are scheduled bi-weekly.  
  - Attendance was light due to the SAGAN workshop, but key insights were gained for yield strategy development.
  
- **Yield Parameter Documentation Task Group**:  
  - Update deferred to an email or the next meeting due to the absence of **Dmitry Savransky** and **Tiffany Glassman**.

---

### 2. Presentation: Photometric and Spectroscopic Characterization for Exo-Earth Survey  
**Presenter:** Avi Mandell

#### Overview:
- Avi Mandell's presentation builds on **Jacob Lustig-Yaeger's** previous talk, focusing on how to characterize rocky, potentially habitable exoplanets through photometry and spectroscopy, and how these findings contribute to yield optimization.
- The discussion aimed to balance detection of planetary characteristics with the optimization of yield for observing the properties of planets, especially Earth-like ones.

#### Key Topics:
- **Planetary Parameter Constraints**:
  - Understanding which planetary parameters can be constrained through observations, including properties like water vapor, atmospheric composition, and biosignatures.
  - The complexity of differentiating between biological and abiotic processes and how to avoid false positives in biosignature detection.
  
- **Challenges with Limited Data**:
  - Working with limited data (e.g., single-spectrum information), and the need to break down observations into wavelength-dependent chunks using different detectors.
  
- **Target Prioritization**:
  - Prioritizing planets and their characteristics based on constraints versus the observing time required to gather meaningful data.
  - The importance of balancing ambiguity (e.g., common signatures like CO2 or CH4) against rarity (e.g., techno-signatures or complex biosignatures).

#### Detailed Sections:
1. **Planetary Characteristics from Spectroscopy**:
   - Focusing on biosignature detection, Mandell reviewed methods to identify key planetary traits using wavelength-dependent spectra.
   - He emphasized the importance of various molecular tracers (e.g., water vapor, CO2, O2) and the challenge of interpreting these with limited observations across different wavelength ranges.

2. **Survey Strategy Considerations**:
   - Mandell discussed how planetary characteristics should guide survey strategies, with initial focus on simple photometric detections of water vapor and progressing towards more complex characteristics like methane or ozone detection.
   - He highlighted the importance of balancing precision and the observational time required to capture this data, using tools like Bayesian retrievals to model the likelihood of key planetary signatures being detectable.

3. **Optimization for Yields**:
   - Yields optimization must incorporate the precision of data needed for specific scientific questions (e.g., determining the abundance of H2O or CH4).
   - Mandell pointed to recent studies, including work by **Amber Young**, to illustrate how spectral bandpass optimization plays a critical role in yield calculation. 

4. **Noise Modeling and Instrument Limitations**:
   - The talk touched on challenges with instrument sensitivity (e.g., coronagraph throughput, quantum efficiency of detectors) and the need for high-fidelity noise modeling across different wavelength ranges.
   - Accurate noise models will be critical to understanding how much observing time is necessary to achieve the desired signal-to-noise ratio for detecting planetary features.

#### Questions & Discussion:
- **Sarah Steiger** asked about bias in focusing observations on detecting water, potentially overlooking non-water planets that could offer interesting insights into planet formation or geophysics.
  - **Avi Mandell** responded by acknowledging the importance of detecting key markers of geophysics (e.g., CO2 and water vapor) first, even if the planets do not appear to support life like Earth. The detection of such markers will provide valuable information about a wide variety of planets.
  
- **Eric Lopez** raised concerns about the detection of planets with massive steam atmospheres (e.g., water worlds) and how their signatures might differ from habitable exoplanets with liquid water.
  - **Avi Mandell** agreed that this is an important area for further modeling, particularly in terms of atmospheric aerosols and how they would affect observations.

### Conclusion:
- The meeting concluded with **Avi Mandell** encouraging members to reach out to join the **Survey Strategy Task Group**. He emphasized the importance of collaboration, particularly in refining noise models and integrating findings into yield optimization tools.
