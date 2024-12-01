# nutrient-reservoir
This is a ESPHOME / HomeAssistant nutrient reservoir. Not everything works perfectly but it has been mixing nutrients for my garden with no issues for the past several years. It consists of a few temperature probes (which do nothing except for report to homeassistant), a few peristaltic pumps to deliver the concentrated nutrient solution (you can use just about any; the volumetric rate can be easily calibrated in homeassistant), a water level sensor (its a pressure sensor at the bottom of the reservoir; this can also be calibrated in homeassistant), and a solenoid valve that is connected to a tap water supply to fill up the reservoir.

# How to set up
Mine has been cobbled together with a wemos c1 mini module. You will need to update the code a bit as needed for your own setup. I don't have a circuit diagram but it should be easy enough to figure out based on the code... I had planned on designing a circuit board but my 'prototype' has worked pretty well and I have not designed the board yet.

You will need to calibrate the sensors - volumetric rate of your peristaltic pumps and the pressure sensor for water level. This is done in the HomeAssistant dashboard.

# Issues
* AFAIK everything is working pretty well except for the nutrient concentrate remaining percent. I'm pretty sure it gets resets when the unit turns off, should be an easy fix just need to store the current percent correctly but I haven't taken the time to look. I just check the concentrate bottle every week or so to make sure they are not empty currently.

* It also has issues with uptime, likely due to the really bad spamming of the log - it just continuously spams it right now.

# What this is for?
I use it to automatically mix nutrients for my outdoor drain-to-waste aeroponic garden. I have a seperate system that controls the water pressure and mist solenoids; this just fills up the nutrient reservoir. If your garden requires a nutrient reservoir, then this can fill and mix it for you from concentrated nutrients. There is no pH/concentration monitoring, so it is only suitable for drain-to-waste currently.

# Disclaimer
Mine has run for several years now without an issue, but I am not responsible for your solenoid valve getting stuck open and costing you lots of money on your water bill or water damage that may result from this. I am not responsible for you neglecting to calibrate your pressure sensor and this flooding your house. I am also not responsible any other issues that may result from your use of this, due to mistakes in the code or your own negligence. This is provided as-is and is strictly use at your own risk. There almost certainly are issues with this in its current state that may make it unsuitable for you - this is mostly here so I don't lose the code or to provide a starting point for your own system.
