# JavaScript Virtual Drum Kit  
An interactive soundboard that plays custom drum samples when the user presses keys or taps the on‑screen buttons. Built using **HTML**, **CSS**, and **JavaScript**, this project demonstrates DOM event handling, audio playback, UI state changes, and responsive design.

---

## Features
- Keyboard‑triggered sound playback (`keydown`)
- Click‑triggered sound playback (mobile‑friendly)
- Rapid‑fire audio (sound restarts instantly)
- Visual feedback using a `.playing` CSS class
- Fully responsive layout for mobile screens
- Organized asset folder for sound files

---

## Project Structure
project-folder/
│
├── index.html
├── styles.css
├── script.js
│
└── assets/
    └── sounds/
        ├── reality-drums.mp3
        ├── atmospheric-drums.mp3
        ├── beat-of-time-drums.mp3
        └── pop-drums.mp3

All sound files are stored in **assets/sounds/** and mapped using `data-key` attributes.

---

## HTML Summary
The HTML file establishes the structure of the soundboard.

Key elements include:

- A <main> container that centers the title and soundboard
- A list containing each drum key
- Each key uses a data-key attribute to link UI elements to audio files
- <audio> elements that match the same data-key values
- External links to styles.css and script.js

Example structure:

html
<li data-key="r" class="key">
    <kbd>R</kbd>
    <span class="sound">REALITY DRUMS</span>
</li>

This pattern is repeated for each sound.

## CSS Summary
The CSS file defines the visual layout and interactive states.

Key concepts:

- CSS variables for theme colors
- Flexbox layout for centering
- Styling for each .key element
- A .playing class that scales and highlights the active key
- A mobile‑responsive media query for smaller screens

Example of the active state:

css
.playing {
  transform: scale(1.1);
  border-color: var(--glow-color);
  box-shadow: 0 0 1.5rem var(--glow-color);
}

## JavaScript Summary
The JavaScript file handles all interaction logic.

Core responsibilities:

- The responsive section adjusts spacing, font sizes, and layout for mobile devices.
- Listen for keydown events
- Listen for click/tap events
- Match the pressed key to the correct <audio> element
- Reset the audio using currentTime = 0
- Play the sound immediately
- Add the .playing class for visual feedback
- Remove the class after a short delay

Example logic:

javascript
audio.currentTime = 0;
audio.play();
keyItem.classList.add('playing');

This ensures rapid‑fire playback and responsive UI behavior.

## Asset Management
All sound files are stored in:

- Code
- assets/sounds/

Best practices followed:

- Lowercase filenames
- Short, descriptive names
- Consistent mapping between data-key and audio file

Example:

html
<audio data-key="a" src="assets/sounds/reality-drums.mp3"></audio>

This keeps the project organized and prevents broken paths.

## Learning Objectives
This project reinforces:

- Attribute‑based DOM selection
- Event object usage (event.key)
- HTML5 Audio API
- CSS transitions as a state machine
- Responsive design
- Clean separation of concerns (HTML, CSS, JS, assets)

## Summary
The JavaScript Virtual Drum Kit demonstrates the full cycle of interactive web development:

- Input → Logic → Audio Output → Visual Feedback

It is a complete beginner‑friendly project that teaches essential front‑end concepts while producing a functional and engaging application.
