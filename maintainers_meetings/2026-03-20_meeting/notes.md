
**Date:** February 20, 2026  
**Time:** 15:00 (CEST)  

#### Present:
 - Yoshi Hidaka
 - Jean-Luc Pons
 - Guillaume Pichon
 - Alexis Gamelin
 - Gayane Amatuni
 - Marco Apollonio
 - Vadim Gubaidulin 
 - Teresia Olsson

#### Discussion: 
- JLP had a discussion with ophyd developers that fixed some issues for pyAML compatibility. 
##### Catalog suggestion discussion. 
- JLP explains what he would expect from a catalog, 
- GP has a concern that JLP options could not cover an edge case of having two control systems in one accelerator
- GP and JLP seem to agree on how the catalog should work
- TO asks GP to explain how a catalog works:
    GP: you need to create it independently with a configuration file
    GP: catalogs also can help to link the configuration to the control system and avoid duplication
    JLP: catalog can hide part of the configuration from the used. For each DeviceAccess only a reference to a catalog could be necessary.
- GP answering TO: right now catalog is static, it could change in the future implementation of a dynamic catalog
- TO: right now the catalog is only for the control system, maybe it is good to have it for everything
    JLP: it is possible already to have many .yaml files, one for tuning tools, one for control system, etc.
- TO, JLP, GP: maybe it will be good to have a global level object that can propagate some changes to different modes: live, design, etc
JLP: maybe we can have sr.set_lowalpha() that will load the low alpha operation mode. 
TO: explains HZB and MML user needs/expectation on configuration
- VG: it would be good to get a use case of this operation mode ramping. 
##### Steering committee pyAML roadmap
- TO shows the document prepared by the steering committee
- JLP: maybe ophyd-async device is OK to use in the binding.
At the moment, in signal level it is not possible to do introspection. JLP explains this and some other issues/concerns. 
JLP discussed this with ophyd-async guys and there's some progress
- Manpower issues (especially EPICS) was discussed
##### Measurement class
  - Jean-Luc was ready to share his proposal for the Measurement Class. 
  - AG asks about how callbacks work
  - AG gives some feedback on metadata requirements
  - TO emphasizes that the measurement tool should have flexibility to do in hardware or in physics units for magnets

  #### Topics of the next meetings
  - Set and wait functionality, async hidden from the user, etc.
