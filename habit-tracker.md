
Build a single-page Vanilla HTML/CSS/JS Habit Tracker (no frameworks).
**Tech Stack:** Vanilla JS, LocalStorage for persistence, modular code structure.

**Core Features:**
1. **Habit Management:** 
   - Add habit: Name (required/unique), Color (fixed palette), Target (integer 1-7 days/week). 
   - Validation: Visible errors for empty names, duplicates, or out-of-range targets.
   - Edit/Delete: Inline/modal editing; Delete requires confirmation and wipes history.
2. **14-Day Grid:** 
   - Show habit rows with 14 days (today is the rightmost column).
   - Toggle cell on click; disable future dates.
3. **Stats & Logic:** 
   - Per habit: Current streak (consecutive days ending today or yesterday) and weekly completion (e.g., "3/5").
   - Global: Total weekly check-offs across all habits.
   - All stats must update immediately on toggle.
4. **Filters:** Combined filter for Color and "Show habits behind target."
5. **UI/UX:** 
   - Dark/Light mode (persisted to localStorage).
   - Empty state for no habits; visual distinction for "Today's" column.
   - Desktop-first design.

**Constraints:**
- No backend/accounts/npm/external libraries.
- Code must be split into logical sections (storage, rendering, logic, filters).

**Deliverables:**
- Source files + README (Run instructions, feature list, and streak logic definition).
