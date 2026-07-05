⏱️ **Reading time: 5 minutes** | #obsidian #howtos #productivity
# Obsidian Auto Daily Planner

## 🎯 TL;DR
Auto-create daily planner that creates a new timestamped note each day with built-in time blocks. Create a daily planner note in under 5 seconds with just two clicks, giving you an instant timelined planning interface.

## 📋 Prerequisites & Setup
- **[Periodic Notes](obsidian://show-plugin?id=periodic-notes)** plugin (installed & enabled)
- **[Day Planner](obsidian://show-plugin?id=day-planner)** plugin (installed & enabled)
- A designated folder for daily notes (e.g., `daily notes/` or `journal/`)
- A daily note template file (we'll create this below)

## 🤔 The Problem
Creating a daily planner from scratch every morning is friction. You either:

**Key pain points:**
- ✗ Manually type the same structure each day (headers, time blocks, etc.)
- ✗ Forget to create a new note and continue writing in yesterday's note
- ✗ Spend 2-5 minutes setting up your daily planning template instead of planning
- ✗ Miss out on the visual timeline view that helps you see your day at a glance

## 💡 The Solution
Automated daily notes with a pre-built template + visual timeline integration. This setup:

**What it does:**
1. Automatically creates a new daily note at midnight (or on-demand with one click)
2. Pre-populates the note with time blocks (e.g., 6 AM – 11 PM in hourly chunks)
3. Provides a visual timeline sidebar that shows your scheduled tasks
4. Keeps all daily plans organized in a single folder by date

## 🚀 How to Set Up

### Step 1: Install & Enable Plugins
1. Open **Settings** → **Community Plugins** → **Browse**
2. Search for **"Periodic Notes"** → Install → Enable
3. Search for **"Day Planner"** → Install → Enable

### Step 2: Configure Periodic Notes for Daily Notes
1. Go to **Settings** → **Periodic Notes**
2. Under **Daily notes**, toggle **Enable daily notes** ON
3. Set the **folder** (e.g., `daily notes`)
4. Set the **date format** (e.g., `YYYY-MM-DD` for `2025-07-05`)
5. Set **Open on startup** to ON (optional, but handy)
6. Under **Template**, point to your daily planner template (see Step 3)

### Step 3: Create Your Daily Planner Template
1. Create a new note: `daily-planner-template.md` (or similar)
2. Add this template content:

```markdown
# Daily Plan — {{date:YYYY-MM-DD dddd}}

## 📅 Overview
- **Date:** {{date:YYYY-MM-DD}}
- **Day:** {{date:dddd}}

---

## ⏰ Timeline

### 06:00 — Morning Routine
- [ ] 

### 07:00 — Deep Work Block 1
- [ ] 

### 08:00 — Deep Work Block 2
- [ ] 

### 09:00 — Meetings / Calls
- [ ] 

### 10:00 — Admin & Emails
- [ ] 

### 11:00 — Lunch Break
- [ ] 

### 12:00 — Afternoon Focus
- [ ] 

### 13:00 — Collaborative Work
- [ ] 

### 14:00 — Project Work
- [ ] 

### 15:00 — Planning & Review
- [ ] 

### 16:00 — Buffer / Overflow
- [ ] 

### 17:00 — Wrap-up
- [ ] 

### 18:00 — Personal Time
- [ ] 

### 19:00 — Evening Wind Down
- [ ] 

### 20:00 — Free Time / Rest
- [ ] 

---

## 🎯 Today's Priorities
1. [ ] 
2. [ ] 
3. [ ] 

---

## 📝 Notes
```

3. Customize the time blocks to match your typical day (or use the template as-is)

### Step 4: Configure Day Planner
1. Go to **Settings** → **Day Planner**
2. Enable **Timeline view**
3. Set **Start time** (e.g., 6:00 AM) and **End time** (e.g., 10:00 PM)
4. Adjust **task indicator** if desired (these are the `- [ ]` checkboxes in your template)

### Step 5: Test It Out
1. Open **Command Palette** (`Cmd/Ctrl + P`)
2. Search for **"Create today's daily note"** (from Periodic Notes)
3. Your new daily planner opens with all time blocks pre-populated ✅
4. Next time, just use the hotkey or click the ribbon icon

## 🚀 Speed Tip: Create a Hotkey
To make it truly 5-second fast:
1. Go to **Settings** → **Hotkeys**
2. Search for **"Create today's daily note"**
3. Assign a hotkey (e.g., `Cmd+Shift+D`)
4. Now press your hotkey → done in 2 seconds!

## 📊 The Impact
Once set up, this workflow eliminates morning friction:

| Metric | Before | After |
|--------|--------|-------|
| Time to create a daily planner | 3–5 minutes | 5 seconds |
| Consistency (notes created daily) | 60–70% | 95%+ |
| Visibility into time blocks | Manual search | Instant timeline sidebar |
| Daily plan abandonment | High | Low (it's ready to go) |

## 📚 Learn More

