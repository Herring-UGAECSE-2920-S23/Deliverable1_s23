# Deliverable 3

For this week's deliverable, you'll be testing some of the functionality of your Raspberry Pi and additional hardware. 

## Verify Hardware (D)

As a continuation from last week, using your [hardware list](./images/PartList.png) check all the parts in your kit and make sure you not only have them but they are in working condition this will be important as you begin your project and at the end when you return the kits. Please turn in a filled our status sheet for your parts.


## Accessing and Using A GPIO 

>***Warning: while connecting up simple components to the GPIO pins is perfectly safe, it's important to be careful how you wire things up. LEDs should have resistors to limit the current passing through them. Do not use 5V for 3.3V components. Do not connect high current devices like motors directly to the GPIO pins, instead use an H-bridge circuit or a motor controller board.***

As you begin to use your Raspberry Pi, you'll need to demonstrate that you can access and use a GPIO as both input and output. Your Raspberry Pi should have come with a breadboard, some jumper wires, and some resistors, LEDs, and a DIP switch for this demonstration.

**Practice:** To demonstrate output, create a Python script to blink an LED, either with user control or on a set interval. To demonstrate input, use the guides below to create a Python script to print a statement once on the screen whenever the switch is flipped in the real world.

For both of these you'll need to use the [`pigpio` Python library](http://abyz.me.uk/rpi/pigpio/index.html#Type_3), with its API [Reference](http://abyz.me.uk/rpi/pigpio/python.html) and some [example code](http://abyz.me.uk/rpi/pigpio/examples.html#Python%20code). Again, make sure to use a current-limiting resistor when using the GPIO as output, and enable the [Pull-Up or Pull-Down](https://en.wikipedia.org/wiki/Pull-up_resistor) feature on the pin when using it as input. (Note: Make sure to use the `pinout` command in a terminal to check wiring and pin numbers).

### Tips on using Using GPIO as input

While you're creating your GPIO input script, you'll notice that a simple polling method of using the GPIO may not give the results desired. To remedy this, we suggesting looking into setting up [interrupts/callbacks](http://abyz.me.uk/rpi/pigpio/python.html#callback) with the GPIO pins.

## Characterize Digital Potentiometers (D)

For this section you will need to characterize digital potientometers to use for the rest of the project.
- Give a concrete description of how the digital potentiometer works.
- Include documentation and code showing how you would program the potentiometer to multiple values (100,1000,5000,10000 Ohms). 

## Datasheet Quiz

There is a quiz on ELC that will assess your ability to read and interpret datasheets. Please review the lecture slides and posted resources in order to prepare.

## PPH Related
- Verify your team's PPH.  It must pass the verification check.  We will run SW to check each GPIO on the PPH.  We will check ground and power shorts.
- Load the PPH Eagle file and answer the design related questions.

# Summary

In summary, for this week you need to:

1. **D**: Make sure all your hardware is in your kit and is in working shapes and fill out the parts checklist

2. **D**: Characterize your digital potentiometers
 
3. **P**: Complete Datasheet Quiz

4. **D**: User Interface Check

5. Update your User Manual and Technical Documentation with your findings.
