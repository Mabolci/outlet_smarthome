# Smarthome - Outlet Controller
ESP8266 micorcontroller code for Domoticz control of power outlet.

This is part of submission for university subject with the shortest acronime possible -- UMPAnUMiW

## Hardware 
* ESP8266 (ESP32 can also be used)
* Any relay switch capable of controlling a regular home power outlet, that is controllable via a digital ~2.7V input
* 2.2V - 3.6V power supply for ESP8266

## Setup and Usage
### Software
Same as in https://github.com/Mabolci/curtain_smarthome#software

Additional outlets can be connected to controller. To do so, connect more relays to chosen GPIO ports. Then define them in code as follows:

```cpp
#define OUTLET_PIN_1 14
```

then, inside **callback** method add

```cpp
digitalWrite(OUTLET_PIN_1, HIGH);
```

and

```cpp
digitalWrite(OUTLET_PIN_1, LOW);
```

In lines commented with *add additional outlets here* accordingly.

### Hardware
Connect all outlet relays with chosen GPIO ports.

### Debugging
Same as in https://github.com/Mabolci/curtain_smarthome#debugging. Addionally, NodeMcu boards' builtin LED will light up when outlets are on, and switch off when off.