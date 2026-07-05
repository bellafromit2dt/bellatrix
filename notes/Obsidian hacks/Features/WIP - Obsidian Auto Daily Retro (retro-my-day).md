#obsidian  #howtos 
#### Pre-requisites
- [Obsidian + Claudian Plugin](../Plugins/Obsidian%20+%20Claudian%20Plugin.md)
- [TODO - Obsidian Auto Daily Planner](TODO%20-%20Obsidian%20Auto%20Daily%20Planner.md)
#### References
- [TODO - retro-my-day](../../Claude%20skills/TODO%20-%20retro-my-day.md) for example command

# Obsidian Auto Daily Retro (retro-my-day)
> **This document help you set up a scheduled daily automation to generate insightful summary of your day based on your daily notes and surface how your actions align with your personal goals.** 
>  
>  **Let's hold ourselves accountable for our future.**

## Context
Many people (maybe, like me for instance) maintain daily planners —structured files that track activities in time-blocks, accomplishments, miss-outs, reflections across areas like health, wealth, life, work, personal projects, etc. (see [TODO - Obsidian Auto Daily Planner](TODO%20-%20Obsidian%20Auto%20Daily%20Planner.md) for examples) 

Separately, they might have personal manifesto or goals documents with their values, long-term goals, strategy, priorities written for AI to gain background knowledge about them for personalised responses.

## Problem
These two systems exist in isolation. At day's end, reviewing your daily planner tells you **_what you did_**, but doesn't tell you **_whether you moved toward your stated goals and values_**. 

Besides, manual daily retrospectives are time-consuming, often shallow, and miss the deeper patterns and meta-insights like 
- Whether today's activities align with your long-term strategy
- Recurring patterns (productive or limiting) that compound over time
- Opportunities or misalignments you're blind to
- How today's choices connect to your larger vision
etc.

**I needed a systematic way to synthesize those daily logs _against_ my personal goals and values**, generating insights like:
- What's working (progress toward goals)
- What's not (activities working against your priorities)
- Patterns I was missing
- how today's actions compound toward your 3-year/5-year vision.
- Clear next steps

## Solution
`/retro-my-day` (see example prompt [TODO - retro-my-day](TODO%20-%20retro-my-day.md) ) command is an automated **Daily Synthesizer** command I created within `Claudian` plugin that:
1. Reads my goals, values etc from my `personal context file`.
2. Analyzes my `timelined daily planner file titled with [Date].md` (completed tasks + personal reflections) 
3. Generates a structured, insightful retro that identifies themes, patterns, and progress towards my personal goals
4. Flags misalignments and opportunities
5. Provides encouraging, actionable next-step recommendations
6. Saves retro file with a timestamped name `[Date]-retro.md` in my designated folder
Better yet, I chained it with `Cron` plugin, which triggers this `/retro-my-day` command automatically at 10pm each night to generate my retro for me to review before bed. 

## Steps
### Preparation
- Install [Obsidian + Claudian Plugin](../Plugins/Obsidian%20+%20Claudian%20Plugin.md)
- Have your `personal context file` ready
	- Have a `me.md` file with your goals, values, strategy, etc. listed
	- Example: 
	```
	```
- Have your `timelined daily note file` ready
	- Keep your daily notes `[date].md` files in a folder to track the timelined activities --- see [TODO - Obsidian Auto Daily Planner](TODO%20-%20Obsidian%20Auto%20Daily%20Planner.md)
	- Example:
	```
	```  
### Execution
#### Create `/retro-my-day` Claudian Command
- Go to Claudian settings
- Create a new `Claudian` command that retros the day: `/retro-my-day`
- Configure the command with personalised prompt: 
	- input and output file folder locations, file format, content, etc
	- Example:
```
```
#### Auto-generate retro with `/retro-my-day` in Claudian
- Open a Claudian window, execute this command and it will auto-generate your retro file in your designated folder
- Review your generated daily retro. 
- If it's not quite what you wanted, provide feedback to Claudian to improve the content, structure, or format — in the end, don't forget to tell Claudian to update the `/retro-my-day` skill based on your new feedback, so the same instructions will be applied for your future retros.
## Summary
Reviewing and writing short retro used to eat at least 15 minutes daily for me, now just 1 minute to review and tweak the auto-generated version. 14 minutes reclaimed every day, that's 98 minutes per week, or 7 hours per month... and compounding.



