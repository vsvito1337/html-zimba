# CSS-Tutorial: Schritt für Schritt Anleitung

Diese Anleitung zeigt dir, wie du HTML-Elemente mit CSS gestalten kannst. Wir werden lernen, wie man:
1. Eine CSS-Datei einbindet
2. Inhalte mit `<div>` gruppiert
3. Klassen zuweist und verwendet

## 1. CSS-Datei einbinden

Um eine CSS-Datei in dein HTML-Dokument einzubinden, musst du einen `<link>`-Tag im `<head>`-Bereich deiner HTML-Datei einfügen.

**Vorher (ohne CSS):**
```html
<head>
   <title>Der König der Löwen</title>
   <meta charset="utf-8">
   <link rel="icon" type="image/x-icon" href="favicon.ico" />
</head>
```

**Nachher (mit CSS):**
```html
<head>
   <title>Der König der Löwen</title>
   <meta charset="utf-8">
   <link rel="icon" type="image/x-icon" href="favicon.ico" />
   <link rel="stylesheet" href="styles.css">
</head>
```

Der `<link>`-Tag hat zwei wichtige Attribute:
- `rel="stylesheet"` - Gibt an, dass es sich um ein Stylesheet handelt
- `href="styles.css"` - Gibt den Pfad zur CSS-Datei an

## 2. Inhalte mit `<div>` gruppieren

Ein `<div>`-Element ist ein Container, der andere Elemente gruppiert. Dies hilft dir, Bereiche deiner Webseite zu organisieren und zu gestalten.

**Vorher (ohne `<div>`):**
```html
<p>Simba</p>
<p><a href="#family">Familie</a></p>
<p><a href="#feature">Eigenschaften</a></p>
<p><a href="#video">Video</a></p>
```

**Nachher (mit `<div>`):**
```html
<div class="navigation">
   <a href="#family">Familie</a>
   <a href="#feature">Eigenschaften</a>
   <a href="#video">Video</a>
   <a href="index.html">Zurück zur Startseite</a>
</div>
```

Beachte, wie wir:
1. Alle verwandten Elemente in einem `<div>` gruppiert haben
2. Dem `<div>` eine Klasse "navigation" zugewiesen haben
3. Die einzelnen `<p>`-Tags entfernt haben, da wir sie in der CSS-Datei anders gestalten werden

## 3. Klassen zuweisen und verwenden

Klassen sind wie Etiketten, die du HTML-Elementen zuweisen kannst, um sie in CSS anzusprechen.

### Klassen zuweisen

**Vorher (ohne Klasse):**
```html
<img src="img/simba.png"/>
```

**Nachher (mit Klasse):**
```html
<img src="img/simba.png" class="character-img" alt="Simba"/>
```

Wir haben:
1. Das Attribut `class="character-img"` hinzugefügt
2. Auch ein `alt`-Attribut für bessere Barrierefreiheit hinzugefügt

### Mehrere Elemente mit Klassen gestalten

**Vorher (ohne Klassen):**
```html
<table>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td></td>
      <td>
         <a href="simba.html"><img align="center" src="img/simba.png" width="150" /></a>
         <p align="center"><a href="simba.html">Simba</a></p>
      </td>
      <td></td>
   </tr>
   <!-- weitere Tabellenzeilen -->
</table>
```

**Nachher (mit Klassen und `<div>`):**
```html
<div class="character-grid">
   <div class="character-card">
      <a href="simba.html"><img class="character-img" src="img/simba.png" alt="Simba" /></a>
      <p><a href="simba.html">Simba</a></p>
   </div>
   
   <div class="character-card">
      <a href="mufasa.html"><img class="character-img" src="img/mufasa.jpg" alt="Mufasa" /></a>
      <p><a href="mufasa.html">Mufasa</a></p>
   </div>
   
   <!-- weitere Charakterkarten -->
</div>
```

Hier haben wir:
1. Die Tabelle durch ein flexibles Grid-Layout ersetzt
2. Jedem Charakter eine eigene "Karte" mit der Klasse `character-card` gegeben
3. Allen Bildern die Klasse `character-img` zugewiesen

## 4. CSS-Regeln schreiben

In deiner `styles.css` Datei kannst du nun Regeln für deine Klassen definieren:

```css
/* Character grid */
.character-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin: 20px 0;
}

.character-card {
    text-align: center;
    padding: 15px;
    background-color: white;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Character images */
.character-img {
    max-width: 100%;
    height: auto;
    border: 3px solid #b8860b;
    border-radius: 10px;
    margin: 10px 0;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    transition: transform 0.3s ease;
}

.character-img:hover {
    transform: scale(1.03);
}

/* Navigation */
.navigation {
    background-color: #b8860b;
    padding: 10px;
    margin-bottom: 20px;
    border-radius: 5px;
}

.navigation a {
    color: white;
    text-decoration: none;
    margin-right: 15px;
    font-weight: bold;
}
```

## 5. Praktisches Beispiel: Einen Abschnitt gestalten

Hier ist ein vollständiges Beispiel, wie du einen Abschnitt deiner Webseite gestalten kannst:

**HTML (vorher):**
```html
<a name="family"></a>
<p>Familie</p>
<p><a href="mufasa.html"> Mufasa</a> (Vater)</p>
<p><a href="sarabi.html">Sarabi</a> (Mutter)</p>
<p><a href="scar.html">Scar</a> (Onkel)</p>
```

**HTML (nachher):**
```html
<div class="section" id="family">
   <h2 class="section-title">Familie</h2>
   <p><a href="mufasa.html">Mufasa</a> (Vater)</p>
   <p><a href="sarabi.html">Sarabi</a> (Mutter)</p>
   <p><a href="scar.html">Scar</a> (Onkel)</p>
</div>
```

**CSS:**
```css
/* Sections */
.section {
    margin: 30px 0;
    padding: 20px;
    background-color: white;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.section-title {
    color: #b8860b;
    border-bottom: 2px solid #b8860b;
    padding-bottom: 10px;
    margin-bottom: 20px;
}
```

Beachte die Änderungen:
1. Wir haben `<a name="family"></a>` durch `id="family"` im `<div>` ersetzt
2. Wir haben den einfachen Text "Familie" durch eine Überschrift `<h2>` ersetzt
3. Wir haben dem Abschnitt die Klasse `section` und der Überschrift die Klasse `section-title` gegeben

## 6. Übung

Versuche nun selbst, einen anderen Teil der Webseite zu gestalten:
1. Finde einen Bereich in einer der HTML-Dateien
2. Gruppiere verwandte Elemente mit `<div>`
3. Weise passende Klassen zu
4. Definiere CSS-Regeln für diese Klassen in der `styles.css` Datei
5. Öffne die Seite im Browser und bewundere deine Änderungen!

Viel Spaß beim Gestalten deiner Webseite!
