
**Date:** April 10, 2026  
**Time:** 15:00 (CEST)  

#### Present:

Simone Liuzzo (ESRF)
Gayane Amatuni (Candle)
Vadim Gubaidulin (SOLEIL)
Jean-Luc Pons (ESRF)
Guillaume Pichon (SOLEIL)
Konstantinos Paraschou (DESY)
Theo Rozier (ESRF)

#### Discussion: 
##### Catalogs, happi, etc.

- Service for configuration (Proposal from GP). Some discussion between JLP and  GP. 
- GP does not have the time yet to go on on this. Draft proposal will be made next week. 
- Simpler ways to access configuration.
- Happi has an interface to change the configuration. This can help to avoid object.cfg to change the configuration
- JLP: validation decorator of TO is a good proposal

##### GUI application for configuration
- There shouldn't be any conflict with the proposal of Guillaume

##### Set and wait
- We can start a discussion on this on GitHub. There are several different use cases: set and wait for magnets to reach setpoint, waiting during measurement,
readback averaging, etc.
- We need to gather some usecases to be able to decide on the implementation

##### New ElementHolder API
- TR can start with this task from next week
- GitHub Issue and discussions have implementation proposal

#### Workload distribution

- TR will work on ElementHolderAPI
- TO [validation decorator](https://github.com/python-accelerator-middle-layer/pyaml/pull/214)
- GP [catalogues](https://github.com/python-accelerator-middle-layer/pyaml/pull/192)
- SOLEIL (AG / VG / Sami Habet) test of pySC via pyAML for orbit correction on SOLEIL storage ring
- SOLEIL (GP, PM, AG, VG) / HZB Digital twin based on HZB solution (simplified for CI/CD, more general one also)
- VG [examples update](https://github.com/python-accelerator-middle-layer/pyaml/pull/191) end of April with hopefully stabilised config
- KP will soon start working on DOOCS bindings

#### Topics of the next meetings
