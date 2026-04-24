
**Date:** April 24, 2026  
**Time:** 15:00 (CEST)  

#### Present:

Jean-Luc PONS (ESRF)
Teresia Olsson (HZB)
Theo Rozier (ESRF)
Patrick Madela (SOLEIL)
Konstantinos Paraschou (DESY)

#### Discussion: 

Orbit response matrix tested at Synchrotron SOLEIL (S. Habet). Small issue for correction (likely,
forgot to attach __manually__ created orbit correction object to sr.live). No major issues.

##### Ophyd-async device integration

- JLP shares an example of integration of ophyd-async device in pyAML (first draft)
- ophyd-cs-oa possily needs to be rewritten 
- JLP and GP will review the backends and do some refurbishment in order to have more freedom in how
to implement pyAML devices
- TO should create an issue describing their use case at HZB of measuring feedforward tables for IDs
- TO will start to attract some EPICS labs and ask them about the requirements for ophyd-async interactions


##### Roadmap
- Release in the end of April. Which issues to close before that?
- VG shares internal SOLEIL document. TO: the format is nice for the roadmap, we should adopt it.
- TO (or someone from MAX IV) should describe 'pole face strips' in a GitHub issue.

Snapshot of foreseen SOLEIL contributions in the roadmap
<img width="1239" height="703" alt="image" src="https://github.com/user-attachments/assets/ef09da0d-2140-484a-b08f-af57b6e65a76" />

##### Future hackathon
- No one knows who will organise it but steering committee wants it before summer vacations
- Purpose should be to make configuration for different people (by themselves)

#### Magnet issue with noninvertable conversions
- KP: proposal of JLP (yaml configuration file, load/save optics corrections) seems good, should be applied to all magnets. 

#### Workload distribution

- TR will work on ElementHolderAPI in May (JLP will have a meeting with TR)
- TO [validation decorator](https://github.com/python-accelerator-middle-layer/pyaml/pull/214)
- GP [catalogues](https://github.com/python-accelerator-middle-layer/pyaml/pull/192)
- SOLEIL (GP, PM, AG, VG) / HZB Digital twin based on HZB solution (simplified for CI/CD, more general one also)
- VG [examples update](https://github.com/python-accelerator-middle-layer/pyaml/pull/191) end of April with hopefully stabilised config
- KP will soon start working on DOOCS bindings

#### Topics of the next meetings

- 
- 
