# RallykatCGN
## Racing for Everyone
---

# 🏆 Bike Battle - Elite Race Director (V26)

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

* **Sidebar ausblenden:** Klicke auf das **☰** Symbol oben links, um mehr Platz für das Bracket zu haben.
* **Hilfe:** Der **?** Button oben rechts öffnet die Kurzanleitung im Overlay.
* **BYE (Freilos):** Wenn du eine ungerade Zahl an Fahrern hast, füllt das System automatisch mit "BYE" auf. Der Gegner kommt automatisch eine Runde weiter.

---

# English 
# RallykatCGN
## Racing for Everyone
---

# 🏆 Bike Battle - Elite Race Director (V26)

The **Bike Battle Race Director** is a professional, browser-based tool for managing knockout tournaments (brackets). It was developed specifically for racing events and offers a unique **dual bracket system** with integrated redemption mechanics, league rankings, and wildcard management.

## ✨ Main Features

* **Dual Bracket System:**
* **Gold Bracket (Championship):** The main tournament.
* **Red Bracket (Redemption):** An automatic “consolation round” for first-round losers.


<<<<<<< HEAD
* **Live League Ranking:** Automatic points calculation across multiple events.
* **Wildcard Management:** Flexible assignment of drivers to empty slots or as substitutes.
* **DNF Logic:** Mark drivers as “Did Not Finish” (retirement/crash).
* **Error Tolerance:** Integrated “Undo/Reset” function for each match.
* **Persistence:** Automatic saving in the browser (LocalStorage) + backup export (JSON).
* **Dark Mode UI:** High-quality “glassmorphism” design, optimized for easy reading on monitors.

---

## 🚀 Quick Start Guide

### 1. Create an event

* Enter a name for the event in the top left corner (e.g., “Race #1”).
* Click **NEW TAB** to create a new tab for the event.

### 2. Import drivers

* Copy your driver list (one name per line) into the text field above.
* Click **🎲 RANDOMIZE**.
* *Note:* The system automatically creates the appropriate bracket size (4, 8, 16, 32...).

### 3. Control the race

Each match field offers the following controls:

* **➔ (Arrow):** The driver wins and advances to the next round.
* **DNF (button):** The driver has retired. They are crossed out and their opponent automatically wins.
* **Name (double-click):** Correct spelling mistakes directly in the bracket.

### 4. Reset & correction (Undo)

Made a mistake?

* Once a match has been decided, a small **↺ (Reset)** button appears in the top right corner of the box.
* Click on it to delete the result. The driver who advanced incorrectly is removed from the next round.

---

## ⚙️ The game logic (ruleset)

### The “Redemption Drop”

The system uses a fair “double chance” mechanism:

1. If a driver loses in the main race (gold) directly in **round 0** (the first round), they are not eliminated.
2. They are **automatically** moved to the lower **Redemption Bracket (red)**.
3. There, they compete for the title of “Redemption King” (3rd place in the overall standings).

*Note:* Losers from round 1 (quarterfinals/semifinals) onwards no longer drop down.

### The Podium 🏆

At the end of the event (when the main winner and redemption winner have been determined), the **“SHOW PODIUM”** button appears.

* **1st place:** Winner of the Gold Bracket.
* **2nd place:** Loser of the Gold Final.
* **3rd place:** Winner of the Red Bracket.

### Points distribution (league)

The sidebar automatically calculates the season points:

* **25 points:** Victory in the main race.
* **18 points:** Finalist in the main race (2nd place).
* **10 points:** Victory in the Redemption Bracket.
* **1 point:** Participation (each driver).

---

## 🃏 Wildcards & Manual Interventions

The **Wildcard Pool** is located in the sidebar.

1. All drivers who are in the Redemption Bracket (or have been added manually) are listed there.
2. **Usage:**
* Click on a name in the list (the name will be saved).
* Now click on any slot in the bracket (e.g., an empty field or a placeholder).
* The driver will be placed there.
* *Important:* This only works if the match has not yet been decided.



---

## 💾 Save & Load

* **Auto-Save:** The tool saves every change immediately in the browser (`localStorage`). When you reload the page, everything is still there.
* **SAVE (Backup):** Downloads a `.json` file. Ideal for transferring or backing up the status to another PC.
* **LOAD:** Imports a previously saved JSON file.
* **RESET:** Deletes **all** data and resets the season (caution!).

---

## ⌨️ Tips & Tricks

* **Hide sidebar:** Click on the **☰** icon in the top left corner to make more room for the bracket.
* **Help:** The **?** button in the top right corner opens the quick guide in an overlay.
* **BYE (bye):** If you have an odd number of drivers, the system automatically fills in with “BYE.” The opponent automatically advances to the next round.

=======
    BYE (Freilos): Wenn du eine ungerade Zahl an Fahrern hast, füllt das System automatisch mit "BYE" auf. Der Gegner kommt automatisch eine Runde weiter.
>>>>>>> 34497b0f2def3fe08e3d337a21c075f7e41a4841
