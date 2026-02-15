The Analysis Results Collector helps you build bullet proof communication showcasing your insights no matter the audience.
It basically collects all the results of the analyses planned by the `analysis-planner` and then proceeds to ask further questions to refine the analysis and get it ready.

# Getting Started

Launch the skill using the `/analaysis-results-collector` command.
If you used the `analysis-planner` before, Claude should find the file containing the goal of the analysis and the different hypoteses.

<img width="877" height="708" alt="ARC launch" src="https://github.com/user-attachments/assets/b3ecc68b-44f0-4046-8067-ca1527d5f4de" />

# Inserting results
## Validation and Confidence
First you will have to tell Claude which hypotheses you actually analyzed and which you did not. In our case we dropepd H6 and H7.
After that you will be asked to insert for each hypothesis the main result (validate/invalidated) and the confidence in that result.
Note that you will do using the Claude multiple-choice/multiple-tab interface.

| | |
|:-------------------------:|:-------------------------:|
|<img width="305" height="140" alt="H1 results" src="https://github.com/user-attachments/assets/d96be621-522c-4723-b8dc-6c08bf414f7a" />
|<img width="305" height="140" alt="H1 confidence" src="https://github.com/user-attachments/assets/ae25f3f5-1025-4aea-bf41-f9b4ad18f32b" /> |

| <img width="305" height="140" alt="H2 Results" src="https://github.com/user-attachments/assets/e14838a5-18fd-43bf-a5d3-a76ecc43a28d" />
| <img width="305" height="140" alt="H2 confidence" src="https://github.com/user-attachments/assets/f9447ba2-bf2a-4efd-8c7b-2e07886d7348" />
|
| <img width="305" height="140" alt="H3 R" src="https://github.com/user-attachments/assets/50037d93-4ae0-4d42-b2f3-d12c54bb3a4e" />
| <img width="305" height="140" alt="H3 C" src="https://github.com/user-attachments/assets/31c984d8-c638-42e5-8838-9c7ac4fad362" />
|
| <img width="305" height="140" alt="H4 R" src="https://github.com/user-attachments/assets/f0d43d4a-17ff-4016-a7c8-cb9e08ebed08" />
| <img width="305" height="140" alt="H4 C" src="https://github.com/user-attachments/assets/8d09ee22-5d0d-49e5-b2f0-22b543c3ad65" />
|
| <img width="305" height="140" alt="H5 R" src="https://github.com/user-attachments/assets/06b2c268-6773-4244-9661-0bbdc5314628" />
| <img width="305" height="140" alt="H5 C" src="https://github.com/user-attachments/assets/84ae6438-7224-4e22-ae3c-52aad7d426d4" />
|

## Impact
Once you have inserted al lthis you will get a recap and be asked to provde a numerical impact for each hypothesis you validated.
If you are lost here, I highly recommend you read my book The Power of Analytics where I explain step by step how to such Impact analysis.

<img width="880" height="799" alt="Hyp recap" src="https://github.com/user-attachments/assets/8a12f551-264f-48ef-9a31-6e174bcb9cf7" />

In our exmaple we proceed to explain how H3/H4/H4 expalin the 20% drop in our metric

<img width="876" height="581" alt="Impact entry" src="https://github.com/user-attachments/assets/bf81c2db-6bd5-4d4a-ae89-cf64f9aa0428" />

## Rationale
After that prepare to be challenged! You will be asked to provide more clarity on the reasons behind your finding. 
It might feel challenging but believe these questions will be ask by your leadership so better answer them now!

| | |
|:-------------------------:|:-------------------------:|
| <img width="308" height="207" alt="H1-2-3" src="https://github.com/user-attachments/assets/07f21c8d-2aab-4f43-a340-6e2ffd9a3e0d" />
| <img width="308" height="207" alt="H4 full" src="https://github.com/user-attachments/assets/528d5b2f-0698-404b-b2c3-93e0840ca03f" />
|
| <img width="305" height="190" alt="H5 full" src="https://github.com/user-attachments/assets/a59d3fab-acec-46a5-9b5e-824306872a27" />
|<img width="305" height="190" alt="H3 full" src="https://github.com/user-attachments/assets/b2a7a19f-23b3-4ae8-8644-d1472036e028" />|

# Finalization
## Draft of findings
Once you are donw Claude will give you a first draft about your findings and ask if this is ok or if you wold change anything befor moving on.

| | | |
|:-------------------------:|:-------------------------:|:-------------------------:|
| <img width="=308" height="231" alt="Draft H1-2" src="https://github.com/user-attachments/assets/c1f095a6-1405-4b0b-a73b-11bd37ce67c0" />
| <img width="308" height="265" alt="Draft H3-4" src="https://github.com/user-attachments/assets/4b85d141-8d5b-4d91-bfaf-083030b777b4" />
| <img width="308" height="203" alt="Draft H5" src="https://github.com/user-attachments/assets/3aeb3380-0f15-4423-9062-93a665ea9e6d" />
|

## Recommendations
Claude might ask you for more questions to finalize the next steps section of the analysis. Again it might challenge you until you gave satisfactory answers!

| | |
|:-------------------------:|:-------------------------:|
| <img width="308" height="203" alt="reco 1" src="https://github.com/user-attachments/assets/1fee165e-1822-4eb7-8613-e6964699ca8e" />
| <img width="309" height="268" alt="reco 2" src="https://github.com/user-attachments/assets/81bec70c-a3db-43ff-bfa1-6169b1f01a19" />|


## Output
After all this Claude will produce an thorough analysis document in markdown format.

<img width="364" height="257" alt="ACR file 1" src="https://github.com/user-attachments/assets/2b0106d8-d67f-4397-ae0a-d1488d61169d" />
<img width="364" height="257" alt="ACR Exec sum" src="https://github.com/user-attachments/assets/6724e113-61d6-492b-a0a7-23dadb34f772" />
<img width="364" height="276" alt="ACR file overview" src="https://github.com/user-attachments/assets/9d5eb68c-37eb-4905-bada-f77dd071f94b" />
<img width="364" height="276" alt="ACR File H1-2" src="https://github.com/user-attachments/assets/2011dbb7-d506-4499-a953-d4bff3917e9c" />
<img width="364" height="276" alt="ACR File reco" src="https://github.com/user-attachments/assets/47cfe9ae-714f-437b-949b-8b1a59b7a39e" />
<img width="364" height="276" alt="ACR file roadmpa   appendix" src="https://github.com/user-attachments/assets/6a0e109d-2f59-4573-9920-1ee6eda754bd" />

As is this document could be shared but you still need to add the charts produced during the analysis to support visually your findings and tune in the wording if needed.

# Next Steps
While this document is a great in depth analysis, it is better to build a nice presentation out of it for your leadership and stakeholders.
No worries, I got you covered with the `presentation-builder`
