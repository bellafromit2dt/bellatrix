> [!info] The goal of this document is to help you build an automated workflow in your `Obsidian` vault to automatically retrospect your day against your pre-defined personal goals.

## Context
Many people (like me) maintain daily planners—structured files that track activities in time-blocks, accomplishments across areas like health, wealth, life, work, personal projects, etc. 

Separately, they might have personal manifesto or goals documents with their values, long-term goals, strategy, priorities written for AI to gain background knowledge about them for personalised responses.

---
## Problem
These two systems exist in isolation. At day's end, reviewing your daily planner tells you _what you did_, but doesn't tell you _whether you moved toward your stated goals and values_. 

Besides, manual daily retrospectives are time-consuming, often shallow, and miss the deeper patterns and meta-insights like 
- Whether today's activities align with your long-term strategy
- Recurring patterns (productive or limiting) that compound over time
- Opportunities or misalignments you're blind to
- How today's choices connect to your larger vision

We need a systematic way to synthesize those daily logs _against_ your personal goals and values, generating insights that show:
- What's working (progress toward goals)
- What's not (activities working against your priorities)
- Patterns you're missing
- how today's actions compound toward your 3-year/5-year vision.
- Clear next steps
---
## Solution
`/retro-my-day` is an automated **Daily Synthesizer** that:
1. Reads your goals, values etc from your `personal context file`.
2. Analyzes your `timelined daily planner file [Date].md` (completed tasks + personal reflections) 
3. Generates a structured, insightful retro that identifies themes, patterns, and progress towards your personal goals
4. Flags misalignments and opportunities
5. Provides encouraging, actionable next-step recommendations
6. Saves retro file with a timestamped name `[Date]-retro.md`
---
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


