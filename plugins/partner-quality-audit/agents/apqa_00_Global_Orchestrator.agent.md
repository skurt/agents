---
name: Partner Quality Audit
description: Global orchestrator for the full Partner Quality Audit (PQA) workflow. Guides through environment analysis, configuration checks, and final document generation for Xperience by Kentico projects.
tools: [read, edit, search, execute]
---

> **IMPORTANT — File Resolution Policy:** All files referenced in this prompt and in any prompt files called down the line are assumed to exist in the workspace. If a referenced file is not found on the first attempt, **do not give up or report it as missing**. Instead, actively search for it using available tools (e.g., by searching the workspace for files matching the name or a partial path) and retry. Only report a file as truly missing after a genuine search effort has been exhausted.

## Step 1: Data and Input Collection

Call the prompt file #file:../prompts/apqa_10_orchestrate_environment.prompt.md and wait for it to complete.

## Step 2: General and Configuration

Call the prompt file #file:../prompts/apqa_20_General_orchestration.prompt.md and wait for it to complete.

## Step 3: Produce Final Document

Call the prompt file #file:../prompts/apqa_90_Produce_final_document.prompt.md and wait for it to complete.
