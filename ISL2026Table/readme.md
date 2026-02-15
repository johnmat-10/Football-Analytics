ISL 2026 Points & Projections Matrix (v1.0)

A high-fidelity, real-time strategic dashboard for the Indian Super League 2026 season. This tool transcends standard standings tables by providing mathematical projections, championship thresholds, and safety buffers derived from live fixture data.

🚀 Core Features

1. Strategic Outcome Matrix

The centerpiece of the application is a visual plotting space that tracks every club's journey through the season:

Current Points Marker: A color-coded circular node showing the team's live points.

Available Window Bar: A translucent bar extending from current points to the team's mathematical maximum (the "ceiling").

Dynamic Cutoff Lines:

Title Ceiling: A dashed line representing the highest points total any rival can still reach.

Safety Ceiling: A dashed line representing the points total of the current bottom-placed team.

2. Live Auto-Sync Engine

Built to operate as a "set and forget" dashboard:

GitHub Integration: Fetches match results directly from a raw CSV hosted on GitHub.

Cache-Busting: Implements a timestamped query protocol to bypass GitHub's raw file caching, ensuring updates are reflected instantly.

Background Polling: The matrix silently re-syncs and re-calculates every 60 seconds without requiring a page reload.

3. Automated Status Tagging

The system evaluates every team's mathematical standing in real-time:

Locked – The team has mathematically secured the top spot.

Active – The team is still within the title race window.

Margin – Displays the points gap between a team's ceiling and the current leader's floor.

At Risk – The team's ceiling is lower than the leader's current points, indicating they are near the basement.

Eliminated – Mathematically impossible for the team to win the league.

4. Team Deep Dives

Clicking any team row opens a strategic profile containing:

Mathematical Thresholds: Clear indicators of "PTS TO LOCK" (to secure the title) and "PTS TO SAFETY."

Full Season Matrix: A complete list of all 26 fixtures for that specific team, highlighting results (W/D/L) and upcoming venues.

🛠 Tech Stack

Component

Technology

Styling

Tailwind CSS (Custom "Glassmorphism" UI)

Icons

Lucide React (via CDN)

Typography

Plus Jakarta Sans & Inter

Logic

Vanilla JavaScript (ES6+)

Data Engine

CSV-to-JSON parsing with automated polling

📂 Data Structure

The app reads from a GitHub-hosted CSV. The data parser expects the following mandatory column headers:

Home_Team, Away_Team, Home_Score, Away_Score


📈 Version 1 Specifications

Total Teams: 14

Matches per Team: 26

Max Points Possible: 78

Sync Interval: 60,000ms (1 Minute)

Developed by John Mathew Strategic Profile / Matrix Engine v1.0
