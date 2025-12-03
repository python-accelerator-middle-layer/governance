 ## pyAML maintainers' meeting notes

**Date:** November 28, 2025  
**Time:** 15:00 (CEST)  
**Participants**: Jean-Luc Pons (ESRF), Simone Maria Liuzzo (ESRF), Teresia Olsson (HZB), Waheed Sulaiman Khail (HZB),
                  Vadim Gubaidulin (SOLEIL), Alexis Gamelin (SOLEIL), Alexandre Moutardier (SOLEIL), Yoshiteru Hidaka (BNL),
                  Konstantinos Paraschou (DESY), Devin Burke (DESY, invited), Ali ? (MAX IV?) 
---

**SML presenting documentation and examples**
- SML have made the initial set up for the documention in readthedocs
- SML shared information on the available example notebooks and on how to create new ones

**Devin started discussion on ophyd-async**
JLP asked and listed many of the points that concern him: Device factory, polling, quality-parameter, async-backend of TANGO chosen for ophyd-async implementation,..
	- DB: There are some factory methods but DB couldn't find them on the fly but they are not intended for writing control system agnostic devices -> for this check fastCS
	- JLP asked some clarification questions on polling
		- DB: it is polling of ophyd that was shown not tango polling
		- DB: Ophyd does not override some tango functionality and TANGO is still the authority on polling
		- DB: If you need to change polling it should be done on TANGO device server
		- DB: there's internal TANGO polling that is already in use at some facilities like ESRF
		- JLP: The problem is that we need to handle some polling of setpoints in TANGO-backend, if it is not done in ophyd this is a problem; Access of internal buffer or the value that you've set -> this does not seem possible in ophyd-async
			- You can access DeviceProxy from ophyd if you want to; this might provide some solution. There might be an easier way to access it. This may provide a solution that can be implemented in ophyd-async "bindings" for pyaml
			- AttributeProxy is an ophyd-async class, it has nothing to do with TANGO AttributeProxy
			- Only one instance of DeviceProxy (TANGO) is created for several ophyd attributes
		- JLP: there might be a bug with timeout 
			- DB: create an issue on GitHub and we will work on it
		- JLP: is there an ophyd documentation on how to implement a backend for DOOCS or some other control system?
			- DB: Yes, this is available in the documentation but also helps to look at the structure for the EPICS and TANGO backends
		- JLP: is it possible to write a backend that will be external?
			- DB: Yes
		- JLP: Is it possible to write a code without using any backend  with control system dependent code inside?
			- DB: Yes (?), something to do with soft signals
			- DB: FastCS is supposed to be agnostic to control systems but it is in development (ask Tom Cobb at Diamond) https://github.com/DiamondLightSource/FastCS
		- TO & DB: Core development team of ophyd-async is at Diamond. It was decided to support both epics and tango.
		- TO: Status object in ophyd-async. Teresia explains that we want sleeps and waits handled on device levels. So when hardware changes, we do not need to change the scripts. 
			- DB this should be possible
		- TO: Asks to say a few words about DerivedSignals and transforms; 
			- DB gives some example of a simple derived signal
			- Derived signal is basically something useful for something like unit conversion
			- TO finds the derived signal to be very easy to use
			- TO asks about format on the signals to be able to specify when a signal is read (only for read_configuration, using cache or not)
		- VG: What is the effort to develop a binding for a new control system
			- DB: 1000 line file, will take a week or two. There are some abstract classes / skeleton to help you out
		- VG & JLP: TANGO asynchronous calls are done with asynchronous APIs in TANGO. There are three of them implemented in TANGO.
			- JLP wants to use C++ version of TANGO asynchronous calls instead of asyncio. For ESRF, this is necessary to use this C++ backend to address thousands of set points.
			- DB: it is possible to collaborate on that topic. And brainstorms some possible ways to make it work. Make an issue about it and it can be discussed. 
	- VG: what is the benefit of ophyd-async when you already have TANGO devices?
		- ophyd has more standardized in interfaces
		- other benefit is bluesky runEngine
	-TO proposed to invite someone from fast-cs development team to have a similar discussion on control system abstraction and learn what they are doing. This will be scheduled for one of the next maintainer meeting.
