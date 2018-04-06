# ICA-4

## Question #1
1. What were the top songs for the past 10 years and their respective artists?

```sql
SELECT song_name,
artist,
year
from datasets.billboard_top_100_year_end
where year >= 2008 and year_rank=1 
group by year, song_name, artist
order by year
```

![ICA-4]（ICA-4/Chart/1.png）

## Question #1
2. Which songs were the most popular in the last 10 years and their respective artists?

```sql
SELECT song_name,
count(song_name),
artist
from datasets.billboard_top_100_year_end
where year >= 2008 and year_rank <= 20
group by song_name, artist
order by count DESC
```

ICA-4/Chart/2.png

