# sqL PROBLEMS

THIS IS A SAMPLE

```sql
--The top 3 stations with the highest total trip duration
SELECT
  s.name,
  SUM(t.duration_minutes) AS total_duration
FROM
  `bigquery-public-data.austin_bikeshare.bikeshare_trips` t
JOIN
  `bigquery-public-data.austin_bikeshare.bikeshare_stations` s
ON
  t.start_station_id = s.station_id
GROUP BY
  s.name
ORDER BY
  total_duration DESC
LIMIT
  3;
```


![image](https://github.com/varshanbhag06/sample-query/assets/153843798/c6b31e52-13fd-4451-a947-38d9bfa7d4e3)


