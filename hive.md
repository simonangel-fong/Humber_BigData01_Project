```sql
%sql
SELECT
    year AS Year,
    COUNT(*) AS Crime_count
FROM crime_view
WHERE year >= 2014
GROUP BY year
ORDER BY year ASC


%sql
SELECT
    dow AS Day_of_Week,
    CASE dow
        WHEN 0 THEN 'Mon'
        WHEN 1 THEN 'Tue'
        WHEN 2 THEN 'Wed'
        WHEN 3 THEN 'Thur'
        WHEN 4 THEN 'Fri'
        WHEN 5 THEN 'Sat'
        ELSE 'Sun'
    END
    AS d_o_w,
    COUNT(*) AS Crime_count
FROM crime_view
GROUP BY 1
ORDER BY 1 ASC

```
