# AeotecHEMgen5
SmartThings Device Handler for Aeotec Home Energy Meter Gen 5

Based on a handler by Classic GOD https://community.smartthings.com/t/aeotec-home-energy-meter-gen-5-composite-dth/

## Important - please read

**You will need to press the action button TWICE when including your Aeotec HEM.** This includes the device in Z-Wave secure mode which is needed to access the aditional features of this device handler. If you didn't do this, you will need to exclude the HEM (use the ST app to remove the device and press the action button when your hub is in exclusion mode). Then re-include the HEM and press the button twice.


### Changes

I updated this based on my own needs but it could easily be extended further.

Added:

* Energy costs displayed based on "Cost per unit" in prefernces
* Resetting the meter doesnt change the energy reading on the device, it jsut adds an offset in software to zero 
the reading. This means you can reset as often as you like but you'll never loose the total energy usage.
* There is another offset value in preferences so that you can match the meter readings up to your existing meter value to keep things consistent.

Changed:

* Fixed the refesh routeen, made parent refresh refresh all children and set it to perform a refresh every 5 mins
* Changed some of the units and rounding so the display is simpler
* Changed default display in devices list to cost instead of kW

Todo:

* Add a reset date so that standing charges can be added to cost based on the last reset date
* Add configurable currency and other options for calculating costs
* Allow choice of unit to display on device list via preferences e.g. cost / kWh / kW etc.

