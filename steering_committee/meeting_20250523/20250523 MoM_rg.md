> ## Agenda:
>
> 1. Approve minutes from last meeting  
> 2. Report from maintainers meeting  
> 3. Working groups and working group leaders  
> 4. Appointment of maintainers  
> 5. Roles on Github  
> 6. pyAML license  
> 7. Specification documents  
> 8. Level of bluesky integration  
> 9. Next meeting time  
> 10. Approve minutes from this meeting  

&nbsp;

### Participants 

Ilya Agapov – DESY    
Konstantinos Paraschou - DESY (Deputy)   
Simon White - ESRF   
Patrick Madela - Synchrotron SOLEIL (Deputy)     
Laurent Nadolski - Synchrotron SOLEIL  
Marco Apollonio – MAX IV (Deputy)  
Stephen Molloy - MAX IV (Deputy)   
Markus Ries – HZB  
Teresia Olsson – HZB (Chair)  
Ronja Grünke – HZB (Notes)

&nbsp;

### 1. Approve Minutes from Last Meeting   
Changes to the Minutes will be notes in ***bold italics***  

Summary and Action Items from the last Minutes:     

**1.1 Organisation:**
- Teresia was appointed chair for one year (to 29. April 2026)  
- Monthly Steering Board meeting schedule of 1 hour meeting every 4 weeks on Fridays 11:00 - 12:00 was decided on  
- Idea: Test minutes life during the meeting with support of Ronja   
- Minutes will be published on Github for the Steering Board ***-> when / approval process?***   
- Placement of the agenda on Github or indico was discussed. ***-> Placement on Github was decided on.***  

**1.2 Email Lists**  
- Two additional emails lists:  
  -  One for the steering committee with all our email addresses  
  -  Second one as a contact email for people who want to get in touch with the steering committee and need a single point of entry. It was decided that Teresia should be on this contact email as a start 
- Someone needs to keep administering the existing community email list ***Simon & Simone***  
- Simon will talk to Simone about this and check if all of the three email lists can be set up and administered by ESRF. **->Yes***  

**1.3 Communication with the Community**  
- ReadMe on Github is not working so well. A calendar is missing.  
- Teresia will investigte if a Github page can be set up. ***-> Would work, to do***  

**1.4 Maintainers Meeting and Working Groups**  
- First meeting on May 22, 2025  
- The meeting should collect interested candidates for being working group leaders. This should also be reported to the steering committee on the 23 May and they will appoint the leaders.  
- A person needs to be appointed to be the link between maintainers group and steering committe. Decision should be made on the next meeting.  
- For results see paragraph 2    

**1.5. Specification Documents**  
- Document 1: tutorial document  
- Document 2: specification document  
- Decision: keep monitoring the process  
  Teresia is involved in the weekly discussion meetings about the tutorial document and also working on extracting the requirements to include in spec. document  

**1.6 Date for next Community Meeting**  
  - Thursday every 3 months  
  - Teresia will come up with a suggestion for the date and can call to it. ***To Do***  

**1.7  Memorandum of Understanding**  
- MoU is not needed, LoS instead  
- Ilya, Simon and Laurent to provide templates ***please provide***  
- Teresia to set up overleaf: https://www.overleaf.com/project/68189102616618255fe525af  

**1.8 License**
- License should be as permissive as possible so we do not run into compatibility issues with other codes  
- pyAT decided to go for Apache 2.0, seems to be a good option  
- Teresia to  send out an email on the community email list to give all labs a chance to object  
- Decision will be found at the next meeting - see Point 7  

&nbsp;

### 2. Report from maintainers meeting     
2.1 Chose a Chair to call the meetings and gather the agenda: -> ***name***  
2.2 Chose a Secretary to write the minutes: -> ***name***     


### 3. Working groups and working group leaders  
as suggested in the maintainers meeting:   

Working Groups by Proposal:    

&nbsp;&nbsp;&nbsp; **1. Inclusion, YRI engagement, inter-disciplinary innovation, impact and dissemination**
&nbsp;&nbsp;&nbsp; Task 1.1: Involvement and co-design by YRIs     
&nbsp;&nbsp;&nbsp; Task 1.2: Training Schools Annual Meetings      
&nbsp;&nbsp;&nbsp; Task 1.3: Dissemination     
&nbsp;&nbsp;&nbsp; Task 1.4: promote collaborative funding applications 

&nbsp;&nbsp;&nbsp; **2. Middle Layer, calibrations and digital twin, CI/CD**  
&nbsp;&nbsp;&nbsp; Task 2.1: development and updates to the main core of the PyAML software libraries, CI/CD    
&nbsp;&nbsp;&nbsp; Task 2.2: calibrations    
&nbsp;&nbsp;&nbsp; Task 2.3: digital twin (virtual accelerator)  

&nbsp;&nbsp;&nbsp; **3. Tuning tools and commissioning simulations**  
&nbsp;&nbsp;&nbsp; Task 3.1: tuning tools  
&nbsp;&nbsp;&nbsp; Task 3.2: sequencing and commissioning-simulation mode  

&nbsp;&nbsp;&nbsp; **4. Operational aspects**  
&nbsp;&nbsp;&nbsp; Task 4.1: code tests in different labs  
&nbsp;&nbsp;&nbsp; Task 4.2: user interfaces  
&nbsp;&nbsp;&nbsp; Task 4.3: data formats/metadata/archiving  
&nbsp;&nbsp;&nbsp; Task 4.4: slow and fast feedbacks  
&nbsp;&nbsp;&nbsp; Task 4.5: compare simulated and measured data for anomaly detection  


Working Groups by Waheeds Notes:    
https://github.com/python-accelerator-middle-layer/governance/blob/main/maintainers_meetings/22052025_meeting/working%20groups  

**1. Analysis**  
- High-level analysis for applications such as BBA (Beam-Based Alignment) and LOCO (Linear Optics from Closed Orbits)  
- Development of analysis applications (e.g., LOCO, BBA, etc.)  

**2. Measurement**  
- Simulated commissioning setups  
- Execution of measurements in real or test environments  

**3. Mathematical Libraries**  
- Development and maintenance of shared mathematical libraries used in analysis and measurement  

**4. Architecture**  
- System architecture and dependency separation (e.g., ensuring clear separation and modularity based on control system requirements)  

**5. Testing** 
- Testing of developed components at your own facilities  
- Collecting user feedback (e.g., usability, setup challenges, execution experience)  

**6. CI/CD & Integration**  
- Setting up and maintaining continuous integration / continuous deployment pipelines  
- Ensuring automated testing and deployment practices are in place  

Things that should to be covered by some group:  
- GUIs    
- Bluesky compatibility (possibility for this for the labs who want it)  
- Running applications as a service (e.g. slow orbit feedback might require this option)  
      
### 4. Appointment of maintainers   
According to the governance document we need to officially appoint the maintainers.   
Working Group Leaders:    

- WG 1: ***name***    
- WG 2: ***name***  
- WG 3: ***name***  
- WG 4: ***name***   

  
###  6. Roles on Github  
Go through the list of the current members and modify roles so not everyone has full permissions to all repositories anymore, but only to the parts that they should be allowed to modify based on their role according to the governance document  

- Users  
- Contributors  
- Maintainers  
- Steering Committee   


### 7. pyAML License  
- Apache 2.0 agreed on?  


### 8. Specification Documents  
- lorem ipsum 

### 9. Level of Bluesky Integration  
Teresia: consequence analysis looking at different options would be helpful  

**PRO arguments:**  
- lorem ipsum 

**CONTRA arguments:**  
- lorem ipsum



### 10. Next Meeting  


### 11. Approve minutes from this meeting  
