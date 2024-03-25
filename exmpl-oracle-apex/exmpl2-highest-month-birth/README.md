## Months with the highest birth rates (2000-2014)

****Description:**** Study of highest number of birth in 2000-2014 in the Unated States.

****SQL Query:**** 
`````SQL
SELECT MONTH,
       SUM(BIRTHS) AS BIRTH,
       CASE WHEN SUM(BIRTHS) = (SELECT MAX(total_births) FROM (SELECT SUM(BIRTHS) AS total_births FROM BIRTHDAYMONTH GROUP BY MONTH)) THEN 'red' ELSE 'blue' END AS COLORS
FROM BIRTHDAYMONTH
GROUP BY MONTH
ORDER BY MONTH
`````

****Access to the dashboard:**** [click here](https://apex.oracle.com/pls/apex/r/analysisstudent/sysan/birthdaymonths?session=106401143719786)

****Dataset (format CSV):**** https://www.kaggle.com/datasets/ayessa/birthday?resource=download

****Platform:**** Oracle Apex

****Conclusions:**** I was curious how many years of data were used in this, and this confirms my hypothesis that the dataset is too small. I noticed that there is a weekly pattern in most of the months (ex: April 4th, 11th, 18th, 25th) and when I checked, these are the only dates that had 3 weekend dates in the period from 2000-2014. All other dates have 4 or 5 weekend dates (Induced deliveries/C sections are usually not scheduled on weekends).

<br>

![](https://i.imgur.com/KAeT7Xj.png)