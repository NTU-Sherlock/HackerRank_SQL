Consider  and  to be two points on a *2D* plane.

- happens to equal the minimum value in *Northern Latitude* (*LAT_N* in **STATION**).
- happens to equal the minimum value in *Western Longitude* (*LONG_W* in **STATION**).
- happens to equal the maximum value in *Northern Latitude* (*LAT_N* in **STATION**).
- happens to equal the maximum value in *Western Longitude* (*LONG_W* in **STATION**).

Query the [Manhattan Distance](https://xlinux.nist.gov/dads/HTML/manhattanDistance.html) between points  and  and round it to a scale of  decimal places.

**Input Format**

The **STATION** table is described as follows:

![https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where *LAT_N* is the northern latitude and *LONG_W* is the western longitude.

Manhattan Distance p1 at (x1, y1) and p2 at (x2, y2), it is |x1 - x2| + |y1 - y2|

```sql
SELECT
ROUND(MAX(LAT_N) - MIN(LAT_N) + MAX(LONG_W) - MIN(LONG_W),4)
FROM
STATION
```

[Euclidean Distance](https://en.wikipedia.org/wiki/Euclidean_distance)

```sql
SELECT
ROUND(sqrt(power(MAX(LAT_N) - MIN(LAT_N),2) + power(MAX(LONG_W) - MIN(LONG_W),2)),4)
FROM
STATION
```


```sql
SELECT ROUND(MEDIAN(Lat_N), 4)
FROM Station;
```