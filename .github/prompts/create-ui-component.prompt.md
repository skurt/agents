---
name: Create UI Component
description: Generate a new UI component with proper HTML, CSS and accessibility. Provide the component name and what it should do.
argument-hint: "Component name and what it should do (e.g. 'A collapsible sidebar nav with icons')"
agent: agent
tools: [read, edit]
---

Create a new UI component based on the description provided.

Requirements:
- Semantic HTML5 structure (use appropriate tags: nav, section, article, button, etc.)
- Responsive CSS using mobile-first approach
- WCAG 2.1 AA accessibility (aria-* attributes, keyboard navigation, sufficient color contrast)
- Match naming conventions and design tokens already present in the codebase if files are available
- Add brief inline comments for non-obvious design decisions

Deliver the component as ready-to-use code. If multiple files are needed (e.g. separate JS and CSS), create them all.
