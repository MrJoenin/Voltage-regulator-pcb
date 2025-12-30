## Adjustable Linear Power Supply Using LM338

This project is a high-current adjustable linear voltage regulator based on the LM338. The design provides a stable and adjustable DC output suitable for electronics prototyping, robotics, and general lab use. A custom PCB was designed in KiCad, making the circuit compact, reliable, and easy to reproduce.

The LM338 is capable of supplying up to 5 A of output current, making this regulator suitable for powering microcontrollers, sensors, small motors, and other moderate-current loads.

# Features
- Adjustable output voltage from 1.2 V up to 32 V
- Input voltage range up to 35 V DC
- Output current up to 5 A (with proper heat sinking)
- Linear regulation for low noise and stable output
- Protection diodes to prevent regulator damage during:
  - Output short circuits
  - Large output capacitor discharge
- Screw terminals for easy power input and output
- Custom PCB designed using KiCad

# Circuit Overview
The output voltage is set using a resistor and potentiometer connected to the ADJ pin of the LM338. The relationship between the resistors determines the regulated output voltage.
Two protection diodes are included:
- One diode between Vout and Vin to protect the LM338 if the input is shorted
- One diode between Vout and ADJ to prevent reverse current through the adjustment pin

Input and output capacitors are used to improve stability and transient response.

Applications

Bench power supply

Robotics projects

Arduino and microcontroller power source

Analog and digital circuit testing

Educational use for learning linear regulators and PCB design

Design Tools

Schematic & PCB: KiCad

Regulator IC: LM338

PCB: Single-board linear regulator design

Notes

A heat sink is required when operating at high current or large input–output voltage differences.

This is a linear regulator, so power dissipation increases with higher current and voltage drop.

Reverse polarity protection can be added externally or in future PCB revisions.
