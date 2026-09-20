

Build a polished Eisenhower Priority Matrix web app using Vanilla HTML, CSS, and JS.
**Tech Stack:** Vanilla JS (modular structure), LocalStorage for persistence. A small D&D library is permitted.

**Core Features:**
1. **The Matrix:** 
   - 4 fixed quadrants (Urgent/Important, Not Urgent/Important, Urgent/Not Important, Not Urgent/Not Important).
   - An "Inbox" strip for unassigned tasks.
2. **Task Management:**
   - CRUD: Create (title required, optional note), Edit (including notes), and Delete (with confirmation).
   - Completion: Checkbox toggles strikethrough and moves the task to the bottom of its current quadrant.
   - Bulk Action: "Clear completed" with confirmation.
3. **Drag-and-Drop Logic:**
   - Full bidirectional movement: Inbox $\leftrightarrow$ Quadrants, Quadrant $\leftrightarrow$ Quadrant.
   - Support reordering within a quadrant.
   - Visual feedback for drop targets during dragging.
4. **UI/UX:**
   - Live counts of open tasks in each quadrant header.
   - Dark/Light mode (persisted to localStorage).
   - Clear empty states and visual feedback for all actions.

**Constraints:**
- No backend/accounts/due dates/labels.
- Code must separate concerns: state, rendering, persistence, and D&D logic.

**Deliverables:**
- Source files + README (Run instructions, feature list, and code structure).
