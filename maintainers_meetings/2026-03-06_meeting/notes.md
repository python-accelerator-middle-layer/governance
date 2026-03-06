
**Date:** February 20, 2026  
**Time:** 15:00 (CEST)  

#### Present:
 - Yoshi Hidaka
 - Konstantinos Paraschou
 - Marco Apollonio
 - Vadim Gubaidulin 
 - Teresia Olsson

#### Discussion: 

Discussion is focused on unit conversion and pint usefulness. YH explains his experience with pint and its usage at PAMILA. One potential use of pint would be to only expose the user to it. But use SI units internally in all pyAML computations. We've agreed to open a GitHub discussion. There are some nice desirable features of pint

- Matplotlib integration
- Unit check at calculations
- ...
#### Actions to take in the short term
- Create a unit conversion discussion:
    - YH can write about PAMILA structure with pint
    - TO can write what is the MML methodology for this
    - TO can write about bluesky/ophyd community
    - One possibility is to have SI internally everywhere (except eV) but give user an opportunity to do sr.magnet.stength.set(pint-object)

- SOLEIL/HZB digital twin meeting (next Tuesday). We could report in some of the next meeting on the common plan.
- GP/JLP (continued): catalogues and yellow page concepts, enhancement of ElementHolder API.
- KP is working on improvement of orbit correction in pyAML (adding rf response, weights, etc)
- VG will check with relevant SOLEIL colleagues if we can test pyAML orbit correction during machine restart next week.
- VG will update SOLEIL examples and make them work for ESRF and BESSY II (in design mode for now).
 

  #### Topics of the next meetings
  - Set and wait functionality, async hidden from the user, etc.
