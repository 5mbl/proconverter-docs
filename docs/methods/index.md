---
title: Methods Overview
layout: home
nav_order: 3
---

### Methodenübersicht

#### `index()`

- **Funktion:** Leitet zur Homepage weiter.
- **Technologie:** Flask-Routing.
- **Grund:** Ermöglicht eine einfache Navigation und einen einheitlichen Einstiegspunkt.

#### `register()`

- **Funktion:** Registrierung neuer Benutzer.
- **Technologie:** Flask, SQLAlchemy.
- **Grund:** Sichert den Registrierungsprozess und speichert Benutzerdaten sicher in der Datenbank.

#### `login()`

- **Funktion:** Anmeldung bestehender Benutzer.
- **Technologie:** Flask, Flask-Session.
- **Grund:** Ermöglicht Benutzern den Zugang zu authentifizierten Bereichen der App.

#### `logout()`

- **Funktion:** Benutzer abmelden.
- **Technologie:** Flask-Session.
- **Grund:** Verbessert die Sicherheit, indem Benutzersitzungen zuverlässig beendet werden.

#### `convert_csv_to_txt()`

- **Funktion:** Konvertiert CSV-Dateien in TXT-Dateien.
- **Technologie:** Python `csv`-Modul.
- **Grund:** Bietet eine einfache Methode zur Umwandlung von tabellarischen Daten in reine Textformate.

#### `convert_png_to_pdf()`

- **Funktion:** Konvertiert PNG-Bilder in PDF-Dokumente.
- **Technologie:** Pillow, reportlab.
- **Grund:** Ermöglicht die Umwandlung von Bildern in ein universell unterstütztes Dokumentenformat.

#### `convert_png_to_jpg()`

- **Funktion:** Konvertiert PNG-Bilder in JPG-Bilder.
- **Technologie:** Pillow.
- **Grund:** Bietet eine effiziente Methode zur Bildkonvertierung, unterstützt durch weitreichende Kompatibilität des JPG-Formats.

#### `png_to_text()`

- **Funktion:** Extrahiert Text aus PNG-Bildern mittels OCR.
- **Technologie:** PyTesseract.
- **Grund:** Nutzt fortschrittliche OCR-Technologie, um Bildinhalte in bearbeitbaren Text umzuwandeln.

#### `convert_pdf_to_png()`

- **Funktion:** Konvertiert PDF-Seiten in PNG-Bilder.
- **Technologie:** pdf2image, Poppler.
- **Grund:** Ermöglicht die Visualisierung von PDF-Inhalten als Bilder, unterstützt durch die präzise Rendering-Fähigkeit von Poppler.

#### `convert_jpg_to_png()`

- **Funktion:** Konvertiert JPG-Bilder in PNG-Format.
- **Technologie:** Pillow.
- **Grund:** Bietet eine verlustfreie Bildkonvertierung für eine bessere Qualität und Transparenzunterstützung im PNG-Format.

#### `text_file_to_png()`

- **Funktion:** Konvertiert Textinhalte in ein PNG-Bild.
- **Technologie:** Pillow.
- **Grund:** Ermöglicht die visuelle Darstellung von Textdaten in einem anpassbaren Bildformat.
