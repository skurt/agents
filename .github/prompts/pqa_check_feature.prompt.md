---
agent: 'ask'
description: 'Looks up a Kentico documentation topic and checks if it is implemented in the project and how'
---

Please locate the following topic or heading in Kentico Documentation: ${input}.
Use Kentico Documentation MCP server for this, if you cannot use it, access it or it doesn't work in any way, report the issue and end this prompt.

Use the documentation article to examine and understand the topic and then search for the described functionality in this project and identify if it is implemented here.
If it's not implemented here, stop and report the absence of implementation.

If it is there, examine the implementation and crossreference it with the documentation article and code samples (if present) and report to me a summary whether the implementation follows the documentation or not.

Do not omit information from your answer, but be brief. Simple "No, the feature is not in use" or some bulletpoints covering the pro's and con's will suffice.

After presenting your findings, explicitly ask the user whether they approve continuing further. Do not proceed with any next steps until the user gives explicit approval.
