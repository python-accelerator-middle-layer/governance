 ## pyAML maintainers' meeting notes
 
**Date:** December 12, 2025  
**Time:** 15:00 (CEST)  
**Participants**: Tom Cobb (DIAMOND, invited), Jean-Luc Pons (ESRF), Simone Maria Liuzzo (ESRF), Teresia Olsson (HZB),  Vadim Gubaidulin (SOLEIL),
Alexis Gamelin (SOLEIL), Alexandre Moutardier (SOLEIL), Patrick Madela (SOLEIL), Alexis Gamelin (SOLEIL), Yoshiteru Hidaka (BNL), Konstantinos Paraschou (DESY), Julian Gethmann (KIT, beginning of meeting), Waheedullah Sulaiman Khail (HZB, end of meeting)

# Next Meeting will be on January 12th at 14:00 !!!

---
### FastCS presentation and discussion

- TC is starting his part from asking a few questions about our requirements because he is only aware of what is necessary for the beamlines
- TO gives a brief explanation
- TC proceed with a FastCS presentation
- Core concepts
  - Core logic using asyncio
  - Modern Python with typehints
  - Robust static type checking with pyright
  - Collaborative device driver development
 
- Different layers can be tested in isolation without a control system
- GUIs are generated made automatically for raw attributes (? ATK panels in TANGO ? / ? TAURUS in TANGO ?)
- FastCS API is stabilized and breaking changes are now more and more rare

#### Questions and discussion
  - JLP: is EPICS transport in an external module
    - TC: FastCS has built-in transports
  - JLP: Can I add something from scratch without integrating in FastCS
    - TC: Yes, but you maybe cannot use the FastCS yaml configuration
    - JLP: I would even avoid having built-in transports and have them as an external module
      - TC: It is mostly philosophical question. They found it easier to for now to include everything. Later on they might split into different modules. TC will discuss it with FastCS development team. 
  - JLP: Some issues with IP connection when it is not necessary. He would expect connection not IP
    - TC:  The example is hardcoded with IP connection but it should be possible to do another kind of connection instead
  - JLP: Would be good to have an example of only an abstract interface
  - TO: Relation between ophyd-async and fastCS. Can you have nested devices?
    - TC: You can have nested devices that kind of mirror the ophyd-async derived signals
  - TO: Will fastCS create ophyd-async devices?
    - ??? TC: No. You would create control system interface in FastCS. TC is showing some example in ophyd-async. The idea is that ophyd-async will slim down the FastCS device with only necessary functionality.
    - 
  - VG: What is the place of FastCS in the ecosystem of FastCS, ophyd-async and bluesky.
  -    TC: Control system abstraction and the idea of writing everything in Python with a unified approach instead of using C++/Java/etc interchangeably.
  - TO: What is the need for an introspection?
    - TC: ???
    - TO: Is there any kind of mapping for when things mean the same things but are not named in the same way in different facilities?
      - TC: It is possible to do with ophyd-async or with fastCS with some mapping of names
      - JLP: There are also some TANGO-native solutions to this question
---

### pyAML tests at ESRF-EBS storage ring

- On 1st December JLP, SML and KP checked the tune correction use case
- The tune test went perfectly well as was expected
  - There are a few comments from a user point of few -> They should be converted to GitHub issues
- pySC orbit correction was tested with and without an integration with pyAML
  - There is also some feedback on the orbit correction part -> This should also be converted to GitHub issues
 
    #### Questions
    - TO: How are the sleeps handled at the moment?
      - JLP: Orbit correction is a single step, so no need for a sleep
      - JLP: Some sleeps were added in the code for the test
    - TO: In the specification, we ask for no sleeps in the measurement scripts / measurement flows / etc.
      - JLP: It is planned to be implemented; we need to implement set_and_wait and also to implement something like wait_and_read. JLP further explains the ideas to implement.
      - TO: ophyd-async has some status objects to handle this
        - JLP: It could be done like that but it introduces polling that are maybe not helping us. So, for pyAML it is planned to do in a synchronous manner for now.
      - TO: Are waits configurable?
        - JLP: There are some steps to implement set point checks and define min/max in the configuration of, for example, power supplies. Wait window can also be added and a method to wait also.
      - TO: MML does it with a tolerance / window and there's a ramp rate to predict when the setting of device will be finished
        - JLP: We need some window likely. But it is not yet implemented and to be addressed. 

### pyAML tests at SOLEIL storage ring

--- 

- On Dec 9th AM tested pyAML at SOLEIL storage ring for a simple chromaticity measurement
- AM gives some feedback on his experience with the pyAML code
  - AM: There are some warnings missing
    - JLP: there's a check peer method that should prevent objects from being attached.
- AM development of chromaticity in pyAML was done fast and checked at SOLEIL. There are some refinements to do with the code. 
- Some old Python scripts were adapted to run with pyAML
- A pull request is on the way

  #### Questions
  - TO: Is the separation of measurement and analysis already done?
    - AM: There are two functions but the values of the result are not saved yet. And there's no metadata
  - JLP: This should be moved to the tuning tools. We can also have chromaticity as a response matrix and as a measurement.
  - KP: chromaticity_monitor -> chromaticity
  - TO: Do you have a step() instead of a set()
    - AM: Not yet
  - YH: Can we avoid the name mangling? Why do we have this name magnling?
    - Everyone: We should make a GitHub discussion or a GitHub issue to get the answer from someone who knows why it's there.

