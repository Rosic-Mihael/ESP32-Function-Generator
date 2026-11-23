# ESP32 WLAN-Funktionsgenerator

## Projektbeschreibung

Ziel dieses Projekts ist die Entwicklung eines WLAN-gesteuerten Funktionsgenerators auf Basis eines ESP32-Mikrocontrollers.

Das Gerät soll verschiedene elektrische Signalformen erzeugen und deren Parameter über eine selbst entwickelte Weboberfläche einstellen können.

Die digitale Signalerzeugung erfolgt durch den integrierten DAC des ESP32. Anschließend wird das Signal durch eine analoge RC-Tiefpassschaltung aufbereitet, um unerwünschte hochfrequente Signalanteile zu reduzieren.

Die Hardware wird mit KiCad entwickelt und auf einer eigenen Platine realisiert.

Zusätzlich wird das Verhalten des analogen Filters theoretisch berechnet und experimentell mit einem Oszilloskop untersucht. Die Messergebnisse werden dokumentiert und ausgewertet.

## Projektziele

- Erzeugung verschiedener Signalformen (Sinus, Rechteck, Dreieck).
- Einstellung der Frequenz über eine Weboberfläche.
- Einstellung der Amplitude, soweit hardwareseitig möglich.
- WLAN-Kommunikation zwischen Benutzer und ESP32.
- Entwicklung einer analogen RC-Tiefpassschaltung.
- Entwicklung und Fertigung einer eigenen PCB mit KiCad.
- Durchführung und Dokumentation von Messungen.
- Vergleich theoretischer und praktischer Ergebnisse.

## Verwendete Technologien

- ESP32-WROOM-32
- Arduino C++
- HTML, CSS und JavaScript
- KiCad
- Git und GitHub
- Microsoft Excel
- MATLAB (optional)

## Zeitrahmen

8 Wochen Entwicklungszeit mit jeweils ungefähr 4 Stunden pro Woche.
