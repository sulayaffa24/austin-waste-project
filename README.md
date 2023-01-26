# austin-waste-project

```sql
SELECT  EXTRACT(YEAR FROM report_date) AS year, 
        load_type, 
        dropoff_site, 
        ROUND(AVG(load_weight),2) avg_load_weight, 
        route_type
FROM `bigquery-public-data.austin_waste.waste_and_diversion`
WHERE load_weight IS NOT NULL
GROUP BY year, load_type, dropoff_site, route_type
```

![image](https://user-images.githubusercontent.com/30465635/214955484-fe7984a6-260f-4259-b263-c2ee685551f0.png)
