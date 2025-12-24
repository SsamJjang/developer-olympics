# The 10x Developer Olympics

> **Optimize your workflow. Destroy your keyboard.**

A suite of high-intensity browser games designed to test the *real* skills of a senior software engineer: copy-pasting, exiting Vim, and sudo-forcing commands. Built entirely with **Vanilla HTML, CSS, and JavaScript** (No Canvas, No Frameworks).

![Project Status](https://img.shields.io/badge/status-stable-green) ![Tech](https://img.shields.io/badge/tech-HTML%2FCSS%2FJS-blue) ![Vim](https://img.shields.io/badge/vim-%3Aq!-red)

## Features

* **Zero Dependencies:** Runs in a single `.html` file. No build steps, no `npm install`.
* **5 Distinct Game Modes:** Tailored to different programming muscle memories.
* **Global Ranking System:** 20 unique ranks ranging from *"Time Traveler"* to *"404 Not Found"*.
* **Retro Hacker Aesthetic:** CRT scanlines, neon terminal colors, and screen shake effects.
* **Accessibility:** Smart focus management ensures keyboard inputs are always captured.

---

## How to Run

1.  **Download:** Download the `index.html` file to your computer.
2.  **Open:** Double-click the file to open it in any modern web browser (Chrome, Firefox, Edge, Brave).
3.  **Initialize:** Click the **"CLICK TO INITIALIZE"** overlay to grant the browser focus permissions.
4.  **Play:** Select a game from the menu using your mouse.

---

## Game Modes

### 1. Copy/Paste Chaos
*The ultimate test of a developer's most used skill.*
* **Objective:** Wait for the background to turn **GREEN**, then paste.
* **Controls:**
    * `Ctrl` + `C` (Spam continuously during RED phase)
    * `Ctrl` + `V` (Press ONCE during GREEN phase)
* **Scoring:** Measured in milliseconds (Reaction Time).

### 2. The "Bug Fix" Combo
*Simulates the panic of fixing a production bug.*
* **Objective:** Execute the sequence of keyboard shortcuts shown on screen.
* **Controls:** `Ctrl` + `[Key Shown]`
* **Scoring:** Total time to complete the sequence.

### 3. Vim Command Drill
*Simon Says, but for people who can't exit their editor.*
* **Objective:** The screen shouts a command (e.g., "SAVE & QUIT"). Type the corresponding Vim keys instantly.
* **Controls:** Standard Vim bindings:
    * Save & Quit -> `:wq`
    * Force Quit -> `:q!`
    * Delete Line -> `dd`
    * Go to Top -> `gg`
    * Undo -> `u`
* **Scoring:** Total time to complete 5 tasks.

### 4. Sudo Suicide
*High-stakes terminal typing.*
* **Objective:** Type a dangerous Linux command (e.g., `sudo rm -rf /`) perfectly character-by-character.
* **Mechanic:** One typo resets the entire line.
* **Scoring:** Typing speed.

### 5. Binary Binge
*Clear the buffer.*
* **Objective:** A stream of 20 random bits (0s and 1s) appears. Clear them in order.
* **Controls:** `0` and `1`.
* **Scoring:** Completion time.

---

## 🏅 Ranking System

The game evaluates your performance and assigns a title. Do you have what it takes to be a **Time Traveler**?

| Rank Title | Copy/Paste Criteria (Reaction) |
| :--- | :--- |
| **Time Traveler ⏳** | < 10ms |
| **Script Kiddie Bot 🤖** | < 50ms |
| **Vim God ⚡** | < 100ms |
| **10x Developer 🚀** | < 130ms |
| **Senior Architect 🏗️** | < 160ms |
| **Senior Developer 👴** | < 220ms |
| **Intern 🎓** | < 400ms |
| **Excel User 📊** | < 600ms |
| **Grandma Jo 👵** | < 3000ms |
| **AFK? 💤** | > 10000ms |

*(Note: Each game mode has its own scaled criteria for these ranks)*

---

## Technical Details

This project demonstrates advanced DOM manipulation without the use of the HTML5 `<canvas>` element.

* **Focus Management:** Uses a "Focus Shield" overlay and forced `focus()` events (with timeouts) on game reset to ensure keystrokes are always captured, solving common browser "blur" issues.
* **CSS Animations:** Uses `@keyframes` for the CRT pulse effect and screen shake feedback on errors.
* **Event Listeners:** A centralized input controller handles keystrokes differently depending on the `currentGame` state variable.
* **Anti-Cheat:** Browser default actions (like saving the page on `Ctrl+S`) are prevented (`e.preventDefault()`) only during active gameplay to ensure immersion.


## License

Open Source. Use it to train your team, but don't blame us if they actually run `sudo rm -rf /` on production.