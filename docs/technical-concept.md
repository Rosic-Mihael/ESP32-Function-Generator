# Technical Concept

## System Architecture

The system consists of three main components:

1. ESP32
   - Generates digital samples.
   - Converts samples into analog voltage using its DAC.
   - Hosts a WiFi web server.

2. Analog Signal Processing
   - RC low-pass filter.
   - Reduces unwanted high-frequency components.

3. Web Interface
   - Allows frequency selection.
   - Allows waveform selection.
   - Communicates with the ESP32 over WiFi.

## Signal Flow

ESP32 DAC -> RC Low-Pass Filter -> Output