# jetsonGPIO
A straightforward C/C++ library to interface with the NVIDIA Jetson NANO Development Kit GPIO pins.

Modified based on https://github.com/jetsonhacks/jetsonTX1GPIO


Based on Software by RidgeRun
https://developer.ridgerun.com/wiki/index.php/Gpio-int-test.c
 * Copyright (c) 2011, RidgeRun
 * All rights reserved.

and ideas from Derek Malloy Copyright (c) 2012
https://github.com/derekmolloy/beaglebone

exampleGPIApp.cpp describes a simple usage case using a tactile button and LED as input and output.


# Description
To add more GPIO pins, modify jetsonGPIO.h and add pin numbers you want.

* Example:
setup and initialize GPIO78 (Pin40) as output pin on NANO:
```
/* To initialize */
jetsonGPIONumber LEDControlPin = gpio78;
gpioExport(LEDControlPin);
gpioSetDirection(LEDControlPin,outputPin);

/* To control pin high or low  */
gpioSetValue(LEDControlPin, on);     //Pull high
gpioSetValue(LEDControlPin, off);    //Pull low
```

That's it, very easy. If you like to use C/C++ to control GPIO Pin, just include "jetsonGPIO.h" in the cpp file.
