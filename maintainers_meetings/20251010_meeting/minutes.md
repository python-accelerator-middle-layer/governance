Minutes pyAML maintainers' meeting 10 October 2025

1. Planning

  Github projects were shown and the discussion about the feature list for the prototype.
  
  One complicated part which we currently have no implementation for is to be able to handle sleeps/waits at device level.
  In addition to a tolerance for setpoint vs readback we also need an option to make use of ramp rates.
  
  It was discussed to take a look at ophyd-async [https://github.com/bluesky/ophyd-async](https://github.com/bluesky/ophyd-async) since it has both TANGO and EPICS bindings and see if we can use it.
  If it wouldn't work well for us, at least there could maybe be things we could copy.
  Jean-Luc and Guilleaume are going to do this. Potentially another choice for asynchronous calls in TANGO would be better.
  Teresia is going to put them in contact with Devin Burke at DESY who has done the implementation.
  
  Yoshi has experience of this from PAMILA. He suggests to only make use of the signal level and make our own implementation of the device level.
  
  Waheed is using ophyd-async devices for EPICS in accml. He is now working on implementing the TANGO version too so we can test.
  
  It was also discussed that we need to start testing at more labs and together with users to get feedback.
  Guilleaume is working together with colleagues at SOLEIL to put together instructions for how to test.
  Teresia is also working with Marco to test at MAX IV.
  Thorsten pointed out that it needs to be a dummy, step-by-step tutorial if we should get people to do it.
  At this point we can assume that the testers are familiar with Python.

  Yoshi asked if the tune correction use case should include the option to use a measurement of the tune instead of a PV.
  This is not planned for the prototype but is an interesting option for the future.
  In PAMILA, you can instead of a PV give a flow object which performs a measurement and extracts the value if you want.

