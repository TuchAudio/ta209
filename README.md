# TuchAudio 209
Discrete, high quality mid-power mono amplifier

## Purpose
A compact but reasonably powerful (depending on supply voltage and heatsinks) audio amplifier.

## Design quirks
This is a discrete, non-symmetrical op-amp with Darlington output stage. The design is pretty versatile, allowing the use as a _headphone amplifier_ as well. The input stage (`Q1/Q2`) has diminished Vce thru a cascode (`Q3/Q4`), allowing the use of **low-noise, higher quality** transistors (BC549C/BC550C/BC559C/BC560C) whenever possible. The use of Darington output transistors (usually BD677/BD678) allows a low current driver stage.

### Stability
_Thermal stability_ is guaranteed by the use of both _emitter-degeneration_ 0.33 Ω resistors `R`, and the location of the _biasing diodes_ `D` **as close as possible to the heatsink**.

In order to prevent _oscillations_, the feedback loop impl

### Suggested mods

#### Standalone mode



## Specs

- **Power supply:** 12 V, asymmetrical, max. 400 mA
- **Gain:** 20x (+26 dB) with +46 dB option.
- **Input sensitivity:** 180 mV
- **Input impedance:** 10 kΩ; with optional buffer for standalone operation, ~108 kΩ.
- **Output level and impedance:** 10 Vpp / 8 Ω
- **Frequency response:** TBD
- **Distortion:** TBD

| Harmonic | nominal output | 50 mW |
| -------- | -------------- | ----- |
| 2nd      |  %         |  %           |
| 3rd      |  %         |  %           |
| 4th      |  %         |  %           |
