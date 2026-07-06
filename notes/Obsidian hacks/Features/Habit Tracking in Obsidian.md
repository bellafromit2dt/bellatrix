⏱️ **Reading time: 2 minutes** | #obsidian #howtos #productivity #habits 
# Habit Tracking in Obsidian

## 🎯 TL;DR
Visualise and manage all your habits in a Github-style heat-map --- Track streaks, build momentum, no scattered notes or apps. Setup takes 5 minutes.

## 📋 Prerequisites & Setup
- [⭐️⭐️⭐️ Obsidian + Habit Tracker 21](../Plugins/⭐️⭐️⭐️%20Obsidian%20+%20Habit%20Tracker%2021.md) installed and enabled
- A dedicated habits folder (required for configuration)

## 🤔 The Problem
Your habits are scattered everywhere --- spreadsheets, daily notes, all kinds of fancy apps --- far away from your Obsidian vault, where you manage all your daily notes and knowledge. 

## 💡 The Solution
Use the `Habit Tracker 21` plugin to keep all your habits in your vault and visualised in one dashboard to review daily, celebrate streaks, and feedback fast.

**What you get:**
1. 📌 **Centralizes** all habits in a single, designated folder
2. 👁️ **Visualizes** daily progress with checkmarks and streak counters
3. 📈 **Tracks** consistency patterns over time
4. 🎯 **Motivates** through momentum—watching your green squares grow as you go
5. 🔄 **Enables** quick iteration when a habit needs redesign

## 🚀 How to Set it Up
### Step 1: Install & Enable Plugin
Settings → Community plugins → Browse → Search `Habit Tracker 21` → Install → Enable

### Step 2: Create a Habits Folder
- Create a new folder: `/habits` (or whatever you prefer)
- Configure the "default path" in the settings of `Habit Tracker 21` plugin to: `/habits`

### Step 3: Add Your Habits
Create notes in that folder with your habit names:
- [Daily 30mins Reading](../../../resources/habits/Daily%2030mins%20Reading.md)
- [Weekly 3 Workouts](../../../resources/habits/Weekly%203%20Workouts.md)
- [Daily 8 glasses of water](../../../resources/habits/Daily%208%20glasses%20of%20water.md)
- (Create whatever habit you want to track)

### Step 4: Display Your Dashboard
Add this code block to any note where you want to see your habits:
``` 
// see https://github.com/zincplusplus/habit-tracker#quick-start
```habittracker
{
  "path": "resources/habits"
}
```

Example screenshot
![Screenshot 2026-07-06 at 21.16.36](../../../resources/screenshots/Screenshot%202026-07-06%20at%2021.16.36.png)
### Step 5: Start Tracking
Check off habits daily. The plugin auto-timestamps each check. Watch your streaks grow.
💡 **Pro tip:** 
- Click any date to add notes about that day
- Click any habit to add notes about that habit

## 📊 The Impact
**Consistency compounds. Small daily wins turn into unstoppable momentum.**

| Before                  | After              |
| ----------------------- | ------------------ |
| Habits scattered everwhere | One dashboard      |
| No visual motivation    | See your streaks   |
| 3–5 min to track habits | 5 seconds          |
| Can't spot patterns     | Instant insights   |

## 💪🏻 Advanced: `Dataview` Analytics
Combine it with `Dataview` plugin to create a summary table showing your weekly and monthly habit completion rates to track if you hit your targets (eg. 80%)

<details>
<summary>📊 Click to show Dataview code for weekly/monthly analytics</summary>
```dataviewjs
const SUCCESS_THRESHOLD = 0.80;

const HABITS = [
  { file: "habits/Daily 8 glasses of water", label: "💧 8 glasses of water",        type: "daily"              },
  { file: "habits/Weekly 3 workouts",    label: "🏋️ 3 Workouts/Week",    type: "weekly", minPerWeek: 3 },
  { file: "habits/Daily 30mins reading", label: "📚 Reading (30mins)",       type: "daily"              },
];

const today      = dv.date("today");
const weekStart  = today.startOf("week");
const weekEnd    = today.endOf("week");
const monthStart = today.startOf("month");
const daysElapsedThisWeek  = Math.floor(today.diff(weekStart,  "days").days) + 1;
const daysElapsedThisMonth = Math.floor(today.diff(monthStart, "days").days) + 1;

function toDate(val) {
  if (!val) return null;
  if (val.year !== undefined) return val;
  const s = String(val);
  if (/^\d{4}-\d{2}-\d{2}/.test(s)) return dv.date(s.slice(0, 10));
  return null;
}

function weekStatus(entries, habit) {
  const thisWeek = entries.filter(d => d >= weekStart && d <= today);
  if (habit.type === "daily") {
    const done = thisWeek.length;
    const pct  = done / daysElapsedThisWeek;
    const e    = pct >= SUCCESS_THRESHOLD ? "✅" : pct >= SUCCESS_THRESHOLD * 0.75 ? "⚠️" : "❌";
    return `${done}/${daysElapsedThisWeek}d ${e}`;
  } else {
    const done   = thisWeek.length;
    const target = habit.minPerWeek;
    const e      = done >= target ? "✅" : done >= target - 1 ? "⚠️" : "❌";
    return `${done}/${target} sessions ${e}`;
  }
}

function monthStatus(entries, habit) {
  const thisMonth = entries.filter(d => d >= monthStart && d <= today);
  if (habit.type === "daily") {
    const done = thisMonth.length;
    const pct  = done / daysElapsedThisMonth;
    const e    = pct >= SUCCESS_THRESHOLD ? "✅" : pct >= SUCCESS_THRESHOLD * 0.75 ? "⚠️" : "❌";
    return `${done}/${daysElapsedThisMonth}d ${e}`;
  } else {
    const weekCounts = {};
    for (const d of thisMonth) {
      const key = `${d.weekYear}-W${String(d.weekNumber).padStart(2, "0")}`;
      weekCounts[key] = (weekCounts[key] || 0) + 1;
    }
    const weeksElapsed = Math.floor(today.startOf("week").diff(monthStart.startOf("week"), "weeks").weeks) + 1;
    const done         = Object.values(weekCounts).filter(c => c >= habit.minPerWeek).length;
    const e            = done >= weeksElapsed ? "✅" : done >= weeksElapsed - 1 ? "⚠️" : "❌";
    return `${done}/${weeksElapsed} wks ${e}`;
  }
}

const rows = [];
for (const habit of HABITS) {
  const page = dv.page(habit.file);
  if (!page) continue;
  const entries = (page.entries || []).map(toDate).filter(d => d && d <= today);
  rows.push([habit.label, weekStatus(entries, habit), monthStatus(entries, habit)]);
}

dv.table(
  ["Habit", `This Week (${weekStart.toFormat("MMM d")} – ${weekEnd.toFormat("MMM d")})`, `${monthStart.toFormat("MMMM")} (${daysElapsedThisMonth}d in)`],
  rows
);
```
</details>

**Example screenshot:**
![Screenshot 2026-07-06 at 21.23.49](../../../resources/screenshots/Screenshot%202026-07-06%20at%2021.23.49.png)

## 🎯 Quick Tips
- **Review weekly:** Every Sunday, check your dashboard and celebrate wins
- **Streaks matter:** When one breaks, just restart immediately. Momentum > perfection
- **Combine with daily notes:** Optional—some people add a habit section to their daily note, others keep it separate

## 📚 Learn More
- [Atomic Habits by James Clear](https://jamesclear.com/) — the science behind habit tracking
