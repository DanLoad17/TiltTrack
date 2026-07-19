# AT42QT1012 Notes

## Purpose
The purpose of this breakout board is to act as a touch sensor. Here, it uses the change in capacitance to alter output as either high or low to a microcontrolelr or to another electrical circuit.
## Electrical Characteristics
Contains onboard sensor, LED and preset timeout (none enabled as it is a toggle switch), though these can be changed. Operating voltage is 1.8-5.5V.
## Pins
5 pins.
GND: Ground. 
OUT: Output signal. High or low, depending on touch to sensor.
TIME: For external timeout features.
VDD: Power in.
LEDA: For external LED control.
## Communication
Communicates high/low signal depending on if touch (change in capacitance) is measured. Can be hardware configured to either. This is done through the OUT pin.
## Design Decisions
Operates between -40 and 85 degrees celcius. Onboard LED and TIMEOUT configured (TIMEOUT disabled) for easy debug and to act as a toggle. 1.8-5.5V operating voltage allows for loose requirements, does not need converters when paired with a typical microcontroller for example.
## Open Questions
