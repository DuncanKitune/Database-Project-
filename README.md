# Database-Project-
	#	Time	Action	Message	Duration / Fetch
3	1	17:19:30	USE test1	0 row(s) affected	0.094 sec

3	2	17:19:54	SELECT * FROM test1.netflix_titles
 LIMIT 0, 1000	100 row(s) returned	0.109 sec / 0.000 sec

 COUNT WHERE TITLE IS MOVIES = 55
3	3	17:24:57	SELECT COUNT(type) From test1.netflix_titles
 WHERE type = 'Movie'
 LIMIT 0, 1000	1 row(s) returned	0.094 sec / 0.000 sec

COUNT WHERE TITLE IS TV SHOW = 45 
3	5	17:25:45	SELECT COUNT(type) From test1.netflix_titles
 WHERE type = 'TV Show'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec

 COUNT WHERE RATING IS TV-MA = 32
3	6	17:27:54	SELECT COUNT(rating) From test1.netflix_titles
 WHERE rating = 'TV-MA'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec

 COUNT WHERE RATING IS PG = 6
3	7	17:28:11	SELECT COUNT(rating) From test1.netflix_titles
 WHERE rating = 'PG' 
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec

 COUNT WHERE RATING IS TV-13 = 0
3	8	17:28:27	SELECT COUNT(rating) From test1.netflix_titles
 WHERE rating = 'TV-13'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec

 COUNT WHERE RATING IS TV-14 = 17
3	9	17:28:32	SELECT COUNT(rating) From test1.netflix_titles
 WHERE rating = 'TV-14'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec

 COUNT WHERE DURATION IS 1 season = 
3	10	17:30:09	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '1 season'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec

 
3	11	17:30:21	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '2 season'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec

 
3	12	17:30:26	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '3 season'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec

 
3	13	17:30:30	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '4 season'
 LIMIT 0, 1000	1 row(s) returned	0.015 sec / 0.000 sec
3	14	17:30:35	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '5 season'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec
3	15	17:30:38	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '6 season'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec
3	16	17:30:42	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '9 season'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec
3	17	17:30:59	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '9 seasons'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec
3	18	17:31:06	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '8 seasons'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec
3	19	17:31:11	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '7 seasons'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec
3	20	17:31:34	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '2 seasons'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec
3	21	17:31:39	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '3 seasons'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec

3	25	17:35:05	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '61 min'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec
3	26	17:35:15	SELECT COUNT(duration) From test1.netflix_titles
 WHERE duration = '>61 min'
 LIMIT 0, 1000	1 row(s) returned	0.000 sec / 0.000 sec

AVERAGE DURATION 56.46
 3	42	18:41:48	SELECT 'country', AVG(duration)
 AS average_duration
 FROM test1.netflix_titles
 GROUP BY 'country'
 LIMIT 0, 1000	1 row(s) returned	0.110 sec / 0.000 sec
 
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
 -- genre = Movie
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


