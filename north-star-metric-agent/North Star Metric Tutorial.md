
The North Star metric agent is here to help you find the North Star Metric of your company or your team.
To learn everything about North Star metrics, why they are crucial, and how to use them I recommend you
to read Chapter 2 of my book "The Power of Analytics" (available on Amazon - paperback and Kindle)

In this tutorial, we play the role of the PM in charge of the Onboarding team at Buildr, a fictional Lovable competitor. 

# Launch
To launch the skill use the /north-star-metric-agent command in Claude Code. 
The agent will start asking you questions about your company and/or team in order to guide in finding the right North Star Metric.

<img width="774" height="548" alt="NS cmd" src="https://github.com/user-attachments/assets/cccedae2-0d6e-43bc-8c88-64959281097a" />

# Converging on a North Star Metric

You just need to converse with the agent to give him the details it needs to help. 
In this example we just need to answer couple of questions due to the simplicty of our perimeter.
When the agent is ready it will make you proposals.

<img width="766" height="547" alt="NS 2" src="https://github.com/user-attachments/assets/ec101009-76f7-4184-aa67-ce30fd566366" />

You can accept one or just challenge it until you are satisfied.
In this example we merged two proposal to fit what we believe is a good North Star Metric for the team.

<img width="760" height="548" alt="NS 3" src="https://github.com/user-attachments/assets/a52ab653-fa48-4e5e-b66a-8f1a43e5cb14" />

Note that the agent will also challenge you back and bring useful perspective to your North-Star Metric as seen on the last question in the screenshot above.
Simply bring your own facts/thoughts and try to agree on what is the best for you.
In the example, the agent is right to challenge the number of visits and identified perfectly a caveat of our metric, caveeat we have to live with for the moment.

<img width="788" height="542" alt="NS 4" src="https://github.com/user-attachments/assets/e48da025-91ac-47aa-b439-d9d3e0bfac66" />

# Saving your North Star Metric and the reasoning behind it

Once you are ready, the agent should offer you to save the North Star Metric and document the reasoning in a .md file.
Just say yes (tap 1 in the multiple choice UI). 

<img width="771" height="546" alt="NS 5" src="https://github.com/user-attachments/assets/f53ff2fc-cfea-4650-8614-c2a1a7aaf27b" />

<img width="768" height="544" alt="NS 6" src="https://github.com/user-attachments/assets/162af94d-a8d2-4dff-962b-b6293af9ae85" />

It can be than on some rare occasion the agent doesn't propose it. 
In that case, or if you want to save your progress in the middle of the discussion, just ask the agent to save the progress until next time.

## The file you will obtain
The file is markdown file you can open with any tool of you choice (here Obsidian).
What it contains is:
 * The Customer Journey the metric represent
 * The rationale behind the choice made
 * The rating of the metric against the 4 criterias making a good North Star Metric (See Chapter 2 of my book The Power of analytics for details)
 * Some placeholder for benchmark values
 * An attemps at 1st layer of KPI Tree (See KPI Tree Architect for a better way though)
 * Known limitations of the exisitng North Star Metric
 * Proposed next steps in terms of measurement etc

| | |
|:-------------------------:|:-------------------------:|
|<img width="364" height="248" alt="NS File 1" src="https://github.com/user-attachments/assets/5958ce18-7ada-4cf3-a1a2-dd24d00b0370" />|<img width="362" height="262" alt="NS File 2" src="https://github.com/user-attachments/assets/6a4fee26-5c57-425b-8139-d14da880667b" />|
|<img width="362" height="260" alt="NS File 3" src="https://github.com/user-attachments/assets/8aa111fe-0cf0-4680-b3a4-29c6124efe12" />|<img width="363" height="236" alt="NS File 5" src="https://github.com/user-attachments/assets/0b860fa2-ce93-47bf-bfd1-e890426fce89" />|

# Iterating
North Start Metrics can evolve over time (See Chapter 2 of my book).
If you want to iterate on your North Star Metric, just launch the agent again, mentionning your existing file using the `@` command.
From there explain why you want to change it and the new info at your disposal.

# Next Steps
Once you have a North Star Metric to measure the main outcomes you want to generate as a team, you need a KPI Tree.
A KPI Tree is the decomposition of your North Star Metrics into its fundamental drivers. 
A crucial tool to be finished with the enless question "Why did th emetric go up/down?"
