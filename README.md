# Adjustable Linear Power Supply Using LM338

This project is a high-current adjustable linear voltage regulator based on the LM338. The design provides a stable and adjustable DC output suitable for electronics prototyping, robotics, and general lab use. A custom PCB was designed in KiCad, making the circuit compact, reliable, and easy to reproduce.

The LM338 is capable of supplying up to 5 A of output current, making this regulator suitable for powering microcontrollers, sensors, small motors, and other moderate-current loads.

## Features
- Adjustable output voltage from 1.2 V up to 32 V
- Input voltage range up to 35 V DC
- Output current up to 5 A (with proper heat sinking)
- Linear regulation for low noise and stable output
- Protection diodes to prevent regulator damage during:
  - Output short circuits
  - Large output capacitor discharge
- Screw terminals for easy power input and output
- Custom PCB designed using KiCad

## Circuit Overview
The output voltage is set using a resistor and potentiometer connected to the ADJ pin of the LM338. The relationship between the resistors determines the regulated output voltage.
Two protection diodes are included:
- One diode between Vout and Vin to protect the LM338 if the input is shorted
- One diode between Vout and ADJ to prevent reverse current through the adjustment pin

Input and output capacitors are used to improve stability and transient response.

## Applications
- Bench power supply
- Robotics projects
- Arduino and microcontroller power source
- Analog and digital circuit testing
- Educational use for learning linear regulators and PCB design

## Design Tools
- Schematic & PCB: KiCad
- Regulator IC: LM338
- PCB: Single-board linear regulator design

## Notes

- A heat sink is required when operating at high current or large input–output voltage differences.
- This is a linear regulator, so power dissipation increases with higher current and voltage drop.
- Reverse polarity protection can be added externally or in future PCB revisions.


# Block Diagram Description
## Block Flow:

DC Input → Protection → LM338 Regulator → Output Filter → Adjustable DC Output

## Block Explanation

1. DC Input
  - Power is supplied through a screw terminal connector.
  - Accepts a DC input voltage up to 35 V.
  - Protection Network
  - Protection diodes prevent reverse current flow through the LM338 during:

2. Input short circuits

Output capacitor discharge

This improves regulator reliability and longevity.

LM338 Adjustable Regulator

The LM338 regulates the input voltage and provides up to 5 A of output current.

Output voltage is set using a fixed resistor and a potentiometer connected to the ADJ pin.

Output Filtering

Output capacitors improve stability and transient response.

Reduces voltage ripple and noise at the load.

Adjustable DC Output

Regulated and adjustable output voltage available at the output screw terminal.

Suitable for powering a wide range of electronic circuits and subsystems.

Future Improvements

Reverse Polarity Protection

Add a P-channel MOSFET–based reverse polarity protection circuit at the input to prevent damage if the power supply is connected backward.

This would eliminate voltage drop compared to a series diode solution.

Current Limiting / Protection

Add external current sensing or foldback current limiting to better protect the load and regulator under fault conditions.

Thermal Protection Enhancements

Include PCB-mounted temperature sensing or thermal cutoff circuitry.

Improve copper pours and thermal vias for better heat dissipation.

Digital Voltage Monitoring

Add a voltmeter or ADC interface to display or measure output voltage digitally.

Useful for bench power supply applications.

Improved PCB Layout

Widen high-current traces.

Optimize ground planes and star grounding to reduce noise and voltage drop.

Enclosure & User Interface

Design a 3D-printable enclosure.

Add labeling, test points, and optional power indicator LEDs.

Multiple Output Versions

Expand the design to support multiple regulated outputs or selectable voltage rails.
