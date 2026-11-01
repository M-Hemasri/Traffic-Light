# 4-Way Traffic Light System

A simple Arduino project that simulates a four-way traffic light system using 12 LEDs. Each road has a green, yellow, and red LED. The traffic lights operate in sequence, allowing one road to show green or yellow while the other three roads remain red.

## Hardware

- Arduino-compatible board
- 4 green LEDs
- 4 yellow LEDs
- 4 red LEDs
- 3 × 220–330 ohm resistors
- Breadboard
- Jumper wires
- USB cable

## Wiring

### Road 1

- Green LED → Digital pin 2
- Yellow LED → Digital pin 3
- Red LED → Digital pin 4

### Road 2

- Green LED → Digital pin 5
- Yellow LED → Digital pin 6
- Red LED → Digital pin 7

### Road 3

- Green LED → Digital pin 8
- Yellow LED → Digital pin 9
- Red LED → Digital pin 10

### Road 4

- Green LED → Digital pin 11
- Yellow LED → Digital pin 12
- Red LED → Digital pin 13

GND connection

- connect the cathode of all green led (small leg) in common and then connect it to Arduino GND through a current-limiting resistor.
- connect the cathode of all yellow led (small leg) in common and then connect it to Arduino GND through a current-limiting resistor.
- connect the cathode of all red led (small leg) in common and then connect it to Arduino GND through a current-limiting resistor.

## Upload

1. Open the Arduino sketch in the Arduino IDE.
2. Select your Arduino board and port from the **Tools** menu.
3. Click **Verify** to compile the code.
4. Click **Upload** to upload the sketch.

## Working Principle

1. All 12 LED pins are configured as outputs.
2. Road 1 gets the green signal while the other three roads show red.
3. Road 1 changes to yellow before Road 2 gets the green signal.
4. Road 2 changes from green to yellow before Road 3 gets the green signal.
5. Road 3 changes from green to yellow before Road 4 gets the green signal.
6. Road 4 changes from green to yellow.
7. The sequence repeats continuously from Road 1.

## LED Timing

| Signal |          Duration |
| ------ | ----------------: |
| Green  | 1000 milliseconds |
| Yellow |  200 milliseconds |
| Red    | 3600 milliseconds |

## Expected Result

The four sets of traffic lights operate one after another. Each road receives a green signal, followed by yellow, while the other roads remain red.

The sequence repeats continuously to simulate a four-way traffic signal system.
