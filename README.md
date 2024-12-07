# 4212 Countdown Timer

Implementiere eine JavaFX-Anwendung, die einen Countdown-Timer verwaltet und die Zeit in einem eigenen Thread herunterzählt.

---

## Funktionen

1. **Zeit eingeben**  
   Der Benutzer kann die Countdown-Zeit (in Sekunden) über ein Eingabefeld festlegen.

2. **Countdown starten**  
   Beim Starten wird die Zeit in einem separaten Task heruntergezählt, ohne die GUI zu blockieren.

3. **Countdown abbrechen**  
   Der Benutzer kann den Countdown jederzeit abbrechen.

4. **Reset**  
   Setzt die Eingabe- und Anzeigefelder zurück.

---

## Klasse: `CountdownTimerController`

Diese Klasse steuert die Verbindung zwischen der GUI und der Logik.

### **GUI-Elemente**

- **TextField:** Eingabe der Zeit in Sekunden.
- **Label:** Zeigt die verbleibende Zeit an.
- **Buttons:**
    - **Start:** Startet den Countdown in einem separaten Task.
    - **Cancel:** Bricht den Countdown ab (falls er läuft).
    - **Reset:** Löscht die Eingabe und die Anzeige.

---

### **Logik**

- Nutze einen `Task`, um den Countdown zu verwalten.  
  Der `Task` läuft in einem separaten Thread.
- Binde das Label, das die verbleibende Zeit anzeigt, an die Änderungen des Tasks.

---

## GUI (Layout)

Ein einfaches Layout (z. B. `VBox` oder `GridPane`) mit:

- **Eingabe-Feld (TextField):** `secondsInput`
- **Anzeige-Label:** `countdownLabel`
- **Buttons:**
    - **Start**
    - **Cancel**
    - **Reset**

---

## Beispiel-Ablauf

1. Der Benutzer gibt **30** in das TextField ein und klickt auf **Start**.
2. Der Countdown startet, und das Label zeigt die verbleibenden Sekunden:  
   `29, 28, 27, ...`
3. Während des Countdowns kann der Benutzer **Cancel** klicken, um den Task zu stoppen.
4. Mit **Reset** wird alles auf den Ursprungszustand zurückgesetzt.
