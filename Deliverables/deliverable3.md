# Deliverable 3

For this week's deliverable, you'll be testing some of the functionality of your Raspberry Pi and additional hardware. 

## Verify Hardware (D)

As a continuation from last week, using your [[hardware list](./images/Parts%20List.png)], check all the parts in your kit. Make sure they are all in your kit AND are in working condition. This will be important as you begin your project and at the end when you return the kits. Please turn in a filled out status sheet for your parts.


## Accessing and Using A GPIO (D)

>***Warning: while connecting up simple components to the GPIO pins is perfectly safe, it's important to be careful how you wire things up. LEDs should have resistors to limit the current passing through them. Do not use 5V for 3.3V components. Do not connect high current devices like motors directly to the GPIO pins.***

Great resource for GPIOS.  Read prior to programming!
The Raspberry PI GPIOS are the primary way to blow up your PI.  They default to certain states and you must program them and make sure you understand the valid state prior to using.  Here are a couple of references.  You may find others online as well.
- https://roboticsbackend.com/raspberry-pi-3-pins/
- https://roboticsbackend.com/raspberry-pi-gpios-default-state/

As you begin to use your Raspberry Pi, you'll need to demonstrate that you can access and use a GPIO as both input and output. Your Raspberry Pi should have come with a breadboard, some jumper wires, and some resistors, LEDs, and a rotary encoder for this demonstration.

**Deliverable:** To demonstrate both input and output functionality, use the guides below to create a Python script that does the following: pressing in on the rotary encoder toggles (meaning button press) an LED on or off. Upload a short video (10 seconds or less) on eLC that shows this in action.

For both of these you'll need to use the [`pigpio` Python library](http://abyz.me.uk/rpi/pigpio/index.html#Type_3), with its API [Reference](http://abyz.me.uk/rpi/pigpio/python.html) and some [example code](http://abyz.me.uk/rpi/pigpio/examples.html#Python%20code). Again, make sure to use a current-limiting resistor when using the GPIO as output if you are not using the PHP (Pi Hat Protector), and enable the [Pull-Up or Pull-Down](https://en.wikipedia.org/wiki/Pull-up_resistor) feature on the pin when using it as input. (Note: Make sure to use the `pinout` command in a terminal to check wiring and pin numbers).

### Tips on using Using GPIO as input

While you're creating your GPIO input script, you'll notice that a simple polling method of using the GPIO may not give the results desired. To remedy this, we suggesting looking into setting up [interrupts/callbacks](http://abyz.me.uk/rpi/pigpio/python.html#callback) or you could use a simple polling routine with the GPIO pins.

## Characterize Digital Potentiometers (D)

For this section you will need to characterize digital potientometers to use for the rest of the project.
- Give a concrete description of how the digital potentiometer works.
- Include documentation and code showing how you would program the potentiometer to multiple values (100,1000,5000,10000 Ohms). Note that you only need to provide code; you do not need to verify the resistance values with a multimeter this week.
- The datasheet for the MCP digital potentiometers can be found [here](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/DataSheets/22060b.pdf).

## Datasheet Quiz (Individual Grade Item)

There is a quiz on ELC that will assess your ability to read and interpret datasheets. Please review the lecture slides and posted resources in order to prepare.
The format of the quiz is as follows: 

- On ELC, 14 questions total, 3 short answer, 11 ELC-graded questions
- Individual, open GitHub
- Need to know:  Raspberry Pi, Digital Potentiometer (MCP4231), ‘1450 equipment use’


## Pi-Protection Hat (PPH) (D)
- Verify your team's PPH.  It must pass the verification check. This will be done in class on Wednesday.  We will run SW to check each GPIO on the PPH.  We will check ground and power shorts.

# Summary

In summary, for this week you need to:

1. **D**: Make sure all your hardware is in your kit and is in working shape and fill out the parts checklist

2. **D**: Characterize your digital potentiometers
 
3. **D**: GPIO Input/Output Check

4. **D**: Pi-Protection Hat Verification

5. Complete Datasheet Quiz (In-class 1/25)

6. Update your User Manual and Technical Documentation with your findings.

When all deliverables are finished, use the template to submit to ELC before the deadline. THERE SHOULD BE ONLY 1 SUBMISSION PER GROUP. Videos can be attached separately.
