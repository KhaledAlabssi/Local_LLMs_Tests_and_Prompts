
Build a Vanilla HTML/CSS/JS Reading List web app.
**Tech Stack:** Vanilla JS (modular), LocalStorage, No frameworks. **Constraint: No Drag-and-Drop; use buttons/selects only.**

**Core Features:**
1. **Book Management (CRUD):**
   - **Fields:** Title (req), Author (req), Status (Want to read/Reading/Finished), Rating (1–5, *only* if status is Finished), Note (opt).
   - **Validation:** Reject empty title/author. Disable/hide rating input unless status is "Finished."
   - **Status Logic:** Moving a book out of "Finished" must automatically clear its rating.
   - **Edit/Delete:** Inline/modal editing; Delete requires confirmation.
2. **Organization & View:**
   - **Grouping:** Three sections by status (Want to read, Reading, Finished) with live counts in headers.
   - **Search:** Global search by Title or Author.
   - **Sort:** Per-section sorting by Title or Date Added. The "Finished" section must also include "Sort by Rating."
   - **Combination:** Search and Sort must work together.
3. **Stats & Theme:**
   - **Stats Line:** Total books, number finished, and average rating of finished books (live updates).
   - **Theme:** Dark/Light mode toggle (persisted to localStorage).

**UX & Code Quality:**
- Handle empty states (no books, no search results, empty sections).
- Modular code (separate state, rendering, storage, and search/sort).
- Deliverables: Source files + README (Run instructions, feature list, and the rating-clearing rule).
