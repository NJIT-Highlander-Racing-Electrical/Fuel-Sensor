# Fuel-Sensor

A subsystem that measures the amount of fuel left in the fuel tank and communicates the percentage to the dashboard via CAN-bus.

## Potential Hardware Solutions:
* Flow-Rate Sensor (that can handle gasoline)
* Microcontroller to subtract the fuel used from the total volume, and calculate a value from 1-9 of how much fuel is left. The dashboard will display this value via the fuel level LEDs
