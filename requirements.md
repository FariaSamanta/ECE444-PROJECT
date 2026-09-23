# Requirements

## Project Goal

## Stakeholders

### General Public
- **Needs:** An understandable view of wildfire locations and general risk conditions.
- **Evidence:** A simplified version of the interactive map could improve public situational awareness without requiring users to interpret raw satellite or environmental datasets.
- 
### Emergency Management Organizations
- **Needs:** Timely information about potential wildfire activity, risk levels, affected areas, and fire progression.
- **Evidence:** These organizations may need to combine information from multiple sources when monitoring developing wildfire situations. Our platform aims to consolidate relevant data into a single dashboard.

### Municipalities and Local Authorities
- **Needs:** Localized wildfire risk information and visualizations that can support situational awareness and planning.
- **Evidence:** The platform will provide geospatial risk heatmaps, potential fire detections, environmental conditions, and historical observations.

## Initial Scope


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
