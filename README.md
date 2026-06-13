SELECT
    source_type,
    COUNT(*) AS total_sources
FROM water_sources
GROUP BY source_type
ORDER BY total_sources DESC;
