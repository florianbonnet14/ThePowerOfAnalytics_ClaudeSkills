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

In the step by step mode, the Architect will first help you define the first layer of KPIs behind the North Start Metric.
After that, it is build-your-own-adventure: you can go deep into one KPI and build 2, 3, 4 layers for it; or build the 2nd layer for all 1st layer's KPIs before going deeper. You are in charge. 

In our Buildr example the Architect starts with offering two possible ways to decompose the North Star Metric.

<img width="780" height="560" alt="KPI Tree Manual 1" src="https://github.com/user-attachments/assets/e20e82b6-312e-496c-8746-094cff15ef8c" />

It does not let me choose blindly and asks a refining question to make a recommendation which is the value of this Architect: it is a copilot. After selecting the way to decompose the metric, the Architect makes a first recommendation on the the 1st Layer of the KPI Tree/.

<img width="779" height="560" alt="KPIT Tree Manual 3" src="https://github.com/user-attachments/assets/68debe6a-87f4-4a2b-95ab-564086d1f71c" />

I am happy with that so I ask it to move on and decompose the Build Rate.

<img width="779" height="560" alt="KPIT Tree Manual 3" src="https://github.com/user-attachments/assets/2b7cbb9f-e6d8-457f-9e71-3d4183d8af13" />

Note that agian it asks clarifying question as the Architect is made to challenge you and make sure you cover all the blindspots.
After that it makes you a proposal which can challenge for how many times as you want before moving forward.

<img width="786" height="661" alt="KPI TRee Manual 4" src="https://github.com/user-attachments/assets/2031b326-7ff6-4a51-ac1e-9e330d509458" />

# Saving and Iterate

You can save your progress at anytime by letting know the Architect and Claude Code you want to stop.

<img width="762" height="525" alt="KPI Tree Manual save" src="https://github.com/user-attachments/assets/420ff99e-113e-4436-8a55-64949d24151e" />

When you are ready to continue, just open Claude code and mention you are ready to start agina on the KPI decomposition.
The Architect should be involed again and the file you saved should be found. You can also proactively summon them using a command alike `Hey /kpi-tree-architect let's resume the KPI tree work where we let it off @KPI_tree.md`.

# Next steps
Once you have a KPI Tree you have several options:
* Use the `influential-factor-detective` to refine the influential factors list of certain KPIs
* Use the `analysis-planner` to help you throroughly plan the analysis of a metric over/under-performance or customer behavior. This skill will rely heavily on the KPI Tree to suggest you the right data deep dives.



