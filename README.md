# AeotecHEMgen5
SmartThings Device Handler for Aeotec Home Energy Meter Gen 5

Based on a handler by Classic GOD https://community.smartthings.com/t/aeotec-home-energy-meter-gen-5-composite-dth/

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


