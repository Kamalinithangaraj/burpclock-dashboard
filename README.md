# Burpclock Dashboard
# "Live demo: https://kamalinithangaraj.github.io/burpclock-dashboard/"
A restaurant operations dashboard with a simulated live order feed.
![Burpclock dashboard screenshot](screenshot.png)

## What it shows
- Stat cards: total orders, revenue, pending orders, average order value
- A recent orders table with a live search box (filters by customer or item as you type)
- Date filtering (Today / This Week) on the orders table
- A "top selling items" panel with simple bar visualizations
- A daily lucky draw that randomly picks one customer from today's orders, with the result saved so it persists on refresh
- A simulated live order feed: new orders appear automatically every few seconds (with a toast notification and highlighted row), then transition from "pending"/"preparing" to "done" - mimicking real-time kitchen activity
- A "Frequent Customers" panel that ranks customers by order count and flags anyone with 3+ orders as eligible for a free gift

## Tech stack
- Plain HTML, CSS, and JavaScript - no backend, no build tools, no installs required
- Data is sample data defined directly in the JavaScript (stands in for what
  a real backend/database would provide)
- The "live" feed is a front-end simulation using `setInterval()` - it is not
  connected to a real server or real customers, but is built to demonstrate
  how a live system would behave and update the UI

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
- Extended the app with a daily lucky draw feature built on top of the
  existing data structure, using localStorage to persist the day's winner
- Added a simulated live order feed and a frequent-customers panel with
  free-gift eligibility, to explore what a more "live" and relationship-aware
  version of the dashboard could look like

## How to run it
No installation needed. Just open `index.html` in any browser (double-click
the file, or right-click → Open with → your browser).

## Possible next steps
- Replace the simulated live feed with a real backend (Node/Express) and a
  database, so orders persist and update from real activity instead of
  being generated client-side
- Add WebSocket support so multiple devices see the same live order stream
  in sync
- Add "This Month" filter option
- Animate the lucky draw reveal further (confetti, sound)
