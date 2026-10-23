
Build a Vanilla HTML/CSS/JS Subscription Tracker (no frameworks).
**Tech Stack:** Vanilla JS, LocalStorage for persistence, modular code structure.

**Core Features:**
1. **Subscription Management (CRUD):**
   - **Fields:** Name (req), Price (req, >0), Cycle (Monthly/Yearly), Next Renewal (req, future date), Category (fixed list), Note (opt).
   - **Validation:** Reject empty fields, non-numeric/negative prices, and renewal dates in the past. Show visible errors.
   - **Edit/Delete:** Edit in-place/modal; Delete requires confirmation.
2. **Subscription List:**
   - Sort by renewal date (soonest first).
   - Display: Name, Price/Cycle, Renewal Date, Category, Note.
   - **Visuals:** Highlight subscriptions renewing within the next 7 days.
3. **Summary & Math:**
   - Calculate **Monthly-Equivalent Cost**: (Yearly price / 12) or Monthly price.
   - Display: Total monthly-equivalent cost, per-category monthly totals, and total active count.
4. **Filters & Theme:**
   - **Filters:** Combined filter for Category AND Billing Cycle.
   - **Theme:** Dark/Light mode toggle (persisted to localStorage).
5. **Design & Animation:**
   - Clean and modern design with animations.

**Constraints:**
- No backend, no payment integration, no external libraries.
- Modular code (separate storage, rendering, math, and filters).
- Handle empty states and consistent currency formatting.

**Deliverables:**
- Source files + README (Run instructions, feature list, and rounding rule documentation).
