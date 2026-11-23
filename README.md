# ESP32 Wi-Fi Function Generator

## Project Description

The goal of this project is to develop a Wi-Fi-controlled function generator based on an ESP32 microcontroller.

The device should be able to generate various electrical waveforms and adjust their parameters via a custom-developed web interface.

Digital signal generation is handled by the ESP32's integrated DAC. Subsequently, the signal is conditioned by an analog RC low-pass filter circuit to reduce unwanted high-frequency signal components.

The hardware is designed using KiCad and implemented on a custom PCB.

Additionally, the behavior of the analog filter is theoretically calculated and experimentally examined using an oscilloscope. The measurement results are documented and evaluated.

## Project Goals

- Generation of various waveforms (sine, square, triangle).
- Frequency adjustment via a web interface.
- Amplitude adjustment, as far as possible on the hardware side.
- Wi-Fi communication between the user and the ESP32.
- Development of an analog RC low-pass filter circuit.
- Design and manufacturing of a custom PCB using KiCad.
- Execution and documentation of measurements.
- Comparison of theoretical and practical results.

## Technologies Used

- ESP32-WROOM-32
- Arduino C++
- HTML, CSS, and JavaScript
- KiCad
- Git and GitHub
- Microsoft Excel
- MATLAB (optional)

## Timeframe

8 weeks of development time with approximately 4 hours per week.
