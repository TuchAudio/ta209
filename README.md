# TuchAudio 209
Discrete, high quality mid-power mono amplifier

## Purpose
A compact but reasonably powerful (depending on supply voltage and heatsinks) audio amplifier.

## Design quirks
This is a discrete, non-symmetrical op-amp with Darlington output stage. The design is pretty versatile, allowing the use as a _headphone amplifier_ as well. The input stage (`Q1/Q2`) has diminished _Vce_ thru a cascode arrangement (`Q3/Q4`), allowing the use of **low-noise, higher quality** transistors (BC549C/BC550C/BC559C/BC560C) whenever possible. The use of Darington output transistors (usually BD677/BD678) allows a low current driver stage.

The use of **current sources** for both the emitters of the input stage (`Q5`) and the load of the inverting stage (`Q6`), with **symmetric power supply**, guarantees good PSRR and decent open-loop gain.

### Stability
_Thermal stability_ is guaranteed by the use of both _emitter-degeneration_ 0.33 Ω resistors `R10/R11`, and the location of the _biasing diodes_ `D4-D7` **as close as possible to the heatsink**.

In order to prevent _oscillations_, the feedback loop implements a **low-pass filter** cutting at around 30 kHz, by means of the `C2` capacitor. In case the _gain_ is changed via `R14`, recompute this capacitor accordingly.

### Suggested mods
As previously mentioned, this is a **very versatile** design, and could serve a huge range of output power ratings.

#### Headphone amp
- Reduce power supply to no more than **+/- 12 Volts**.
- Remove `Q3/Q4` and make a **bridge** between each unused Collector and Emitter.
- Do NOT populate `Q10/Q11/R10/R11/F1/F2`.
- Replace `D4/D5` and `D6/D7` by **jumpers**.
- At `R9/R16` use **1Ω5** instead of 330.
- At `R15` use **10 KΩ** instead of 680. Then, `C3` could be as low as **2µ2**.
- You may consider using a **BC337** for `Q9` and a **BC327** for `Q8`.
- You might leave out either `R12/R13` and one of `C6/C7`.

## Specs

- **Power supply:** from +/- 6 V to +/- 30 V
- **Gain:** typically x50 (+26 dB)
- **Input sensitivity:** 180 mV
- **Input impedance:** 47 kΩ
- **Output level and impedance:** 26 Vpp / 4 Ω
- **Frequency response:** TBD
- **Distortion:** TBD

| Harmonic | nominal output | 50 mW |
| -------- | -------------- | ----- |
| 2nd      |  %         |  %           |
| 3rd      |  %         |  %           |
| 4th      |  %         |  %           |
