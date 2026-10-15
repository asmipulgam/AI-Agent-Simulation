# AI Agent in Production: A Chain of Consequences

A decision-driven simulation where each choice about an AI agent's permissions and actions changes the system state, creating cascading consequences for security, data integrity, and recovery.

**▶ Play it here:** https://YOUR-USERNAME.github.io/ai-agent-simulation/

---

## The scenario

You are the Head of Operations at **Brightleaf Market**, an online grocery store with 50,000 customers. The company is about to give an AI agent named **Atlas** real access to its systems: answering customers, issuing refunds and maintaining the order database.

You make 12 decisions about how Atlas is set up and run. The system remembers each choice, and later events check those choices. The same attack can be blocked or succeed, and the same mistake can be a near miss or a disaster, depending on what you decided earlier.

No technical background is needed. Every decision includes an "In plain English" explanation, and the site has a built-in glossary.

## How it plays

| Phase | What happens |
|---|---|
| **I · Build the Agent** | Choose Atlas's access level, login, when a human must approve, logging, backups and launch plan. |
| **II · Go Live** | Launch week, pressure from the CEO to scale up, a "poisoned email" (prompt injection) attack, and Atlas asking for more power. |
| **III · Crisis & Recovery** | At 2 AM, Atlas starts deleting 48,000 orders. Your earlier choices decide whether this is a disaster or a near miss. Then you respond, recover and communicate. |
| **IV · Debrief** | See your scores, how your choices connected, and how you compare with a safer path. |

## What you're scored on

Five scores start at 50 and move with every decision and consequence:

- 🛡️ **Security**: how well the system keeps attackers and accidents out
- 🗄️ **Data Integrity**: whether the company's information is still correct and complete
- 🛟 **Recovery Readiness**: how quickly you can undo damage
- ⚡ **Productivity**: how much useful work the agent gets done
- 🤝 **Customer Trust**: whether customers still believe in the company

Live gauges also track **Blast Radius** (how much damage Atlas could do), **Visibility** (whether you would see problems) and **Undo Power** (how well you could restore data).

## Features

- **Choice-driven chain of consequences:** earlier decisions change how later events turn out
- **Animated illustration** that reacts to the system's state: the shield weakens, the database cracks, and data visibly leaks during a breach
- **Debrief analytics:**
  - an overall score gauge and a letter grade for each score
  - a domino diagram of which links in the chain fell
  - a line chart of all five scores over time
  - a radar chart and bar comparison against a safer path
  - a timeline of your choices and what they caused
  - lessons based on your own choices
- **Player profiles:** for example "The Trusted Architect", "The Move-Fast Gambler" or "The Fortress Keeper"
- **Exports:** download your results (.txt) and a certificate of completion (.png)
- Light and dark themes, a mobile-friendly layout, and progress saved in your browser

## Key ideas you'll learn

Least privilege · separate identities for AI agents · human-in-the-loop approval · audit logging and alerts · tested backups · staged rollouts · rate limits · prompt injection defences · kill switches · blameless postmortems

## Run it locally

No installation or build step is needed. Download or clone the repo and open `index.html` in any modern browser.

```bash
git clone https://github.com/YOUR-USERNAME/ai-agent-simulation.git
cd ai-agent-simulation
open index.html        # macOS. On Windows, double-click index.html
```

## Project structure

```
index.html   page shell
styles.css   layout, light/dark themes, animations
app.js       simulation engine, scenarios, scoring, charts and illustrations
```

The project is plain HTML, CSS and JavaScript with no frameworks or libraries. All illustrations and charts are drawn in code (SVG), so there are no third-party image licensing issues.

## Credits

Inspired by the structure of [Data Center Genesis](https://sunburnedship.github.io/Responsible-Data-Center-Genesis/).
Brightleaf Market and Atlas are fictional.
