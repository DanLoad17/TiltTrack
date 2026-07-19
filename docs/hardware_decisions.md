# Hardware Decisions

## AT42QT1012

### Used Pins
- VDD: Connected to ESP32 3.3V
- GND: Connected to ESP32 GND
- OUT: Connected to ESP32 GPIO

### Unused Pins
- TIME: Not used because no timeout behavior is required
- LEDA: Not used because onboard LED indication is unnecessary

### Reasoning
The AT42QT1012 handles capacitance measurement, calibration, filtering, and touch detection internally. The ESP32 only needs the digital output state.
