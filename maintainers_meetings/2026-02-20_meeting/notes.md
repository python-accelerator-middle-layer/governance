
**Date:** February 20, 2026  
**Time:** 15:00 (CEST)  

#### Present:
- Alexis Gamelin
- Teresia Olsson
- Jean-Luc Pons
- Guillaume Pichon
- Marco Apollonio
- Konstantinos Paraschou
- Gayane Amatuni

#### Discussion:

##### Alexis' report summary from the workshop working group
  - Callback functions are a very good idea
  - Some typical measurement steps were identified
  - There's a need for some watcher class (are orbit feedbacks running? Is tune feedback running?)
  - Measurement steps should be reusable for different measurements
  - JLP: Maybe there's a tricky point to do a scan on the design, where a thread will take all CPUs
  - TO: What are the generators Kostas is using for measurements in pySC? Should we use them? -> JLP: callback seems to be more convenient
###### Yoshi reports on PAMILA and the user interface specification for HLAs
  - Yoshi reintroduces to us the written specification (that was not discussed a lot before)
  - There are no predefined stages; it's completely flexible at the moment (but can change)
  - Data should be saved in files (to separate postprocessing and visualisation as well), as was suggested by the dedicated working group during the workshop
  - A good usecase will be to do chromaticity and dispersion measurement (separately and combined in one measurement)
  - JLP: pint was used in PAMILA example. Some syntax question relating to pint.
  - JLP: can point contain a lot of data? -> TO: Yes, uncertainties can be there, timestamps ; YH: I'm not sure it's this customizable.
- TO: what callback action is taken when? -> JLP -> callback is triggered by ACTION_MEASURE / ACTION_RESTORE / etc.

#### Actions to take for the measurement topic:
  - List of required pyAML measurements from each facility (by March 6th). The aim is to see how many measurements reuse common concepts
  - GitHub discussion with specifications and initial discussion on implementation
  - TO: some examples will be useful -> KIT could possibly share their measurement class

- TO proposes some online testing sessions for users -> maybe too soon and virtual accelerator is key for this

#### Actions to take in the short term
- SOLEIL will work with HZB on EPICS/TANGO digital twin
- TO can work on documentation update (some initial discussion with JLP) was done -> but TO can only start in a few weeks from now
- GP/JLP: catalogues and yellow page concepts; enhancement of ElementHolder API
- VG will update SOLEIL examples and make them work for ESRF and BESSY II (in design mode for now).
- VG will ask Alexandre Moutardier if he can finish the chromaticity tuning tool; if not VG can do it
- JLP: Will pyLOCO be integrated in pySC/pyAML? KP: Yes, we are working on this
- TO: Will tuning tools be moved to a separate repository -> JLP first, we need to figure out what the interface should be and implement a few. Then move them out.

  #### Topics of the next meetings
  - Unit conversion (pint, no pint, etc)
  - Set and wait functionality, async hidden from the user, etc.
