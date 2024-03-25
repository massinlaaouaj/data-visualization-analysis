<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:640/format:webp/1*_X3fZWx8SGAxC8mj1CPuCA.png" alt="" width="190px"/>
</p>

## Data visualization study

The visualization of data is as important as its collection and analysis.

<br>

****Content:****

- [Intro](#intro)
- [Examples of graphs, using Oracle Apex and datasets](#id1)
  - [Example1: Migration to and from the EU](./exmpl-oracle-apex/emxpl1-migration-europe/README.md)
  - [Example2: Months with the highest birth rates (2000-2014)](./exmpl-oracle-apex/emxpl1-migration-europe/README.md)
- [Project documentation (ES)](./data-visualization_DOC-ES.pdf)
- [Okay... but why should I care?](#id2)
- [Context](#id3)
- [Human psychology](#id4)
- [Colour psychology](#id5)
- [Sure... but what's wrong with putting everything in a color that I like?](#id6)
- [What tools are available?](#id7)
- [Cheatsheet](#id8)
- [TL;DR](#id9)

<br>

### Introduction <a name="intro"></a>

For me, data visualization is like recounting a journey you took, or a music festival you attended.

Just like with good communication, you need to express ideas well and actively listen to other parties, adapting the message to the target audience using clear and adaptive language to ensure effective transmission (because you don't speak the same way with your friend as you do with your boss).
The same applies when creating data visualizations, as without good communication, data can be a powerful tool to understand what they reflect, their impact, ...

<br>

### Okay... but why should I care? <a name="id2"></a>

Well, for example, let's say we want to tally and visualize the people who have voted for cats or dogs as their favorite pet.

With this simple example, we could consider representing it in many different ways, but we'll narrow it down to just two options: the 'Donut' chart and the 'Bar' chart.

![img](https://miro.medium.com/v2/resize:fit:828/format:webp/1*wUweohrrAg29UUgf6T1Zcg.png)

We can see at a glance which one communicates the votes better: the Donut chart.

But why...?

Take a closer look:
the colors in the Donut chart very clearly represent each category,
the information in the Donut chart presents the percentage, the total number of votes, and the title of what we are seeing.

Now you see the difference in why representing information well is important.

<br>

### Context <a name="id3"></a>

When we start thinking about visualizing our task, we need to define its main objective or the context of the visualization. There are two important use cases for creating graphics: exploratory and explanatory analysis.

- ****Exploratory analysis**** involves taking a pen and paper and starting to understand the analysis, that is, an internal conversation to eventually explain the data effectively.

- ****Explanatory analysis**** comes after you've had that internal conversation and know how to explain it (exploratory analysis). Now it's time to know who you're addressing:
Who is my audience?
What do I want to achieve?
Am I showing too much?

In this analysis, you must decide on colors, adaptation, which graph to use, ...

<br>

### Human psychology <a name="id4"></a>

According to the following [study](http://snoid.sv.vt.edu/~npolys/projects/safas/science.pdf), it shows how well people understand the message represented in different types of charts, concluding the following order (from most understandable to least):

- Positional charts — e.g., scatter plot
- Length-based charts — e.g., bar chart
- Directional charts — e.g., line chart
- Angle-based charts — e.g., pie chart
- Area-based charts — e.g., bubble chart
- Volume-based charts — e.g., 3D chart
- Color tone and saturation-based charts — e.g., heat map

The main objective of visualization is to effectively convey information and focus on our audience and how they perceive the message. That's why we're interested in adaptation.


<br>

### Color psychology <a name="id5"></a>

The selection of colors in data visualization is primarily used for categorizing and distinguishing data groups.

The mind associates colors with real situations or events in nature. For example, the use of warm colors like red or orange represents a relationship with warmth or energy, while the use of cool colors like blue or green represents relationships with calmness or nature.

Colors also accompany the message and convey a message themselves.

![](https://miro.medium.com/v2/resize:fit:828/format:webp/1*MToLV4Xy2NOyuPC4iwC4ZQ.png)

<br>

### Sure... but what's wrong with putting everything in a color that I like? <a name="id6"></a>

Let me give you an example. Imagine we have a set of random numbers, and we want to identify them within a set.

We'll leave the left part without color (let them figure it out, they can count...), and on the right part, we'll add color.

![](https://miro.medium.com/v2/resize:fit:828/format:webp/1*dx2fyOnP6XDsgaJjD47QHw.png)

Well... now you see how important color is!

Data isn't just represented in graphs, but also in text form. With the combination of colors and font size, we can highlight/emphasize data. 

For example:

![](https://miro.medium.com/v2/resize:fit:828/format:webp/1*maywlQIXceciFDXLE71e2A.png)

<br>

### What tools are available? <a name="id7"></a>

- Google Charts
- Oracle Analysis
- Power BI
- Tableau
- ChartJS
- …

<br>

### Cheatsheet <a name="id8"></a>

You can print this cheat sheet, or you can visit this [page](https://www.data-to-viz.com/):

![](https://miro.medium.com/v2/resize:fit:828/format:webp/1*IV8RXJ0eUNijn0RJqEKScQ.png)

### Examples: <a name="id1"></a>

<br>

- [Example1: Migration to and from the EU](./exmpl-oracle-apex/emxpl1-migration-europe/README.md)

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

![](https://i.imgur.com/l7WaAKK.png)

<br>

- [Example2: Months with the highest birth rates (2000-2014)](./exmpl-oracle-apex/emxpl1-migration-europe/README.md)

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

<br>

### TL;DR <a name="id9"></a>

![](https://miro.medium.com/v2/resize:fit:828/format:webp/1*y2xLrYzN5N3jkWbT8pwu9A.jpeg)



> [Read in Medium](https://medium.com/@massin.laaouaj/data-visualization-73819cb5c212)