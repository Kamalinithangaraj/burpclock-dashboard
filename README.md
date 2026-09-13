# Burpclock Dashboard

A simple restaurant operations dashboard

## What it shows
- Stat cards: total orders today, revenue, pending orders, average order value
- A recent orders table with a live search box (filters by customer or item as you type)
- A "top selling items" panel with simple bar visualizations
- Date filtering (Today / This Week) on the orders table
- A daily lucky draw that randomly picks one customer from today's orders, with the result saved so it persists on refresh

## Tech stack
- Plain HTML, CSS, and JavaScript 
- Data is sample data defined directly in the JavaScript (stands in for what
  a real backend/database would provide)

## How I built this
I used Claude (AI coding assistant) to generate the structure, then reviewed
and adjusted it myself:
- Asked for stat cards, a searchable orders table, and a top-items panel,
  one piece at a time
- Read through the search filter function line by line to understand how
  `.filter()` and `.includes()` work together
- Tested the search box manually with different inputs (partial names,
  empty search, no matches) to confirm it behaves correctly
- Found and fixed a bug where the date filter wasn't reading input values
  correctly (was capturing the return value of addEventListener instead of
  the actual .value) — traced it by reading through the function logic
  rather than guessing
- Extended the app with a new feature (daily lucky draw) built on top of
  the existing data structure, including using localStorage to persist
  the day's winner

## How to run it
No installation needed. Just open `index.html` in any browser (double-click
the file, or right-click → Open with → your browser).

## Possible next steps
- Add "This Month" filter option
- Animate the lucky draw reveal further (confetti, sound)
- Connect to a real backend so orders update live instead of static sample data
