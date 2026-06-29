## Context

## Problem
Manual daily retrospectives are time-consuming, often shallow, and miss the deeper patterns and meta-insights. Without systematic synthesis against your stated goals and strategy, you can't easily spot misalignments, recurring behavioral patterns, or how today's actions compound toward your 3-year/5-year vision.
## Solution
`/retro-my-day` is an automated **Daily Synthesizer** that:
1. Reads your goals, values, and strategy from your `personal context file`.
2. Analyzes your `timelined daily planner file` (completed tasks + personal reflections) from your `[Date].md`
3. Generates a structured, insightful retro that identifies themes, patterns, and progress towards your personal goals
4. Flags misalignments and opportunities
5. Provides encouraging, actionable next-step recommendations
6. Saves a timestamped retro as `[Date]-retro.md`
## Steps
### Preparation
- Install [[Obsidian + Claudian Plugin]]
- Install [[Obsidian + Cron Plugin]]
- Have your `personal context file ready`
	- Example: 
	```
	```
- Have your `timelined daily note file` ready
	- Example:
	```
	```  
### Execution
#### Create /retro-my-day Claudian Command
- Go to Claudian settings
- Create a Claudian command that retros the day: /retro-my-day
- Configure the command with personalised prompt: 
	- input and output file folder locations, file format, content, etc
	- Example:
```
```
#### Create a Daily Cron Job for /retro-my-day Command
- Go to Cron settings
- Create a new cron job to trigger /retro-my-day command on a daily basis
- Screenshot
## Conclusion
Now you have a cron job that triggers daily to automatically retro your daily planner and give you a insightful summary of your day,  


