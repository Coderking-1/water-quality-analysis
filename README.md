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
