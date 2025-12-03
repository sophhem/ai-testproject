# Changelog für test1–test4

## test1.html / test1.css
- Erste Version der Folien als 3×2-Matrix.
- Umsetzung **ohne JavaScript**, Navigation über `radio`-Buttons und `label`.
- Jede Folie:
  - Zeigt „Folie 1–6“ als Titel.
  - Enthält eine Liste mit 5 Punkten.
  - Hat eine eigene Hintergrundfarbe.
- Navigation über Pfeil-Buttons **direkt in jeder Folie** (oben/unten/links/rechts) entsprechend der Matrix:
  - Zeile 1: Folie 1–3
  - Zeile 2: Folie 4–6
- Immer nur **eine** Folie sichtbar, komplett horizontal und vertikal zentriert.

## test2.html
- Datei existiert im Projekt, wurde aber in diesem Verlauf **nicht von mir angepasst**.
- Kein definierter Changelog-Eintrag, da Inhalt unbekannt.

## test3.html / test3.css
- Verfeinerte Version von test1, weiterhin **ohne JavaScript**.
- Logik wie in test1 (3×2-Matrix, 6 Folien, eigene Farben, 5 Punkte), aber:
  - Navigation wurde in eine **globale Steuerung unten auf der Seite** verschoben.
  - Es gibt nur noch **einen Satz Pfeil-Buttons** (↑, ↓, ←, →).
  - Über CSS wird je nach aktueller Folie genau der passende Button eingeblendet:
    - z.B. von Folie 1 nur → und ↓, von Folie 6 nur ← und ↑.
- Dadurch ist der Code in den Folien selbst schlanker, die Navigationslogik liegt überwiegend in der CSS-Datei.

## test4.html / test4.css
- Alternative, deutlich **einfachere und elegantere** Navigation mit CSS `scroll-snap`.
- Keine `radio`-Buttons oder `label`-Navigation mehr.
- Jede Folie:
  - Füllt den gesamten Viewport (`100vh` × `100vw`).
  - Ist zentriert und hat ihre eigene Hintergrundfarbe.
  - Enthält wieder Titel „Folie 1–6“ und 5 Punkte.
- Die Folien liegen untereinander in einem scrollbaren Container:
  - Mit Maus, Touchpad oder Touch-Geste wird gescrollt.
  - `scroll-snap-type: y mandatory` sorgt dafür, dass der Browser auf jeder Folie „einrastet“.
- Oben gibt es einen kleinen Hinweistext zur Bedienung.


