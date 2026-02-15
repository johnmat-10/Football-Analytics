# ISL 2026 Points & Projections Matrix (v1.0)

A high-fidelity, real-time strategic dashboard for the **Indian Super League 2026** season.

This tool transcends standard standings tables by providing **mathematical projections, championship thresholds, and safety buffers** derived from live fixture data.

---

## 🚀 Core Features

### 1️⃣ Strategic Outcome Matrix

The centerpiece of the application is a visual plotting space that tracks every club's journey through the season:

* **Current Points Marker**
  A color-coded circular node displaying the team’s live points.

* **Available Window Bar**
  A translucent bar extending from current points to the team’s mathematical maximum (the *ceiling*).

* **Dynamic Cutoff Lines**

  * **Title Ceiling** – A dashed line representing the highest points total any rival can still reach.
  * **Safety Ceiling** – A dashed line representing the points total of the current bottom-placed team.

---

### 2️⃣ Live Auto-Sync Engine

Designed as a true **“set and forget”** dashboard:

* **GitHub Integration**
  Fetches match results directly from a raw CSV hosted on GitHub.

* **Cache-Busting Protocol**
  Uses timestamped query parameters to bypass GitHub raw file caching for instant updates.

* **Background Polling**
  Re-syncs and re-calculates automatically every **60 seconds** — no page reload required.

---

### 3️⃣ Automated Status Tagging

The system evaluates every team’s mathematical standing in real time:

* 🏆 **Locked** – Team has mathematically secured the top spot.
* 🔵 **Active** – Still within the title race window.
* 📊 **Margin** – Displays the points gap between a team’s ceiling and the current leader’s floor.
* ⚠️ **At Risk** – Team’s ceiling is lower than the leader’s current points.
* ❌ **Eliminated** – Mathematically impossible to win the league.

---

### 4️⃣ Team Deep Dives

Clicking any team row opens a detailed strategic profile:

* **Mathematical Thresholds**

  * `PTS TO LOCK` – Points required to secure the title.
  * `PTS TO SAFETY` – Points required to avoid basement risk.

* **Full Season Matrix**

  * All **26 fixtures** listed.
  * Results clearly marked: **W / D / L**
  * Upcoming venues highlighted.

---

## 🛠 Tech Stack

| Component       | Technology                                 |
| --------------- | ------------------------------------------ |
| **Styling**     | Tailwind CSS (Custom *Glassmorphism* UI)   |
| **Icons**       | Lucide React (via CDN)                     |
| **Typography**  | Plus Jakarta Sans & Inter                  |
| **Logic**       | Vanilla JavaScript (ES6+)                  |
| **Data Engine** | CSV-to-JSON parsing with automated polling |

---

## 📂 Data Structure

The app reads from a GitHub-hosted CSV file.

**Required column headers:**

```csv
Home_Team, Away_Team, Home_Score, Away_Score
```

---

## 📈 Version 1 Specifications

* **Total Teams:** 14
* **Matches per Team:** 13
* **Maximum Points Possible:** 39
* **Sync Interval:** 60,000 ms (1 minute)

---

### Developed by John Mathew

**John Mathew**
Strategic Profile / Matrix Engine v1.0
