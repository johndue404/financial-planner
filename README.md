# 📊 Financial Planner

> **A simple, intuitive web app to help you plan, track, and analyze your finances over a customizable 6-month “semester.”**  
> View incomes, expenses, savings, and account balances at a glance.

---

## Features

- **Semester Planning:**  
  Plan and review your budget for a 6-month window (“semester”), choosing a January or July start and any year.
  
- **Multiple Accounts:**  
  Add any number of accounts (such as “Main Bank”, “Savings”, etc.) with custom starting balances.
  
- **Flexible Income & Expense Tracking:**  
  - Add incomes or expenses as either:
    - **Fixed:** Recurring items applied to all months.
    - **One-time:** Specific to a single month.
  - Assign every item to a particular account.
  - Mark fixed items for easy management.
  
- **Savings Goals:**  
  - Set savings targets per month, assigned to any account.
  - Savings reduce available balance for that month.
  
- **Detailed Overview and Summaries:**
  - Semester summary:  
    See the total incomes, expenses, savings, and net result for your entire semester.
  - Month-by-month cards:
    - See incomes, expenses, savings, and net for each month.
    - Lists of all fixed and one-off items.
    - Automatic highlighting if income minus expenses meets or misses the savings goal for the month.
  - Account summary:  
    See all accounts with starting balance, semester-wide sums for income/expense/savings, and the final balance.
    
- **Data Export & Import:**
  - Export your semester plan (including accounts, items, and settings) as a JSON file.
  - Import a previously saved plan from JSON for backup or transfer.
  
- **Cycle Management:**
  - Start a “New Cycle” to wipe all data and begin a fresh plan (preserving semester selection).

---

## Quick Start

1. **Open the app in your browser** (simply open the HTML file).
2. **Set your semester** (via ⚙️ “Manage” → 🗓️ “Semester”).
3. **Add one or more accounts** (⚙️ → 🏦 “Accounts”).
4. **Add incomes and expenses** (➕ “Income/Expense” button).
5. **Set savings goals** (⚙️ → 💰 “Savings”).
6. **Review monthly and semester summaries.**
7. **Save/export your plan** as needed (📂 “Data” → ⬇️ “Export”).

---

## Controls & UI Overview

- **Navbar:**
  - ➕ **Income/Expense:** Add an entry (choose month, type, account, amount, fixed/one-time).
  - ⚙️ **Manage Dropdown:**  
    - 🗓️ Semester: Set semester period.
    - 🏦 Accounts: Add/manage accounts.
    - 💰 Savings: Set monthly goals.
  - 📂 **Data Dropdown:**  
    - ⬇️ Export: Download all data (.json)
    - ⬆️ Import: Restore from backup (.json)
    - 🗑️ New Cycle: Clear all items and accounts.
  
- **Semester Overview Card:**  
  - Shows total incomes, expenses, savings, and net balance.

- **Account Balances Card:**  
  - Detailed per-account breakdown of starting, transactional, savings, and final balances.

- **Monthly Cards:**  
  - Incomes/Expenses/Savings details per month
  - Summed net per month
  - Highlights months where savings goals are hit/missed

---

## Data Model

Internally, data is structured as:
- `semester`: `{year, startMonth}` — basis for the 6-month period
- `accounts`: array of user-defined accounts (with unique id)
- `fixed`: `{incomes:[], expenses:[]}` — repeating monthly items
- `months`: mapping `YYYY-MM` → `{ incomes:[], expenses:[], savings:[] }`
- All entries are mapped to account ids and tracked by unique ids.

---

## Installation

No installation or dependencies required:
- The app is a **single HTML file**, using Bootstrap CDN for UI.  
- Just open the file in a modern browser (Edge, Chrome, Firefox, Safari).

---

## Technologies Used

- **HTML5**
- **Vanilla JavaScript (ES6+)**
- **Bootstrap 5** (via CDN)
- No build steps or external packages.

---

## Export/Import Format

- **Export:** JSON file representing all current data.
- **Import:** Only supports valid app-exported files.

---

## Customization & Extending

- The code is fully client-side and easily extensible!
- You may enhance with persistent storage, analytics, or more advanced reports.

---

## License

MIT License

---

## Screenshots

<img width="1566" height="933" alt="Screenshot 2025-08-17 at 1 59 53 PM" src="https://github.com/user-attachments/assets/67333c22-68bf-44cf-bbe6-89c9d98156d8" />

---

## Author

Dwight Schrute
