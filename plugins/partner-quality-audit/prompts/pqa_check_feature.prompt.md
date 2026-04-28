---
agent: agent
description: 'Looks up a Kentico documentation topic and checks if it is implemented in the project and how'
---

## Step 0: Notify User

Inform the user: **"Feature check for: ${input}"**

## Step 1: Retrieve Documentation

Look up the following topic in Kentico Documentation using the Kentico Documentation MCP server: **${input}**.
If the MCP server is unavailable or fails for any reason, report the issue and stop.

## Step 2: Analyze Project Implementation

Use the retrieved documentation article to understand the feature, then search the project codebase to determine whether this feature is implemented.

- If the feature is **not implemented**, stop and report its absence.
- If the feature **is implemented**, cross-reference the implementation against the documentation and any provided code samples, then produce a summary of whether the implementation follows the documented approach.

Keep findings concise — a single sentence or a short bulleted list covering key observations is sufficient.

## Step 3: Save Output

Write the findings to a file named `temp_Output.md` in the root folder of this project. If the file already exists, overwrite it.

## Step 4: Review Output

Open `temp_Output.md` in the editor so the user can review its contents.

## Step 5: Confirm Before Continuing

Present the following message to the user:

> "Please review `temp_Output.md`. Are you satisfied with the findings? Reply **yes** to continue, or describe any changes you would like made."

If the user requests changes, apply them to `temp_Output.md` and repeat Step 4 and Step 5.
Do not proceed past this step until the user explicitly confirms they are satisfied.

## Step 6: Append to Workflow Output

Read the contents of `temp_Output.md` and append them to the workflow output file (`output_structured.md`) in the root folder of this project.
Do not overwrite or replace any existing content in `output_structured.md` — only append to the end of the file.
