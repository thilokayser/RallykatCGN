# RallykatCGN
Racing for Everyone


Hier ist eine strukturierte README.md Datei, die genau auf den Funktionen der Version 26 (Complete Edition) basiert. Du kannst diesen Text direkt als Dokumentation für dein Projekt nutzen.
🏆 Bike Battle - Elite Race Director (V26)

Der **Bike Battle Race Director** ist ein professionelles, browserbasiertes Tool zur Verwaltung von K.O.-Turnieren (Brackets). Es wurde speziell für Renn-Events entwickelt und bietet ein einzigartiges **Dual-Bracket-System** mit integrierter "Redemption"-Mechanik, Liga-Ranking und Wildcard-Verwaltung.

## ✨ Hauptfunktionen

* **Dual Bracket System:**
* **Gold Bracket (Championship):** Das Hauptturnier.
* **Red Bracket (Redemption):** Eine automatische "Trost-Runde" für Verlierer der ersten Runde.


* **Live Liga-Ranking:** Automatische Punkteberechnung über mehrere Events hinweg.
* **Wildcard Management:** Flexible Zuweisung von Fahrern in leere Slots oder als Ersatz.
* **DNF-Logik:** Markiere Fahrer als "Did Not Finish" (Ausfall/Sturz).
* **Fehlertoleranz:** Integrierte "Undo/Reset"-Funktion für jedes Match.
* **Persistenz:** Automatische Speicherung im Browser (LocalStorage) + Backup-Export (JSON).
* **Dark Mode UI:** Hochwertiges "Glassmorphism"-Design, optimiert für gut lesbare Darstellung auf Monitoren.

---

## 🚀 Schnellstart Anleitung

### 1. Event erstellen

* Gib oben links einen Namen für das Event ein (z.B. "Race #1").
* Klicke auf **NEW TAB**, um ein neues Reiter für das Event zu erstellen.

### 2. Fahrer importieren

* Kopiere deine Fahrerliste (ein Name pro Zeile) in das Textfeld oben.
* Klicke auf **🎲 RANDOMIZE**.
* *Hinweis:* Das System erstellt automatisch die passende Bracket-Größe (4, 8, 16, 32...).

### 3. Das Rennen steuern

Jedes Match-Feld bietet folgende Kontrollen:

* **➔ (Pfeil):** Der Fahrer gewinnt und rückt eine Runde weiter.
* **DNF (Button):** Der Fahrer ist ausgefallen. Er wird durchgestrichen, der Gegner gewinnt automatisch.
* **Name (Doppelklick):** Korrigiere Schreibfehler direkt im Bracket.

### 4. Reset & Korrektur (Undo)

Ein Fehler ist passiert?

* Sobald ein Match entschieden ist, erscheint oben rechts in der Box ein kleiner **↺ (Reset)** Button.
* Klicke darauf, um das Ergebnis zu löschen. Der fälschlicherweise weitergekommene Fahrer wird aus der nächsten Runde entfernt.

---

## ⚙️ Die Spiel-Logik (Ruleset)

### Der "Redemption Drop"

Das System nutzt eine faire "Double Chance" Mechanik:

1. Verliert ein Fahrer im Hauptrennen (Gold) direkt in **Runde 0** (der ersten Runde), scheidet er nicht aus.
2. Er wird **automatisch** in das untere **Redemption Bracket (Rot)** verschoben.
3. Dort kämpft er um den Titel des "Redemption King" (Platz 3 der Gesamtwertung).

*Hinweis:* Verlierer ab Runde 1 (Viertelfinale/Halbfinale) droppen nicht mehr nach unten.

### Das Podium 🏆

Am Ende des Events (wenn Hauptsieger und Redemption-Sieger feststehen) erscheint der Button **"PODIUM ANZEIGEN"**.

* **Platz 1:** Gewinner des Gold Brackets.
* **Platz 2:** Verlierer des Gold Finales.
* **Platz 3:** Gewinner des Red Brackets.

### Punkteverteilung (Liga)

Die Sidebar berechnet die Saison-Punkte automatisch:

* **25 Punkte:** Sieg im Hauptrennen.
* **18 Punkte:** Finalist im Hauptrennen (Platz 2).
* **10 Punkte:** Sieg im Redemption Bracket.
* **1 Punkt:** Teilnahme (jeder Fahrer).

---

## 🃏 Wildcards & Manuelle Eingriffe

In der Sidebar befindet sich der **Wildcard Pool**.

1. Dort werden alle Fahrer gelistet, die sich im Redemption-Bracket befinden (oder manuell hinzugefügt wurden).
2. **Verwendung:**
* Klicke auf einen Namen in der Liste (der Name wird gespeichert).
* Klicke nun auf einen beliebigen Slot im Bracket (z.B. ein leeres Feld oder einen Platzhalter).
* Der Fahrer wird dort eingesetzt.
* *Wichtig:* Dies funktioniert nur, wenn das Match noch nicht entschieden ist.



---

## 💾 Speichern & Laden

* **Auto-Save:** Das Tool speichert jede Änderung sofort im Browser (`localStorage`). Beim Neuladen der Seite ist alles noch da.
* **SAVE (Backup):** Lädt eine `.json` Datei herunter. Ideal, um den Stand auf einen anderen PC zu übertragen oder zu sichern.
* **LOAD:** Importiert eine zuvor gespeicherte JSON-Datei.
* **RESET:** Löscht **alle** Daten und setzt die Saison zurück (Vorsicht!).

---

## ⌨️ Tipps & Tricks

    Sidebar ausblenden: Klicke auf das ☰ Symbol oben links, um mehr Platz für das Bracket zu haben.

    Hilfe: Der ? Button oben rechts öffnet die Kurzanleitung im Overlay.

    BYE (Freilos): Wenn du eine ungerade Zahl an Fahrern hast, füllt das System automatisch mit "BYE" auf. Der Gegner kommt automatisch eine Runde weiter.