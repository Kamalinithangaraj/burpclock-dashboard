# Burpclock Dashboard

A simple restaurant operations dashboard - built as a portfolio project for
a hospitality-tech internship application.

## What it shows
- Stat cards: total orders today, revenue, pending orders, average order value
- A recent orders table with a live search box (filters by customer or item as you type)
- A "top selling items" panel with simple bar visualizations

## Tech stack
- Plain HTML, CSS, and JavaScript - no backend, no build tools, no installs required
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

## How to run it
No installation needed. Just open `index.html` in any browser (double-click
the file, or right-click → Open with → your browser).

## Possible next steps
- Connect it to a real backend (Flask/Node) serving live order data
- Add a working chart library (e.g., Chart.js) instead of the CSS bar chart
- Add date filtering (today / this week / this month)
