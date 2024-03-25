## Migration to and from the EU

****Description:**** Study of number of migrations in Europe, compare with other years.

****SQL Query:**** 
`````SQL
SELECT TIME_PERIOD, SUM(OBS_VALUE) AS VALUE
FROM SYSAN
WHERE OBS_VALUE IS NOT NULL
GROUP BY TIME_PERIOD
ORDER BY TIME_PERIOD
`````

****Access to the dashboard:**** [click here](https://apex.oracle.com/pls/apex/r/analysisstudent/sysan/migrationan?session=8997699073184)

****Dataset (format CSV):**** https://ec.europa.eu/eurostat/databrowser/bookmark/8737850f-31e9-4e43-8f9c-dea6fdff1028?lang=en

****Platform:**** Oracle Apex

****Conclusions:**** In 2021, 2.3 million immigrants came to the EU from non-EU countries. This is an increase of nearly 18% compared with 1.9 million in 2020, but still below the pre-COVID-19 level of 2.7 million in 2019. In 21 out of 27 EU countries, 50% or more immigrants came from outside the EU in 2021. The largest shares were observed in Lithuania (81% of all its immigrants), Spain (80%) and Slovenia (79%). In contrast, the lowest share was recorded in Luxembourg, where immigrants from outside the EU made up 9% of all its immigrants. In absolute numbers, the most popular countries of destination for immigrants from outside the EU in 2021 were Germany (439 000 persons or 19% of all immigrants who came to the EU from non-EU countries) and Spain (421 000 or 19%), ahead of Italy (248 000 or 11%) and France (238 000 or 11%). People who migrated to these 4 EU members represented 60% of all immigrants who entered the EU from non-EU countries in 2021. In the same year, about 1.1 million people emigrated from the EU to a non-EU country. This is also an increase compared with 956 000 people in 2020, and almost back to the pre-COVID-19 level of 1.2 million. In 8 out of 27 EU countries, more than 50% of emigrants went to a country outside the EU in 2021. The largest share of people who emigrated to a non-EU country was recorded in France (68% of all its emigrants), followed by Slovenia (65%), Lithuania (64%) and Spain (63%). On the other hand, the lowest shares were observed in Slovakia (18% of all its emigrants) and Luxembourg (16%). In absolute terms, the largest number of emigrants was recorded in Spain (239 000 or 21% of all emigrants to a non-EU country), followed by Germany (158 000 or 14%) and France (120 000 or 11%). Emigrants from these 3 EU members made up 46% of all emigrants leaving the EU countries in 2021. At EU level, the difference between the number of immigrants and emigrants resulted in a positive net migration in 2021, meaning that over 1 million more people moved to the EU than moved out.

<br>

![](https://i.imgur.com/l7WaAKK.png)