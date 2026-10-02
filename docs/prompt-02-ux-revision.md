I tested the current app and need the following changes.

### IMPORTANT:

* Preserve the current overall visual design and reading-first philosophy.
* Do not redesign the application or replace working features unnecessarily.
* Do not remove existing functionality unless explicitly requested below.
* The sidebar/tool controls should remain available while reading. The annotation toolbar/sidebar must NOT scroll away with the book/document.
* The PDF/book should scroll independently beside the fixed annotation controls.
* I want annotations to feel like physical book marginalia, not like a graphic-design/Canva editor.
* Prioritize precise, natural annotation behavior over decorative UI.

---

# FIX THE ANNOTATION TOOLBAR

### Current problem:
The left sidebar currently scrolls with the book. If I am on page 3 and want to highlight something, I have to scroll back to the toolbar.

### Change:

* Make the left annotation toolbar/sidebar fixed/sticky to the viewport.
* It must remain visible while the book/PDF scrolls.
* The book/document itself should scroll independently.
* I should be able to access Select & move, Text note, Speech bubble, Highlight text, Draw, Doodle, Image stickers, etc. from any page without scrolling back.
* Do not make the sidebar excessively wide.
* Allow the sidebar to minimize with an arrow on top.
* Keep the reading area as large as possible.

---

# TEXT NOTE RESIZING & EDITING

### Current problem:
The text note cannot be resized properly.

### Change:

* Text notes must be freely resizable horizontally AND vertically.
* Font size must respond appropriately to resizing or have a clear font-size control.
* Text boxes should support:
  * Move
  * Resize from corners
  * Rotate freely
  * Edit text
  * Change font
  * Change text color
* Rotation must allow arbitrary angles, including diagonal text.

---

# SPEECH BUBBLES

### Change:

* Keep the current speech bubble functionality.
* Add a transparent/no-fill option.
* Also allow:
  * Opaque fill
  * Transparent fill
  * Adjustable opacity
  * Border on/off
  * Border thickness
  * Text editing
  * Resize
  * Move
  * Free rotation
* The speech bubble itself and its text should remain independently readable.
* It should work for comic-strip-style conversations between me and characters/the author.

---

# TEXT-ANCHORED HIGHLIGHTING

I want highlighting to behave more like physical/highlighter ink and less like a rectangular graphic object.

### Current problems:

* The highlight creates a rectangular markup area.
* The resize behavior is restricted.
* The highlight can move upward/downward through a rectangular bounding area.
* The highlight currently behaves like a box around the selected text.

### Desired behavior:

#### A. TEXT HIGHLIGHT
* When I select text, highlight ONLY the selected text.
* Do not create a large rectangular markup box around the whole region.
* Do not allow the highlight's bounding box to move vertically independently from the text.
* The highlight should remain anchored to the underlying text.

#### B. MULTI-LINE HIGHLIGHT
* If selected text spans multiple lines, highlight each relevant line/segment individually.
* Do NOT create one giant rectangle around all the selected text.

#### C. FREE-FLOWING HIGHLIGHT
I want the visual appearance to be more organic, like:
* a real highlighter stroke
* ink
* a soft cloud/water-like stroke
rather than a perfect rectangular selection.

If technically feasible, implement the highlight as text-anchored highlight segments/strokes rather than one rectangular annotation object.

#### D. HIGHLIGHT COLOR
* Preserve multiple highlight colors.
* Make the highlight opacity slightly translucent, like real highlighter ink.
* Allow the user to change the highlight color.

#### E. IMPORTANT INTERACTION
* Once text is highlighted, I do NOT want a visible resize rectangle that lets me freely drag the highlight away from the text.
* The highlight should remain associated with the text.

If free-flowing text highlighting is technically incompatible with the current PDF/text-rendering architecture, use the closest robust implementation rather than breaking text selection.

---

# DRAW TOOL

### Rename:
`Freehand` → `Draw`

The current Freehand tool behaves like another highlighter. That is incorrect.

Draw should be a genuine drawing tool.

### Provide at minimum:

#### TOOLS:
* Coarse pencil
* Pen
* Fountain pen

Each should have adjustable size/thickness.

#### Also include:
* Eraser
* Undo
* Redo

#### COLORS:
Provide at least 5–7 colors total, including approximately:
* 3 solid colors
* 2 pastel colors
* 1–2 additional useful colors

The exact colors can be chosen sensibly, but the palette should be readable and pleasant.

### Drawing must:
* Actually draw freehand strokes.
* Not behave like text highlighting.
* Allow organic imperfect human-looking lines.
* Preserve the natural variation of hand-drawn marks.
* Support arbitrary directions and shapes.

---

# DRAWING GRIDS

Add a simple grid option within Draw.

I want grids that can be turned on/off with one click.

### Include several options such as:
* Small square grid
* Large square grid
* Dotted grid
* Optional lined/grid-paper style

### Requirements:
* Grid should be easy to toggle.
* Grid should be removable with one click.
* Grid should appear as an annotation/background layer rather than permanently modifying the book.
* It must not interfere with the book text.
* The grid should remain aligned to the page.

---

# DOODLE TOOL & EXPANDED LIBRARY

### Bug fix:
The current Doodle tool contains:
★ • ↗ ♡

Currently, regardless of which doodle I choose, only the star appears. Fix this bug first.

Each selected doodle must actually render as the selected doodle.

### Expanded Library:
I want the doodle library expanded substantially.

#### Keep the existing:
* Star
* Dot
* Arrow
* Heart

#### Add:

##### BOTANICAL / NATURE:
* 2–3 simple flower designs
* Simple leaves
* Vines with simple leaves
* Falling petals
* Crescent moon
* Rising sun
* Clouds
* 2–3 snowflake patterns
* 2–3 simple "starry light" patterns inspired by the visual feeling of Van Gogh's Starry Night (do NOT copy artwork; make original decorative patterns)
* 2–3 simple aurora patterns

##### SYMBOLS / REACTIONS:
* Exclamation mark
* Question mark
* Colon
* Hollow dot
* Opaque dot
* Heartbreak/broken heart
* Fire
* Skull
* Dollar symbol

##### OBJECTS:
* Paper plane
* Bow
* Lantern
* Nail polish / painted fingernail-style symbol
* Trash can

##### CELEBRATION:
* 2–3 simple fireworks patterns

##### CREATURES:
* Butterfly

The doodles should be simple, small, hand-drawn-looking decorative marks rather than large illustrations.

### Each doodle should:
* Be selectable independently.
* Be draggable.
* Be resizable.
* Be rotatable.
* Support an invert option.
* Ideally support color changes if compatible with the current implementation.

Organize doodles into small categories if needed so the sidebar does not become enormous.

---

# HANDWRITING FONTS

### Current fonts:
* Book Italic
* Kalam
* Patrick Hand

Keep all three.

### Add at least TWO of the following handwriting-style fonts, if they are legally available for web use:
* Hiragenda
* Cattalague
* Amsterdam Handwriting
* Rustic Roadway

#### IMPORTANT:
Before adding any font, verify that its license permits use in this application.
If a requested font is not legally available for embedding, DO NOT download/use it anyway. Instead use a visually similar legally embeddable handwriting font.

The font selector should make it easy to preview/select the handwriting styles.

### Text should support:
* Horizontal placement
* Diagonal placement
* Arbitrary rotation
* Resize
* Color
* Opacity where appropriate

---

# GLOBAL STICKER LIBRARY

This is VERY IMPORTANT.

Currently uploaded stickers appear to belong only to the current PDF.

I want my uploaded stickers to become part of my personal sticker library.

### Example:
I upload:
* Blackie reaction face
* Mousse reaction face
* Miu reaction face
* Chand Begum reaction face
* Meme images

Those stickers should remain available when I:
* close the current book
* open another PDF
* upload a new PDF
* refresh the application

The sticker library should be GLOBAL across all books/documents.

Do NOT store the sticker only inside the current document's annotation state.

### Separate:

#### GLOBAL USER ASSETS:
* Uploaded stickers
* Custom doodles if implemented
* Preferred colors
* Preferred fonts/settings where appropriate

#### DOCUMENT-SPECIFIC DATA:
* Highlights
* Text notes
* Speech bubbles
* Drawings
* Doodles
* Sticker placements
* Grid placements

Use local browser persistence for the initial version. No backend/account system is necessary.

---

# INVERT FUNCTIONALITY

Add an "Invert" option for:
* Speech bubbles
* Doodles
* Highlights
* Image stickers

The exact implementation can vary depending on the object.

For example:
* Black → white
* Light → dark
* Normal → inverted appearance

* For images, use an appropriate visual invert/filter.
* For vector doodles and bubbles, invert foreground/fill/border appropriately.
* For highlights, provide a sensible inverted/contrasting appearance rather than making the page itself invert.

The original object must remain editable.

---

# SELECTION & INTERACTION MODEL

All movable annotation objects should have a consistent interaction model.

### When an object is selected:
* Move
* Resize
* Rotate
* Delete
* Duplicate where useful

The rotation handle should remain intuitive.

Do not show large ugly selection boxes unless the object is actively selected.

### For text-anchored highlights specifically:
Do NOT allow the highlight to be detached from its text.

This is crucial.

---

# PHILOSOPHY & NON-GOALS

The application should NOT feel like Canva.

The book is the primary interface.

Annotations should be lightweight and unobtrusive.

### The sidebar should be:
* Fixed
* Compact
* Easy to collapse
* Available while scrolling

The user should be able to read normally without constantly seeing editing controls.

### Do not add:
* Social features
* Accounts
* Sharing
* Comments
* Payments
* Unnecessary dashboards
* AI chat
* Excessive animations

Those are not part of this version.

---

# ARCHITECTURE & PERSISTENCE

Use a clean separation between:

### GLOBAL:
* Sticker library
* Uploaded assets
* Fonts/preferences
* Drawing preferences where appropriate

### PER DOCUMENT:
* PDF/document identity
* Annotation positions
* Highlights
* Notes
* Speech bubbles
* Doodles
* Drawing strokes
* Sticker placements
* Grid settings

Refreshing the browser should NOT erase annotations.

Switching to another book should NOT erase the global sticker library.

Opening the original book again should restore its annotations if it was previously annotated.

---

# BUGS TO FIX FIRST

Before adding new features, fix these existing bugs:

1. **Sidebar scrolls with the book.**
   → Make it fixed.
2. **Text note resizing does not work correctly.**
   → Make it freely resizable.
3. **Speech bubble is opaque.**
   → Add transparent/no-fill option.
4. **Highlight resizing only works in limited directions.**
   → Replace with proper text-anchored behavior.
5. **Highlight creates rectangular markup regions.**
   → Make highlights text-anchored and multi-line aware.
6. **Freehand is functioning as another highlighter.**
   → Replace with genuine drawing.
7. **Doodle selection is broken.**
   → Selecting star/dot/arrow/heart/etc. must render the correct selected doodle.
8. **Uploaded stickers are document-specific.**
   → Move uploaded sticker assets into global persistent storage.

---

# IMPLEMENTATION PLAN

Implement in this order:

### PHASE 1 — Fix existing functionality
1. Fixed sidebar
2. Text note resizing
3. Speech bubble transparency
4. Correct doodle selection
5. Genuine Draw tool 

### PHASE 2 — Fix annotation architecture
6. Correct text-anchored highlighting
7. Multi-line highlighting
8. Global sticker persistence
9. Document-specific annotation persistence

### PHASE 3 — Expand tools
10. Drawing tools
11. Colors
12. Grids
13. Expanded doodle library
14. Additional handwriting fonts
15. Invert functionality

Do NOT sacrifice existing working functionality simply to add more features.

After each phase, test the application before proceeding.

---

# VERIFICATION CHECKLIST

Before declaring the task complete, manually test:

* Upload a PDF.
* Scroll to page 3.
* Confirm the annotation toolbar is still visible.
* Add a text note on page 3.
* Resize it horizontally and vertically.
* Rotate it diagonally.
* Add a transparent speech bubble.
* Highlight text across multiple lines.
* Confirm the highlight follows the selected text rather than becoming a movable rectangle.
* Select every doodle and confirm each produces the correct symbol.
* Draw using pencil, pen and fountain pen.
* Change drawing sizes.
* Erase a drawing.
* Undo and redo.
* Add a grid and remove it.
* Upload a sticker.
* Place it on page 3.
* Refresh the browser.
* Confirm the annotation remains.
* Upload/open a different PDF.
* Confirm the uploaded sticker is still available.
* Return to the first PDF.
* Confirm its annotations remain.
* Test invert on a speech bubble, doodle, highlight and sticker.

---

If something cannot be implemented reliably with the current architecture, explain the technical limitation and implement the closest stable alternative rather than creating a broken feature.

Do not claim a feature is complete unless it has been tested.
