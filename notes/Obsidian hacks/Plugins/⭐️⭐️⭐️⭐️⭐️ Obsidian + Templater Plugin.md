#obsidian #plugins

## What is Templater?

**Templater** is a powerful Obsidian plugin that lets you create **dynamic templates** with custom commands, functions, and JavaScript. Instead of just static boilerplate text, you can build templates that:

- 📅 Automatically insert dates, times, and dynamic content
- 🔗 Pull data from your vault (titles, metadata, linked notes)
- ⚙️ Run custom JavaScript to transform and generate content
- 🎯 Ask you for input and customize templates on the fly
- 🚀 Execute shell commands and integrate with external tools

## Why Use Templater?

**Templater saves time and reduces friction:**

- Create consistent notes without manual formatting
- Automatically populate metadata and frontmatter
- Generate daily notes, meeting notes, or project templates with one click
- Keep your vault organized by enforcing structure automatically
- Eliminate repetitive typing—let templates do the work

## Key Features at a Glance

| Feature | What It Does |
|---------|------------|
| **Template Variables** | `<% tp.file.title %>`, `<% tp.date.now() %>` - insert dynamic content |
| **User Input** | `<% tp.system.prompt() %>` - ask for user input when creating notes |
| **File Operations** | Access and manipulate files in your vault |
| **Date/Time Functions** | Format dates, create recurring schedules |
| **JavaScript Support** | Write custom logic for complex templates |
| **Folder Templates** | Auto-apply templates based on folder structure |
| **Hotkeys** | Trigger templates with keyboard shortcuts |

## How It Works

1. **Write a template** — Create a `.md` file with Templater commands mixed in
2. **Use Templater syntax** — Wrap dynamic content in `<% ... %>` or `<%= ... %>`
3. **Trigger it** — Create a new note from your template via:
   - Command palette (`Templater: Create new note from template`)
   - Hotkey
   - Folder auto-template
4. **Content fills in** — All the dynamic parts execute and populate your note

## Example: A Simple Template

```markdown
# <% tp.file.title %>

**Created:** <% tp.date.now("YYYY-MM-DD HH:mm") %>
**Status:** 🚀 In Progress

## Summary
<% tp.system.prompt("What's this note about?") %>

## Tasks
- [ ] 

## Tags
#template/basic
```

When you create a note from this template:
- ✅ Title is auto-filled
- ✅ Current date and time are inserted
- ✅ You're prompted to enter a summary
- ✅ Everything else stays as-is

