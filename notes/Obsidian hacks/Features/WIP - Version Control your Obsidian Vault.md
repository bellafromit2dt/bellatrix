⏱️ **Reading time: 5 minutes** | #obsidian #howtos #productivity
# Obsidian Auto Version Control

## 🎯 TL;DR
Use the Obsidian Git and Link Converter plugins to automatically commit and push your vault changes to GitHub, creating a complete version history of your notes with proper link formatting for cross-platform compatibility.
**Get started in 5 minutes --- just follow this guide!**

## 📋 Prerequisites & Setup
 - [⭐️⭐️⭐️⭐️ Obsidian + Git Plugin](⭐️⭐️⭐️⭐️%20Obsidian%20+%20Git%20Plugin.md)
 - [⭐️⭐️⭐️ Obsidian + Link Converter Plugin](⭐️⭐️⭐️%20Obsidian%20+%20Link%20Converter%20Plugin.md)

## 🤔 The Problem
Notes in your Obsidian vault are crucial knowledge assets, but they're often stored only locally. Without version control, you lose the ability to track changes, recover older versions, or maintain a backup in case of data loss. Additionally, Obsidian's native wiki-links may not render properly on GitHub, making your vault inaccessible or poorly formatted when shared externally.

**Key questions or pain points:**
- How do I maintain a complete history of changes to my notes?
- What happens if I accidentally delete important notes or need to revert to a previous version?
- How can I share my vault on GitHub while ensuring links work properly across platforms?

## 💡 The Solution
This solution combines two powerful Obsidian plugins to create an automated version control system for your vault. The **Obsidian Git Plugin** handles the Git operations—tracking changes, committing updates, and pushing to your remote GitHub repository. Meanwhile, the **Link Converter Plugin** ensures that Obsidian's wiki-link syntax (`[note-name](note-name)`) is converted to standard markdown links (`[note-name](note-name.md)`) for proper rendering on GitHub and other platforms.

**What it does:**
1. **Automatically commits vault changes** — The Git plugin monitors your vault and creates regular commits with timestamped messages, building a complete version history without manual intervention
2. **Pushes updates to GitHub** — All commits are automatically synced to your remote repository, ensuring your notes are backed up and accessible from anywhere
3. **Converts links for compatibility** — The Link Converter plugin transforms internal wiki-links to markdown format, ensuring your vault displays correctly on GitHub and external tools

## 🚀 How to Set it Up
### Step 1: Install and Configure the Obsidian Git Plugin
1. Open Obsidian and go to **Settings → Community plugins**
2. Search for and install the **Obsidian Git** plugin (by Denis Yalunin)
3. Enable the plugin and configure in **Settings → Obsidian Git**:
   - Set **Commit Author** to your name and email
   - Enable **Auto pull** to fetch remote changes on startup
   - Enable **Auto push** after commit (set interval, e.g., every 5 minutes)
   - Set commit message format (e.g., "vault backup: {{date}}")
4. Initialize your vault as a Git repository (use terminal: `git init` in your vault root)
5. Add your GitHub remote: `git remote add origin https://github.com/yourusername/vault.git`

### Step 2: Set Up Your GitHub Repository
1. Create a new repository on GitHub (public or private, as you prefer)
2. Push your initial vault commit: `git push -u origin main`
3. Verify the remote connection is working with the Git plugin's push button in the command palette

### Step 3: Install and Configure the Link Converter Plugin
1. Go to **Settings → Community plugins** and search for **Link Converter**
2. Install and enable the plugin
3. Configure in **Settings → Link Converter**:
   - Set conversion format to **Markdown** (to convert `[wiki-links](wiki-links)` → `[text](link)`)
   - Enable **Auto-convert on file save** if you want automatic link conversion
   - Alternatively, manually convert links using the command palette when needed

## 📊 The Impact
With auto-sync enabled, your vault becomes a living, versioned knowledge base. You gain peace of mind knowing every change is tracked and backed up, can collaborate with others through GitHub, and maintain a professional, shareable vault. The combination of Git's powerful version control with proper link formatting ensures your second brain is both secure and accessible.

| Metric | Before | After |
|--------|--------|-------|
| Data Loss Risk | High (local only) | Minimized (GitHub backup) |
| Change Recovery | Impossible | Full history with timestamps |
| GitHub Compatibility | Links broken | Links properly formatted |
| Manual Backup Effort | Required after each session | Automatic (every 5 min) |
| Collaboration Capability | Not possible | Enabled via Git branches |

## 📚 Learn More
- [⭐️⭐️⭐️⭐️ Obsidian + Git Plugin](⭐️⭐️⭐️⭐️%20Obsidian%20+%20Git%20Plugin.md) — Full documentation on configuring the Git plugin for your vault
- [⭐️⭐️⭐️ Obsidian + Link Converter Plugin](⭐️⭐️⭐️%20Obsidian%20+%20Link%20Converter%20Plugin.md) — Details on link formatting and compatibility options
- [Obsidian Git Plugin GitHub](https://github.com/denolehov/obsidian-git) — Official repository with advanced configuration options
- [Link Converter Plugin GitHub](https://github.com/ozntel/obsidian-link-converter) — Source code and feature documentation
- [GitHub Markdown Guide](https://guides.github.com/features/mastering-markdown/) — Best practices for displaying Markdown on GitHub
