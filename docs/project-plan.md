# Project Plan: ESP32 Wi-Fi Function Generator

- **Period:** November 24, 2026 – January 18, 2027 (8 weeks)
- **Effort:** approx. 4 hours per week in the HTL workshop + supplementary software/documentation work at home
- **Strategy:** Hardware-First (complete schematic, PCB design, and manufacturing in the first 4 weeks, followed by a focus on firmware, web interface, and measurement technology)

---

## Schedule & Work Packages

### Week 1 – Research, Concept & Filter Dimensioning
- **Workshop / School (4 hrs):**
  - Define requirements, frequency range, and hardware limits (DAC output of the ESP32-WROOM-32).
  - Theoretically calculate the analog RC low-pass filter (cutoff frequency, damping behavior).
  - Establish block diagram and initial circuit design.
- **At Home:** Draft `requirements.md` and `technical-concept.md`, optionally start initial filter simulation in MATLAB.
- **Result:** Completed technical concept & component values.

### Week 2 – Schematic & Breadboard Verification
- **Workshop / School (4 hrs):**
  - Build and pre-test the RC low-pass filter with the calculated components on a breadboard.
  - Clarify component selection (footprints, packages for the HTL workshop).
- **At Home:** Draw schematic fully in KiCad (`function-generator.kicad_sch`) and perform Electrical Rules Check (ERC).
- **Result:** Verified circuit & completed KiCad schematic.

### Week 3 – PCB Layout in KiCad
- **Workshop / School (4 hrs):**
  - Layout check with the workshop teacher (check trace widths, drill diameters, clearances for manufacturing).
  - Make any necessary adjustments to the board design.
- **At Home:** Route PCB layout (`function-generator.kicad_pcb`) completely, create ground planes, and complete Design Rules Check (DRC).
- **Result:** Production-ready PCB layout.

### Week 4 – PCB Manufacturing & Hardware Commissioning
- **Workshop / School (4 hrs):**
  - Manufacture PCB (etch/mill and drill).
  - Populate components and solder cleanly.
  - Check all traces and solder joints for short circuits and continuity using a multimeter.
  - Insert ESP32 and test basic functions (power supply, programmability).
- **Result:** Fully populated and tested hardware board.

### Week 5 – Digital Signal Generation (ESP32 Firmware)
- **Workshop / School (4 hrs):**
  - Verify initial signal output (sine, square, triangle) at the actual hardware output using an oscilloscope.
  - Observe the behavior of the soldered RC low-pass filter at various frequencies.
- **At Home:** Program firmware in C++ (`software/esp32/`) (DAC control, lookup tables for sine/triangle, frequency control).
- **Result:** Functional signal generator on the custom board.

### Week 6 – Wi-Fi Communication & Web Interface
- **Workshop / School (4 hrs):**
  - Overall test of the Wi-Fi control directly on the hardware in the workshop.
  - Optimize signal quality and response time during parameter changes.
- **At Home:** Set up ESP32 web server / Access Point and develop web interface (`index.html`, `style.css`, `script.js`) for setting waveform, frequency, and amplitude.
- **Result:** Function generator controllable via Wi-Fi.

### Week 7 – Systematic Measurements & Evaluation
- **Workshop / School (4 hrs):**
  - Record all waveforms (sine, square, triangle) across the entire frequency range using an oscilloscope (`results/oscilloscope/`).
  - Measure the frequency response (amplitude response) of the RC low-pass filter.
- **At Home:** Evaluate measurement data in Excel (and optionally MATLAB) and compare with theoretical calculations from Week 1.
- **Result:** Complete measurement protocol and graphical target-vs-actual comparison.

### Week 8 – Fine-Tuning, Documentation & Project Completion
- **Workshop / School (4 hrs):**
  - Buffer time for any hardware corrections or re-measurements.
  - Final acceptance / functional demonstration in the workshop.
- **At Home:** Finalize documentation (`docs/`), `logbook.md`, and `README.md`, clean up repository on GitHub, and prepare presentation.
- **Result:** Completed project including full GitHub documentation.
