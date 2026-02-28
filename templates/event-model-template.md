---
title: "Your Feature Name"
status: draft
domain: "YourDomain"
version: 1
created: "YYYY-MM-DD"
tags:
  - your-tag
---

# Your Feature Name

## Overview

<!-- Describe the feature in 1-3 paragraphs: what it does, who benefits, and why it matters. -->

## Key Ideas

<!-- List the core concepts. Each idea is a candidate for one or more slices. -->

- **Idea name** -- description of the core concept and why it matters

## Slices

<!-- Define one slice per vertical unit of work. Each slice follows a pattern:
     - Command pattern: trigger -> view -> command -> event -> view
     - View pattern: events -> view -> trigger
     - Automation pattern: event -> automation -> command -> event
     - Translation pattern: external system -> translation -> event

     Use emlang notation inside fenced code blocks. -->

### Slice: YourSliceName

**Wireframe:** Describe the UI screen or trigger for this slice

```emlang
slices:
  YourSliceName:
    steps:
      - t: YourTrigger
      - v: YourInputView
      - c: YourCommand
      - e: YourEvent
      - v: YourResultView
```

## Scenarios

<!-- Add Given/When/Then scenarios for cross-slice or edge-case behavior. -->

### Scenario: Your Scenario Name

- **Given** some precondition
- **When** an action occurs
- **Then** an expected outcome

## Data Flows

<!-- Describe what data enters, transforms within, and exits the system. -->

| Source | Enters as | Transforms via | Exits as |
|--------|-----------|---------------|----------|
| Your source | `YourCommand` command | `YourEvent` event | `YourView` view |

## Dependencies

<!-- Link to other Event Model files this feature depends on. -->

## Sources

<!-- Link to requirements documents, research, or stakeholder interviews. -->
