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

**Resolution:**  Feature priorities were finalized through the team's candidate-story selection and review process. The selected requirements and their priorities are documented in the Selected Candidate Requirements section below.

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

---

# Selected Candidate Requirements

## Functional Requirements

### #13 – Report a Fire – Fire Entry and Fire Lifecycle History

**Source:** [GitHub Issue #13](https://github.com/RianaMalhotra/ECE444-PROJECT/issues/13)

**Priority:** High

#### User Story

As a member of the public in a local community, I want to use a "Report a Fire" button to report a wildfire I can see, even in a place where fires have never happened before, so that the fire appears on the platform when satellites may not have detected it yet, and becomes part of the historical record once it ends.

#### Source and Rationale

The General Public is identified in the project requirements as a stakeholder group that needs an understandable view of wildfire locations. The Problem Statement also notes that existing wildfire monitoring relies partly on public reporting and that satellite detection can be delayed by revisit times, cloud, or smoke. As a result, people on the ground may observe a wildfire before it is detected by satellite.

The feature also supports two Initial Success Criteria: storing and retrieving historical wildfire observations and demonstrating the system using at least one historical wildfire event. Once a reported fire ends, it becomes part of the historical wildfire record.

Public reporting is also valuable for fires occurring in locations with little or no recorded fire history. Because historical fire activity is an input to the wildfire-risk model, such locations may initially receive a low predicted risk. Confirmed public reports provide additional historical information showing that the area can experience wildfire activity.

Canadian provinces already provide mechanisms for members of the public to report wildfires, and Canadian fire agencies track fires through stages of control. The proposed fire lifecycle follows this general approach.

The system will not automatically contact emergency services. Reports are stored and displayed within the platform and are not sent to fire services or 911.

Only confirmed public reports are included in historical fire activity data used by the wildfire-risk heatmap. Unverified and rejected reports are excluded. Confirmed reports retain their `public report` source tag so that they can be distinguished from satellite detections.

#### Acceptance Criteria

##### Reporting a Fire

1. Any user, whether logged in or not, can see a **Report a Fire** button on the map page.

2. The report form collects:
   - Location
   - Time observed
   - What the user observed: flames, smoke, or both
   - An optional description of up to 500 characters

3. The user can provide the fire location by either:
   - Selecting **Use my current location**, or
   - Selecting a point on the map or entering coordinates.

4. **Use my current location** uses the browser's location permission request.

5. If location permission is denied, location is unavailable, or reported accuracy is worse than 1 km, the system asks the user to select the location manually on the map. The report can still be submitted.

6. Only the reported fire location is stored. The user's ongoing location is not stored.

7. Before submission, the system displays a prominent warning:

   **"This is not an emergency service. If there is immediate danger, call 911."**

8. After submission, the user receives confirmation that the report was received and that it was not sent to emergency services.

9. A report can be submitted regardless of the area's previous fire history or current predicted risk level, including areas with no previous recorded fires or a **Low** risk rating.

##### Storage and Display

10. Each report is stored in the database with:
    - `source = public report`
    - `status = Unverified`
    - Submission time

11. The report appears on the map within **5 seconds**, measured using the test environments defined by Issue #9. It is displayed using a label and icon that clearly distinguish it from satellite detections and confirmed fires, such as **Unverified public report**.

12. User-provided descriptions are displayed as plain text. HTML and scripts are escaped, and links are not clickable.

##### Validation and Abuse Cases

13. A report is rejected with a clear error message if:
    - Its location is outside the supported region.
    - Its observation time is in the future.
    - A required field is missing.

14. Rate limiting is applied as follows:
    - Maximum **5 reports per hour per device**, identified using a browser token.
    - Maximum **30 reports per hour per IP address**.
    - Attempts exceeding these limits are blocked and are not stored.

15. If the database is unavailable, the user receives an error message and no partial report is stored.

##### Duplicate Reports

16. If a new report is within **2 km and 24 hours** of an existing report or satellite detection, it is linked to the existing fire rather than creating a separate fire.

17. Duplicate detection runs on the server at save time within the same database transaction as the save. If two reports for the same fire are submitted simultaneously, they are linked to one fire rather than creating two separate fires.

##### Status Updates and History

18. Only logged-in staff users can change a report's status to:
    - Confirmed
    - Rejected
    - Out of Control
    - Being Held
    - Under Control
    - Out

    Public users cannot edit or delete submitted reports.

19. When a report is marked **Rejected**, it is immediately removed from the public map but remains in the database with its rejection time and the staff user responsible for the rejection for auditing purposes.

20. Each status change is stored as a new timestamped record. Previous statuses are not overwritten.

21. When a fire is marked **Out**, it is no longer displayed as an active fire on the map but remains in the database and appears in the historical view with its complete timeline, including:
    - Report time
    - Status changes
    - End time

22. Historical fires from both public reports and satellite detections can be searched by date range and geographic area.

##### Historical Data and Risk Model

23. Only **Confirmed** public reports are included in the historical fire activity data available to the Wildfire Risk Heatmap (#3).

24. **Unverified** and **Rejected** public reports are excluded from the historical fire activity data used by the risk model.

25. Confirmed reports retain `source = public report` in the historical dataset so that the risk model and its evaluation can include, exclude, or weight public reports separately from satellite detections.

### Verification

The requirement will be verified by:

- Submitting a report as a logged-out user and confirming that the 911 warning appears, the report is stored as `Unverified` with the correct provenance, and it appears on the map with an **Unverified** label within 5 seconds.
- Denying browser location permission and confirming that the user can still report a fire by selecting a location on the map.
- Submitting a description containing HTML, scripts, and a link and confirming that the content is displayed only as plain text.
- Submitting a report in an area with no previous fire history and a **Low** risk rating and confirming that the report is accepted.
- Submitting two reports for the same location simultaneously and confirming that they are linked to one fire.
- Exceeding the per-device rate limit and confirming that additional reports are blocked.
- Submitting reports from multiple devices sharing one IP address and confirming that they remain accepted until the per-IP limit is reached.
- Rejecting a report as a staff user and confirming that it disappears from the public map but remains stored for auditing.
- Confirming another report, progressing it through each fire status to **Out**, and confirming that its complete timeline appears in the historical view.
- Confirming that a confirmed report is included in historical fire activity data with its `public report` source tag.
- Testing each invalid-input and database-failure case and confirming that no invalid or partial record is stored.

### #2 – Fire & Risk Information Dashboard

**Source:** [GitHub Issue #2](https://github.com/RianaMalhotra/ECE444-PROJECT/issues/2)

**Priority:** Medium

#### User Story

As an emergency-management user, I want to select a wildfire detection or geographic area and view its relevant fire and risk information, so that I can quickly understand the conditions and severity associated with that location.

#### Source and Rationale

Emergency-management organizations are identified as primary users who need timely information about potential wildfire activity, risk levels, affected areas, and fire progression.

The project requirements also identify a Fire and Risk Information Dashboard as part of the semester scope. The dashboard will provide information such as location, detection time, confidence, risk level, and relevant environmental conditions.

**Original Source:** `docs/requirements.md` — Stakeholders: Emergency Management Organizations; Features Planned for This Semester: Fire and Risk Information Dashboard.

#### Acceptance Criteria

1. The dashboard displays active or historical wildfire detections.

2. A user can select an individual wildfire detection or a predefined geographic region available through the interface.

3. The selected detection or region displays its location.

4. Detection time is displayed when available.

5. Model confidence and wildfire risk level are displayed when available.

6. Relevant environmental conditions are displayed when available.

7. Missing information is clearly shown as unavailable rather than replaced with fabricated values.

8. If a selected geographic region has no available wildfire or risk data, the dashboard clearly indicates that no information is available for that region rather than displaying fabricated or misleading values.

9. Selecting a different wildfire detection or geographic region updates the displayed information.

### #3 – Wildfire Risk Heatmap

**Source:** [GitHub Issue #3](https://github.com/RianaMalhotra/ECE444-PROJECT/issues/3)

**Priority:** High

#### User Story

As a municipal or local-authority user, I want to view wildfire-risk levels geographically, so that I can identify areas experiencing elevated wildfire risk and examine the environmental factors contributing to that risk.

#### Source and Rationale

Municipalities and local authorities are identified as primary users who need localized wildfire-risk information and visualizations.

The requirements specify a wildfire-risk heatmap based on environmental factors including vegetation/fuel conditions, temperature, wind, terrain, and historical fire activity where data is available.

The requirements also state that users should be able to see the primary environmental factors contributing to a predicted risk level and that these factors should not be presented as definitive causation.

#### Acceptance Criteria

##### 1. Geographic Risk Visualization

**Measure:** Geographic risk visualization.

**Target:** The system displays a risk level for every geographic area for which sufficient input data is available.

**Conditions:** Using the geographic region and environmental dataset configured for the semester prototype.

**Verification Method:** Load the test dataset and visually inspect the map to confirm that risk levels are displayed for eligible areas.

##### 2. Risk Information for a Selected Geographic Area

**Measure:** Risk information associated with a selected geographic area.

**Target:** Selecting an area displays its risk level and the available environmental factors contributing to the prediction.

**Conditions:** For an area with valid environmental and model data.

**Verification Method:** Select multiple test areas on the map and verify that the displayed information corresponds to the stored model output.

##### 3. Missing Environmental Data Handling

**Measure:** Missing environmental data handling.

**Target:** Areas with unavailable environmental inputs are clearly identified as having incomplete or unavailable risk information rather than being assigned fabricated values.

**Conditions:** Test cases where one or more required environmental inputs are missing.

**Verification Method:** Remove selected environmental inputs from the test dataset and inspect the resulting map and risk information.

##### 4. Explanation of Model Inputs

**Measure:** Explanation of model inputs.

**Target:** The interface identifies the environmental factors that contributed most strongly to the displayed risk prediction without claiming that they definitively caused the wildfire risk.

**Conditions:** Whenever a user views detailed risk information for an area.

**Verification Method:** Manually inspect explanations for a representative set of test areas.

### #5 – Explainable Risk Factors

**Source:** [GitHub Issue #5](https://github.com/RianaMalhotra/ECE444-PROJECT/issues/5)

**Priority:** Medium

#### User Story

As a municipal or local-authority user, I want to see the environmental factors contributing to a predicted wildfire-risk level, so that I can understand why an area has been assigned a particular risk level.

#### Source and Rationale

Municipalities and local authorities need localized wildfire-risk information and visualizations to support situational awareness and planning.

The requirements specifically state that the system should display the primary environmental factors contributing to a predicted wildfire-risk level and provide a short explanation of why an area received that risk level.

The system may use factors such as temperature, vegetation dryness, wind conditions, terrain, and recent fire activity where data is available.

These explanations should describe model inputs and their contribution to the prediction rather than claim that the factors definitively caused the predicted risk.

#### Acceptance Criteria

##### 1. Environmental Factors Displayed for a Risk Prediction

**Measure:** Environmental factors displayed for a risk prediction.

**Target:** The system displays the top 3 available environmental factors contributing to the predicted risk level, ranked according to the model's per-prediction feature-contribution values. If fewer than 3 contributing factors are available, the system displays the available contributing factors.

**Conditions:** A user selects a geographic area with a completed risk prediction and available environmental data.

**Verification Method:** Select test areas with known model inputs and feature-contribution values. Verify that the factors displayed by the interface correspond to the highest-ranked available contributing factors for each prediction.

##### 2. Method Used to Determine Contributing Factors

**Measure:** Method used to determine contributing factors.

**Target:** The system uses a documented feature-contribution or equivalent explainability method to determine which environmental factors contributed most strongly to each prediction.

**Conditions:** A risk prediction has been generated using environmental inputs.

**Verification Method:** Inspect the model output and implementation documentation to verify that the displayed factors are selected using the defined contribution-ranking method rather than simply being selected because they were model inputs.

##### 3. Risk Explanation Displayed to the User

**Measure:** Risk explanation displayed to the user.

**Target:** The system provides a short explanation describing why the area received its displayed risk level, referencing the relevant contributing factors.

**Conditions:** A geographic area has a valid risk prediction.

**Verification Method:** Manually inspect the explanation for a representative set of test areas and verify that it references factors identified by the model's contribution-ranking method.

##### 4. System Behavior When an Environmental Factor Is Unavailable

**Measure:** System behavior when an environmental factor is unavailable.

**Target:** The system identifies unavailable information rather than displaying fabricated or assumed environmental values.

**Conditions:** One or more environmental inputs are missing for a geographic area.

**Verification Method:** Run the system using test data with missing environmental inputs and verify that the interface indicates the missing information.

##### 5. Wording of the Generated Explanation

**Measure:** Wording of the generated explanation.

**Target:** The explanation describes factors contributing to the model's prediction without presenting them as definitive causes of wildfire risk.

**Conditions:** Whenever an explanation is displayed.

**Verification Method:** Review generated explanations against predefined examples and verify that they describe model inputs/contributions rather than claiming definitive causation.

#### Remaining Assumption

The specific feature-contribution method will depend on the final predictive model selected for the prototype.

If the model does not provide per-prediction contribution values directly, the team must document and agree on an alternative explainability method before implementation and testing.

### #10 – Wildfire Detection and Confidence Scoring

**Source:** [GitHub Issue #10](https://github.com/RianaMalhotra/ECE444-PROJECT/issues/10)

**Priority:** High

#### User Story

As an emergency-management user, I want the system to classify satellite and environmental data to identify potential wildfire locations, along with a detection confidence score, so that I can evaluate the reliability of each detection before acting on it.

#### Source and Rationale

The project requirements state that one of the features planned for this semester is Wildfire Detection. The feature commits the team to processing historical and/or near-real-time satellite fire data using a baseline AI/computer vision approach, and to displaying detection confidence and relevant information for each detected fire.

**Original Source:** `docs/requirements.md` — Features Planned for This Semester: Wildfire Detection.

This story covers the underlying detection/classification step of identifying a potential fire and scoring confidence in it. It is a dependency of the Early-Warning Alert Simulation story, which consumes these detections to trigger alerts.

#### Acceptance Criteria

1. Given satellite/geospatial data, such as NASA FIRMS, for a monitored region, the system classifies whether the data indicates a potential wildfire.

2. Each detection is assigned a confidence score reflecting the model's certainty.

3. The detection's location, timestamp, and confidence score are displayed alongside the classification result.

4. Detections below a minimum confidence threshold are visually distinguished from higher-confidence detections rather than displayed identically.

5. The minimum confidence threshold is implemented as a configurable constant rather than a hardcoded value.

6. The initial confidence threshold is selected after backtesting against the historical dataset and is treated as a provisional assumption to validate rather than a fixed target.

7. If input data for a region is incomplete or unavailable, no detection is fabricated and the gap is reported instead.

#### Related

The Early-Warning Alert Simulation on Historical Wildfire Events depends on this story's detection and confidence output.

## Quality Requirements

### #12 – Maintainable and Modular System Architecture

**Source:** [GitHub Issue #12](https://github.com/RianaMalhotra/ECE444-PROJECT/issues/12)

**Priority:** Medium

#### Quality Requirement

As a development team member, I want the frontend, backend, AI/ML, and data-processing components to have clearly defined and modular interfaces, so that individual components can be modified, tested, and maintained without requiring unnecessary changes to other parts of the system.

#### Source and Rationale

The project requirements identify maintainability as an important non-functional requirement. The system consists of several distinct components, including the frontend, backend, AI/ML models, and data-processing pipeline. Clearly defined interfaces and modular code will reduce coupling between these components and make future development, debugging, testing, and integration easier.

Automated testing of critical functionality also helps ensure that changes to one component do not unintentionally break existing functionality.

**Original Source:** `docs/requirements.md` — Non-Functional Requirements: Maintainability.

#### Acceptance Criteria

1. **Defined Interfaces**
   - Communication between the frontend, backend, AI/ML, and data-processing components must be performed through documented APIs or clearly defined module interfaces.
   - **Verification:** Code review and interface documentation will be used to verify that component communication occurs through these defined interfaces.

2. **Component Independence**
   - Replacing or modifying one component, such as the AI/ML model, must not require changes to more than **two unrelated components**.
   - **Verification:** The files and components changed during integration will be reviewed to determine whether modifications remain within this limit.

3. **Reusable Modules**
   - Functionality used in more than one component must be placed in a shared reusable module rather than duplicated.
   - **Verification:** Code review will be used to identify duplicated functionality and confirm that shared functionality is implemented through reusable modules.

4. **Automated Testing**
   - Critical functionality, including API communication, AI/ML model integration, and core data-processing operations, must have automated tests.
   - At least **80% of identified critical functions** must have an associated automated test.
   - **Verification:** The set of identified critical functions will be compared against the project's automated tests to confirm that the 80% target is met.

5. **Documentation**
   - All public APIs and component interfaces must be documented.
   - Documentation must specify the expected **inputs, outputs, and purpose** of each public API or interface.
   - Important non-obvious implementation decisions must include documentation or explanatory comments.
   - **Verification:** Code and documentation review will confirm that all public APIs and component interfaces contain the required information.

6. **Regression Verification**
   - All existing automated tests must pass before a change is merged into the `main` branch.
   - **Verification:** The project's automated test suite or CI pipeline must report that all existing tests pass before the change is merged.

#### Measurement Details

Maintainability will be evaluated using the following measurable targets and verification methods:

- **Interface definition:** Frontend, backend, AI/ML, and data-processing communication must occur through documented APIs or module interfaces, verified through code review and interface documentation.
- **Component independence:** A modification or replacement of one component must require changes to no more than **two unrelated components**, verified by reviewing the affected files and components during integration.
- **Automated test coverage:** At least **80% of identified critical functions** must have an associated automated test.
- **Documentation:** **All public APIs and component interfaces** must document their expected inputs, outputs, and purpose.
- **Regression testing:** **100% of existing automated tests must pass** before a change is merged into `main`.
- **Reusable functionality:** Functionality shared by multiple components must be implemented as a reusable module rather than duplicated, verified through code review.

### #4 – Reliable Handling of Data and Service Failures

**Source:** [GitHub Issue #4](https://github.com/RianaMalhotra/ECE444-PROJECT/issues/4)

**Priority:** Medium

#### User Story

As an emergency-management user, I want the wildfire monitoring platform to remain usable when an external data source, API, or model component fails, so that I can continue accessing available wildfire information without being misled by missing or invalid data.

#### Source and Rationale

The project requirements state that failures in one external data source should not cause the entire application to become unavailable. Missing environmental data should be clearly indicated rather than replaced with fabricated values, and model or API failures should be handled gracefully.

This requirement supports emergency-management users who depend on the platform for wildfire situational awareness. Because the platform relies on external wildfire, environmental, and model components, failure of one dependency should not prevent users from accessing information from components that remain available.

**Original Source:** `docs/requirements.md` — Non-Functional Requirements: Reliability; Stakeholders: Emergency Management Organizations.

#### Target Justification

The reliability targets below are provisional project constraints. In particular, the 100% unavailable-value handling target is used because displaying fabricated replacement data could mislead users about wildfire or environmental conditions.

These targets may be refined following testing and stakeholder feedback.

#### Acceptance Criteria

##### Measure

Application availability and correct handling of unavailable data when an external dependency fails.

##### Target

- The application remains accessible when one external data source or service fails.
- **100% of tested unavailable values** are clearly identified as unavailable rather than replaced with fabricated values.
- Failure of an individual API, external data source, or model component does not crash the entire application.
- Derived outputs that depend on unavailable required input data are clearly identified as incomplete or unavailable rather than displayed as fully valid results.

##### Conditions

Testing will be performed in the team's deployment or test environment by individually simulating:

- An unavailable external data source.
- A failed API request.
- A model-processing failure.

##### Verification Method

For each simulated dependency failure, verify that:

1. The application continues to load unaffected functionality.
2. Unaffected wildfire information remains accessible.
3. Affected information displays an appropriate error or unavailable state.
4. Missing environmental information is clearly identified as unavailable.
5. The system does not fabricate replacement values.
6. An API or model failure does not crash the entire application.
7. If unavailable data is required to compute a derived output, such as a wildfire risk score, the derived output is marked as incomplete or unavailable and is not presented as a complete result.

### #6 – Usability/Understandability

**Source:** [GitHub Issue #6](https://github.com/RianaMalhotra/ECE444-PROJECT/issues/6)

**Priority:** Medium

#### User Story

As a wildfire-monitoring user without specialist knowledge of satellite or geospatial datasets, I want wildfire-risk information and confidence values to be clearly labelled and understandable, so that I can interpret the displayed information correctly.

#### Source and Rationale

The requirements state that wildfire-risk information should be understandable without specialist knowledge and that risk levels, confidence values, and environmental conditions should be clearly labelled.

The 90% task-completion rate is a provisional team assumption for the semester prototype and may be adjusted if user testing provides evidence for a different threshold.

#### Acceptance Criteria

##### 1. Interpretation Success Rate

**Measure:** Percentage of representative non-specialist users who can correctly interpret the displayed risk level and confidence information.

**Target:** At least **90% of test participants** must correctly identify the displayed risk level and explain the meaning of the confidence indicator.

If exactly **5 participants** are tested, **all 5 participants must pass** to meet the 90% target.

##### 2. Participant Conditions

Participants must:

- Not have been involved in developing the application.
- Have no formal or professional background in remote sensing, GIS, or wildfire-risk modelling.

Because actual emergency-management users may not be available for semester testing, non-specialist participants will be treated as proxy users.

##### 3. Test Scenarios

Participants will be shown representative wildfire-risk map and dashboard views that include:

- High risk + high confidence.
- High risk + low confidence (e.g., 40%).
- At least one view with missing or unavailable environmental data.

##### 4. Risk-Level Interpretation

A participant passes the risk-level task if they correctly identify the risk category displayed by the application.

##### 5. Confidence Interpretation

A participant passes the confidence task only if their explanation indicates that the confidence value represents the model's confidence in its own output and does not represent:

- A guarantee of wildfire occurrence; or
- By itself, the probability that a wildfire will occur.

For example, interpreting a 40% confidence value as meaning that there is a 40% chance of a wildfire would be considered incorrect.

#### Verification Method

Conduct a usability test with at least **5 participants**.

For each participant:

1. Present the selected representative wildfire-risk scenarios.
2. Record whether the participant correctly identifies the displayed risk level.
3. Record whether the participant correctly explains the confidence indicator according to the defined scoring rule.
4. Determine whether the participant successfully completed both interpretation tasks.

Calculate the percentage of participants who pass both tasks.

At least **90% must pass**. If exactly 5 participants are tested, all 5 must pass.

#### External Supporting Evidence

Nielsen Norman Group's usability-testing guidance will be used as supporting evidence for using a small participant group, but not as justification for the 90% success-rate threshold.

The Canadian Wildland Fire Information System (CWFIS) will be considered as a reference for established public wildfire-danger terminology and classification conventions.

#### Remaining Assumptions

- The **90% task-completion target** is provisional and may be revised following user testing.
- A minimum of **5 participants** is feasible for the semester prototype.
- Non-specialist proxy participants are an acceptable substitute when representative emergency-management users cannot be recruited.
- Proxy participants should have no formal or professional background in remote sensing, GIS, or wildfire-risk modelling.
- Risk categories, confidence terminology, and missing-data indicators will be defined consistently before usability testing.
- The selected test views will represent the types of risk/confidence combinations and missing-data situations that users may encounter.

### #9 – Responsive Interactive Map Performance

**Source:** [GitHub Issue #9](https://github.com/RianaMalhotra/ECE444-PROJECT/issues/9)

**Priority:** High

#### User Story

As a wildfire-monitoring user, whether a member of the public on a phone or an emergency-management/municipal analyst on desktop or mobile, I want the wildfire map to load and respond quickly when I pan, zoom, switch layers, and inspect detections, so that I can check fire locations and risk levels without losing focus during time-sensitive situations.

#### Source and Rationale

The existing Performance requirement states that the map should load and respond to user interactions within a reasonable time. This story replaces that non-testable requirement with measurable performance targets.

The Primary Users requirements identify rapid interpretation of wildfire detections as an interface priority. The application is also mobile-first for general-public users, while emergency-management and municipal users may use both desktop and mobile devices.

Expensive AI and geospatial processing is intended to run asynchronously, so map interactions must not wait for model inference.

#### Assumptions

- **A1:** All numeric targets and workload sizes are provisional. They will be re-checked against the first deployed prototype and revised if necessary.
- **A2:** A dataset containing up to **10,000 detection points** is assumed to represent a busy period in one region. This assumption will be validated using FIRMS detection counts for the selected region during a severe fire period.

#### Definitions

**Accepts input:** The map responds to a pan or zoom action and the view visibly moves.

**Fully displayed:** All visible detection points and heatmap tiles for the current view have finished rendering and no loading indicator is displayed.

#### Test Environments

**Mobile**

- Playwright/Chrome mobile emulation of a mid-range Android phone, such as a Pixel 7 profile.
- 4× CPU slowdown.
- Chrome DevTools Slow 4G network throttling.

**Desktop**

- Laptop with at least 8 GB RAM.
- Latest desktop Chrome.
- Unthrottled connection of at least 25 Mbps download, measured before each test run.

**Both environments**

- Team's deployed backend.
- One region containing up to 10,000 detection points and its risk heatmap grid.

#### Q1 – Initial Map Load

**Measure:** Time from navigating to the map page until the map accepts input and the basemap, detection layer, and risk heatmap are fully displayed.

**Target:**

- Mobile: At least **95% of loads complete within 5 seconds**.
- Desktop: At least **95% of loads complete within 3 seconds**.

**Conditions:** Each defined test environment with a cold browser cache.

**Verification Method:** Perform 30 scripted page loads per environment using Playwright plus a Lighthouse run in both mobile and desktop modes on the deployed site. Report the 95th-percentile load time for each environment.

#### Q2 – Map Interaction Response

**Measure:** Time from a user action until the updated view is fully displayed, measured separately for pan, zoom, and layer-toggle actions.

**Target:** For each action type, at least 95% of interactions complete within:

- Mobile: **1.5 seconds**
- Desktop: **1 second**

If an update takes longer, a loading indicator must appear within **0.5 seconds**.

**Conditions:** Each defined test environment with the page already loaded.

**Verification Method:** Use a Playwright script to perform:

- 30 pans
- 30 zooms
- 30 layer toggles

per environment. Mobile testing uses touch events in mobile emulation. Record timings and report the 95th-percentile time for each action type and environment.

Manually confirm the loading indicator by throttling the network using Chrome DevTools.

#### Q3 – Detection / Area Detail API

**Measure:** Server response time and error rate for requests returning details about a selected detection or area.

**Target:**

- At least **95% of requests return within 500 ms**, measured at the server.
- Fewer than **1% of requests** return an error, defined as a 5xx response or timeout.

**Conditions:**

- Deployed backend.
- 20 concurrent users (provisional).
- Same dataset used in the other performance tests.
- Request mix:
  - 70% single-detection detail requests.
  - 30% area-detail requests.

**Verification Method:** Conduct a load test using k6 or Locust with 20 concurrent users for 5 minutes. Report the 95th-percentile response time and error rate.

#### Boundary and Failure Cases

1. If the visible area contains more points than can be rendered within the performance target, detections are clustered rather than dropped or allowed to freeze the page.

2. Map interactions do not wait for AI model inference. Model results load asynchronously and display a **Processing…** state until ready.

3. If a data layer fails to load, the rest of the map remains interactive and the failed layer displays an error state, consistent with #4 – Reliable Handling of Data and Service Failures.

4. On a phone-sized screen, map controls including zoom, layer toggle, and **Report a Fire** remain usable without horizontal scrolling.

#### Related Requirements

- #2 – Fire & Risk Information Dashboard
- #3 – Wildfire Risk Heatmap
- #4 – Reliable Handling of Data and Service Failures
- #6 – Usability/Understandability
