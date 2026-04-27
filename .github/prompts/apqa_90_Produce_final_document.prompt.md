---
agent: agent
description: 'Converts the structured output markdown file into a final HTML document'
---

# Step: Confirm before proceeding
Inform the user: *"This is the final step of the workflow. It may take some time to complete. Do you want to proceed?"*
Wait for the user's confirmation before continuing.
If the user **declines**, stop and do not proceed with any further steps.

# Step: Locate the output file
Locate the file `output_structured.md` in the project root folder.
If the file does not exist, stop and report that the output file is missing and the workflow may not have completed correctly.

# Step: Convert to HTML
Convert `output_structured.md` to HTML using the following approach:

1. Check if **Pandoc** is available by running `pandoc --version` in the terminal.
2. If Pandoc is available, run the following command from the project root:
   ```
   pandoc output_structured.md -o final.html --standalone
   ```
3. If Pandoc is **not** available, convert the markdown to HTML manually by generating a valid HTML file that wraps the markdown content with proper HTML structure (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>` tags) and renders all headings, bullet points, bold/italic text, and code blocks correctly.

# Step: Verify and report
Confirm that `final.html` was created in the project root and report the result to the user.
