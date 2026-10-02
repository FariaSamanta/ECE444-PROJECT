# Wildfire Early Detection and Risk Assessment Platform - Team Ash Detectives

## Overview

This project is a wildfire early-detection and risk-assessment platform developed for **ECE444 – Software Engineering** at the University of Toronto.

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

The application is organized into several major components:

### Frontend

Provides the user interface and interactive wildfire map. It is responsible for displaying wildfire detections, risk information, environmental data, and system status.

### Backend

Provides APIs used by the frontend and coordinates communication between application components.

### AI/ML

Processes relevant input data to support wildfire detection and risk assessment.

### Data Processing

Collects, validates, and transforms environmental and geospatial data required by the application.

The components use clearly defined interfaces to reduce coupling and improve maintainability and testability.

## Requirements

The project's functional and non-functional requirements are documented in:

`docs/requirements.md`

The requirements document contains the selected user stories, priorities, rationale, acceptance criteria, and references to the corresponding GitHub Issues.

## Development Process

Development is managed using **GitHub Issues** and a **GitHub Project Kanban board**.

Implementation work is broken into tasks linked to the originating user stories and requirements.

The project board follows the workflow:

**Todo → In Progress → Done**

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

Automated testing is used for critical functionality.

Testing focuses on:

- Core application functionality
- API behaviour
- Data validation and error handling
- AI/ML and risk-processing components
- Integration between major system components
- Regression prevention

Continuous integration checks are used to run relevant automated tests as the project develops.

## Team

Developed as part of **ECE444 – Software Engineering** at the University of Toronto.

## Project Status

🚧 **Under Development**

The team is currently progressing from requirements engineering into implementation. Development tasks and progress are tracked through the repository's GitHub Issues and Project board.
