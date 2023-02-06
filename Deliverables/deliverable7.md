# Deliverable 7
In this deliverable you will begin creating the DC Voltage supply for your function generator and the ohmmeter.  You will continue your work on the ADC and Negative reference.  If you have not completed the Negative reference, you may use +/- voltage from lab dc supply to make progress.

## Ohmmeter Manual (P)
Using something like a Wheatstone bridge (Hint-Hint), create a stand-alone Ohmmeter.  Show your Ohmmeter working with a manual potentiometer.
The Ohmmeter should measure 500-10KOhms.  The design must include an indicator for the measurement point (perhaps a comparator of some sort). Characterize your Ohmmeter.  That is, what is the measured resistance vs the actual resistance for 500, 1000, 2000, 3000, 4000, 5000, 6000, 7000, 8000, 9000, and 10K Ohms. Provide:
- Eagle Schematic of your design
- Characterization table for your Ohmmeter with manual potentiometer
- Photo of your design working at 500, 5K, and 10K Ohms with manual potentiometer

## Ohmmeter Auto (P)
Now, using your Checkpoint C as starting point and your manual ohmeter design, update your ohmmeter design with a digital potentiometer.  Use the PWM knob press to take the resistance measurement from your pi.  Display the value on the LCD. 

- Eagle Schematic
- Characterization table for your Ohmmeter with digital potentiometer.
- Photo of your LCD reading values for 500, 5K, and 10K Ohms
- Commited code on github

## Voltmeter (P)
For this Deliverable your team will be required to design a voltmeter that is able to measure a power supply. The voltmeter should have a quarter volt resolution and measure from 0 - 3.33 V (positive only). Your team will need to build an analog to digital converter (ADC) to achieve this.  Design a stand-alone Voltmeter.
- Eagle Schematic
- ADC table of Analog voltage to digital values
- Multisim simulation of your design working with 0, 1, 2, 3, and 4 volts (yes, 4V is higher than 3.33).
- Use your PWM knob press to take measurement from PI.  Display the result on the LCD.
- Provide photos of your results for the 5 0, 1, 2, 3, and 4 volts

## Negative Voltage (P)
By now your Negative voltage should be working.  Provide photo evidence of this.
If you have not shown a working negative voltage reference, you must still do so in order to get the +12V DC supply.


# Summary

In summary, for this week you need to:

1. **P**: Ohmmeter Manual
2. **P**: Ohmmeter Auto
3. **P**: DC Voltage Supply
4. **P**: Negative Voltage
5. Update your User Manual and Technical Documentation with your findings.
