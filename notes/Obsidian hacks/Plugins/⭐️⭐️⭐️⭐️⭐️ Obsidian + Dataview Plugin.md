#obsidian #plugins

# Dataview

**GitHub:** https://github.com/blacksmithgu/obsidian-dataview

## What is Dataview?

**Dataview** is the most powerful plugin for Obsidian—it transforms your vault into a **queryable database**. Instead of manually organizing notes, Dataview lets you:

- 🔍 Query your notes using JavaScript or SQL-like syntax
- 📊 Create dynamic tables, lists, and visualizations from your data
- 🔗 Pull information across multiple notes automatically
- 📈 Build dashboards that update in real-time
- 🎯 Organize and display data without touching individual files
- 🚀 Create complex relationships between notes
- 💡 Turn your vault into a personal knowledge management system

## Why Use Dataview?

**Dataview unlocks superpowers for your Obsidian vault:**

- **Dynamic organization** — No manual sorting; data updates automatically
- **Connected insights** — See relationships across your entire vault
- **Time-saving** — Query once, update everywhere automatically
- **Flexible views** — Display the same data in multiple useful ways
- **Personal database** — Transform Obsidian into a CMS for your knowledge
- **Advanced workflows** — Enable complex use cases (project tracking, reading lists, etc.)
- **Total control** — Query exactly what you need, how you need it

## Key Features at a Glance

| Feature | What It Does |
|---------|------------|
| **DQL Queries** | Query language similar to SQL for filtering and sorting |
| **JavaScript Support** | Use JavaScript for custom logic and calculations |
| **Dynamic Tables** | Create tables that pull data from your notes automatically |
| **List View** | Display query results as organized, formatted lists |
| **Inline Queries** | Embed queries within notes for dynamic updates |
| **Metadata Extraction** | Pull frontmatter, tags, and custom fields from notes |
| **Grouping & Sorting** | Organize results by any field you choose |
| **Calculations** | Perform math on your data (sum, average, count, etc.) |

## How Dataview Works

1. **Add metadata to notes** — Use frontmatter (YAML) to tag important information
2. **Write a Dataview query** — Use DQL or JavaScript syntax to ask questions
3. **Embed in a note** — Place the query in a ```dataview``` code block
4. **See results instantly** — Dataview renders a dynamic table or list
5. **Update automatically** — When you edit notes, results update instantly

## Example: A Simple Dataview Query

**Your notes with metadata:**
```markdown
---
status: completed
date: 2026-07-10
category: work
rating: ⭐⭐⭐⭐⭐
---
# Project Alpha Review
Completed the quarterly review...
```

**A Dataview query:**
````markdown
```dataview
LIST
FROM #work
WHERE status = "completed"
SORT date DESC
```
````

**Result:** A dynamic list showing:
- ✅ All work-related notes with "completed" status
- ✅ Sorted by date (newest first)
- ✅ Updates automatically when you change notes

---

## Real-World Examples

### Example 1: Book Tracking
```dataview
TABLE title, author, rating, "Read Date"
FROM #book AND status = "read"
WHERE rating
SORT "Read Date" DESC
```

**Shows:** All books you've read with authors and ratings, newest first

### Example 2: Project Dashboard
```dataview
TABLE status, deadline, priority
FROM #project
WHERE status != "archived"
GROUP BY status
SORT deadline ASC
```

**Shows:** All active projects grouped by status, sorted by deadline

### Example 3: Weekly Tasks Summary
```dataview
LIST WITHOUT ID
FROM #task
WHERE due >= date(2026-07-08) AND due <= date(2026-07-14)
GROUP BY priority
```

**Shows:** This week's tasks organized by priority level

---

## Practical Use Cases

✅ **Reading Tracker** — Track books, articles, and papers with ratings and notes
✅ **Project Dashboard** — Overview of all projects, deadlines, and status
✅ **Meeting Notes Index** — Auto-generated list of all meetings sorted by date
✅ **Financial Tracking** — Query expenses and income across notes
✅ **Learning Progress** — Track courses, completion status, and grades
✅ **Research Library** — Organize papers, sources, and citations
✅ **Habit Tracker** — Visual summary of habit completion
✅ **Content Calendar** — Plan and track blog posts, videos, tweets
✅ **Team Directory** — Maintain contact information with metadata
✅ **CRM System** — Track clients, deals, and communications

---

## DQL vs JavaScript Queries

### Simple DQL Query (Easy)
```dataview
LIST title
FROM #inbox
WHERE type = "article"
SORT created DESC
```

### Advanced JavaScript Query (Powerful)
```dataview
const result = dv.pages("#article")
  .where(p => p.status === "reading")
  .groupBy(p => p.category)
  .sort(p => -p.rating);
dv.table(["Category", "Title", "Rating"], result);
```

**DQL:** Easy, readable, great for 80% of use cases
**JavaScript:** Powerful, flexible, handles complex logic

---

## Why Dataview is Game-Changing

**Before Dataview:**
- 📝 Manually update lists and indexes
- 🔍 Manually find and organize notes
- 😫 Copy-paste data between notes
- ❌ Lists go out of sync with actual data

**After Dataview:**
- ✅ Automatic dynamic lists that always stay current
- ✅ Query your vault like a database
- ✅ Build sophisticated dashboards and views
- ✅ Save hours on manual organization
- ✅ Create relationships between notes automatically

---

## Getting Started

**Start simple:** Begin with a basic LIST query filtering by a tag
**Gradually add:** Sort, WHERE conditions, GROUP BY
**Level up:** Learn JavaScript for custom calculations
**Combine:** Mix DQL with inline queries in multiple notes

---

**Ready to unlock your vault's potential?** Continue reading for query recipes, advanced techniques, and real-world dashboard examples. 
