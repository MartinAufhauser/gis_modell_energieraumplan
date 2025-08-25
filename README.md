# Energieraumplan 2.0 – GIS-Modell

## Beschreibung

Dieses Repository enthält das datengestützte GIS-Modell zur Vorbereitung der Erstellung eines **Energieraumplans 2.0** für den 14. Wiener Bezirk. Das Modell dient der systematischen Identifikation optimaler energieraumplanerischer Transformationslösungen auf Baublockebene.  

Das GIS-Modell wurde im **ArcGIS Pro ModelBuilder** umgesetzt und nutzt drei Submodelle:  

1. **Fernwärme** – Entscheidung für oder gegen die Fernwärmeversorgung eines Baublocks.  
2. **Lokale Wärmenetze** – Entscheidung für oder gegen die Errichtung lokaler Wärmenetze, Auswahl geeigneter Temperaturniveaus und Aussagen zur Zusammensetzung der lokalen Wärmequellen.  
3. **Einzellösungen** – Definition objektbezogener Einzellösungen für alle verbleibenden Gebäude.

Die Submodelle werden nacheinander ausgeführt. Jeder Baublock der Eingangs-Feature-Class durchläuft die Entscheidungsbäume der Submodelle. Erfolgreiche Zuordnungen werden an ein Output-File angehängt. Das Modell nutzt ArcGIS-Funktionen wie `Select`, `Delete Rows`, `Copy`, `Erase`, `Merge` und `Append`.  

**Hinweis:** Die Berechnung kann aufgrund der umfangreichen Iterationen etwa 20 Minuten dauern.

---

## Eingabedaten

- Feature Class aller 746 Baublöcke des 14. Bezirks  
- Attributdaten zu energieraumplanerischen Indikatoren, u. a.:
  - Wärmebedarfsdichten  
  - Sanierungsaufwände  
  - Sozialräumliche Voraussetzungen  
  - Schutzbestimmungen 

**Achtung:** Das Modell wurde speziell für den 14. Bezirk entwickelt. Für andere Bezirke oder Städte müssen Schwellenwerte und lokale Gegebenheiten angepasst werden.

---

## Installation und Nutzung

1. **Software:** ArcGIS Pro (Version 3.2.2 oder höher)  
2. **Dateien:**  
   - `Energieraumplan2_0.atbx` – Geoverarbeitungs-Toolbox, die das Hauptmodell und alle Submodelle enthält
3. **Öffnen in ArcGIS Pro:**  
   - Toolbox im Catalog Pane hinzufügen  
   - Submodelle können direkt über das Hauptmodell-Interface ausgeführt werden, nachdem die für den jeweiligen Raum erforderlichen Eingangsdaten hinzugefügt wurden
4. **Ausgabe:** Feature Class mit den Baublöcken und den zugewiesenen Transformationstypen (0–10)  

---

## Lizenz

Dieses Modell wird unter der **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)** Lizenz bereitgestellt.  

**Bedingungen:**  
- Namensnennung: Bitte geben Sie als Urheber:in „Martin Aufhauser“ an.  
- Weitergabe unter gleichen Bedingungen: Änderungen oder Weiterentwicklungen müssen ebenfalls unter CC BY-SA 4.0 geteilt werden.  
- Lizenzdetails: [https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/)

---

## Zitation

Wenn Sie dieses Modell in wissenschaftlichen Arbeiten oder Projekten nutzen, zitieren Sie bitte:

**Aufhauser, Martin (2025): Energieraumpläne 2.0. Entwurf einer integrativen räumlichen Energieplanung für Bestandsquartiere in Wien, Diplomarbeit, Technische Universität Wien.**

