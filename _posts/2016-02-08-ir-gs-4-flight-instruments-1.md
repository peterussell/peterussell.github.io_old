---
layout: post
title:  "IR GS4 - Instruments: Airspeed Indicator"
date:   2016-02-08 21:48:00
categories: instrument-training
---

# Airspeed Indicator - Part 1
**How it works**

 - measures the difference between ram (moving) and static (not moving) air
 - an expandable metallic capsule is housed inside a chamber filled with air at atmospheric pressure:
   - the outer chamber connects to the static port, pressure increases and decreases with outside air pressure
   - the inner capsule connects to the pitot port, pressure increases with an increase in airspeed
   - expansion of the capsule moves the airspeed indicator needle

**Icing**

 - pitot tubes are particularly subsceptible to icing
 - ice blockage can occur even without airframe icing
 - results in an unpredictable airspeed, from gradual decrease to a 0kts reading depending on where ice forms and how much tube is obstructed
 - recommend flying with pitot heat on any time you expect to encounter visible moisture (ie. clouds), regardless of freezing level

Pitot heat must be checked before every IFR flight - turn on the pitot heat switch and touch the pitot tube to verify it's warming up.

 **Double Blockage: pitot tube and pitot drain hole (static unblocked)**

  - ram air pressure blocked in lines and metallic bellow
  - static air pressure still increases/decreases with atmospheric pressure
  - therefore airspeed indicator works like an altimeter:
    - **In a climb:** static air pressure *decreases*, bellow expands (replicating an increase in ram air pressure), and airspeed increases. May pull back to compensate and/or reduce power, possibly entering a stall scenario.
    - **In a descent:** static air pressure *increases*, bellow contracts (replicating a decrease in ram air pressure), and airspeed decreases. May push forward on the yoke to compensate and/or increase power - possible to exceed Vne (see below) and/or fly into terrain.
    - **In level flgiht:** static air pressure remains the same, airspeed indicator reads constant regardless of power changes.

**Airspeed Indicator Coloring**

 - **White Arc:** "flap operating range"
   - low end - **Vso**: power-off stall speed in landing configuration (flaps fully extended, gear down). This speed is at the maximum allowable **landing** (because we're configured for landing) weight, lighter weights reduce the stall speed
   - high end - **Vfe**: maximum speed you can fly with flaps fully extended

 - **Green Arc:** "normal operating range"
   - low end - **Vs1**: power-off stall speed in a specified configuration (for smaller airplanes, this is max **takeoff** weight, with flaps and gear retracted)
   - high end - **Vno**: operations above this speed are allowed only in smooth air
     - *specifically, below planes certified on or after Sep 14 1969 are certified to withstand 'substantial sharp-edge vertical gusts of 50fps without experiencing structural damage - or 30fps before Sep 14 1969*

 - **Red Line:** "never exceed speed"
   - **Vne**: the maximum speed at which the airplane can be operated in smooth air. Exceeding it can cause aerodynamic flutter, often an uncontrollable and destructive vibration of certain airfoil surfaces.

**Airspeeds Not Shown On Indicator**

 - **Va:** "maneuvering speed"
   - the speed at which an abrupt movement of the flight controls will cause the airplane to stall before structural damage occurs
   - found in POH and sometimes placards
   - Va is defined at the airplane's maximum design weight, so the FAA has defined another term:

 - **Vo:** "operating maneuvering speed"
   - because Va decreases with a decrease in weight, Vo defines maneuvering speeds associated with lighter weights - some manufacturers provide one or more Vo's for weights less than max gross.

 - **Vlo:** "landing gear operating speed"
   - maximum speed at which the gear may be raised or lowered
 - **Vle:** "landing gear extended speed"
   - maximum speed the airplane can be flown with the gear down

*If you ever exceed these last two speeds, it's often a good idea to leave the gear down until you can inspect the gear doors for damage.*
