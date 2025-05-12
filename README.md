# 🧠 DOM Reconciliation Concepts in JavaScript

This project demonstrates **step-by-step evolution of DOM manipulation techniques**, leading up to concepts used in modern frameworks like **React** — such as Virtual DOM and reconciliation.

Each file simulates different levels of optimization in updating the DOM when data changes over time.

---

## 📁 Program Breakdown

### ✅ `1. fullDomReplacement.js` — 🔁 Brute Force DOM Re-render
- **Approach**: Clears the entire DOM using `innerHTML = ''` and re-adds all elements from scratch every 5 seconds.
- **Downside**: Inefficient. Causes performance issues in larger UIs.
- **Learning**: What *not* to do in dynamic rendering.

---

### ✅ `2. manualReconciliation.js` — 🔍 DOM Diffing with Manual Updates
- **Approach**: Compares new data with existing DOM elements by ID.
- **Actions**: Updates existing items, adds new ones, and removes those no longer needed.
- **Learning**: Manually performing what React does with its reconciliation algorithm.

---

### ✅ `3. pureVirtualReconciliation.js` — 🧠 Old vs New Virtual DOM
- **Approach**: Introduces a `vDOM` array (virtual representation of UI).
- **Comparison**: Compares old vDOM and new vDOM **without touching the real DOM** until it knows exactly what to change.
- **Learning**: Mimics how React minimizes DOM updates for performance.

---

### ✅ `4. vdomBatch.js` — ⏱️ Batched vDOM + DOM Sync (Async Reconciliation)
- **Approach**: 
  - `updateVirtualDom(data)` runs every 5s → updates only the virtual DOM.
  - `createDomElements()` runs every 1s → syncs the virtual DOM with real DOM.
- **Learning**: Separates update and render cycles like React’s fiber architecture.

---

## 📦 Setup

1. Clone this repo:
   ```bash
   git clone https://github.com/itsnaved/Reconcilation-Programs.git
