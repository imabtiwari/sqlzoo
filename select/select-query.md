- Find all details of the prize won by EUGENE O'NEILL
> SELECT * FROM nobel WHERE winner='EUGENE O''NEILL'

- List the winners, year and subject where the winner starts with Sir. Show the the most recent first, then by name order.
> SELECT winner, yr, subject FROM nobel WHERE winner like Sir% ORDER BY yr DESC, winner

- Show the 1984 winners and subject ordered by subject and winner name; but list Chemistry and Physics last.
> SELECT winner, subject 
> FROM nobel 
> WHERE yr=1984 
> ORDER BY 
> CASE WHEN subject IN ('Physics','Chemistry') THEN 1 ELSE 0 END, subject, winner