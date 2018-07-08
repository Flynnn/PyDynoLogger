# PyDynoLogger
Open Source Iterative Dynamic Logging based on DynamoDB and Python


What is Iterative Dynamic Logging?

In short, it is a framework to support long-term iterative data collection projects.

I, often, have had need for a stable data logging platform that:
1) Is stable and capable of handling data collection programs crashing
2) Capable of handling multiple data collection programs as sources at once

And, most importantly,
3) Capable of handling two competing data collection programs of different versions at once.

This last capability means that, should one ever need to change the manner in which data is collected, they may simply spin up a new test version while the old version is still running, allowing there to be no gaps in data collection. Once the new version is safely spun up, the old versin may be spun down.

This framework also has the potential to act as a logging data flow manager -- supporting multiple data sources, and progressive data access and filtering, this framework is ideal for applications where distributed data acquisitioners need to be combined and processed at a single location.

This framework, internally, uses event-based chronological data, but supports binning this into regular-timestep data.
