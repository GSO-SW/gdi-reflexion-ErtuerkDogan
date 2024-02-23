# GDI+
Eine Sammlung von Tipps und Tricks zum Thema Grafikprogrammierung mit GDI+.

## Klassen / Ereignisse
### Timer
Ein Timer führt in regelmäßigen Abständen ein `Tick`-Event aus. Der [`System.Windows.Forms`.`Timer`](https://learn.microsoft.com/de-de/dotnet/api/system.windows.forms.timer?view=windowsdesktop-8.0&viewFallbackFrom=net-6.0) kann über die Toolbox auf die GUI gezogen werden. 

Anschließend können wir 
- die Zeit zwischen jedem `Tick`-Event einstellen (`+ Interval { get; set; }: int`) und
- den Timer starten (`+ Start():void`) oder
- stoppen (`+ Stop():void`) oder
- den Zustand abfragen. (`+ Enabled{ get; set; }: bool`) (Standard ist ausgeschaltet: `enabled = false`)

### Keycode
Der Keycode ist die Bezeichnung von jeder Taste auf der Tastatur. Mit dem Keycode können wir auch festellen wann eine Taste gedrückt und das programm Befehle ausführen lassen.
Beispiel:
```ruby
private void FrmFrogger_KeyDown(object sender, KeyEventArgs e)
{
  if(e.KeyCode == Keys.Up)     
    {
        Spieler.Y += 5;              
    }
}
```
Wenn Der Keycode vom Event 'e' den Keycode von der Taste mit dem code 'Up' übereinstimmt, soll die Spielerposition auf der Y Achse um 5 verschoben werden.


## Tipps und Tricks
Ergänzen Sie hier die notwendigen Code-Ausschnitte, um zu zeigen, wie man es macht. 
- Sie können [CodeBlöcke mit Syntax-Highlighting](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks#syntax-highlighting) einsetzen
- Wird es zu unübersichtlich? Sie können auch Unterordner mit Beispiel-Code anlegen und auf die entsprechenden Dateien verlinken. [Inspiration](https://github.com/gsoTH/flaskShowcase/tree/master/datenbanken).
- Die folgende Liste kann gerne ergänzt werden :)

### Bewegung animieren

### Objekte mit Tasten steuern
```ruby
if (e.KeyCode == Keys.Right)
    {
        spieler.X = spieler.X + hoeheJeBereich;
    }
```
### Verhindern, dass ein Spieler aus dem Bild läuft
```ruby
if (spieler.X > breite) 
{
    spieler.X = breite - spieler.Width;
}
```
https://github.com/GSO-SW/frogger-hasanerturk/commit/407f7d6f236036f53f1be57ebeadce6820b1d286

### Spiel pausieren

### Ihr schönstes Ergebnis





