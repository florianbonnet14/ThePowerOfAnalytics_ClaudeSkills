# The Power Of Analytics - Claude Skills
This folder contains a list of skills helping anyone to automatize crucial steps with regards to the analysis of their product performance and customer behaviors. The skills are based on my book The Power of Analytics, published in June 2025.

Here are all the available skills:

  | Skill | Description |                                                                                                                                      
  |-------|-------------|                                                                                                                                      
  | **analytics-orchestrator** | Intelligent entry point to the analytics ecosystem. Guides you to the right agent based on your needs. |                      
  | **north-star-metric-agent** | Helps identify and validate your single most important metric (North Star Metric). |                                         
  | **kpi-tree-architect** | Builds comprehensive KPI trees by decomposing metrics into hierarchical driver structures. |                                      
  | **analysis-planner** | Structures analysis investigations before diving into data, preventing wasted time. |
  | **cohort-analysis-specialist** | Tracks customer behavior over time by grouping customers based on shared characteristics. |
  | **segmentation-expert** | Identifies and analyzes customer segments to uncover hidden patterns. |
  | **influential-factors-detective** | Identifies qualitative factors influencing KPIs that can't be measured as numbers. |
  | **analysis-results-collector** | Transforms data collected into structured, communication-ready documentation while challenging findings and pushing for clarity of arguments. |
  | **executive-summary-writer** | Transforms findings into clear executive summaries using the MAIN framework. |
  | **presentation-builder** | Converts analysis documents into structured presentation slide plans. |

Each skill can be used independently but you can also call the analytics-orchestrator skill to help you figure out what you need.

# Getting Started
## Install Claude Code

Follow the instruction of Anthropic on their install page: `https://code.claude.com/docs/en/setup`.

## Installing the skills

Create a folder in your Documents or anywhere related to your project. 
Then create a `.claude` folder under which you will create a `skills` folder. You can do so manually or via terminal commands.

<img width="1043" height="559" alt="Screenshot 2026-02-15 at 22 14 04" src="https://github.com/user-attachments/assets/476528ec-bc6f-4cc9-9a1d-ec5ba678b461" />

Once you have done that, download the folder in this repo and paste them into the newly created `skills` folder.

<img width="745" height="450" alt="Screenshot 2026-02-15 at 22 14 47" src="https://github.com/user-attachments/assets/d13993de-ce2a-48f6-a897-ff2a53eb1144" />

## Launching Claude Code

If you have not done so open a Terminal and go to your folder using the cd command (in my case `cd Documents/test_demo_tPoA_skills`).
There just tap the command `claude` to open Claude Code.

## Using skills

Each tutorial shows you how to launch each skills but simply a skill is launche dusing the `/` command. 
When you type `/` you will see a list of skills appear and you can use arrows to select the one you want or just type the full name.

<img width="871" height="385" alt="Screenshot 2026-02-15 at 22 23 48" src="https://github.com/user-attachments/assets/dea0b7fe-0959-413d-86c7-ec2eda83d5f5" />

You can see the list of skills also by asking Claude.

<img width="864" height="687" alt="Screenshot 2026-02-15 at 22 23 20" src="https://github.com/user-attachments/assets/730efea3-32f5-4fa7-84b6-574b8f159669" />

I recommand you reading Claude Code documentation as well at some point.

## Pointing to files

During your conversation with Claude you might want to point to a specific file in your folder(s).
To do so use the `@` command e.g `Use the @kpi_tree.md file for the analysis`.

