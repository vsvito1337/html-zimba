# Projekt-Struktur: "Der König der Löwen" Website

## Übersicht

Dieses Projekt ist eine Website über "Der König der Löwen" mit verschiedenen Charakterseiten. Das Projekt ist in zwei Branches organisiert:

- `main`: Enthält die Basis-HTML-Version ohne CSS-Styling
- `with-css`: Enthält die erweiterte Version mit CSS-Styling (aktueller Branch)

## Dateien und Status

### Hauptdateien

| Datei | Beschreibung | CSS-Status |
|-------|-------------|------------|
| `index.html` | Startseite mit Links zu allen Charakteren | ✅ Fertig mit CSS |
| `simba.html` | Detailseite für Simba | ✅ Fertig mit CSS |
| `mufasa.html` | Detailseite für Mufasa | ❌ Noch ohne CSS |
| `sarabi.html` | Detailseite für Sarabi | ❌ Noch ohne CSS |
| `scar.html` | Detailseite für Scar | ❌ Noch ohne CSS |
| `styles.css` | CSS-Datei mit allen Stilen | ✅ Fertig |
| `css-tutorial.md` | Schritt-für-Schritt Anleitung für CSS | ✅ Fertig |

### Zusätzliche Dateien

- `mufasa_struktur.html` und `mufasa_ziel.html`: Beispieldateien für die Struktur und das Ziel der Mufasa-Seite
- `img/`: Ordner mit allen Bildern für die Website

## Was ist bereits fertig?

1. **Startseite (index.html)**:
   - CSS-Styling vollständig implementiert
   - Responsive Grid-Layout für Charakterkarten
   - Stilvoller Footer

2. **Simba-Seite (simba.html)**:
   - Vollständiges CSS-Styling
   - Navigationsleiste
   - Strukturierte Abschnitte mit Überschriften
   - Responsive Bildergalerie
   - Formatierte Tabelle für Eigenschaften
   - Video-Container für YouTube-Einbettung
   - Footer mit Links

3. **CSS-Datei (styles.css)**:
   - Globale Stile (Schriftart, Farben, Abstände)
   - Komponenten-Stile (Navigationsleiste, Charakterkarten, Tabellen)
   - Responsive Layouts
   - Interaktive Elemente (Hover-Effekte)

4. **CSS-Tutorial**:
   - Schritt-für-Schritt Anleitung zur Implementierung von CSS
   - Beispiele für die Umwandlung von HTML zu CSS-gestyled HTML

## Was muss noch gemacht werden?

Die folgenden Seiten müssen noch mit CSS aktualisiert werden:

1. **Mufasa-Seite (mufasa.html)**
2. **Sarabi-Seite (sarabi.html)**
3. **Scar-Seite (scar.html)**

## Wie fange ich an?

### Schritt 1: CSS-Datei einbinden

Füge in jede HTML-Datei im `<head>`-Bereich den Link zur CSS-Datei ein:

```html
<link rel="stylesheet" href="styles.css">
```

### Schritt 2: HTML-Struktur anpassen

Folge dem Muster der Simba-Seite, um die HTML-Struktur anzupassen:

1. Füge das Logo mit der Klasse `logo` hinzu
2. Erstelle eine Navigationsleiste mit der Klasse `navigation`
3. Gruppiere den Hauptinhalt in `<div>`-Elemente mit passenden Klassen
4. Verwende `section`-Klassen für die verschiedenen Abschnitte
5. Füge einen einheitlichen Footer hinzu

### Schritt 3: Klassen zuweisen

Weise den HTML-Elementen die entsprechenden Klassen zu:

- Bilder: `class="character-img"`
- Überschriften: `class="character-name"` oder `class="section-title"`
- Abschnitte: `class="section"`
- Beschreibungen: `class="character-description"`

### Beispiel: Mufasa-Seite aktualisieren

Beginne mit der Mufasa-Seite, indem du die folgenden Änderungen vornimmst:

1. CSS-Datei einbinden
2. Logo mit Klasse versehen
3. Navigationsleiste erstellen
4. Inhalte in Abschnitte gruppieren
5. Tabelle formatieren
6. Video-Container hinzufügen
7. Footer aktualisieren

Folge dem `css-tutorial.md` für detaillierte Anweisungen und Beispiele.

## Tipps

- Verwende die Simba-Seite als Referenz für die Struktur und Klassen
- Teste regelmäßig im Browser, um die Änderungen zu sehen
- Achte auf einheitliche Formatierung auf allen Seiten
- Nutze die vorhandenen CSS-Klassen in `styles.css`, anstatt neue zu erstellen

Viel Erfolg beim Gestalten der Website!
