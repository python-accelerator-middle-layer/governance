
**Date:** April 24, 2026  
**Time:** 15:00 (CEST)  

### Present:
Simone Maria Liuzzo (ESRF)
Teresia Olsson (HZB)
Guillaume Pichon (SOLEIL)
Vadim Gubaidulin (SOLEIL)


### Discussion: 

#### Community hackathon in September

- Community meeting is usually Thursday afternoon (2 hours)
- 2 hours is probably not enough
- Thursday afternoon in September is probably date of the hackathon

#### Schema registry

- Some plan was agreed upon in the GitHub discussions
- TO, GP and JLP had a discussion about the configuration. The outcome is the following:

    - Separation of validation from other parts of the code
    - Removing config models from the code
    - JLP suggested to dynamically generate the ConfigModel
    - TO will try to implement this idea
    - JSON schema will also be possible for configuration

#### Walkthrough of catalogs features

    - GP already showed TO 
    - It's repeated for SML

#### ControlSystem refurbishment / simplification 

- Mainly simplification concerning some of the methods
- The aim is to have a simpler control system backend that can be written in one day

#### Abstraction of pyAML devices for ophyd-async

- Only TuneMonitor is done for the moment
- Devices will be abstracted to allow some external device implementation (for example with ophyd-async)

#### BPM

- Decision to remove the model to simplify the implementation (no model of ABCD electrodes necessary)

#### Virtual accelerator for CI/CD

- End of June will be first release (at least same functionality of DT of SOLEIL during the workshop)
- After it can be inserted into CI/CD pipeline

#### Workload distribution

- TO will on the config refurbishment (there's a draft PR for the RFplant only)
- VG will convert the list of JLP to GitHub issues
- VG will correct the lack of BPM offset addition in simulation
- SML will work with Teresia on the documentation

#### Future work

- Deprecated decorator
- One task to do is probably a conversion from MML to PyAML congfigure

#### Topics of the next meetings

