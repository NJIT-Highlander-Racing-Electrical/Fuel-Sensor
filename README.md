# Fuel-Sensor

A subsystem that measures the amount of fuel left in the fuel tank and communicates the percentage to the dashboard via CAN-bus.

## Potential Hardware Solutions:
* Flow-Rate Sensor (that can handle gasoline)
 - A flow rate sensor could present many issues:
   * Drift in the readings over time
   * Manual reset with each refuel
  
* Volume sensor
  * Difficult because must not modify the fuel tank or increase the fuel capacity\
 
* Or, could we just relate the engine RPM to fuel flow rate? From initial research, these are not quite linear, but they may give a good estimate

* Could we place a magnetic float in the tank and use several hall effects to check the level? This may require some rule checking

* Microcontroller to subtract the fuel used from the total volume, and calculate a value from 1-9 of how much fuel is left. The dashboard will display this value via the fuel level LEDs
* ESP32 with TJA1051T works?
