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

![ica4]（ICA-4/Chart/1.png）
