---
agent: agent
description: 'Loads questionnaire responses from the project root folder'
---

## Step: Load Questionnaire Data

1. Look for a file named `structured_questionnaire_responses.json` in the `root folder` (as defined by the terminology step).
2. If the file **cannot be found**, report that it could not be located and **stop processing any further instructions**.
3. If the file **is found**, read its contents and remember all keywords and values defined in it. These keywords will be referenced throughout the rest of this workflow.
