---
layout: post
title:  "IR GS6 - Instruments: Altimeter"
date:   2016-02-10 21:36:00
categories: instrument-training
---

# Altimeter
 - **True Altitude / MSL:** the value provided on the altimeter, which is the height above 'sea level'
   - sea level is a worldwide standard, providing consistent reference for altimeter measurement
 - **Absolute Altitude / AGL:** height the airplane is above terrain, = (MSL - terrain height)

# How an altimeter works
 - measures the difference in pressure at sea level and the pressure at the airplane's altitude
 - an expandable capsule (*aneroid wafers*) is inside the altimeter's casing
   - the capsule is *mechanically calibrated* to represent the pressure at sea level (via the altimeter setting in inches of Mercury, set by the knob on the face of the altimeter)
   - the casing is connected to the static port
 - as the airplane ascends, air pressure in the casing surrounding the capsule decreases, allowing the capsule to expand
 - expansion of the capsule moves the altimeter's needles
 - the rate of change used to calibrate altimeters is constant: **1"Hg per 1000'**
   - for example, if the pressure at sea level is 32"Hg, we know that the pressure at 1000' is about 31"Hg, and 29"Hg at 3000'
 - the standard pressure setting, under 'standard conditions' at sea level is 29.92"Hg

# Altimeter Settings
 - pressure at sea level is the value set in the altimeter using the altimeter's adjustment knob, which changes the value shown in the altimeters **Kollsman Window**
 - because pressure varies all over the earth, the altimeter setting needs to be updated regularly during flight
 - altimeter settings are given by controllers, towers, ATIS, Flight Service etc.

**Failure to adjust the altimeter setting:**

 - if moving from one place to another with two different altimeter settings/sea level air pressures, then you'll track the pressure level either up or down, while still think you're flying at the same altitude

 - if airport A has a *higher* pressure than airport B, and flying from A to B:
   - you will continue to fly at the higher pressure level
   - by the time you get to B, you *should* have reduced your altimeter setting, but haven't
   - therefore, thinking about what would happen if you decreased the altimeter setting to the *correct* setting at B, the actual altitude of the airplane would decrease. Therefore, you're flying lower than you thought you were.

 - similarly, if airport C has a *lower* pressure than airport D, and flying from C to D:
   - you continue to fly at the lower pressure level
   - by the time you reach D, you *should* have increased your altimeter setting, but haven't
   - therefore, if you were to adjust the altimeter to the correct setting, your altitude would go up. Therefore you're actually flying higher than you thought you were.

**"High** (pressure) **to low** (pressure)**, look out below."**

# Temperature Impact on Altimeters
 - generally not something that really needs to be worried about, but...
 - at standard temperature (15 deg C, 59 deg F) there's no altimeter error
 - *warmer temperatures **expand** air* - the column of air below an airplane on a hot day is bigger, but weighs the same as the column of air that is shorter than it would on a standard day
   - therefore, the airplane is *higher* than what the altimeter reads
   - **warmer air = higher than the altimeter reading**
 - *colder temperatures **contract** air* - column of air below the airplane on a cold day is shorter, but weighs the same as a standard day
   - therefore, the airplane is **lower** than what the altimeter reads
   - **colder air = lower than the altimeter reading**

 - **Rule of thumb:** without correcting the altimeter for temperature, going from higher temperatures to lower temperatures means the airplane is descending, so the same applies as above:

**"High** (temperature) **to low** (temperature)**, look out below."**

# What to do if an Altimeter Setting Isn't Given
 - if you know the field elevation for the airport you're at, turn the altimeter knob until the field elevation is displayed in the altimeter. The altimeter setting (ie. "Hg) for the field is displayed in the Kollsman window.

# Verifying Altimeter Settings
 - the AIM recommendation is to verify the value of the altimeter is +/- 75' within field elevation

# Pressure Altitude
 - the value shown on an altimeter when the altimeter setting is set to 29.92"Hg
 - this is used for performance calculations

# Density Altitude
 - pressure altitude correct for temperature
 - this is the altitude the airplane 'thinks' it's flying at
