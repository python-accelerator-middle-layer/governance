## Agenda pyAML maintainers' meeting

**Date:** October 31, 2025  
**Time:** 15:00 (CEST)  

---
1. Tests of pyaml repository functionality and  tune correction use case with a digital twin at SOLEIL [G. Pichon / V. Gubaidulin, SOLEIL] 15' + 5'

    V. Gubaidulin have shown the recent tests on a digital twin of SOLEIL II. 
    - Automatic generation of PyAML config from a lattice file and nomenclature database
    - Tune correction use case on a digital twin (but using the tune response matrix measurement done in the 'simulator' mode of pyAML)
    - Generally the feedback is positive. A GitHub discussion was open with suggestions. GitHub Issues were identified and created based on the discussion and the feedback.
    Questions:
    - T. Olsson have asked how the configuration is automatically generated and pointed out that at MAX IV there were several issues (serialized magnets and lack of a clear and efficient way to generate the .yaml configuration file)
3. Progress of accml repository tune correction use case [W. Sulaimankhail, HZB] 15' + 5'

    W. Sulaimankhail have shown the tune correction use case for accml repository using HZB digital twin (both EPICS and TANGO). There were some issues on the side of TANGO digital twin, there were no issue in the use case for the EPICS.
    Questions:
    - V. Gubaidulin asked about configuration -> .yaml files, generally similar to pyaml-repository configuration
    - V. Gubaidulin asked about the simulator mode -> Waheed has some scripts in the simulator mode but they are not ready for a demonstration yet
4. Proposal for merging of configuration layer of pyaml and accml repositories [T. Olsson, HZB] Teresia have started a GitHub discussion with her suggestion already (https://github.com/orgs/python-accelerator-middle-layer/discussions/27) 10'+5' 
5. Requirements for functionality present in MATLAB Middle Layer Accelerator Object (AO) [T. Olsson, HZB] (Teresia have started a GitHub discussion with her suggestion already (https://github.com/orgs/python-accelerator-middle-layer/discussions/27))

    Items 3 and 4 were merged and discussed together.
    T. Ollson have shown her proposal to improve configuration layer in pyaml-repository by cherry-picking from accml-repository. 
    There was a long discussion with clarifiyng questions.
    Jean-Luc Pons explained why certain choices were made (for example, tango-host initialisation before middle layer object initialization). 
    Generally the feedback for the suggestion was positive. 
    **T. Ollson will try to make mergeable proposals.**
    **Ophyd-async utilisation was discussed. It was stressed that there's no problem for example to implement the EPICS-bindings of pyAML with ophyd-async to demonstrate its features.**
6. Progress and distribution of tasks 10'

    GitHub projects and kanban issue board were shown at the meeting by V. Gubaidulin with some encouragement to people to actively participate in the development. 
    V. Gubaidulin asked Y. Hidaka if he can contribute EPICS-bindings for pyaml-repository (as ideally this should be done by EPICS-experienced person from an EPICS lab).
    Y. Hidaka replied that he will try to do it. 
    **V. Gubaidulin underlined that he and G. Pichon will be available if there are any questions.**
    **T. Olsson and W. Sulaimankhail in three weeks will test accml-repository with MAX IV using HZB digital twin (TANGO version)**
    **T. Olsson will present pyAML project at ROCK-IT meeting in Hamburg next week (November 3 --)**
    **T. Olsson will look for an ophyd-async expert to present it either at a maintainers meeting or at a community meeting.**
    **T. Olsson open a GitHub discussion on ophyd-async. Examples were added there by W. Sulaimankhail and T. Olsson.**

9.  Project documentation [J.-L. Pons, ESRF / V. Gubaidulin, SOLEIL]
    Not discussed in the meeting. A merge request was open by S. Liuzzo to fix the readthedocs documentation generation https://github.com/python-accelerator-middle-layer/pyaml/pull/48
