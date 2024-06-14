# Database-Project-
SELECT * FROM test1.netflix_titles;

-- USE test1
-- SELECT type
-- FROM netflix_titles
-- ORDER BY type ASC;
-- SELECT * FROM test1.netflix_titles;
-- SELECT DISTINCT director
-- FROM netflix_titles
-- ORDER BY director ASC;
-- SELECT 
-- title,
-- cast,
-- country
-- FROM netflix_titles
-- WHERE release_year >=2020
-- ORDER BY release_year ASC;
-- SELECT
-- title,
-- director,
-- duration,
-- AGGREGATE_FUNCTION (duration)
-- FROM netflix_titles
-- GROUP BY
-- title,
-- director,
-- duration;
 -- = Movie
-- AND 
-- duration <= 60min;
-- SELECT
-- title,
-- director,
-- release_year,
-- MIN(duration) duration,
-- max(duration) duration,
-- round(avg(duration),2) duration
-- FROM 
-- netflix_titles
-- GROUP BY title;
SELECT
title,
director,
duration,
rating
FROM netflix_titles
WHERE 
type = Movie
AND 
duration <= 60min;


