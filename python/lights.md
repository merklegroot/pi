# Lights

The Pi 400 the standard RasperryPi 40-pin header.  
To access it, you'll need to remove the black rubber tab on the back.  

<https://www.raspberrypi.org/documentation/usage/gpio/images/GPIO-Pinout-Diagram-2.png>
![](https://www.raspberrypi.org/documentation/usage/gpio/images/GPIO-Pinout-Diagram-2.png)

## Turning on an LED

We can use these pins to light up an LED without writing any code.  

Try creating the following circuit.  

``` text
5V -> LED -> Resistor -> GND  
```

## Blinking LED

Now let's use Python to get that LED to blink.  
First off, we'll want to switch the source of the circuit to start with a GPIO pin instead of the direct 5V pin.
For this example, let's go with GPIO 7.

``` text
GPIO 7 -> LED -> Resistor -> GND
```

``` python
import RPi.GPIO as GPIO
from time import sleep

pin = 7

GPIO.setmode(GPIO.BOARD)
GPIO.setup(pin, GPIO.OUT, initial=GPIO.LOW) 

while True:
    GPIO.output(pin, GPIO.HIGH)
    sleep(1)
    GPIO.output(pin, GPIO.LOW)
    sleep(1)
```