# Crew Pod Planner

A single-page tool for planning how people are grouped into agile pods across three crews (A, B, C).

Open `index.html` in a browser. No install, no build, no backend.

## What it does
- Assign people to 10 pods by drag-and-drop or tap-to-place
- Pick a Pod Tech Lead (PTL) for each pod; a PTL can lead 1–3 pods
- **Auto-assign** builds a plan that satisfies the hard rules
- Live rule checks:
  - Max 7 members per pod
  - PTL has 4–9 direct reports
  - Pod spans at most 2 locations
  - Optional (on by default): same-location reports must earn less than their PTL. Turn it off to work without comp data
  - Optional: block reports who outrank their PTL
  - Skill balance warning when a pod's average skill is off the org average by more than 0.5
- Load your own roster as CSV: `name, rank, location, skill, comp`. Comp can be blank, or the column left out, when the comp check is off
- Export the plan as CSV
- Export an org chart (PNG or SVG) showing name, rank and location only. Comp and skill are left out.

## Data
Ships with 60 generated sample employees. Your edits are saved in the browser's local storage and never leave the device.

## Stack
Plain HTML, CSS and JavaScript in one file. Fonts from Google Fonts.
