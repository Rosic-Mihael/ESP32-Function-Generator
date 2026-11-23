# Projektplan: ESP32 WLAN-Funktionsgenerator

* **Zeitraum:** 24. November 2026 – 18. Jänner 2027 (8 Wochen)[cite: 8]
* **Aufwand:** ca. 4 Stunden pro Woche in der HTL-Werkstatt + ergänzende Software-/Dokumentationsarbeit zuhause
* **Strategie:** Hardware-First (Schaltplan, PCB-Design und Fertigung in den ersten 4 Wochen abschließen, danach Fokus auf Firmware, Webinterface und Messtechnik)

---

## Zeitplan & Arbeitspakete

### Woche 1 – Recherche, Konzept & Filter-Dimensionierung
* **Werkstatt / Schule (4 Std.):**
  * Anforderungen, Frequenzbereich und Hardware-Limits (DAC-Ausgang des ESP32-WROOM-32) definieren[cite: 8].
  * Analogen RC-Tiefpass theoretisch berechnen (Grenzfrequenz, Dämpfungsverhalten)[cite: 8].
  * Blockschaltbild und ersten Schaltungsentwurf festlegen[cite: 8].
* **Zuhause:** `requirements.md` und `technical-concept.md` ausformulieren, optional erste Filter-Simulation in MATLAB starten[cite: 8].
* **Ergebnis:** Abgeschlossenes technisches Konzept & Bauteilwerte[cite: 8].

### Woche 2 – Schaltplan & Steckbrett-Verifikation
* **Werkstatt / Schule (4 Std.):**
  * RC-Tiefpass mit den berechneten Bauteilen auf dem Steckbrett aufbauen und vorab testen[cite: 8].
  * Bauteilauswahl (Footprints, Bauformen für die HTL-Werkstatt) abklären.
* **Zuhause:** Schaltplan in KiCad (`function-generator.kicad_sch`) vollständig zeichnen und Electrical Rules Check (ERC) durchführen.
* **Ergebnis:** Verifizierte Schaltung & fertiger KiCad-Schaltplan.

### Woche 3 – PCB-Layout in KiCad
* **Werkstatt / Schule (4 Std.):**
  * Layout-Check mit dem Werkstättenlehrer (Leiterbahnbreiten, Bohrdurchmesser, Abstände für die Fertigung prüfen).
  * Eventuelle Anpassungen am Platinen-Design vornehmen.
* **Zuhause:** PCB-Layout (`function-generator.kicad_pcb`) fertig routen, Masseflächen anlegen und Design Rules Check (DRC) abschließen[cite: 8].
* **Ergebnis:** Produktionsfertiges PCB-Layout[cite: 8].

### Woche 4 – Platinenfertigung & Hardware-Inbetriebnahme
* **Werkstatt / Schule (4 Std.):**
  * Platine fertigen (ätzen/fräsen und bohren)[cite: 7].
  * Bauteile bestücken und sauber verlöten[cite: 7].
  * Alle Leiterbahnen und Lötstellen mit dem Multimeter auf Kurzschlüsse und Durchgang prüfen[cite: 7].
  * ESP32 einsetzen und Grundfunktion (Spannungsversorgung, Programmierbarkeit) testen[cite: 7].
* **Ergebnis:** Vollständig bestückte und geprüfte Hardware-Platine[cite: 7].

### Woche 5 – Digitale Signalerzeugung (ESP32 Firmware)
* **Werkstatt / Schule (4 Std.):**
  * Erste Signalausgabe (Sinus, Rechteck, Dreieck) am realen Hardware-Ausgang mit dem Oszilloskop überprüfen[cite: 8].
  * Verhalten des aufgelöteten RC-Tiefpasses bei verschiedenen Frequenzen beobachten[cite: 8].
* **Zuhause:** Firmware in C++ (`software/esp32/`) programmieren (DAC-Ansteuerung, Lookup-Tables für Sinus/Dreieck, Frequenzsteuerung)[cite: 8].
* **Ergebnis:** Funktionsfähiger Signalgenerator auf der eigenen Platine[cite: 8].

### Woche 6 – WLAN-Kommunikation & Webinterface
* **Werkstatt / Schule (4 Std.):**
  * Gesamttest der WLAN-Steuerung direkt an der Hardware in der Werkstatt.
  * Optimierung der Signalqualität und Reaktionszeit bei Parameteränderungen.
* **Zuhause:** ESP32-Webserver / Access Point einrichten und Weboberfläche (`index.html`, `style.css`, `script.js`) zur Einstellung von Signalform, Frequenz und Amplitude entwickeln[cite: 7].
* **Ergebnis:** Über WLAN steuerbarer Funktionsgenerator[cite: 7].

### Woche 7 – Systematische Messungen & Auswertung
* **Werkstatt / Schule (4 Std.):**
  * Alle Signalformen (Sinus, Rechteck, Dreieck) über den gesamten Frequenzbereich am Oszilloskop aufnehmen (`results/oscilloscope/`)[cite: 7].
  * Frequenzgang (Amplitudengang) des RC-Tiefpasses messtechnisch erfassen[cite: 7].
* **Zuhause:** Messwerte in Excel (und optional MATLAB) auswerten und mit den theoretischen Berechnungen aus Woche 1 vergleichen[cite: 7].
* **Ergebnis:** Vollständiges Messprotokoll und grafischer Soll-Ist-Vergleich[cite: 7].

### Woche 8 – Feinschliff, Dokumentation & Projektabschluss
* **Werkstatt / Schule (4 Std.):**
  * Pufferzeit für eventuelle Hardware-Korrekturen oder Nachmessungen[cite: 7].
  * Finale Abnahme / Funktionsdemonstration in der Werkstatt.
* **Zuhause:** Dokumentation (`docs/`), `logbook.md` und `README.md` finalisieren, Repository auf GitHub aufräumen und Präsentation vorbereiten[cite: 7].
* **Ergebnis:** Abgeschlossenes Projekt inkl. vollständiger GitHub-Dokumentation[cite: 7].