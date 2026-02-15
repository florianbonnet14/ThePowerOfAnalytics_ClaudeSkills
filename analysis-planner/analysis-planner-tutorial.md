The Analysis Planner is here to help you plan which metric to analyse, which data to collect and how to look at them in order to understand your problem at hand.
It leverages the content of my book The Power of Analytics so if you want to improve your own skills go there to learn more about how to run a good analysis.

# Getting Started

To launch the Analysis Planner just type the command `/analysis-planner`.

<img width="870" height="605" alt="AP launch" src="https://github.com/user-attachments/assets/8dfd31e7-7777-410f-8bdd-b9d0585fe040" />

You will be asked about the decision you need to make and problem to solve.

# Getting the Plan build

Once you provided the problem, the context built in the previous steps (building a North Metric and KPI Trees) will come into play and be used as a a reference.
Look at the tutorial for the North Star Metric agent and KPI Tree Architect to learn more about the Buildr example here. 

<img width="876" height="746" alt="AP 1 prep" src="https://github.com/user-attachments/assets/fabb0fe3-9c17-450f-8312-8db5e30c60f1" />

All this will be used for Claude to build a set of hypothesis based on what it understand of your business/product, the metric you are focusing one and its drivers.

<img width="874" height="577" alt="AP 1 hyps" src="https://github.com/user-attachments/assets/4253ca39-fdbe-43a2-a3b8-946304b10d8d" />

Note that each hypothesis has a probability, impact potential and actionability.
We do not show it in this tutorial but you can of course challenge these and also add more hypotheses or remove some if you want to.

## Step 0 - Confirm the issue
The first step of the analysis plan recommended in our example is to confirm the issue we have and the drop in our metric.
As you can see below, it recommend in details which metric to look at, but also how to look ait (what type of chart, breakdwon ...) in order to answer specific questions.
That is one of the incredible power of this skill. Once you collected the data getting to INSIGHTS will take no time.

<img width="872" height="479" alt="AP 1 Approach" src="https://github.com/user-attachments/assets/d2c301a1-4aef-4c9d-8ec7-d7940c610eac" />

## Hypotheses
After that, you will see for each hypothesis a list of to-do to validate/invalidate it.
In details:
* Which Data to collect (based on KPI Tree)
* Analyses to be run and for what purpose
* What to look for on the charts produced to validate/invalidate the hypothesis
* Further deep dives to get to the root cause of the behavior

<img width="877" height="500" alt="AP 2 H1 plan" src="https://github.com/user-attachments/assets/92f3d2e9-bee6-422f-913b-c03cf92a3a51" />

| | |
|:-------------------------:|:-------------------------:|
| <img width="879" height="503" alt="AP 2 H2 plan" src="https://github.com/user-attachments/assets/33633d24-5dcc-4e63-a3c7-237d7c3adb76" />
| <img width="879" height="500" alt="AP 2 H3 plan" src="https://github.com/user-attachments/assets/32d95023-82ed-467a-ae91-75ee8b3c6eff" />
|
| <img width="870" height="504" alt="AP 2 H4 plan" src="https://github.com/user-attachments/assets/ca82564b-dd4f-4d76-a761-0bd8832b892c" />
| <img width="880" height="709" alt="AP 2 H5:6 plan" src="https://github.com/user-attachments/assets/24081f5c-99c7-48d2-968b-c68f3116c9be" />
|

## Plan of Action
At some point you might have been asked for a timeline to get results.
Based on that you will be recommended a plan of action along this timeline to ensure you are ready on time!

<img width="881" height="713" alt="AP 2 end" src="https://github.com/user-attachments/assets/9d2b7431-f32c-4577-a3c2-ff947f63fa78" />

# Saving
To save your work just reply yes if prompted by Claude or simply ask to save the plan into a markdown file.
