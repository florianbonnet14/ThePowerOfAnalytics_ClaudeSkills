The KPI Tree Architect is here to help you define the drivers behind your North Star Metric Performance.
It is powered by the content of my book The Power of Analytics (see Chapter 2) and years of experience in that exercise.
Note that there are may ways to breakdwon a North Star metric into drivers so I created two modes:
* Full automation - the Architect define the entire KPI tree in oen go afer asking you questions
* Step-by-Step - Each layer and metric is defined through discussions

Note that even after a full automation you can discuss with the Architect and refine the KP Tree as you see fit

# Getting Started

Launch the KPI Tree Architect using the `/kpi-tree-architect` command.

<img width="772" height="514" alt="KPI Tree manual open" src="https://github.com/user-attachments/assets/8981d611-ca13-433f-ad73-fda18e1512c7" />

As you can see it asks for a North Star Metric. Refer to it using the `@` command.
You can also launch the Architect mentionning directly the file e.g. `Hey /kpi-tree-architect help me define the KPI tree of my North Star Metric defined in @North-Star.md`.
Note as well that if you launch the Architect within the same Claude Code session as the one where you defined your North Star Metric,
the Architect will find the file on its own.

<img width="762" height="543" alt="KPItree 1" src="https://github.com/user-attachments/assets/73f2c94e-bf1f-40de-b644-3f9e9c5a8ef4" />

# Full Automation mode
In full automation the Architect will ask few questions before going at it.

<img width="768" height="542" alt="KPI Tree 1-3" src="https://github.com/user-attachments/assets/b033a1d1-85e4-4b34-8828-b97b454f2ffb" />

Then once it got what it needs it will be thinking for a while and produce an entire KPI Tree.

<img width="768" height="662" alt="KPI Tree 4 full" src="https://github.com/user-attachments/assets/b2454a9d-6861-4305-970f-8ed865c53c55" />

You will note that the KPI tree contains layers of branches and leafs and that ceertain leafs have a magnifier symbol.
These are called Influential Factors: elements of the experience that cannot always be measured but impact a metric.
For example a Subject Line in an email will impact the Open Rate. to learn more about Influential Factors, go to Chpater 8 of my book.
I also made a skill to help you find more of the influential factors of a KPI (See the `influential-factors-detective`).

<img width="464" height="114" alt="KPI Tree 4 influential" src="https://github.com/user-attachments/assets/02c58141-80f1-42d9-b9bd-c711b1020891" />

Below the KPI Tree, the Architect will give you elements of rationale behind the decomposition.

<img width="776" height="621" alt="KPI Tree 5 explanations" src="https://github.com/user-attachments/assets/7e09bba9-d101-4af9-b7cc-f5e98fbed3f8" />

The Architect will also offer you to amend/change/complete the KPI Tree. Feel free to do so.
If you are happy with it or just want to save ti for further iteration ask the Architect to save the work.

<img width="783" height="522" alt="KPI Tree 6 save" src="https://github.com/user-attachments/assets/d9e2519a-6011-4a97-86ec-947c27ff79ed" />

You will obtain a markdown file that contains all the elments printed in the Terminal.
<img width="719" height="466" alt="KPI Tree Folder File" src="https://github.com/user-attachments/assets/8e332793-e8b5-4a6a-ad90-70acc8990867" />

| | |
|:-------------------------:|:-------------------------:|
| <img width="363" height="235" alt="KPI Tree file 1" src="https://github.com/user-attachments/assets/257d1c39-8511-4406-8968-94b0b4aef3b2" />
| <img width="363" height="232" alt="KPI Tree file 2" src="https://github.com/user-attachments/assets/76f113ab-4d44-4b19-9f60-3810d5d6cf47" />
|

# Step-by-Step


