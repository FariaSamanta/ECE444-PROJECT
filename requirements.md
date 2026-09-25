# Requirements

## Project Goal
Wildfires in at-risk regions are often detected too late; existing monitoring relies on delayed satellite passes, manual observation, or public reporting, giving communities and responders little lead time to act. Team Ash Detectives is building a wildfire early-detection and risk-monitoring platform that applies AI/computer vision to satellite and geospatial data to flag emerging fire risk sooner. Beyond detecting active fires, the platform will use AI to predict wildfire risk by analyzing contributing factors such as vegetation dryness, fuel density, terrain, and weather conditions. 

## Stakeholders

### General Public
- **Needs:** An understandable view of wildfire locations and general risk conditions.
- **Evidence:** A simplified version of the interactive map could improve public situational awareness without requiring users to interpret raw satellite or environmental datasets.
  
### Emergency Management Organizations
- **Needs:** Timely information about potential wildfire activity, risk levels, affected areas, and fire progression.
- **Evidence:** These organizations may need to combine information from multiple sources when monitoring developing wildfire situations. Our platform aims to consolidate relevant data into a single dashboard.

### Municipalities and Local Authorities
- **Needs:** Localized wildfire risk information and visualizations that can support situational awareness and planning.
- **Evidence:** The platform will provide geospatial risk heatmaps, potential fire detections, environmental conditions, and historical observations.

### Environmental Researchers
- **Needs:** Access to historical wildfire observations, environmental conditions, satellite imagery, and model outputs for analysis.
- **Evidence:** The system will store observations over time and support historical wildfire event analysis and model evaluation.

### Organizations Monitoring Wildfire Activity
- **Needs:** A centralized way to monitor potential fire activity and changes in wildfire conditions.
- **Evidence:** The proposed system combines satellite observations, environmental data, risk predictions, and fire progression tracking.

### Development Team
- **Needs:** A realistic software engineering project that allows the team to practice full-stack development, AI/ML, APIs, databases, and collaborative development.
- **Evidence:** The project will involve React/TypeScript, Python/Flask, REST APIs, SQL, AI/ML libraries, geospatial visualization, and Git/GitHub.

## Initial Scope

### Scope Statement

> For the semester, Team Ash Detectives will focus on developing a prototype wildfire monitoring platform that combines satellite/geospatial data, environmental conditions, and AI-based analysis to detect potential wildfire activity and visualize wildfire risk. The core system will provide an interactive map, wildfire detections, risk heatmaps, fire progression visualization, and simulated early-warning alerts. The team will evaluate its detection and risk models using historical wildfire data. Advanced capabilities such as fully real-time raw satellite-image processing, precise fire-spread forecasting, direct emergency-service integration, global deployment, and automated emergency notifications will be deferred to keep the project feasible within the semester.

### Features Planned for This Semester

#### 1. Interactive Wildfire Monitoring Map

- Interactive geospatial map displaying wildfire detections and wildfire risk.
- Display detected fire locations using satellite and geospatial datasets such as NASA FIRMS.
- Allow users to zoom, pan, and inspect specific geographic areas.
- Display relevant environmental information such as temperature, wind, and vegetation conditions where available.

#### 2. Wildfire Detection

- Process historical and/or near-real-time satellite fire data to identify potential wildfire locations.
- Use a baseline AI/computer vision approach to classify satellite imagery or environmental observations associated with potential fire activity.
- Display detection confidence and relevant information for each detected fire.
- Evaluate the detection system using historical wildfire observations.

#### 3. Wildfire Risk Heatmap

- Generate a wildfire risk score for geographic areas based on available environmental factors.
- Incorporate factors such as vegetation/fuel conditions, temperature, wind, terrain, and historical fire activity where data is available.
- Visualize risk levels on the map using an intuitive heatmap or categorical risk indicators.

#### 4. Fire and Risk Information Dashboard

- Provide a dashboard summarizing active or historical fire detections.
- Display information such as location, detection time, confidence, risk level, and relevant environmental conditions.
- Allow users to select individual fires or geographic areas for more detailed information.

#### 5. Early-Warning Simulation

- Simulate an early-warning workflow when the system identifies a potential wildfire or an area with elevated risk.
- Generate an alert containing the approximate location, risk/detection level, and supporting environmental information.
- Use historical data to demonstrate how the alerting system would have behaved during previous wildfire events.

#### 7. AI Model Evaluation

- Evaluate wildfire detection and risk-prediction models using historical wildfire data.
- Report appropriate metrics such as precision, recall, false-positive rate, and detection confidence.
- Compare model predictions against historical observations to identify strengths and limitations.

### Features expected to be deferred

The following features may be considered for future development if time and resources permit, but will not be required for the initial semester implementation:

- **Fully real-time satellite imagery processing:** Processing raw satellite imagery continuously as soon as it becomes available may require significant computational resources and specialized infrastructure.
- **High-resolution satellite computer vision:** Using very high-resolution imagery to directly identify fire or smoke could be explored later depending on data availability, licensing, and computational requirements.
- **Advanced wildfire spread prediction:** Predicting the exact future boundaries or trajectory of a wildfire would require more sophisticated physical and environmental modeling than the initial semester scope.
- **Automated emergency-service integration:** Direct integration with municipal emergency-management systems, dispatch systems, or public alert infrastructure will be deferred.
- **SMS/email/mobile emergency notifications:** The initial alert feature will be demonstrated within the application rather than delivering real-world emergency notifications.
- **Continuous automated monitoring:** Fully autonomous 24/7 monitoring and automatic model retraining will be deferred.
- **Multi-region/global deployment:** The initial implementation will focus on a defined geographic region rather than supporting all wildfire-prone areas worldwide.
- **Precise fire-spread forecasting:** Estimating the exact rate and direction of fire spread will be treated as a future enhancement rather than a core requirement.
- **Public reporting:** Allowing users to submit and verify wildfire reports could be considered in a future version but is outside the initial detection and monitoring workflow.

## Questions to Clarify

1. **Which wildfire datasets should we use as our primary data source?**
   - Investigate available public datasets such as NASA FIRMS and evaluate their coverage, format, update frequency, and API availability.

2. **What geographic area should the system support?**
   - Discuss the expected project requirements and determine whether the system should focus on Canada, North America, or a smaller geographic region.

3. **What level of wildfire prediction is feasible within one semester?**
   - Build an initial baseline model using historical data and evaluate its accuracy before committing to a more complex ML approach.

4. **What satellite imagery is practical for computer vision?**
   - Investigate available imagery datasets, image resolution, licensing, API access, and computational requirements.

5. **How should wildfire risk be represented to users?**
   - Review existing wildfire monitoring systems and conduct team/user feedback sessions to determine appropriate risk scores, heatmaps, and visual indicators.

6. **What constitutes a successful wildfire detection?**
   - Define evaluation metrics such as precision, recall, false-positive rate, and detection confidence using historical wildfire observations as ground truth.

7. **How frequently should the system update its data?**
   - Investigate the update frequency of the selected data sources and determine an appropriate refresh interval for the application.

8. **Which features should be prioritized for the semester?**
   - Use the team's user stories, requirements review, and development capacity to finalize the minimum viable feature set.

At this stage, these questions remain open and will be addressed through dataset research, technical prototyping, requirements discussions, and user story review.
