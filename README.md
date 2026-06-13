# Water Quality Data Analysis

## Project Overview

Access to safe drinking water remains one of the most important public health challenges in many communities. This project analyzes water quality data collected from multiple sampling locations to assess the safety and suitability of water for human consumption.

The analysis focuses on identifying patterns in key water quality indicators, detecting potential contamination risks, and generating evidence-based recommendations for improving water resource management.

## Problem Statement

Poor water quality can contribute to the spread of waterborne diseases and negatively affect community health. Government agencies, water providers, and environmental health professionals require reliable data to monitor water safety and prioritize interventions.

This project seeks to answer the following questions:

- Which locations meet recommended water quality standards?
- Which indicators show the greatest variation across locations?
- Are there signs of potential contamination?
- What actions should be prioritized to improve water quality?

## Objectives

1. Clean and validate raw water quality data.
2. Analyze trends across multiple sampling sites.
3. Compare measurements against accepted standards.
4. Visualize findings through charts and summary reports.
5. Provide recommendations based on analytical findings.

## Dataset

The dataset contains water quality measurements collected from various water sources.

### Variables

| Variable | Description |
|-----------|-------------|
| pH | Measure of acidity or alkalinity |
| Turbidity | Water clarity measurement |
| Dissolved Oxygen | Oxygen available in water |
| Temperature | Water temperature |
| Total Coliforms | Indicator of microbial contamination |
| Location | Sampling location |

## Methodology

### Data Cleaning

- Removed duplicate records.
- Checked for missing values.
- Standardized variable names.
- Validated measurement ranges.
- Corrected formatting inconsistencies.

### Exploratory Data Analysis

The following analyses were conducted:

- Descriptive statistics
- Distribution analysis
- Location comparison
- Trend identification
- Outlier detection

### Visualization

Visualizations were created to:

- Compare water quality indicators by location.
- Identify high-risk sampling sites.
- Communicate findings clearly to stakeholders.

## Key Findings

- Most sampling locations recorded acceptable pH levels.
- Several sites exhibited elevated turbidity levels.
- Dissolved oxygen varied significantly across locations.
- A small number of observations indicated possible contamination risks requiring further investigation.

## Recommendations

Based on the findings:

1. Increase monitoring frequency in high-risk areas.
2. Improve water treatment procedures where turbidity exceeds recommended levels.
3. Conduct microbial testing in locations showing contamination indicators.
4. Implement community awareness programs on safe water handling.

## Tools Used

- Microsoft Excel
- SQL
- Python
- GitHub

## Skills Demonstrated

- Data Cleaning
- Data Validation
- Statistical Analysis
- Data Visualization
- Report Writing
- Public Health Analytics

## Author

Malack Bogonko

Bachelor of Science in Information Technology (Expected Graduation: November 2027)

ALX Africa Data Analytics Bootcamp Graduate

SELECT
    source_type,
    COUNT(*) AS total_sources
FROM water_sources
GROUP BY source_type
ORDER BY total_sources DESC;
SELECT
    community_name,
    AVG(queue_time) AS average_wait_time
FROM visits
GROUP BY community_name
ORDER BY average_wait_time DESC
LIMIT 20;
SELECT
    community_name,
    water_quality_score,
    queue_time
FROM water_sources
WHERE water_quality_score < 60
AND queue_time > 30;
SELECT
    source_type,
    AVG(water_quality_score) AS quality_score
FROM water_sources
GROUP BY source_type;
SELECT
    community_name,
    water_quality_score,
    queue_time
FROM water_sources
WHERE water_quality_score < 60
AND queue_time > 30;
SELECT
    source_type,
    AVG(reliability_score) AS reliability
FROM water_sources
GROUP BY source_type;
## Key Findings

- Boreholes provided the most reliable water access in the majority of communities.
- Several communities experienced average queue times exceeding 30 minutes.
- Water quality scores varied significantly across regions.
- Infrastructure failures contributed to reduced service availability.
- Communities with the lowest water quality often experienced the longest waiting times.
- ## Recommendations

1. Prioritize repairs in communities with low reliability scores.
2. Expand borehole coverage in underserved areas.
3. Increase routine water quality monitoring.
4. Reduce queue times through additional access points.
5. Strengthen maintenance programs to improve infrastructure performance.
maji-ndogo-project/
│
├── README.md
├── datasets/
│   ├── water_sources.csv
│   ├── visits.csv
│   └── communities.csv
│
├── sql/
│   ├── water_quality_queries.sql
│   ├── queue_analysis.sql
│   └── intervention_analysis.sql
│
├── dashboards/
│   ├── water_access_dashboard.pbix
│
├── reports/
│   └── final_report.pdf
│
└── images/
    ├── dashboard.png
    └── charts.png
