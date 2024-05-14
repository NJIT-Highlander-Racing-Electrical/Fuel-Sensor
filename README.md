# Fuel-Sensor

* A subsystem that measures the amount of fuel left in the fuel tank and communicates the percentage to the dashboard via CAN-bus.
* It will be a part of the DAS because of their physical close proximity, the ability to add a button to the DAS enclosure to reset the fuel reading, and to use the SD card onboard the DAQ. 
* It subtracts the fuel used from the total volume, and calculate a value from 1-9 of how much fuel is left. The dashboard will display this value via the fuel level LEDs

## Potential Hardware Solutions:
* Flow-Rate Sensor (that can handle gasoline)
 - A flow rate sensor could present many issues:
   * Drift in the readings over time
 - We can put a manual reset button on the DAS that is pressed with each refuel
 - We can store a data file on the DAS SD Card with the fuel level so when the vehicle is powered back on, the last known fuel level is used.
  
* Volume sensor
  * Difficult because must not modify the fuel tank or increase the fuel capacity
  * Could we place a magnetic float in the tank and use several hall effects to check the level? This may require some rule checking

 
* Or, could we just relate the engine RPM to fuel flow rate? From initial research, these are not quite linear, but they may give a good estimate
