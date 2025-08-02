# Simon Game

A simple web-based memory game inspired by the classic **Simon Game**. Test your memory by repeating increasingly complex sequences of button presses!

## Table of Contents

* [How to Play](#how-to-play)
* [Folder Structure](#folder-structure)
* [Technologies Used](#technologies-used)
* [How It Works](#how-it-works)
* [Setup Instructions](#setup-instructions)
* [Future Improvements](#future-improvements)

---

## How to Play

1. Open the game in a browser.
2. Press any key to start.
3. Watch the sequence of colors flashing.
4. Click the buttons in the same order as shown.
5. With every correct sequence, the game adds a new color to the pattern.
6. If you click a wrong button, the game ends and you can restart by pressing any key again.


---

## Tech Stack

* HTML5
* CSS3
* JavaScript (mostly jQuery)

---

## How It Works

### Game Flow:

1. **Game Start**: User presses a key → `nextSequence()` is triggered → level 0 begins.
2. **Sequence Generation**: A random color is chosen and added to `gamePattern`. The button flashes and plays a sound.
3. **User Input**: User clicks on buttons which are stored in `userClickedPattern`.
4. **Answer Checking**: After each click, the game compares `userClickedPattern` with `gamePattern` using `checkAnswer()`.
5. **Level Up / Game Over**:

   * If correct, and sequence is complete → advance to next level after a delay.
   * If wrong → play "wrong" sound, flash screen red, display "Game Over" message, and reset game.

### Key Functions in `game.js`:

* `nextSequence()`: Generates the next color in the sequence.
* `checkAnswer(currentLevel)`: Verifies if the user's current input matches the sequence.
* `playSound(name)`: Plays sound corresponding to the color.
* `animatePress(currentColor)`: Briefly animates button press.
* `startOver()`: Resets the game after a wrong input.

### Visuals & Styling:

* CSS is used to create the colored buttons and layout.
* Animations for button presses and game over effects are handled with CSS classes (`.pressed`, `.game-over`).

---

## Setup Instructions

1. Clone or download this repository.
2. Open `index.html` in a browser to play.

---

## Future Improvements

* Add **high score tracking**.
* Add **difficulty modes** (faster sequences).
* Add **mobile touch optimizations**.
* Add **visual feedback** for level progression.
* Add **background music**.
* Add **multiplayer mode**.

---

## Credits

Built as a practice project to learn **DOM Manipulation** and **Event Handling** using jQuery.

---
