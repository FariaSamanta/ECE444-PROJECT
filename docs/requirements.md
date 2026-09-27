# Requirements

## Project Goal

Wildfires in at-risk regions are often detected too late; existing monitoring relies on delayed satellite passes, manual observation, or public reporting, giving communities and responders little lead time to act. Team Ash Detectives is building a wildfire early-detection and risk-monitoring platform that applies AI/computer vision to satellite and geospatial data to flag emerging fire risk sooner. Beyond detecting active fires, the platform will use AI to predict wildfire risk by analyzing contributing factors such as vegetation dryness, fuel density, terrain, and weather conditions.

## Problem Statement and Motivation

Wildfire monitoring systems often depend on satellite observations, environmental datasets, and manual interpretation by users or agencies. Satellite revisit times, cloud or smoke interference, fragmented data sources, and delayed interpretation can reduce the amount of lead time available for identifying developing wildfire conditions.

The proposed system aims to reduce this information gap by combining multiple data sources into a single platform and applying AI-based analysis to identify patterns associated with wildfire activity and elevated wildfire risk.

The objective is not to replace emergency-management systems or professional wildfire forecasting tools, but to provide an additional decision-support layer that consolidates available information, highlights areas requiring attention, and presents model outputs in an understandable and traceable way.

## Stakeholders

### General Public

* **Needs:** An understandable view of wildfire locations and general risk conditions.
* **Evidence:** A simplified version of the interactive map could improve public situational awareness without requiring users to interpret raw satellite or environmental datasets.

### Emergency Management Organizations

* **Needs:** Timely information about potential wildfire activity, risk levels, affected areas, and fire progression.
* **Evidence:** These organizations may need to combine information from multiple sources when monitoring developing wildfire situations. Our platform aims to consolidate relevant data into a single dashboard.

### Municipalities and Local Authorities

* **Needs:** Localized wildfire risk information and visualizations that can support situational awareness and planning.
* **Evidence:** The platform will provide geospatial risk heatmaps, potential fire detections, environmental conditions, and historical observations.

### Environmental Researchers

* **Needs:** Access to historical wildfire observations, environmental conditions, satellite imagery, and model outputs for analysis.
* **Evidence:** The system will store observations over time and support historical wildfire event analysis and model evaluation.

### Organizations Monitoring Wildfire Activity

* **Needs:** A centralized way to monitor potential fire activity and changes in wildfire conditions.
* **Evidence:** The proposed system combines satellite observations, environmental data, risk predictions, and fire progression tracking.

### Development Team

* **Needs:** A realistic software engineering project that allows the team to practice full-stack development, AI/ML, APIs, databases, and collaborative development.
* **Evidence:** The project will involve React/TypeScript, Python/Flask, REST APIs, SQL, AI/ML libraries, geospatial visualization, and Git/GitHub.

### Electric Utilities and Transmission/Distribution Operators

* **Needs:** Localized wildfire-risk information around transmission lines, substations, and other electrical infrastructure to support preventive maintenance, situational awareness, vegetation management, and operational decisions during extreme fire conditions.
* **Evidence:** Utilities already combine weather observations, fuel conditions, cameras, sensors, and wildfire-risk models to reduce ignition risk and determine when additional mitigation measures may be necessary. The proposed platform could provide an additional geospatial risk layer that helps identify infrastructure located within elevated-risk areas.

### Insurance and Reinsurance Companies

* **Needs:** Wildfire-risk information that can help evaluate geographic exposure, understand portfolio risk, monitor active wildfire threats, and prioritize areas requiring closer assessment.
* **Evidence:** Insurers already use property-level wildfire intelligence for underwriting, portfolio analysis, and response planning. The platform's historical observations, environmental risk factors, and geographic risk heatmaps could provide an additional source of wildfire-risk information for these workflows.

### Critical Infrastructure Operators

* **Needs:** Early awareness of wildfire activity near critical assets such as telecommunications infrastructure, pipelines, transportation systems, and data centres.
* **Evidence:** A wildfire-risk platform could allow operators to monitor geographic exposure and identify assets located near emerging wildfire detections or high-risk regions, supporting contingency planning and asset-protection decisions.

### Forestry and Land-Management Organizations

* **Needs:** Information about vegetation conditions, fuel density, historical wildfire activity, and geographic areas experiencing elevated fire risk.
* **Evidence:** Combining vegetation, terrain, weather, and historical wildfire observations could support prioritization of vegetation management, monitoring, and wildfire-mitigation activities.

### Utility and Public-Safety Regulators

* **Needs:** Reliable wildfire-risk information and historical observations that can support oversight of wildfire-mitigation programs and infrastructure-related wildfire risk.
* **Evidence:** Regulators in wildfire-prone regions already require utilities to develop wildfire-mitigation plans and report infrastructure-related fire events. Historical risk and detection data from the platform could support analysis and reporting activities.


## Primary Users

For the initial semester implementation, the primary users will be emergency-management organizations, municipalities and local authorities, electric utilities, and organizations responsible for monitoring wildfire activity.

These users are most likely to require timely wildfire detections, localized risk information, environmental context, and geospatial visualizations to support monitoring and operational decision-making.

Insurance and reinsurance companies, environmental researchers, forestry and land-management organizations, critical-infrastructure operators, and the general public will be treated as secondary users for the initial implementation.

The application interface will therefore prioritize:

* rapid interpretation of wildfire detections,
* geographic risk visualization,
* access to supporting environmental information,
* infrastructure or regional risk awareness where applicable,
* historical comparison,
* and clear indication of model confidence and uncertainty.


## Initial Scope

### Scope Statement

> For the semester, Team Ash Detectives will focus on developing a prototype wildfire monitoring platform that combines satellite/geospatial data, environmental conditions, and AI-based analysis to detect potential wildfire activity and visualize wildfire risk. The core system will provide an interactive map, wildfire detections, risk heatmaps, fire progression visualization, and simulated early-warning alerts. The team will evaluate its detection and risk models using historical wildfire data. Advanced capabilities such as fully real-time raw satellite-image processing, precise fire-spread forecasting, direct emergency-service integration, global deployment, and automated emergency notifications will be deferred to keep the project feasible within the semester.

## System Boundaries

The system will operate as a monitoring and decision-support platform rather than an emergency-response or dispatch system.

For the initial implementation:

* The platform will not issue official evacuation orders or emergency instructions.
* AI-generated wildfire detections and risk estimates will be presented as advisory outputs rather than authoritative emergency decisions.
* The system will rely primarily on public or openly accessible datasets.
* The platform will not attempt to replace professional wildfire forecasting or emergency-management systems.
* Automated real-world actions will not be triggered directly from model outputs.
* Model predictions will include confidence or uncertainty information where appropriate.

### Features Planned for This Semester

#### 1. Interactive Wildfire Monitoring Map

* Interactive geospatial map displaying wildfire detections and wildfire risk.
* Display detected fire locations using satellite and geospatial datasets such as NASA FIRMS.
* Allow users to zoom, pan, and inspect specific geographic areas.
* Display relevant environmental information such as temperature, wind, and vegetation conditions where available.

#### 2. Wildfire Detection

* Process historical and/or near-real-time satellite fire data to identify potential wildfire locations.
* Use a baseline AI/computer vision approach to classify satellite imagery or environmental observations associated with potential fire activity.
* Display detection confidence and relevant information for each detected fire.
* Evaluate the detection system using historical wildfire observations.

#### 3. Wildfire Risk Heatmap

* Generate a wildfire risk score for geographic areas based on available environmental factors.
* Incorporate factors such as vegetation/fuel conditions, temperature, wind, terrain, and historical fire activity where data is available.
* Visualize risk levels on the map using an intuitive heatmap or categorical risk indicators.

#### 4. Fire and Risk Information Dashboard

* Provide a dashboard summarizing active or historical fire detections.
* Display information such as location, detection time, confidence, risk level, and relevant environmental conditions.
* Allow users to select individual fires or geographic areas for more detailed information.

#### 5. Early-Warning Simulation

* Simulate an early-warning workflow when the system identifies a potential wildfire or an area with elevated risk.
* Generate an alert containing the approximate location, risk/detection level, and supporting environmental information.
* Use historical data to demonstrate how the alerting system would have behaved during previous wildfire events.

#### 6. Explainable Risk Factors

* Display the primary environmental factors contributing to the predicted wildfire-risk level for a geographic area.
* Show relevant factors such as temperature, vegetation dryness, wind conditions, terrain, and recent fire activity where available.
* Provide users with a short explanation of why an area received a particular risk level.
* Avoid presenting the explanation as definitive causation; it should describe the model inputs that most strongly contributed to the prediction.

#### 7. AI Model Evaluation

* Evaluate wildfire detection and risk-prediction models using historical wildfire data.
* Report appropriate metrics such as precision, recall, false-positive rate, and detection confidence.
* Compare model predictions against historical observations to identify strengths and limitations.

#### 8. Backend and Data Infrastructure

* REST APIs for communication between the frontend and backend.
* SQL database for storing wildfire observations, environmental data, and system results.
* Data processing pipelines for external wildfire and environmental datasets.

## AI-Specific Features

The system will use AI/ML in multiple parts of the wildfire-monitoring workflow.

### Wildfire Detection

A baseline machine-learning or computer-vision model will be used to classify observations or imagery associated with potential wildfire activity.

### Wildfire Risk Estimation

A predictive model will combine environmental variables such as temperature, vegetation/fuel conditions, wind, terrain, and historical wildfire observations to estimate relative wildfire risk.

### Confidence and Uncertainty Reporting

Model outputs will include confidence scores or uncertainty indicators so that users can distinguish between stronger and weaker predictions.

### AI-Assisted Explanation

Where feasible, the system will generate a short explanation of the main factors contributing to a wildfire-risk prediction, such as elevated temperature, dry vegetation, or high wind conditions.

### Model Verification

AI-generated results will be compared with historical wildfire observations and evaluated using quantitative metrics before being presented as reliable system outputs.

## Non-Functional Requirements

### Performance

* The interactive map should load and respond to user interactions within a reasonable time under normal usage.
* API requests for stored wildfire observations and environmental information should return without unnecessary delay.
* Expensive AI or geospatial processing tasks should be performed asynchronously where appropriate.

### Scalability

* The backend should support adding additional geographic regions without requiring major architectural changes.
* Data-processing components should be modular so that additional wildfire, weather, or satellite data sources can be integrated later.
* The application architecture should support increasing numbers of users, observations, and geographic regions through horizontal scaling where appropriate.

### Reliability

* Failures in one external data source should not cause the entire application to become unavailable.
* Missing or unavailable environmental data should be clearly indicated rather than silently replaced with fabricated values.
* Model and API failures should be handled gracefully.

### Maintainability

* Frontend, backend, AI/ML, and data-processing components should have clearly defined interfaces.
* Code should be modular and documented.
* Automated tests should be used for critical functionality.

### Usability

* Wildfire risk information should be understandable without requiring specialist knowledge of satellite or geospatial datasets.
* Risk levels, confidence values, and environmental conditions should be clearly labelled.

### Security

* API endpoints should validate incoming requests.
* Authentication and authorization should be implemented for functionality requiring restricted access.
* Sensitive configuration values such as API keys should not be exposed in source code or frontend code.
* External data should be validated before being stored or processed.

### Privacy

* The initial platform will avoid collecting unnecessary personal information.
* If user accounts are introduced, only information required for system functionality will be stored.

## Safety and AI Guardrails

Because wildfire monitoring may influence how users interpret emergency conditions, the system will include safeguards around AI-generated outputs.

* AI predictions will not be presented as guaranteed wildfire detections.
* Detection confidence and uncertainty will be visible to users.
* Historical or simulated alerts will be clearly distinguished from real emergency alerts.
* The system will not automatically contact emergency services.
* Users will be informed that model outputs are intended for situational awareness and decision support.
* Predictions should be supported by observable environmental or satellite data where possible.
* The system should avoid presenting unsupported explanations or fabricated environmental values.
* Model errors and false positives will be evaluated explicitly during testing.
* High-risk or uncertain predictions should be presented with appropriate caution rather than exaggerated certainty.

### Features expected to be deferred

The following features may be considered for future development if time and resources permit, but will not be required for the initial semester implementation:

* **Fully real-time satellite imagery processing:** Processing raw satellite imagery continuously as soon as it becomes available may require significant computational resources and specialized infrastructure.
* **High-resolution satellite computer vision:** Using very high-resolution imagery to directly identify fire or smoke could be explored later depending on data availability, licensing, and computational requirements.
* **Advanced wildfire spread prediction:** Predicting the exact future boundaries or trajectory of a wildfire would require more sophisticated physical and environmental modeling than the initial semester scope.
* **Automated emergency-service integration:** Direct integration with municipal emergency-management systems, dispatch systems, or public alert infrastructure will be deferred.
* **SMS/email/mobile emergency notifications:** The initial alert feature will be demonstrated within the application rather than delivering real-world emergency notifications.
* **Continuous automated monitoring:** Fully autonomous 24/7 monitoring and automatic model retraining will be deferred.
* **Multi-region/global deployment:** The initial implementation will focus on a defined geographic region rather than supporting all wildfire-prone areas worldwide.
* **Precise fire-spread forecasting:** Estimating the exact rate and direction of fire spread will be treated as a future enhancement rather than a core requirement.
* **Public reporting:** Allowing users to submit and verify wildfire reports could be considered in a future version but is outside the initial detection and monitoring workflow.

## Data Sources and Provenance

The platform will maintain information about the origin of data used in wildfire detections and risk predictions.

For each observation or model output, the system should record where appropriate:

* source dataset,
* observation timestamp,
* geographic location,
* data retrieval time,
* model version,
* prediction confidence,
* and relevant environmental inputs.

This will allow users and developers to trace how a wildfire detection or risk prediction was produced and support debugging, model evaluation, and reproducibility.

## Initial Success Criteria

The semester prototype will be considered successful if it can:

* ingest wildfire and environmental data from at least one reliable public source,
* display wildfire observations on an interactive map,
* generate a geographic wildfire-risk visualization,
* produce AI/ML-based wildfire detection or risk predictions,
* report confidence or evaluation metrics for model outputs,
* store and retrieve historical wildfire observations,
* allow users to inspect individual wildfire events or geographic regions,
* simulate an early-warning workflow using historical wildfire data,
* demonstrate the system using at least one historical wildfire event,
* and provide a deployed web interface accessible to users outside the development environment.

## Questions to Clarify

1. **Which wildfire datasets should we use as our primary data source?**

   * Investigate available public datasets such as NASA FIRMS and evaluate their coverage, format, update frequency, and API availability.

2. **What geographic area should the system support?**

   * Discuss the expected project requirements and determine whether the system should focus on Canada, North America, or a smaller geographic region.

3. **What level of wildfire prediction is feasible within one semester?**

   * Build an initial baseline model using historical data and evaluate its accuracy before committing to a more complex ML approach.

4. **What satellite imagery is practical for computer vision?**

   * Investigate available imagery datasets, image resolution, licensing, API access, and computational requirements.

5. **How should wildfire risk be represented to users?**

   * Review existing wildfire monitoring systems and conduct team/user feedback sessions to determine appropriate risk scores, heatmaps, and visual indicators.

6. **What constitutes a successful wildfire detection?**

   * Define evaluation metrics such as precision, recall, false-positive rate, and detection confidence using historical wildfire observations as ground truth.

7. **How frequently should the system update its data?**

   * Investigate the update frequency of the selected data sources and determine an appropriate refresh interval for the application.

8. **Which features should be prioritized for the semester?**

   * Use the team's user stories, requirements review, and development capacity to finalize the minimum viable feature set.

At this stage, these questions remain open and will be addressed through dataset research, technical prototyping, requirements discussions, and user story review.
