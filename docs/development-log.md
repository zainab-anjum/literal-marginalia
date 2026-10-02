# Development Log

## Day 1: Initial Prototype

### Goal
> Create a reading-first PDF annotation application that supports expressive marginalia rather than conventional ebook notes.

---

### Initial Requirements
The first build focused on proving the core workflow rather than polishing interaction design:

* PDF rendering
* Highlights
* Text notes
* Speech bubbles
* Stickers
* Basic doodles
* Local persistence

---

### Result
A functional prototype was generated.

---

### Testing Notes
Testing the prototype against real-world reading workflows surfaced several UX and architectural issues:

* **Sidebar Pinning:** Sidebar scrolled away with the document instead of remaining fixed.
* **Text Scaling:** Text resizing behaved inconsistently across viewports.
* **Bubble Styling:** Speech bubbles lacked proper fill transparency.
* **Highlight Semantics:** Highlights behaved like detached, movable rectangles rather than anchored text marks.
* **Asset Mapping:** Doodle selection occasionally produced incorrect visual output.
* **Tool Separation:** Freehand drawing shared behavioral logic with highlighting instead of acting as an independent stroke tool.
* **Asset Scope:** Uploaded stickers were scoped to the active document rather than persisting globally to the user's library.

---

### Next Iteration
Focus on interaction quality and core annotation architecture before expanding the feature scope.
