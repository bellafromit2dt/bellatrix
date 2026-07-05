⏱️ **Reading time: 5 minutes** | #obsidian #howtos #productivity
# Obsidian Auto Daily Planner

## 🎯 TL;DR
Create timestamped daily planner in seconds, skipping the mental overhead of daily setup and freeing your brain for meaningful work only.

## 📋 Prerequisites & Setup
- [[Obsidian + Daily Notes Plugin]] (Obsidian built-in) -- enabled & configured
- [[Obsidian + Day Planner Plugin]] (community plugin) -- installed & enabled & configured
- A **daily planner template** file (instructions below)

## 🤔 The Problem
**Manually planning your day wastes time and reduces consistency**.

**Key pain points:**
- Manually recreating the same structure each day (headers, time blocks, etc.)
- Accidentally continuing to yesterday's note and become unorganised
- Spending 2-5 minutes on setup instead of planning and prioritising tasks
- Missing the visual timeline view that shows your entire day at a glance

## 💡 The Solution
**Use automated daily notes with a pre-built template and visual timeline.**

**What it does:**
1. Creates new daily note on-demand with one click
2. Pre-fills the note with hourly time blocks (e.g. 6 AM – 11 PM in hourly chunks)
3. Displays a visual timeline sidebar showing all scheduled tasks
4. Keeps all daily plans organized in one folder by date

## 🚀 How to Set Up

### Step 1: Install & Enable Plugins
1. Open **Settings** → **Core Plugins** → Find **"Daily Notes"** → Enable 
2. Open **Settings** → **Community Plugins** → **Browse** → Find **"Day Planner"** → Install → Enable

### Step 2: Configure "Daily Notes" Plugin
This plugin automatically creates daily note using a template 
1. Go to **Settings** → **Daily Notes** 
2. Set **date format** for naming the daily notes (example: `YYYY-MM-DD` creates `2026-07-05.md`)
3. Set **folder** for daily notes (e.g. `daily notes/`)
4. Set daily note **template** (e.g. `templates/daily-planner-template`)

### Step 3. Create Your Daily Planner Template
1. Create a new note named `daily-planner-template.md` in your templates folder
2. Add content in your template, for example:
```markdown
# ⏰ Day planner
- [ ] 06:00 - 07:00
- [ ] 07:00 - 08:00 
- [ ] 08:00 - 09:00
- [ ] 09:00 - 10:00
- [ ] 10:00 - 11:00
- [ ] 11:00 - 12:00
- [ ] 12:00 - 13:00
- [ ] 13:00 - 14:00
- [ ] 14:00 - 15:00
- [ ] 15:00 - 16:00
- [ ] 16:00 - 17:00
- [ ] 17:00 - 18:00
...

## 🎯 Today's Priorities
- [ ] 
- [ ] 
- [ ] 

## 📝 Notes
```
- These time blocks will automatically appear in the visual timeline 
3. Adjust the time blocks to match your typical daily schedule

### Step 4: Configure "Day Planner" Plugin
This plugin creates a timeline view of all your tasks in a day
1. Go to **Settings** → **Day Planner** 
2. Enable **Timeline view**
3. Set **Start time** (e.g., 6:00 AM) and **End time** (e.g., 10:00 PM)
4. Set **task indicator** to match the checkboxes in your template ( `- [ ]`)
5. Enable **Sort tasks in planner chronologically after edits**
6. Optional: Configure "First day of Week", "Date Time Format", or "Planner heading text"

### Step 5: Test It Out
1. Click "Open today's daily note" ribbon icon (left sidebar) to open today's planner
2. Verify that your template `daily-planner-template.md` loads with all time blocks pre-filled
3. Click the "Timeline" ribbon icon (right sidebar) to see the visual timeline

## 📊 The Impact
Once configured, this workflow eliminates daily planning friction:

| Metric                            | Before        | After                    |
| --------------------------------- | ------------- | ------------------------ |
| Time to create a daily planner    | 3–10 minutes  | 5 seconds                |
| Consistency (notes created daily) | 30–70%        | 95%+                     |
| Visibility into time blocks       | Manual search | Instant timeline sidebar |
| Daily plan abandonment            | High          | Low (it's ready to go)   |

## 📚 Learn More
- [[Obsidian Auto Daily Retro]]

