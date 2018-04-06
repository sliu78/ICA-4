ICA4

Topic: Billboard Top 100

##Question #1
What were the top songs for the past 10 years and their respective artists?

```sql
SELECT song_name,
artist,
year
from datasets.billboard_top_100_year_end
where year >= 2008 and year_rank=1 
group by year, song_name, artist
order by year
```

ICA-4/Chart/1.png

##Question #2
Which songs were the most popular in the last 10 years and their respective artists?

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

##Question #3
Which songs were the most popular in the last 50 years and their respective artists?

```sql
SELECT song_name,
count(song_name),
artist
from datasets.billboard_top_100_year_end
where year >= 1968 and year_rank <= 8
group by song_name, artist
order by count DESC
```

ICA-4/Chart/3.png

##Question #4
Which actor or actress has been nominated for the most awards?

```sql
SELECT nominee,
count(nominee) as times
from datasets.oscar_nominees
GROUP by nominee 
order by times DESC
```

ICA-4/Chart/4.png

##Question #5
What is average ratio of nominees that actually win an Oscar?

```sql
SELECT winner,
count(winner)
from datasets.oscar_nominees
GROUP by winner
```

ICA-4/Chart/5.png
