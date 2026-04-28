---
agent: agent
description: 'Describe the project environment'
---
# Step: Title
Add a subtitle "Project environment" to the output file

# Step: Identify project's hosting model
From the available information, determine how is this project hosted.
There are three available options:
- [On premise] means the client operates their own server(s), Operating system and related tech stack to run and upkeep Xperience by Kentico
- [Cloud] means the client uses a cloud service provider, such as Azure, AWS or Google Cloud
- [SaaS] refers specificaly to the cloud environment that Kentico provides with the sole purpose of running, sustaining and upkeeping and XbK instance as simply as possible.

# Step: Confirm hosting model
Call #file:.github/prompts/apqa_21a_Confirm_hosting_model.prompt.md and wait for it to complete.

# Step: Non hosting related questions
Based on the available information try to determine all of the following points.
If you can find information on a point, answer by one bullet point.
If you cannot find the the related information, still answer with one bullet point, but in this case, name the topic and say it is undetermined.
Enter the bullet point into the output file.
- Does the project use multiple website channels?
- Where are the projects servers located, where is their audience located and is that reasonable?

# Step: Hosting related questions
The following questions will be hosting related. Based on the hosting determined in previous steps, only use questions from the related subtitle
Based on the available information try to determine all of the following points.
If you can find information on a point, answer by one bullet point.
If you cannot find the the related information, still answer with one bullet point, but in this case, name the topic and say it is undetermined.
Enter the bullet point into the output file.
## Step: Questions related to SaaS
- Is this project performing well or are the in need of additional auto scale instances?
- Call #file:.github/prompts/pqa_check_feature.prompt.md with parameter SaaS configuration.
- What is their strategy for backups and restores? 
## Step: Question related to Cloud
- Name their Cloud provider
- What is their service plan?
- What is their method of auto-scaling?
- What is their strategy for backups and restores?
- What security measures do they take advantage of on their cloud service?
- What about for file/storage/DB access?
## Step: Question related to On Premise
- What is their method of scaling the application?
- How many copies of the application are connected to the same production database?
- What Operation System and it's version are they on?
- What is their strategy to keep their Operating system updated?
- What is their strategy for backups and restores?
- What security measures do they take advantage of on their on-premise environment?
- What about for file/storage/DB access?
