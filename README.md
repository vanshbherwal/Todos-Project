# To-Do List (Vanilla JS) — CRUD + Local Storage

A lightweight to-do list web app built with **HTML, CSS, and JavaScript** (no frameworks). Users can **create, view, edit, and delete** to-dos, and the list persists across refreshes using **browser localStorage**.

## Live Demo
- (Add a link here once you deploy with GitHub Pages)

## Features
- ✅ **Create** a to-do
- ✅ **Read / Display** all to-dos on the page
- ✅ **Update / Edit** an existing to-do (loads the selected to-do back into the textarea)
- ✅ **Delete** a to-do
- ✅ **Persistence**: to-dos are saved to `localStorage` and restored on page reload
- ✅ Clean, responsive layout with Flexbox and icon buttons (Font Awesome)

## What I learned / skills demonstrated
### Frontend fundamentals
- **HTML structure & semantics**: forms, sections, headings, and containers
- **CSS styling**:
  - Flexbox layouts (`display: flex`, `flex-direction`, `gap`)
  - reusable class-based styling (e.g., `.todo`, `.btnContainer`, `.iconBtn`)
  - hover states and UI polish
- **JavaScript DOM manipulation**:
  - selecting elements (`querySelector`, `getElementById`)
  - updating the DOM dynamically by rebuilding the list (`innerHTML`)
  - handling user events (`addEventListener`)

### CRUD logic (core app behavior)
- **Create**: add a new to-do to an in-memory array
- **Read**: render the array into UI cards
- **Update**: load a selected to-do back into the textarea and replace it
- **Delete**: remove a selected to-do by index

### Data persistence
- Saving and restoring state via **localStorage**
  - `localStorage.setItem(...)`
  - `localStorage.getItem(...)`
  - storing arrays using `JSON.stringify(...)` and restoring with `JSON.parse(...)`

## How it works (high-level)
- The app keeps to-dos in an array: `todoList`
- After every change (add/edit/delete), `updateUI()`:
  1. rebuilds the to-do HTML
  2. injects it into `.todoContainer`
  3. saves the updated list to localStorage
- On page load, `initialLoad()` restores saved to-dos from localStorage and renders them.

## Tech stack
- HTML5
- CSS3 (Flexbox)
- JavaScript (ES6+)
- Font Awesome (icons)
- Google Fonts
## Run locally
No build tools needed.

1. Download/clone the repo
2. Open `index.html` in your browser **or** use VS Code Live Server
3. Add to-dos — refresh the page to confirm persistence

## Notes / next improvements
If I continue this project, I’d like to:
- Add “completed” status and filtering (active/completed)
- Improve edit UX (edit-in-place or a modal, instead of removing then re-adding)
- Replace inline `onclick` handlers with event delegation (cleaner separation of concerns)
- Add basic tests for the CRUD functions

## Screenshots
- (Optional: add a screenshot of your UI here)

---
**Author:** Vansh Bherwal 
**Contact:** vanshbherwal@gmail.com
