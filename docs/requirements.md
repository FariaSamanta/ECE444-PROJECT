# Requirements

## Project Goal

Wildfires in at-risk regions may not be identified immediately, and wildfire monitoring can depend on satellite observations, environmental datasets, manual interpretation, and public or agency reporting. Satellite revisit times, cloud or smoke interference, fragmented data sources, and the time required to interpret observations can reduce the amount of information available when wildfire conditions are developing.

Team **Ash Detectives** is building a wildfire early-detection and risk-monitoring platform that applies AI/machine learning to satellite, environmental, and geospatial data to identify potential wildfire activity and areas of elevated wildfire risk.

Beyond detecting active fires, the platform will estimate relative wildfire risk by analyzing contributing factors such as vegetation dryness, fuel conditions, terrain, weather, and historical wildfire activity.

The objective is not to replace emergency-management systems or professional wildfire forecasting tools. Instead, the system will provide an additional decision-support layer that:

- consolidates wildfire and environmental information,
- highlights geographic areas requiring attention,
- visualizes wildfire detections and risk,
- communicates model confidence and uncertainty,
- and presents model outputs in an understandable and traceable way.

### Evidence Supporting the Project Need

NASA's Fire Information for Resource Management System (FIRMS) demonstrates an existing operational need for timely satellite-derived fire information. FIRMS uses observations from instruments such as MODIS and VIIRS to identify active fires and thermal anomalies and provides this information through maps, downloadable data, web services, and alerts for use in fire monitoring and analysis.

For the United States and Canada, FIRMS provides real-time and near-real-time active-fire information. NASA also notes important limitations: satellite-derived active-fire detections have limited accuracy, cloud cover may obscure detections, and thermal anomalies can originate from sources other than wildfires.

These limitations support our decision to treat model outputs as decision-support information rather than authoritative emergency information and to display confidence, environmental context, and uncertainty where possible.

**Sources:**

- NASA FIRMS — Fire Information for Resource Management System:  
  https://firms.modaps.eosdis.nasa.gov/

- NASA FIRMS — Active Fire Data:  
  https://firms.modaps.eosdis.nasa.gov/active_fire/

- NASA FIRMS — Fire Map and detection limitations:  
  https://firms.modaps.eosdis.nasa.gov/map/


---

# Stakeholders

## Primary Users

For the initial semester implementation, the primary users will be:

1. Emergency-management organizations
2. Municipalities and local authorities
3. Electric utilities and transmission/distribution operators
4. Organizations responsible for monitoring wildfire activity

These users are expected to benefit most directly from timely wildfire detections, localized risk information, environmental context, and geospatial visualizations.

The application interface will therefore prioritize:

- rapid interpretation of wildfire detections,
- geographic risk visualization,
- access to supporting environmental information,
- infrastructure or regional risk awareness where applicable,
- historical comparison,
- and clear indication of model confidence and uncertainty.

---

## Emergency Management Organizations

**Needs:**  
Timely information about potential wildfire activity, risk levels, affected areas, environmental conditions, and changes in wildfire activity.

Emergency-management users may need to combine information from multiple sources when monitoring developing wildfire situations. A centralized dashboard could reduce the amount of manual work required to interpret separate wildfire and environmental datasets.

**Supporting Evidence:**  
NASA FIRMS specifically provides satellite-derived active-fire information for near-real-time monitoring and applications. FIRMS provides fire information through maps, alerts, downloadable datasets, and web services and describes its active-fire information as being provided to decision-makers.

This supports the need for timely, geographically organized wildfire information that can contribute to situational awareness.

**Source:**  
NASA FIRMS — Fire Information for Resource Management System  
https://firms.modaps.eosdis.nasa.gov/

**Assumption:**  
Our specific dashboard layout and combination of risk predictions, environmental conditions, and historical information have not yet been validated directly with an emergency-management organization. These requirements will therefore be treated as initial assumptions to be refined through feedback and testing.

---

## Municipalities and Local Authorities

**Needs:**  
Localized wildfire-risk information and visualizations that can support situational awareness and planning.

The platform should allow local users to inspect geographic areas and understand nearby wildfire detections, risk levels, environmental conditions, and historical observations.

**Supporting Evidence:**  
NASA FIRMS supports geographic monitoring of active fires and thermal anomalies and allows users to examine recent fire activity geographically. FIRMS also provides area-based fire alerts, including alerts for custom geographic regions.

The existence of geographically scoped monitoring and alerting supports the need for localized wildfire information rather than only national or global summaries.

**Sources:**

NASA FIRMS — Fire Map  
https://firms.modaps.eosdis.nasa.gov/map/

NASA FIRMS — Fire Alert Subscription  
https://firms.modaps.eosdis.nasa.gov/alerts/

**Assumption:**  
The exact information and geographic granularity required by municipalities have not yet been validated through direct stakeholder interviews. The current requirements represent an initial interpretation that will be refined during development.

---

## Electric Utilities and Transmission/Distribution Operators

**Needs:**  
Localized wildfire-risk information around transmission lines, substations, and other electrical infrastructure to support situational awareness, vegetation management, preventive maintenance, and operational decision-making during elevated fire conditions.

The proposed platform could provide an additional geospatial risk layer that helps identify infrastructure located within elevated-risk areas.

**Supporting Evidence:**  
Utility wildfire-mitigation programs in wildfire-prone regions consider factors such as weather, vegetation, infrastructure conditions, and wildfire risk when planning mitigation activities. Regulatory wildfire-mitigation requirements also demonstrate that utilities need information about wildfire conditions surrounding electrical infrastructure.

**Source:**  
California Public Utilities Commission — Wildfire Mitigation Plans / Utility Wildfire Mitigation  
https://www.cpuc.ca.gov/industries-and-topics/wildfires

**Assumption:**  
The semester prototype will not integrate directly with utility infrastructure-management systems. Infrastructure overlays and utility-specific risk views are currently considered potential decision-support functionality and should be validated with stakeholder feedback before being treated as finalized requirements.

---

## Organizations Monitoring Wildfire Activity

**Needs:**  
A centralized way to monitor potential fire activity and changes in wildfire conditions.

These organizations may benefit from combining satellite observations, environmental data, risk predictions, historical observations, and fire progression information.

**Supporting Evidence:**  
NASA FIRMS exists specifically to provide active-fire and thermal-anomaly information for near-real-time monitoring and applications. It distributes MODIS and VIIRS detections through maps, downloadable datasets, web services, and alerts.

FIRMS also provides archived fire observations, making both current monitoring and historical analysis possible.

**Sources:**

NASA FIRMS  
https://firms.modaps.eosdis.nasa.gov/

NASA FIRMS — Active Fire Data  
https://firms.modaps.eosdis.nasa.gov/active_fire/

**Assumption:**  
The benefit of combining FIRMS observations with our proposed environmental-risk model and dashboard is an initial project hypothesis that will need to be evaluated during the semester.

---

# Secondary Users

## General Public

**Needs:**  
An understandable view of wildfire locations and general risk conditions, and a way to report fires they can see.

A simplified, mobile-friendly version of the interactive map could improve public situational awareness without requiring users to interpret raw satellite or environmental datasets. Members of the public may also see fires before satellites detect them, so the platform will let them submit reports through a "Report a Fire" feature.

**Supporting Evidence:**  
NASA FIRMS provides a publicly accessible interactive map for viewing active fires and thermal anomalies, demonstrating an existing public-facing use case for geographically visualizing wildfire information.

**Source:**  
NASA FIRMS Fire Map  
https://firms.modaps.eosdis.nasa.gov/map/

**Assumption:**  
The specific needs and preferred presentation format for members of the general public have not yet been validated through user interviews. We assume most public users will access the platform on mobile devices.

---

## Environmental Researchers

**Needs:**  
Access to historical wildfire observations, environmental conditions, satellite imagery, and model outputs for analysis.

The system will store observations over time and support historical wildfire-event analysis and model evaluation.

**Supporting Evidence:**  
NASA FIRMS provides archived MODIS and VIIRS active-fire products in addition to recent fire data. Historical observations can therefore support retrospective wildfire analysis and model evaluation.

**Source:**  
NASA FIRMS — Active Fire Data  
https://firms.modaps.eosdis.nasa.gov/active_fire/

---

## Insurance and Reinsurance Companies

**Needs:**  
Wildfire-risk information that can help evaluate geographic exposure, understand portfolio risk, monitor active wildfire threats, and prioritize areas requiring closer assessment.

The platform's historical observations, environmental risk factors, and geographic risk heatmaps could provide an additional source of wildfire-risk information for these workflows.

**Assumption:**  
Insurance-specific workflows have not yet been validated with an insurer or reinsurer. This stakeholder is therefore considered a secondary potential user rather than a primary semester target.

---

## Critical Infrastructure Operators

**Needs:**  
Early awareness of wildfire activity near critical assets such as telecommunications infrastructure, pipelines, transportation systems, and data centres.

A wildfire-risk platform could allow operators to monitor geographic exposure and identify assets located near emerging wildfire detections or high-risk regions.

**Assumption:**  
Specific critical-infrastructure workflows have not yet been validated with infrastructure operators. This represents a potential future application of the platform.

---

## Forestry and Land-Management Organizations

**Needs:**  
Information about vegetation conditions, fuel density, historical wildfire activity, and geographic areas experiencing elevated fire risk.

Combining vegetation, terrain, weather, and historical wildfire observations could support prioritization of vegetation management, monitoring, and wildfire-mitigation activities.

**Assumption:**  
Specific forestry workflows and requirements have not yet been validated directly with a forestry or land-management organization.

---

## Utility and Public-Safety Regulators

**Needs:**  
Reliable wildfire-risk information and historical observations that can support oversight of wildfire-mitigation programs and infrastructure-related wildfire risk.

**Supporting Evidence:**  
Wildfire-prone jurisdictions such as California require regulated electric utilities to prepare wildfire-mitigation plans. This demonstrates a regulatory need for documented wildfire-risk mitigation, monitoring, and evaluation.

**Source:**  
California Public Utilities Commission — Wildfires  
https://www.cpuc.ca.gov/industries-and-topics/wildfires

---

## Development Team

**Needs:**  
A realistic software-engineering project that allows the team to practice full-stack development, AI/ML, APIs, databases, testing, and collaborative development.

The project will involve technologies such as:

- React/TypeScript
- Python/Flask
- REST APIs
- SQL
- AI/ML libraries
- geospatial visualization
- Git/GitHub

This is an internal project stakeholder rather than an external user whose needs define the wildfire-monitoring problem.

---

# Initial Scope

## Scope Statement

For the semester, Team Ash Detectives will focus on developing a prototype wildfire-monitoring platform that combines satellite/geospatial data, environmental conditions, and AI-based analysis to detect potential wildfire activity and visualize wildfire risk.

The core system will provide:

- an interactive, mobile-friendly map,
- wildfire detections,
- risk heatmaps,
- fire-progression visualization,
- public fire reporting with a fire lifecycle history,
- and simulated early-warning alerts.

The team will evaluate its detection and risk models using historical wildfire data.

Advanced capabilities such as fully real-time raw satellite-image processing, precise fire-spread forecasting, direct emergency-service integration, global deployment, and automated emergency notifications will be deferred to keep the project feasible within the semester.

---

# System Boundaries

The system will operate as a monitoring and decision-support platform rather than an emergency-response or dispatch system.

For the initial implementation:

- The platform will not issue official evacuation orders or emergency instructions.
- AI-generated wildfire detections and risk estimates will be presented as advisory outputs rather than authoritative emergency decisions.
- The system will rely primarily on public or openly accessible datasets.
- The platform will not attempt to replace professional wildfire forecasting or emergency-management systems.
- Automated real-world actions will not be triggered directly from model outputs.
- Model predictions will include confidence or uncertainty information where appropriate.

These boundaries are consistent with limitations documented by NASA FIRMS, which warns that satellite-derived active-fire observations have limited accuracy and should not be used independently for preservation of life or property.

**Source:**  
NASA FIRMS Fire Map  
https://firms.modaps.eosdis.nasa.gov/map/

---

# Features Planned for This Semester

## 1. Interactive Wildfire Monitoring Map

- Interactive geospatial map displaying wildfire detections and wildfire risk.
- Display detected fire locations using satellite and geospatial datasets such as NASA FIRMS.
- Allow users to zoom, pan, and inspect specific geographic areas.
- Display relevant environmental information such as temperature, wind, and vegetation conditions where available.

## 2. Wildfire Detection

- Process historical and/or near-real-time satellite fire data to identify potential wildfire locations.
- Use a baseline AI/computer-vision or machine-learning approach to classify imagery or environmental observations associated with potential fire activity.
- Display detection confidence and relevant information for each detected fire.
- Evaluate the detection system using historical wildfire observations.

## 3. Wildfire Risk Heatmap

- Generate a wildfire-risk score for geographic areas based on available environmental factors.
- Incorporate factors such as vegetation/fuel conditions, temperature, wind, terrain, and historical fire activity where data is available.
- Visualize risk levels using a heatmap or categorical risk indicators.

## 4. Fire and Risk Information Dashboard

- Provide a dashboard summarizing active or historical fire detections.
- Display information such as location, detection time, confidence, risk level, and relevant environmental conditions.
- Allow users to select individual fires or geographic areas for more detailed information.

## 5. Early-Warning Simulation

- Simulate an early-warning workflow when the system identifies a potential wildfire or area with elevated risk.
- Generate a simulated alert containing the approximate location, risk/detection level, and supporting environmental information.
- Use historical data to demonstrate how the alerting system could have behaved during previous wildfire events.
- Clearly distinguish simulated alerts from real emergency alerts.

## 6. Explainable Risk Factors

- Display the primary environmental factors contributing to the predicted wildfire-risk level.
- Show relevant factors such as temperature, vegetation dryness, wind conditions, terrain, and recent fire activity where available.
- Provide a short explanation of why an area received a particular risk level.
- Avoid presenting explanations as definitive causation.

## 7. AI Model Evaluation

- Evaluate wildfire-detection and risk-prediction models using historical wildfire data.
- Report appropriate metrics such as precision, recall, false-positive rate, and detection confidence.
- Compare predictions against historical observations to identify strengths and limitations.

## 8. Backend and Data Infrastructure

- REST APIs for frontend/backend communication.
- SQL database for storing wildfire observations, environmental data, and system results.
- Data-processing pipelines for external wildfire and environmental datasets.

## 9. Report a Fire and Fire Lifecycle History

- Provide a "Report a Fire" button that lets any user, including members of the public, report a wildfire they can see, even in areas with no previous fire history.
- Show reports on the map clearly labelled as unverified and distinct from satellite detections.
- Allow only authenticated staff users to confirm or reject reports and update a fire's status through stages of control (e.g. Out of Control, Being Held, Under Control, Out).
- Store every status change as a timestamped record, and move fires into the historical record once marked Out.
- Make confirmed historical fires available as historical fire activity for the risk model and as events for the Early-Warning Simulation.
- Reports are never sent to emergency services; the form directs users to call 911 in an emergency.

---

# AI-Specific Features

## Wildfire Detection

A baseline machine-learning or computer-vision model will be used to classify observations or imagery associated with potential wildfire activity.

## Wildfire Risk Estimation

A predictive model will combine environmental variables such as temperature, vegetation/fuel conditions, wind, terrain, and historical wildfire observations to estimate relative wildfire risk.

## Confidence and Uncertainty Reporting

Model outputs will include confidence scores or uncertainty indicators so users can distinguish between stronger and weaker predictions.

## AI-Assisted Explanation

Where feasible, the system will generate a short explanation of the main factors contributing to a wildfire-risk prediction, such as elevated temperature, dry vegetation, or high wind conditions.

## Model Verification

AI-generated results will be compared with historical wildfire observations and evaluated using quantitative metrics before being presented as reliable system outputs.

---

# Non-Functional Requirements

## Performance

- The interactive map should load and respond quickly on both mobile and desktop. The platform is mobile-first for general-public users, while primary users (emergency-management, municipal, and utility staff) use both desktop and mobile.
- Measurable targets for load time, interaction response, and API response time are defined in [#9 Responsive Interactive Map Performance](https://github.com/RianaMalhotra/ECE444-PROJECT/issues/9).
- Expensive AI or geospatial processing tasks should be performed asynchronously where appropriate.

## Scalability

- The backend should support adding additional geographic regions without requiring major architectural changes.
- Data-processing components should be modular so additional wildfire, weather, or satellite data sources can be integrated later.
- The architecture should support increasing numbers of users, observations, and geographic regions through horizontal scaling where appropriate.

## Reliability

- Failures in one external data source should not cause the entire application to become unavailable.
- Missing environmental data should be clearly indicated rather than replaced with fabricated values.
- Model and API failures should be handled gracefully.

## Maintainability

- Frontend, backend, AI/ML, and data-processing components should have clearly defined interfaces.
- Code should be modular and documented.
- Automated tests should be used for critical functionality.

## Usability

- Wildfire-risk information should be understandable without requiring specialist knowledge of satellite or geospatial datasets.
- Risk levels, confidence values, and environmental conditions should be clearly labelled.
- The interface should be usable on phone-sized screens without horizontal scrolling, with map controls and the "Report a Fire" button reachable by touch.

## Security

- API endpoints should validate incoming requests.
- Authentication and authorization should be implemented for functionality requiring restricted access.
- Sensitive configuration values such as API keys should not be exposed in source code or frontend code.
- External data should be validated before being stored or processed.
- Public fire reports should be rate-limited per device/IP to reduce spam and abuse.

## Privacy

- The initial platform will avoid collecting unnecessary personal information.
- Public fire reports do not require an account or personal details; only the report content, location, and time are stored, plus device/IP information used solely for rate limiting.
- If user accounts are introduced, only information required for system functionality will be stored.

---

# Safety and AI Guardrails

Because wildfire-monitoring information may influence how users interpret emergency conditions, the system will include safeguards around AI-generated outputs.

- AI predictions will not be presented as guaranteed wildfire detections.
- Detection confidence and uncertainty will be visible to users.
- Historical or simulated alerts will be clearly distinguished from real emergency alerts.
- The system will not automatically contact emergency services.
- Public fire reports will be clearly labelled as unverified until confirmed by staff, and will not be used for model training or evaluation unless confirmed.
- The "Report a Fire" form will state that it is not an emergency service and direct users to call 911 in an emergency.
- Users will be informed that model outputs are intended for situational awareness and decision support.
- Predictions should be supported by observable environmental or satellite data where possible.
- The system should avoid presenting unsupported explanations or fabricated environmental values.
- Model errors and false positives will be evaluated explicitly during testing.
- High-risk or uncertain predictions should be presented with appropriate caution rather than exaggerated certainty.

NASA FIRMS itself warns that satellite-derived active-fire/thermal-anomaly observations have limited accuracy, may represent sources other than wildfires, and may be obscured by cloud cover. These limitations reinforce the need to communicate uncertainty clearly.

**Source:**  
NASA FIRMS Fire Map  
https://firms.modaps.eosdis.nasa.gov/map/

---

# Features Expected to Be Deferred

The following features may be considered for future development but will not be required for the initial semester implementation.

## Fully Real-Time Raw Satellite Imagery Processing

Processing raw satellite imagery continuously as soon as it becomes available may require significant computational resources and specialized infrastructure.

## High-Resolution Satellite Computer Vision

Using very high-resolution imagery to directly identify fire or smoke could be explored later depending on data availability, licensing, and computational requirements.

## Advanced Wildfire Spread Prediction

Predicting exact future wildfire boundaries or trajectories would require more sophisticated physical and environmental modelling than the initial semester scope.

## Automated Emergency-Service Integration

Direct integration with municipal emergency-management systems, dispatch systems, or public-alert infrastructure will be deferred.

## SMS/Email/Mobile Emergency Notifications

The initial alert feature will be demonstrated within the application rather than delivering real-world emergency notifications.

## Continuous Automated Monitoring

Fully autonomous 24/7 monitoring and automatic model retraining will be deferred.

## Multi-Region/Global Deployment

The initial implementation will focus on a defined geographic region rather than supporting all wildfire-prone areas worldwide.

## Precise Fire-Spread Forecasting

Estimating the exact rate and direction of fire spread will be treated as a future enhancement rather than a core requirement.

## Direct Emergency Notification from Public Reports

Public fire reporting is in scope via the "Report a Fire" feature (Feature 9), but reports are only stored and displayed on the platform. Automatically forwarding reports to fire services, 911, or public-alert systems is deferred.

---

# Data Sources and Provenance

The platform will maintain information about the origin of data used in wildfire detections and risk predictions.

For each observation or model output, the system should record where appropriate:

- source dataset,
- observation timestamp,
- geographic location,
- data retrieval time,
- model version,
- prediction confidence,
- relevant environmental inputs,
- and entry source (satellite detection, public report, or staff update) with the updating staff user where applicable.

This will allow users and developers to trace how a wildfire detection or risk prediction was produced and support debugging, model evaluation, and reproducibility.

All timestamps will be stored in UTC and displayed in the user's local time zone with the zone labelled. NASA FIRMS acquisition times are provided in UTC; other sources will be converted on import.

NASA FIRMS is currently being considered as a primary wildfire-observation source. FIRMS provides MODIS, VIIRS, and Landsat active-fire products through downloadable files and web services.

**Source:**  
NASA FIRMS — Active Fire Data  
https://firms.modaps.eosdis.nasa.gov/active_fire/

---

# Initial Success Criteria

The semester prototype will be considered successful if it can:

- ingest wildfire and environmental data from at least one reliable public source,
- display wildfire observations on an interactive map,
- generate a geographic wildfire-risk visualization,
- produce AI/ML-based wildfire detection or risk predictions,
- report confidence or evaluation metrics for model outputs,
- store and retrieve historical wildfire observations,
- allow users to inspect individual wildfire events or geographic regions,
- simulate an early-warning workflow using historical wildfire data,
- demonstrate the system using at least one historical wildfire event,
- and provide a deployed web interface accessible outside the development environment.

---

# Questions to Clarify

## Question 1: Which wildfire datasets should we use as our primary data source?

**How to clarify:**  
Investigate public datasets such as NASA FIRMS and compare their geographic coverage, data format, spatial resolution, update frequency, API availability, historical availability, and licensing.

NASA FIRMS is currently a strong candidate because it provides active-fire products from MODIS, VIIRS, and Landsat and supports downloadable and web-service access.

---

## Question 2: What geographic area should the system support?

**How to clarify:**  
Discuss the expected project requirements and available datasets and determine whether the prototype should focus on Canada, North America, a province, or a smaller geographic region.

---

## Question 3: What level of wildfire prediction is feasible within one semester?

**How to clarify:**  
Build an initial baseline model using historical data and evaluate its performance before committing to a more complex ML approach.

---

## Question 4: What satellite imagery is practical for computer vision?

**How to clarify:**  
Investigate available imagery datasets, image resolution, historical availability, licensing, API access, preprocessing requirements, and computational requirements.

---

## Question 5: How should wildfire risk be represented to users?

**How to clarify:**  
Review existing wildfire-monitoring systems and conduct team or user-feedback sessions to determine appropriate risk scores, heatmaps, categories, and visual indicators.

---

## Question 6: What constitutes a successful wildfire detection?

**How to clarify:**  
Define evaluation metrics such as precision, recall, false-positive rate, and detection confidence and determine an appropriate historical dataset to use as ground truth.

---

## Question 7: How frequently should the system update its data?

**How to clarify:**  
Investigate the update frequency and limitations of selected data sources and determine an appropriate refresh interval for the application.

NASA FIRMS, for example, provides near-real-time and real-time products for active-fire monitoring, but the appropriate application refresh rate still needs to be determined.

---

## Question 8: Which features should be prioritized for the semester?

**How to clarify:**  
Use the team's user stories, requirements review, stakeholder evidence, technical prototypes, and development capacity to finalize the minimum viable feature set.

This section will be updated after user-story selection and review, as required by the milestone.

---

## Question 9: Where will reference start times for historical fire events come from?

**How to clarify:**  
Compare official agency fire records (e.g. the Canadian National Fire Database and provincial fire records) for coverage in our chosen region and whether they record start dates or exact times.

---

## Question 10: How will staff review public fire reports in practice?

**How to clarify:**  
Ask a municipal or emergency-management contact how public reports are currently handled, and test the review workflow with the team during the prototype.

---

# Current Assumptions

The following requirements have not yet been fully validated and should therefore be treated as assumptions:

- The four identified primary user groups will benefit from a shared wildfire-monitoring dashboard.
- Combining wildfire observations with environmental conditions will improve the usefulness of the information presented to users.
- A risk heatmap is an appropriate visualization for primary users.
- Infrastructure overlays would be useful to electric utilities.
- Users will benefit from explanations of the environmental factors contributing to model predictions.
- Historical wildfire events can provide suitable data for demonstrating and evaluating the early-warning workflow.
- Members of the public will use a "Report a Fire" feature to report fires, and genuine reports will outweigh false or duplicate ones.
- Most general-public users will access the platform on mobile devices.
- At least one historical fire event in our chosen region has complete enough data to demonstrate the early-warning workflow.

These assumptions will be refined through dataset investigation, technical prototyping, requirements discussions, user-story review, and stakeholder/user feedback where feasible.
