# Wildfire Early Detection and Risk Assessment Platform — Team Ash Detectives

## Overview

This project is a **wildfire early-detection and risk-assessment platform** developed for **ECE444 – Software Engineering** at the University of Toronto.

The system combines environmental data, geospatial information, and AI/ML techniques to help detect potential wildfire events and communicate wildfire risk through an interactive map.

The platform is designed to provide users with clear and accessible information about wildfire detections, environmental conditions, and risk levels while handling incomplete or unavailable data reliably.

## Key Features

- **Wildfire Detection** – Analyze available data to identify potential wildfire events.
- **Detection Results** – Display detected wildfire locations, timestamps, and confidence levels.
- **Wildfire Risk Assessment** – Calculate wildfire-risk levels using relevant environmental factors.
- **Interactive Risk Map** – Visualize wildfire-risk information geographically using a heatmap.
- **Risk Details** – Allow users to select an area and inspect its wildfire-risk information.
- **Environmental Data Handling** – Clearly identify missing or unavailable environmental information.
- **Failure Handling** – Gracefully handle failures involving external APIs, data sources, and model processing.
- **Modular Architecture** – Maintain clear interfaces between frontend, backend, AI/ML, and data-processing components.
- **Automated Testing** – Use automated tests and CI checks to protect critical functionality from regressions.

## System Architecture

The application is organized into four major components:

### Frontend

Provides the user interface and interactive wildfire map. It is responsible for displaying wildfire detections, risk information, environmental data, and system status.

### Backend

Provides APIs used by the frontend and coordinates communication between application components.

### AI/ML

Processes relevant input data to support wildfire detection and risk assessment.

### Data Processing

Collects, validates, and transforms environmental and geospatial data required by the application.

These components use clearly defined interfaces to reduce coupling and improve maintainability, extensibility, and testability.

## Requirements

The project's functional and non-functional requirements are documented in:

`docs/requirements.md`

The requirements document contains the selected user stories, priorities, rationale, acceptance criteria, and references to the corresponding GitHub Issues.

## Project Management

Development is managed using **GitHub Issues** and a **GitHub Projects Kanban board**.

Implementation work is divided into development tasks linked to the originating user stories and requirements.

The project board follows the workflow:

**Todo → In Progress → Done**

### Project Management Tools

| Tool | Purpose | URL |
|---|---|---|
| GitHub Repository | Source code, documentation, and version control | [Repository](https://github.com/RianaMalhotra/ECE444-PROJECT) |
| GitHub Issues | User stories, requirements, bugs, and implementation tasks | [Issues](https://github.com/RianaMalhotra/ECE444-PROJECT/issues) |
| GitHub Projects | Kanban board for tracking development progress | [Project Board](https://github.com/users/RianaMalhotra/projects/1) |
| GitHub Pull Requests | Code review and integration of changes | [Pull Requests](https://github.com/RianaMalhotra/ECE444-PROJECT/pulls?q=is%3Apr+state%3Aclosed) |

## Repository Structure

```text
ECE444-PROJECT/
├── docs/
│   └── requirements.md
├── frontend/
├── backend/
├── tests/
└── README.md
```

The repository structure may evolve as additional components are implemented.

## Testing

Automated testing is used to protect critical functionality and identify regressions throughout development.

Testing focuses on:

- Core application functionality
- API behaviour
- Data validation and error handling
- AI/ML and risk-processing components
- Integration between major system components
- Regression prevention

Continuous integration checks will be introduced as the project develops.

## Development Workflow

Development follows an issue-driven workflow:

1. User stories and requirements are documented and linked to GitHub Issues.
2. Implementation work is divided into development tasks.
3. Tasks are tracked using the GitHub Projects Kanban board.
4. Developers implement changes on dedicated Git branches.
5. Changes are reviewed through Pull Requests before being merged.
6. Automated tests are used to verify changes and reduce regressions.

## Team

Developed by **Team Ash Detectives** as part of **ECE444 – Software Engineering** at the University of Toronto.

## Project Status

🚧 **Under Development**

The project is currently progressing from requirements engineering into implementation. Development tasks and progress are tracked through the repository's GitHub Issues and Project board.
