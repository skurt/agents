# Partner Quality Audit (PQA)

**Version:** 1.0.2  
**Author:** Kentico  
**Category:** Quality  
**License:** MIT

## Overview

The Partner Quality Audit plugin is an AI-guided orchestration workflow for performing a full Partner Quality Audit on [Xperience by Kentico](https://www.kentico.com) projects. It walks through environment analysis and configuration checks, then produces a final HTML audit report.

## Features

- Automated environment discovery and terminology setup
- Interactive questionnaire to collect project-specific details
- Analysis of hosting model (SaaS, Cloud, On-Premise)
- Configuration checks (application startup, middleware order, NuGet package versions, route registration)
- Final HTML report generation

## Usage

1. Open GitHub Copilot Chat.
2. Select the **Partner Quality Audit** agent from the agent picker.
3. Follow the guided steps — the agent will walk you through data collection, analysis, and report generation.

## Requirements

- GitHub Copilot with agent mode enabled
- An Xperience by Kentico project open in your workspace
- [Pandoc](https://pandoc.org) installed (used for final HTML report generation)

## Plugin Structure

```
plugins/partner-quality-audit/
├── plugin.json          # Plugin manifest
├── README.md            # This file
├── agents/
│   └── apqa_00_Global_Orchestrator.agent.md
└── prompts/
    ├── apqa_10_orchestrate_environment.prompt.md
    ├── apqa_11_terminology.prompt.md
    ├── apqa_12_questionaire.prompt.md
    ├── apqa_13_script.prompt.md
    ├── apqa_20_General_orchestration.prompt.md
    ├── apqa_21_Environment.prompt.md
    ├── apqa_21a_Confirm_hosting_model.prompt.md
    ├── apqa_22_Configuration.prompt.md
    ├── apqa_90_Produce_final_document.prompt.md
    └── pqa_check_feature.prompt.md
```

## Changelog

### 1.0.2
- Fixed prompt file references to use relative paths, compatible with the plugin marketplace.

### 1.0.1
- Initial release.
