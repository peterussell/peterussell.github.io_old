---
layout: post
title:  "IR GS5 - Types of Airspeed"
date:   2016-02-09 21:50:00
categories: instrument-training
---

# Indicated Airspeed (IAS)
 - the value shown on the airspeed indicator
 - the difference between ram air pressure and static air pressure
   - anything affecting either of those will affect the indicated airspeed
 - if a controller asks for your airspeed, this is the value they want

# Calibrated Airspeed (CAS)
 - at variable angles of attack, the pitot tube may not scoop up a sample of air that accurately reflects the current airspeed
   - sometimes it doesn't scoop up as much air as is actually striking it, giving a slower reading than actual
   - sometimes air may be artificially accelerated by a curved surface or similar, giving a faster reading than actual
 - a chart can be used to adjust the indicated air speed to account for the known errors
 - this results in a more accurate airspeed, known as Calibrated Airspeed (CAS)
 - generally, critical airspeeds (Vso, Vs1, Va, Vne..) are IAS, so there's no need to convert to CAS
 - CAS still doesn't give you the airplane's *true* speed through the air...

# True Airspeed (TAS)
 - air at sea level is dense, but becomes less dense with altitude because there are fewer air molecules
 - this allows airplanes to travel faster at the same power setting at higher altitudes
 - however, there are less molecules being scooped into the pitot tube/bellow the higher you go
   - therefore, at higher altitudes the True Airspeed (TAS) increases faster than the IAS
 - keep in mind that the reduced air density also hinders the ability of the engine to produce power

 - Two factors affect air *density*: pressure, and temperature
   - **TAS can be calculated using an E6-B:** inputs are the outside air temperature (OAT) eg. -12 deg C, and the pressure altitude, eg. 5000', then the TAS is read on the outside scale opposite the *calibrated* (note: not the *indicated*) airspeed on the inside scale
   - some PFDs will do this automatically for you and show the TAS, eg. the Garmin G1000
