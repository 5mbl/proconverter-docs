---
title: Start
layout: home
nav_order: 1
---

## Inhaltsverzeichnis

- [Teammitglieder](#teammitglieder)
- [Unser Projekt](#unser-projekt)
- [Aufteilung](#aufteilung)
- [How to Run the Code](#how-to-run-the-code)

Präsentationsfolie aus der mündlichen Prüfungsleistung [hier](Präsentationsfolien-fswd.pdf)

## Teammitglieder

### Serdar Palaoglu

- **Matrikelnummer:** 77211970278

### Moritz Michael Kocibelli

- **Matrikelnummer:** 77211965225

### Samed Cevat Ünal

- **Matrikelnummer:** 77211918612

## Unser Projekt

Im Rahmen unseres Full Stack Webentwicklungskurses hatten wir das Ziel, die in den Vorlesungen und Seminaren erlernten Technologien praktisch anzuwenden und dabei eine Lösung für ein reales Problem zu entwickeln, um echten Mehrwert für Nutzer zu generieren. Nach mehreren Brainstorming-Sitzungen und einem strategischen Kurswechsel – ursprünglich fokussierten wir uns mit dem Projekt "TextExtractPro" hauptsächlich auf OCR (Optische Zeichenerkennung) – entschieden wir uns, ein allgegenwärtiges Problem anzugehen, mit dem fast jeder irgendwann konfrontiert wird: die Dateikonvertierung.

Während der Umsetzung unseres Projekts wurde uns klar, dass wir die Idee skalieren und weitere Optionen für den Benutzer hinzufügen könnten. Nach einer Diskussion in der Gruppe beschlossen wir, der Anwendung zusätzliche Konvertierungsmethoden hinzuzufügen:

PDF <-> PNG

JPG <-> TXT

TXT <-> PDF

CSV <-> TXT

Daher haben wir unser Team in "ProConverter" umbenannt, da wir nun mehr Optionen für die Benutzer anbieten. Unsere neue Philosophie lautet: "Wir wollen das **Schweizer Taschenmesser für die Dateikonvertierung** sein."

Unsere Entscheidung für dieses Thema war von der Erkenntnis geleitet, dass trotz der Vielzahl vorhandener Tools, die Fragmentierung und die Ineffizienz in diesem Bereich nach wie vor groß sind. Mit ProConverter beabsichtigen wir, eine umfassende, benutzerfreundliche Lösung bereitzustellen, die es Nutzern ermöglicht, mühelos zwischen verschiedenen Dateiformaten zu konvertieren, und so eine Lücke in der digitalen Werkzeugpalette effektiv zu schließen.

In der folgenden Dokumentation vertiefen wir die Details unserer Applikation. Sie erhalten einen Einblick in die Funktionsweise und die Architektur unser App.

Sollten Sie die Applikation noch nicht in Betrieb genommen haben, finden Sie im weiteren Verlauf eine detaillierte Anleitung, die Sie Schritt für Schritt durch den Installations- und Einrichtungsprozess führt. Diese Anleitung ist ebenfalls im README auf unserem GitHub-Repository verfügbar, um Ihnen einen unkomplizierten Start mit ProConverter zu ermöglichen.

## Aufteilung

**Moritz:** Startseite & Navigation

**Serdar:** Upload-Funktionalität in allen Konverter

**Samed:** Login/Registrierungsseite

**Alle Teammitglieder:** Konvertierung & Download-Funktionalität

### Moritz:

**Aufgabenbereich:**

- Gestaltung des Layouts der Startseite, einschließlich Navigationsmenüs.
- Erstellung einer klaren Navigationsstruktur.
- Zusammenarbeit mit dem Team, um das Design der Startseite mit anderen Projektkomponenten zu verbinden.

### Serdar:

**Aufgabenbereich:**

- Umsetzung der Upload-Funktion in allen Konvertern
- Zuständig für OCR und alle anderen Technologien bei der Konvertierung
- Lead im organisieren
  Samed - Login/Registrierungsseite:
  Aufgabenbereich:

### Samed:

**Aufgabenbereich:**

- Entwicklung des Benutzerauthentifizierungssystems, einschließlich Registrierung und Login.
- Zusammenarbeit mit dem Team, um die Login/Registrierungsfunktionalität mit anderen Projektelementen zu integrieren.

### Alle Teammitglieder:

**Gemeinsamer Aufgabenbereich:**

- Implementierung der Konvertierungsfunktionalität, die einen automatischen Download nach der Konvertierung ermöglicht.

- Kompatibilität der Download-Funktion in verschiedenen Browsern.

**Zusätzliche Zusammenarbeitsdetails:**

Das Team arbeitete hauptsächlich gemeinsam an der Repository am Projekt, was eine enge Zusammenarbeit und effiziente Kommunikation förderte.

Serdar übernahm meist die Führung beim Hochladen der Projektergebnisse, was eine rechtzeitige Einreichung und Dokumentation des Fortschritts sicherstellte.

_Weitere Punkte:_

Das Git-Repository ist gut organisiert und frei von unnötigem Ballast, wie z.B. überflüssigen virtuellen Umgebungsdateien (z.B. venv/), was eine einfache Navigation ermöglicht.

Dieses Einreichungspaket spiegelt die gemeinsamen Anstrengungen aller Teammitglieder wider und zeigt einen kohärenten Ansatz bei der Entwicklung von ProConvert.

## How to Run the Code

### Installation Steps:

1. **Clone the Repository:**
   ```sh
   git clone https://github.com/5mbl/ocr-backend.git
   ```
2. **Install Dependencies:**

- **Pytesseract:** ¹

  - Download and install [tesseract-ocr-w64-setup-5.3.3.20231005.exe](https://digi.bib.uni-mannheim.de/tesseract/tesseract-ocr-w64-setup-5.3.3.20231005.exe).
  - After installation, locate the installed directory (e.g., `C:\Program Files (x86)\Tesseract-OCR`).
  - Download the German training data file from [here](https://github.com/tesseract-ocr/tessdata/blob/main/deu.traineddata).
  - Copy the downloaded file into the "tessdata" directory within the installed Tesseract directory (e.g., `C:\Program Files (x86)\Tesseract-OCR\tessdata`).
  - Specifying tesseract.exe Path in Code:

    ```python
    # app.py (line 35)

    #pytesseract for OCR
    pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
    ```

- **Poppler:** ²

  - Go to [Poppler Windows Releases](https://github.com/oschwartz10612/poppler-windows/releases/).
  - Under **Release 23.11.0-0 Latest v23.11.0-0**, navigate to **Assets 3**
  - Download **Release-23.11.0-0.zip**.
  - Extract the downloaded zip file.
  - Add the extracted Poppler folder to a location such as: `C:\Users\UserName\Downloads\Release-23.11.0-0`.
  - Add the path `C:\Users\UserName\Downloads\Release-21.11.0-0` to the system variable **Path** in the **Environment Variables**.
  - Specifying Poppler Path in Code:

    ```python
    # app.py (line 38)

    # poppler for pdf2img
    poppler_path = r"C:\poppler-23.11.0\Library\bin"

    ```

- **Activating the virtual enviroment:**
  - Terminal: `python -m venv myenv`
- **Install requirements.txt:**

  - `pip install -r requirements.txt`

- **Start the Application**
  - `run flask`

## References

¹ https://smartextract.ai/pytesseract/

² https://stackoverflow.com/questions/53481088/poppler-in-path-for-pdf2image
