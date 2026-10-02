# Build a Simple Web App for Annotating Books (Primarily PDF Books)

The app should be designed for personal reading and digital marginalia, **NOT** as a general-purpose note-taking app.

---

## CORE FEATURES

### 1. PDF reader
* Allow the user to upload a PDF from their device.
* Display the PDF in a readable book-like interface.
* Allow scrolling through pages.
* Keep the interface visually minimal so annotations don't interfere with reading.

### 2. Highlighting
* Allow text to be highlighted.
* Provide several highlight colors.
* Highlights should remain attached to the correct location in the PDF.

### 3. Text annotations
* Allow the user to add small text boxes anywhere on a page.
* Allow text to be moved, resized and rotated freely.
* Include several handwriting-style fonts.
* Text must be rotatable to arbitrary angles, including diagonal placement.
* Allow small reaction text such as "FAAA", "bruh", "EW", "CRINGE", etc.

### 4. Image stickers
* Allow the user to upload an image from their device.
* Treat uploaded images as draggable stickers.
* Allow stickers to be resized and rotated.
* Preserve transparency when the uploaded image has a transparent background.
* Make it easy to reuse previously uploaded stickers.
* Include a small default sticker panel with simple reaction symbols.

### 5. Speech bubbles
* Add speech bubbles that can be placed anywhere on the page.
* Allow the user to type inside them.
* Allow them to move, resize and rotate them.
* They should work for comic-strip-style conversations between the reader and characters/the author.

### 6. Drawing
* Add a simple freehand drawing tool.
* Include basic doodle tools such as stars, dots, arrows and hearts.
* Drawing should be optional and unobtrusive.

### 7. Annotation layers
* Annotations must appear above the PDF.
* They should not modify the underlying book.
* Users should be able to select, move, resize, rotate and delete annotations.

### 8. Reading-first interface
* The PDF should remain the dominant element.
* Do NOT make the interface look like Canva or a scrapbook editor.
* Controls should be small and unobtrusive.
* The goal is to make annotations feel like physical marginalia.

### 9. Persistence
* Save the current book and its annotations locally in the browser so that refreshing the page does not immediately erase everything.
* Do not require a backend or user account for the initial version.

### 10. Export
* Add an option to export/download the annotated book as a PDF if technically feasible.
* If full export is too complicated for the first version, prioritize reliable local saving and annotation over export.

---

## TECHNICAL REQUIREMENTS

* Make this a responsive web application.
* It should work on desktop and mobile browsers.
* Use a sensible existing PDF rendering library rather than implementing PDF rendering from scratch.
* Keep dependencies minimal.
* Do not add unnecessary login, payments, social features, cloud storage or AI features.
* Prioritize a functional prototype over visual complexity.

---

## Before finishing, test that:

* PDF upload works.
* Pages render.
* Highlights work.
* Text can be moved and rotated.
* Images can be uploaded, moved, resized and rotated.
* Speech bubbles work.
* Annotations persist after refreshing.
* The application does not lose annotations when moving between pages.

---

**Build the simplest functional version first.**
