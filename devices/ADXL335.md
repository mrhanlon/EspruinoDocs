<!--- Copyright (c) 2014 Your Name. See the file LICENSE for copying permission. -->
ADXL335 Accelerometer
==================

* KEYWORDS: Module,ADXL335,Acceleration,Accelerometer,Analog,Sensor

Simple wrapper module for the cheap and readily available analog ADXL335 accelerometer.
Use the [[ADXL335.js]] module for it.

You can wire this up as follows:

| Device Pin | Espruino |
| ---------- | -------- |
| 1 (GND)    | GND      |
| 2 (VCC)    | 3.3      |
| 3 (X)      | Any ADC  |
| 4 (Y)      | Any ADC  |
| 5 (Z)      | Any ADC  |

How to use my module:

```
  var foo = require("ADXL335").connect(C3,A0,A1);
  setInterval(function() {
    var d= adxl.readG();
    console.log("x " + d[0] + " y " + d[1] + " z " + d[2]);
  }, 1000);
```
